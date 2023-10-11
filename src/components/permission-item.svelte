<script lang="ts">
import CheckButton from "./check-button.svelte";

const data = {
  name: 'Perm 1',
  checked: false,
  subPermissions: [
    { name: 'sub 1', checked: false },
    { name: 'sub 2', checked: false },
    { name: 'sub 3', checked: false },
    { name: 'sub 4', checked: false },
  ],
};

function handleClick() {
  for (let sub of data.subPermissions) {
    sub.checked = !data.checked;
  }
}
</script>

<div>
  <div class="permission-area">
    <CheckButton
      bind:value={data.checked}
      on:click={handleClick}>
      {data.name}
    </CheckButton>
  </div>
  <ul>
    {#each data.subPermissions as sub}
      <li>
        <CheckButton bind:value={sub.checked}>
          {sub.name}
        </CheckButton>
      </li>
    {/each}
  </ul>
</div>

<style>
ul {
  margin: 0;
  padding: 0;
}

li {
  list-style-type: none;
  border-bottom: solid thin rgba(0, 0, 0, .1);
  color: rgba(0, 0, 0, .5);
  padding: .3rem 1rem;
}

.permission-area {
  border-bottom: solid 2px rgba(0, 0, 0, .7);
  padding-top: 1rem;
}
</style>