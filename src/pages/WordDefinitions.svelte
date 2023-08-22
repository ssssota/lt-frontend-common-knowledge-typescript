<script lang="ts">
  import Markdown from "svelte-exmarkdown";
  import PaddingPane from "../components/PaddingPane.svelte";
  const md = `\
### 解説の前に用語の確認

#### トランスパイルとは

Trans-Compileの略。  
フロントエンド文脈ではJSやTSをJSに変換すること。  
それをしてくれるツールがトランスパイラ。

コンパイルは**型チェックを含む**ことが多く、  
トランスパイルは**型チェックを含まない**ことが多い。

#### バンドルとは

複数のファイルを一つにまとめること。  
正確には別の概念だが、多くの文脈でトランスパイルを含む。
`;
</script>

<PaddingPane>
  <Markdown {md} />
</PaddingPane>
