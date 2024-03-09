<script lang="ts">
</script>

<div class="note-main">
  <article>제목1</article>
  <article>제목2</article>
  <article>제목3</article>
</div>

<style>
  .note-main {
    display: grid;
    gap: 10px;
    color: #856539;
    justify-items: center;
    padding: 15px 0px;
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
    transform: scale(1.1);
    box-shadow: 2px 2px 2px 2px;
  }
</style>
