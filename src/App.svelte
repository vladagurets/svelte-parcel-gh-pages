<script>
  import { onMount } from 'svelte'
  import { text } from 'src/store'
  
  onMount(() => {
    setInterval(() => {
      text.set($text === 'Hello' ? 'World' : 'Hello' )
    }, 1000)
  })
</script>

<style>
  div {
    font-size: 50px;
  }
</style>

<div>
  {$text}
</div>
