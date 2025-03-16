<script>
    import Heading from '$lib/atoms/Heading.svelte';

    let { data } = $props();
</script>

<div id="experienceSection" class="flex flex-col justify-start w-full">
    <Heading>Technical Skills</Heading>
    <div class="flex flex-wrap mt-5 gap-1.5">
        {#each data as skill}
            <div class="flex items-center justify-center py-2 px-2.5 text-tertiary text- font-medium text-xs space-x-[7px] bg-background-tertiary rounded-md border border-background-secondary">
                {@html skill.icon}
                <div>{skill.text}</div>
            </div>
        {/each}
    </div>
</div>