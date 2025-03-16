<script lang="ts">
	import { page } from '$app/state';

	interface NavLink {
		route: string;
		text: string;
	}

	function isActive(routeName: string): boolean {
		return page.route.id === routeName;
	}


	let navigationItems: NavLink[] = [
		{ route: '/', text: 'Home' },
		{ route: '/contact', text: 'Contact' },
		{ route: '/blog', text: 'Blog' },
	];

	console.log(page.route.id)

	const data = {
		name: 'Rick Whalley',
		occupation: 'Software Engineering Consultant',
		avatar: 'https://avatars.githubusercontent.com/u/5675120?v=4',
		socials: {
			email: 'mailto:hello@rickwhalley.xyz',
			linkedin: 'https://www.linkedin.com/in/rick-whalley-93b31650'
		}
	};


</script>

<nav>
	<div class="flex flex-col sm:flex-row items-center justify-between w-full">
		<div class="flex flex-col sm:flex-row items-center w-full">
			<img alt="avatar of {data.name}" src={data.avatar}
					 class="sm:h-16 sm:w-16 w-24 h-24 rounded-full shadow-lg shadow-background-secondary mb-2 sm:mb-0" />
			<div class="flex flex-col items-center sm:items-start sm:ml-4 w-full">
				<h1 class="text-primary text-3xl">{data.name}</h1>
				<div class="text-faint font-mono text-sm sm:-mt-[2px]">{data.occupation}</div>
			</div>
		</div>
		<div class="hidden md:flex items-center justify-start justify-items-center">
			{#each navigationItems as item}
				<a href={item.route} class="text-lg ps-6 font-medium font-mono cursor-pointer hover:text-white {isActive(item.route) ? 'text-white' : 'text-zinc-500'}">
					{item.text}
				</a>
			{/each}
			<div class="md:hidden flex items-center space-x-3">
				<span class="cursor-pointer">
					<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
							 stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
							 class="lucide-icon lucide lucide-menu h-10 w-10 text-white">
						<line x1="4" x2="20" y1="12" y2="12"></line>
						<line x1="4" x2="20" y1="6" y2="6"></line>
						<line x1="4" x2="20" y1="18" y2="18"></line>
					</svg>
				</span>
			</div>
		</div>
	</div>
	<div class="hidden md:flex items-center justify-start justify-items-center p-6 space-x-6">

	</div>
</nav>

