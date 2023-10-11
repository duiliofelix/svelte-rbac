<script lang="ts">
export let value = false;
</script>

<label>
  <input type="checkbox" bind:checked={value} on:click />
  <slot />
</label>
