<script>
	export let components, allLayouts, allContent;
</script>

{#each components as {name, fields}}
  <svelte:component this={allLayouts["layouts_components_" + name + "_svelte"]} {...fields} {allContent} />
{/each}
