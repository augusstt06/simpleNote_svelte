<script lang="ts">
  export let handlePostOpen: () => void
</script>

<div class="note-head">
  <svg class="close" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24" {...$$props}>
    <path
      fill="currentColor"
      d="M12 20c-4.41 0-8-3.59-8-8s3.59-8 8-8s8 3.59 8 8s-3.59 8-8 8m0-18C6.47 2 2 6.47 2 12s4.47 10 10 10s10-4.47 10-10S17.53 2 12 2m2.59 6L12 10.59L9.41 8L8 9.41L10.59 12L8 14.59L9.41 16L12 13.41L14.59 16L16 14.59L13.41 12L16 9.41z"
    />
  </svg>
  <svg
    class="post"
    xmlns="http://www.w3.org/2000/svg"
    width="1em"
    height="1em"
    viewBox="0 0 24 24"
    role="button"
    tabindex="0"
    {...$$props}
    on:click={handlePostOpen}
  >
    <path
      fill="currentColor"
      d="M19 13c.7 0 1.37.13 2 .35V9l-6-6H5c-1.11 0-2 .89-2 2v14a2 2 0 0 0 2 2h8.35c-.22-.63-.35-1.3-.35-2c0-3.31 2.69-6 6-6m-5-8.5l5.5 5.5H14zM23 18v2h-3v3h-2v-3h-3v-2h3v-3h2v3z"
    />
  </svg>
</div>

<style>
  .note-head {
    display: flex;
    justify-content: space-between;
  }

  .post {
    color: #fff;
    margin-right: 20px;
    height: 25px;
    width: 25px;
    transition: all ease-in-out 1s;
    cursor: pointer;
  }
  .post:hover {
    transform: scale(1.2);
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
</style>
