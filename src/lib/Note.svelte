<script lang="ts">
  import NoteHeader from './NoteHeader.svelte'
  import NoteList from './NoteList.svelte'

  let isPostOpen: boolean = false
  function handlePostOpen(): void {
    isPostOpen = !isPostOpen
  }
</script>

<section>
  <NoteHeader {handlePostOpen} />
  {#if !isPostOpen}
    <NoteList />
  {:else}
    <div>Write a note</div>
  {/if}
</section>

<style>
  section {
    background-color: #e5c08f;
    width: 60vh;
    padding: 15px;
    border-radius: 5%;
  }
</style>
