<script lang="ts">
  import Markdown from "svelte-exmarkdown";
  import PaddingPane from "../components/PaddingPane.svelte";
  const md = `\
### 想定質問

#### 仕様がないのにサードパーティのトランスパイラはどうやってTypeScriptをトランスパイルしているの？

TypeScriptはJavaScriptのスーパーセットであるため、TypeScript独自の文法を消すだけで基本的にはOK。

#### ブラウザで動くJSコードにTypeScriptコンパイラを使わないなら、TypeScriptコンパイラは何のためにあるの？

TypeScriptコンパイラの真髄は型チェック。  
トランスパイラとして利用せずとも、型チェックだけを行うことができる。（CIやIDEの補完機能など）
`;
</script>

<PaddingPane>
  <Markdown {md} />
</PaddingPane>
