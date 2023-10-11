<script lang="ts">
import { createEventDispatcher } from "svelte";
import PermissionItem from "./permission-item.svelte";

export let isOpen: boolean = false;

const dispatch = createEventDispatcher();

function handleCloseClick() {
  dispatch('close');
}
</script>

<div class="permission-selector" class:open={isOpen}>
  <button on:click={handleCloseClick}>close</button>
  <PermissionItem />
  <PermissionItem />
  <PermissionItem />
  <PermissionItem />
  <PermissionItem />
</div>

<style>
.open {
  transform: translateX(0%) !important;
}

.permission-selector {
  background-color: white;
  box-shadow: -1px 0 5px 0 rgba(0, 0, 0, .5);
  padding: 1rem;
  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  overflow-y: scroll;
  width: min(300px, 20vw);

  transform: translateX(100%);
  transition: transform 350ms ease;
  
  display: flex;
  flex-direction: column;
}

</style>
