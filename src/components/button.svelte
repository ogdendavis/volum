<script>
  /**
   * action should be either a link path (string) or an executable function with no return value
	 * @type {(() => void) | string}
	 */
   export let action;

   /**
    * @type {string}
    */
   export let customStyle;

  const buttonType = typeof action === "string"
    ? "link"
    : "onClick";

  const onClick = () => {
    if ( typeof action === "function" ) {
      action();
    }
    else {
      window.location.href = action;
    }
  }
</script>

<style>
  button {
    background: var(--color-orange-dark);
    border: 2px solid var(--color-orange-dark);
    border-radius: var(--border-radius);
    box-shadow: none;
    color: var(--color-white-bright);
    font-family: var(--default-font);
    font-size: 1.25rem;
    font-weight: 600;
    padding: 0.5rem 1rem;
    transition: var(--transition);
  }

  button:hover {
    background: var(--color-white-bright);
    color: var(--color-orange-dark);
    cursor: pointer;
    transform: scale(1.1);
  }
</style>

<button on:click={ onClick } style={ customStyle }>
  <slot />
</button>
