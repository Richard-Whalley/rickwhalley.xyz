<script lang="ts">
	import Heading from '$lib/atoms/Heading.svelte';

	let { data } = $props();
</script>

<div id="aboutSection" class="flex flex-col justify-start w-full mt-3">
	<Heading>About</Heading>
	<p class="text-primary mt-3">{data.description}</p>
</div>