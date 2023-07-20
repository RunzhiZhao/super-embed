<script>
  import { getContext } from "svelte"

  const { styleable } = getContext("sdk")
  const component = getContext("component")

  export let text
</script>

<div class="embed" use:styleable={$component.styles}>
  {@html text}
</div>

<style>
  .embed {
    position: relative;
  }
  .embed :global(> *) {
    width: 100%;
    height: 100%;
  }
</style>