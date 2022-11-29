<script>
  import Login from './Login.svelte';
</script>

<main> <!-- <body> 요소의 주 콘텐츠(main content)를 정의할 때 사용-->
  <h1 class="hero">Travel Packing Checklist</h1>
  <Login />
</main>

<style>
  :global(body) {
    background-color: cornflowerblue;
  }

  .hero {
    --height: 7rem; /*css 변수 정의 */

    background-color: orange;
    color: white;
    font-size: 4rem;
    height: var(--height);
    line-height: var(--height);
    margin: 0 0 3rem 0;
    text-align: center;
    vertical-align: middle;
    width: 100vw;
  }

  main {
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
  }
</style>
