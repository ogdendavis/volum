<script>
  import Button from "../components/button.svelte";

  const customStyle = "margin: 0 0.5rem;";
</script>

<style>
  nav {
    text-align: center;
  }
</style>

<nav>
  <Button action="/login" customStyle={customStyle}>log in</Button>
  <Button action="/signup" customStyle={customStyle}>sign up</Button>
</nav>
