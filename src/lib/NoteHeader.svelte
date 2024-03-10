<script lang="ts">
  export let addNoteItem: (item: string) => void
  let noteInput: string = ''
</script>

<section class="note-head">
  <div class="icon-container">
    <svg class="close" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
      <path
        fill="currentColor"
        d="M12 20c-4.41 0-8-3.59-8-8s3.59-8 8-8s8 3.59 8 8s-3.59 8-8 8m0-18C6.47 2 2 6.47 2 12s4.47 10 10 10s10-4.47 10-10S17.53 2 12 2m2.59 6L12 10.59L9.41 8L8 9.41L10.59 12L8 14.59L9.41 16L12 13.41L14.59 16L16 14.59L13.41 12L16 9.41z"
      />
    </svg>
  </div>
  <div class="note-input">
    <input type="text" placeholder="Write Memo!" bind:value={noteInput} />
    <svg
      class="post"
      xmlns="http://www.w3.org/2000/svg"
      width="1em"
      height="1em"
      viewBox="0 0 24 24"
      {...$$props}
      role="button"
      tabindex="0"
      on:click={() => {
        addNoteItem(noteInput)
        noteInput = ''
      }}
    >
      <path
        fill="currentColor"
        d="M11 13v3q0 .425.288.713T12 17q.425 0 .713-.288T13 16v-3h3q.425 0 .713-.288T17 12q0-.425-.288-.712T16 11h-3V8q0-.425-.288-.712T12 7q-.425 0-.712.288T11 8v3H8q-.425 0-.712.288T7 12q0 .425.288.713T8 13zm-6 8q-.825 0-1.412-.587T3 19V5q0-.825.588-1.412T5 3h14q.825 0 1.413.588T21 5v14q0 .825-.587 1.413T19 21z"
      />
    </svg>
  </div>
</section>

<style>
  .note-head {
    display: flex;
    flex-direction: column;
    padding: 5px;
  }
  .icon-container {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }

  .close {
    margin-left: 20px;
    border-radius: 100%;
    color: red;
    height: 25px;
    width: 25px;
    transition: all ease-in-out 1s;
    cursor: pointer;
  }
  .close:hover {
    transform: scale(1.2);
    background-color: red;
    color: #fff;
  }

  .note-input {
    margin: 15px 10px 0px 0px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .note-input input {
    width: 70%;
    border: none;
    padding: 10px;
    border-radius: 10px;
    background-color: #f4eadd;
    display: relative;
    margin-right: 15px;
  }
  .note-input input:focus {
    outline: none;
  }
  .post {
    display: absolute;
    top: 10px;
    color: #fff;
    margin-right: 20px;
    height: 35px;
    width: 35px;
    transition: all ease-in-out 1s;
    cursor: pointer;
  }
  .post:hover {
    transform: scale(1.2);
  }
</style>
