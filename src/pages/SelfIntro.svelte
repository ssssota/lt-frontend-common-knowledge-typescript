<script lang="ts">
  import PaddingPane from '../components/PaddingPane.svelte';
  import Markdown from 'svelte-exmarkdown';

  const md = `\
### だれ

TOMIKAWA Sotaro

- X: [@ssssotaro](https://x.com/ssssotaro)
- GitHub: [ssssota](https://github.com/ssssota)
- Slack: [#times-tomikawa](https://st-zozo.slack.com/archives/C03EV50CJR3)

趣味はカメラ(street photography)とアニメ
`
</script>

<PaddingPane>
  <Markdown {md}></Markdown>
</PaddingPane>
