<script lang="ts">
  export let noteList: string[]
  export let deleteNoteItem: (item: string) => void
</script>

<section class="note-main">
  {#each noteList as noteItem}
    <div class="item-container">
      <article>{noteItem}</article>
      <button class="delete-note" on:click={() => deleteNoteItem(noteItem)}>Delete</button>
    </div>
  {:else}
    <h1>No Memo</h1>
  {/each}
</section>

<style>
  .note-main {
    display: grid;
    gap: 10px;
    color: #856539;
    justify-items: center;
    padding: 15px 0px;
  }
  .item-container {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  .note-main article {
    width: 80%;
    border: 2px solid #f4eadd;
    border-radius: 15px;
    padding: 10px;
    cursor: pointer;
    transition: all ease-in-out 0.6s;
  }
  .note-main article:hover {
    transform: scale(1.05);
    box-shadow: 2px 2px 2px 2px;
  }
  .delete-note {
    cursor: pointer;
    padding: 10px;
    border: none;
    border-radius: 5px;
    transition: all ease-in-out 0.6s;
  }
  .delete-note:hover {
    background-color: #ec5353;
    color: #fff;
  }
</style>
