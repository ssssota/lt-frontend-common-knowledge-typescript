<script lang="ts">
  import Markdown from "svelte-exmarkdown";
  import PaddingPane from "../components/PaddingPane.svelte";
  const md = `\
### 2. 一般的にTypeScriptコンパイラで出力したものをブラウザで動かさない

TypeScriptコンパイラ(TSC)はJavaScriptを出力するが、ブラウザで実行するのに適した形式ではない。

多くの場合、TypeScriptコンパイラの代わりにサードパーティのトランスパイラを使う。

#### フロントエンド開発者向け補足

トランスパイラの例: [Babel](https://babeljs.io/), [esbuild](https://esbuild.github.io/), [swc](https://swc.rs/), [Bun](https://bun.sh/), [TSC](https://www.typescriptlang.org/)  
webpack, Rollup, Parcel, Turbopack, Rspackなどはバンドラーで、トランスパイラではない(Viteはバンドラーでもない)
`;
</script>

<PaddingPane>
  <Markdown {md} />
</PaddingPane>
