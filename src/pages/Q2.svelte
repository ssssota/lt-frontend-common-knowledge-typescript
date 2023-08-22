<script lang="ts">
  import { onMount } from "svelte";
  import CenteringPane from "../components/CenteringPane.svelte";
  let countDown = 10;
  onMount(() => {
    let id = setInterval(() => {
      countDown--;
      if (countDown === 0) clearInterval(id);
    }, 1000);
  });
</script>

<CenteringPane>
  <h3>Q. 一般的にTypeScriptコンパイラで<br />出力したものをブラウザで動かす</h3>
  <p>{countDown || "❌"}</p>
</CenteringPane>

<style>
  h3 {
    text-align: center;
  }
</style>
