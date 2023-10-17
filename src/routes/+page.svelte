<script lang="ts">
  let items: string[] = [];
  let newItemText = "";

  function handleSubmit(e: SubmitEvent) {
    e.preventDefault();

    items = [...items, newItemText];
    newItemText = "";
  }
</script>

<form on:submit={handleSubmit}>
  <input type="text" bind:value={newItemText} />
  <button>Add</button>
</form>

<ul>
  {#each items as item}
    <li>{item}</li>
  {/each}
</ul>

<style>
  ul {
    list-style: none;
  }
</style>
