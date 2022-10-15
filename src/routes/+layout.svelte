<style>
  .siteHeader {
    text-align: center;
  }

  .siteHeader a {
    color: var(--color-gray-dark);
    display: inline-block;
    text-decoration: none;
  }

  .slotContainer {
    padding: 0.5rem;
  }
</style>

<header class="siteHeader">
  <a href="/">
    <h1>volum</h1>
  </a>
</header>
<div class="slotContainer">
  <slot />
</div>
