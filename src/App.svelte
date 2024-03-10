<script lang="ts">
  import NoteMain from './lib/NoteMain.svelte'
</script>

<main>
  <h1>Simple Note</h1>
  <section><NoteMain /></section>
  <footer>footer</footer>
</main>

<style>
  main {
    height: 100vh;
    display: grid;
    grid-template-areas:
      'h1'
      'section'
      'footer';
    grid-template-rows: 10vh 80vh 10vh;
  }
  h1 {
    grid-area: h1;
    text-align: center;
  }
  section {
    grid-area: section;
    display: flex;
    justify-content: center;
  }
  footer {
    grid-area: footer;
    background: purple;
  }
</style>
