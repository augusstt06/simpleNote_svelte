<script lang="ts">
  import NoteHeader from './NoteHeader.svelte'
  import NoteList from './NoteList.svelte'

  let noteList: string[] = []
  function addNoteItem(item: string): void {
    if (item.length === 0) return
    noteList = [...noteList, item]
  }
  function deleteNoteItem(item: string): void {
    noteList = noteList.filter(data => data !== item)
  }
</script>

<section>
  <NoteHeader {addNoteItem} />
  <NoteList {noteList} {deleteNoteItem} />
</section>

<style>
  section {
    background-color: #e5c08f;
    width: 60vh;
    padding: 15px;
    border-radius: 5%;
  }
</style>
