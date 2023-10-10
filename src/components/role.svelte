<div class="container">
  <div class="content">
    Role 1
    <hr />
    <span>
      Role that do something something
    </span>
  </div>
  <button on:click>Edit</button>
</div>

<style>
.container {
  border: solid thin rgba(0, 0, 0, .5);
  border-radius: 5px;
  display: flex;
  gap: 1rem;
  padding: 1rem .5rem;
}

.content {
  flex-grow: 1;
}

hr {
  margin: 0;
}

span {
  font-size: smaller;
}
</style>
