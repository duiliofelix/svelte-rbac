<script lang="ts">
	import Permissions from "../components/permissions.svelte";
import Role from "../components/role.svelte";

  let isOpen = false;
  
  function open() {
    isOpen = true;  
  }
</script>

<div class="role-list">
  <Role on:click={open}/>
  <Role />
  <Role />
  <Role />
  <Role />
</div>

<div>
  group 1
</div>

user

{#if isOpen}
  <Permissions />
{/if}

<style>
.role-list {
  display: grid;
  grid: auto-flow / 1fr 1fr;
  gap: 1rem;
}
</style>