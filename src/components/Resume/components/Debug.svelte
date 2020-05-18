<script>
  export let section = ""
  export let data = {}
</script>

<main>
<h1 >{section}</h1>
<pre>{JSON.stringify(data, null, 2)}</pre>
<hr>
</main>

<style>
  h1 {
    color: var(--primary-color)
  }
  
  pre {
    color: var(--secondary-color)
  }
</style>