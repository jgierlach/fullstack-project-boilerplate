<script>
  const currentYear = new Date().getFullYear()
</script>

<footer class="footer flex flex-none bg-base-100 p-4">
  <div class="text-center">
    <strong>{`Your Company Name © ${currentYear} - All Rights Reserved.`}</strong>
  </div>
</footer>

<style>
  footer {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 60px; /* Adjust as needed */
  }
</style>
