<script>
  import Debug from './components/Debug.svelte'

  // props
  export let resume = {}

  // dev options
  const DEBUG_MODE = true

  // code starts here
  const registry = {
    // "basics",
    // "work",
    // "volunteer"
    // "education"
    // "awards"
    // "publications"
    // "skills"
    // "languages"
    // "interests"
    // "references"
  }

  const getSectionComponent = (section) => {
    if (!DEBUG_MODE) return registry[section]

    const component = registry[section]
    
    if (!component) console.warn(`Unsupported section: ${section}`)

    return component || Debug
  }
</script>

<main>
	{#each Object.entries(resume) as [section, data]}
    <svelte:component this={getSectionComponent(section)} {section} {data} />
  {/each}
</main>

<style>
</style>