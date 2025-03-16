<script lang="ts">
    import Heading from '$lib/atoms/Heading.svelte';

    let { data } = $props();
</script>

<div id="experienceSection" class="flex flex-col justify-start w-full mt-12">
    <Heading>Experience</Heading>
    <div class="flex flex-col items-start justify-center mt-6">
        {#each data as experience, index}
            <div class="flex w-full">
                <div class="flex flex-col items-center shrink-0">
                    <img 
                        src={experience.image} 
                        alt="{experience.company} logo"
                        class="h-12 w-12 rounded-full shrink-0"
                    />
                    {#if index !== data.length - 1}
                        <div class="w-[2px] grow bg-background-tertiary"></div>
                    {/if}
                </div>
                <div class="flex ml-3 flex-col grow pb-14">
                    <div class="flex justify-between items-center w-full h-12">
                        <div class="flex flex-col justify-start items-start">
                        <div class="text-primary text-xl font-semibold">
                            {experience.company}
                        </div>
                        <p class="text-tertiary text-sm">
                            {experience.role}
                        </p>
                        </div>
                        <div class="text-tertiary text-sm flex items-center">
                        {#if experience.duration === "Present"}
                            <div class="bg-green-600 w-1.5 border-green-700 animate-pulse h-1.5 rounded-full mr-2"></div>
                        {/if}
                        {experience.duration}
                        </div>
                    </div>
                </div>
            </div>
        {/each}
    </div>
</div>