# Fullstack project boilerplate

## Components, stores, base.css, and utils.js

For ease of reference using $lib/path shorthand the components and stores folders along with base.css and utils.js files are placed under the lib directory

## Environment variable instructions

Out of the box this project is configured to work with Supabase.com. Create a .env at the root of this project and create the following environment variables

PUBLIC_SUPABASE_URL='Your projects supabase url'

PUBLIC_SUPABASE_ANON_KEY='Your projects supabase anon key'

# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/main/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
