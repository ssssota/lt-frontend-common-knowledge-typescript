<script lang="ts">
  import ProgressBar from "./components/ProgressBar.svelte";
  import SlideView from "./components/SlideView.svelte";
  import "./global.css";
  import A1 from "./pages/A1.svelte";
  import A2 from "./pages/A2.svelte";
  import A3 from "./pages/A3.svelte";
  import Faq from "./pages/Faq.svelte";
  import Q1 from "./pages/Q1.svelte";
  import Q2 from "./pages/Q2.svelte";
  import Q3 from "./pages/Q3.svelte";
  import Quiz from "./pages/Quiz.svelte";
  import SelfIntro from "./pages/SelfIntro.svelte";
  import Title from "./pages/Title.svelte";
  import WordDefinitions from "./pages/WordDefinitions.svelte";
  import { page } from "./utils/page";
  export let listView = false;

  const pages = [
    Title,
    SelfIntro,
    Quiz,
    Q1,
    Q2,
    Q3,
    WordDefinitions,
    A1,
    A2,
    A3,
    Faq,
    // INSERT YOUR PAGE HERE!
  ];

  const handleKeydown = (e: KeyboardEvent) => {
    switch (e.code) {
      case "ArrowRight":
      case "Space":
      case "Enter":
        page.next();
        break;
      case "ArrowLeft":
        page.prev();
        break;
    }
  };
</script>

<svelte:window on:keydown={handleKeydown} />

{#if !listView}
  <SlideView onLeftClick={page.prev} onRightClick={page.next}>
    <svelte:component this={pages[$page - 1]} />
  </SlideView>
  <ProgressBar progress={($page - 1) / (pages.length - 1)} />
{:else}
  {#each pages as p}
    <SlideView>
      <svelte:component this={p} />
    </SlideView>
  {/each}
{/if}
