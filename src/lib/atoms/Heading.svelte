<script lang="ts">
	let { children } = $props();
</script>

<div class="text-lg text-zinc-500 font-mono">
	{@render children?.()}
</div>
