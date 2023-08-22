<script lang="ts">
  import Markdown from "svelte-exmarkdown";
  import PaddingPane from "../components/PaddingPane.svelte";
  const md = `\
### 1. TypeScriptはブラウザで直接実行できない

TypeScriptがそのまま動かないのでJavaScriptにコンパイル（トランスパイル）して実行する。

サーバーサイドJS(Node.jsなど)も基本的には同じ。

#### フロントエンド開発者向け補足

DenoやBunはTypeScriptを直接実行できるように見えるが、内部ではトランスパイルしている。  
Denoは組み込みで型チェック機能あり。
Bunは型チェック機能はなく、チェックしたいならTSC使ってねというスタンス。
`;
</script>

<PaddingPane>
  <Markdown {md} />
</PaddingPane>
