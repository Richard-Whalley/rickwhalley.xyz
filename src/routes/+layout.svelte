<script lang="ts">
	import '../app.css';
	import MainNav from '$lib/organisms/MainNav.svelte';

	let { children } = $props();

</script>


<div class="overflow-x-hidden bg-background flex flex-col justify-center items-center relative">
	<div class="w-full max-w-[1024px] flex flex-col my-24 lg:px-0 px-5 mb-[100px] sm:mb-[200px]">
		<MainNav/>
		{@render children()}
	</div>
</div>
