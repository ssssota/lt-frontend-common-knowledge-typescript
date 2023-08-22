<script lang="ts">
  import Markdown from "svelte-exmarkdown";
  import PaddingPane from "../components/PaddingPane.svelte";
  const md = `\
### 3. 現行のTypeScriptには仕様書がない

昔(TypeScript v1)は仕様書が存在していたが、  
現在(TypeScript v2以降)は存在しない。

「TypeScriptコンパイラの実装が仕様」状態。

JavaScript(ECMAScript)には言語仕様が存在する。  
（みんなも普段使う言語の仕様書があるか確認してみよう）
`;
</script>

<PaddingPane>
  <Markdown {md} />
</PaddingPane>
