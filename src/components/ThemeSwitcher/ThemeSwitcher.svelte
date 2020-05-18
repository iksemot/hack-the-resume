<script>
  import Themes from './Themes.svelte'

  const themes = [
    "light",
    "dark"
  ]

  let selectedTheme = themes[0]

  const onThemeChange = (event) => {
    document.documentElement.setAttribute('data-theme', selectedTheme)
  }
</script>

<label>
  Theme:
  <select bind:value={selectedTheme} on:change="{onThemeChange}">
    {#each themes as theme}
      <option value={theme}>{theme}</option>
    {/each}
  </select>
</label>

<Themes/>

<style>
  label {
    color: var(--heading-color)
  }
</style>
