<script lang="ts">
import Permissions from "../components/permissions.svelte";
import Role from "../components/role.svelte";

let isOpen = false;

function openPermModal() {
  isOpen = true;  
}

function handleClose() {
  isOpen = false;
}
</script>

<div class="role-list">
  <Role on:click={openPermModal}/>
  <Role />
  <Role />
  <Role />
  <Role />
</div>

<div>
  group 1
</div>

user

<Permissions
  isOpen={isOpen}
  on:close={handleClose}
/>

<style>
.role-list {
  display: grid;
  grid: auto-flow / 1fr 1fr;
  gap: 1rem;
}
</style>