<script>
  import "../app.postcss";
</script>

<slot />
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap');
  :global(body) {
    font-family: 'Poppins', sans-serif;
    background-image: linear-gradient(#a502b7 -800rem, #131316);
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    color: #fff;
  }
</style>