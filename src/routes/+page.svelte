<script lang="ts">
  let newItemText = "";

  function handleSubmit(e: SubmitEvent) {
    e.preventDefault();

    newItemText = "";
  }
</script>

<form on:submit={handleSubmit}>
  <input type="text" bind:value={newItemText} />
  <button>Add</button>
</form>
