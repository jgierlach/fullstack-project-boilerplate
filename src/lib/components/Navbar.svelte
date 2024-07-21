<script>
  import { page } from '$app/stores'

  let isLoggedIn = false
  let menuOpen = false
  let currentRoute = 'Home'

  function login() {
    isLoggedIn = true
  }

  function logout() {
    isLoggedIn = false
  }

  function setRoute(route) {
    currentRoute = route
    menuOpen = false // Close the menu on mobile after selecting a route
  }
</script>

<nav class="navbar flex flex-none bg-base-100 px-4 py-2 shadow-lg">
  <div class="flex flex-1 items-center">
    <a href="/" class="btn btn-ghost text-xl normal-case">Brand</a>
    <div class="ml-4 hidden space-x-4 md:flex">
      <a href="/" class={`btn btn-ghost`} class:btn-active={$page.url.pathname === '/'}>Home</a>
      <a href="/about" class={`btn btn-ghost`} class:btn-active={$page.url.pathname === '/about'}
        >About</a
      >
    </div>
  </div>
  <div class="md:hidden">
    <button class="btn btn-ghost" on:click={() => (menuOpen = !menuOpen)}>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        class="inline-block h-6 w-6 stroke-current"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M4 6h16M4 12h16m-7 6h7"
        ></path>
      </svg>
    </button>
  </div>
  <div class="hidden items-center space-x-4 md:flex">
    {#if isLoggedIn}
      <button class="btn btn-primary" on:click={logout}>Logout</button>
    {:else}
      <button class="btn btn-secondary" on:click={login}>Login</button>
    {/if}
  </div>
</nav>

{#if menuOpen}
  <div
    class="absolute left-0 right-0 top-14 z-50 flex flex-col items-start bg-base-100 p-4 shadow-lg md:hidden"
  >
    <a
      href="/"
      class={`btn btn-ghost mb-2 ${currentRoute === 'Home' ? 'btn-active' : ''}`}
      on:click={() => setRoute('Home')}>Home</a
    >
    <a
      href="/about"
      class={`btn btn-ghost mb-2 ${currentRoute === 'About' ? 'btn-active' : ''}`}
      on:click={() => setRoute('About')}>About</a
    >
    {#if isLoggedIn}
      <button class="btn btn-primary mb-2" on:click={logout}>Logout</button>
    {:else}
      <button class="btn btn-secondary mb-2" on:click={login}>Login</button>
    {/if}
  </div>
{/if}
