<script lang="ts">
	import Experience from '$lib/organisms/Experience.svelte';
	import Education from '$lib/organisms/Education.svelte';
	import Skills from '$lib/organisms/Skills.svelte';
	import PersonalProjects from '$lib/organisms/PersonalProjects.svelte';
	import About from '$lib/organisms/About.svelte';

	const portfolioContent: any = {
		about: {
			description: 'I am a full stack software engineer with a passion for building scalable, reliable and secure software. I am a keen learner and enjoy working with a team to build great software.',
		},
		experiences: [
			{
				company: 'Accenture (Next Gen Engineering)',
				role: 'Full Stack Software Engineering Manager',
				duration: 'Present',
				image: 'https://media.licdn.com/dms/image/v2/C4E0BAQF-MdoC0rwXuQ/company-logo_100_100/company-logo_100_100/0/1652887987433/accenture_uk_logo?e=1747872000&v=beta&t=EtjAjEWlQll9qkncIxY9eBR7b4UQMX0yVPw-Uyy_gU0'
			},
			{
				company: 'Infinity Works (acquired by Accenture)',
				role: 'Senior Consultant',
				duration: 'Apr. 2021 to Nov. 2021',
				image: 'https://images.crunchbase.com/image/upload/v1473415844/vxbvjn01j1daqypambq6.png'
			},
			{
				company: 'Daisy Group',
				role: 'AWS Solutions Architect',
				duration: 'Jan. 2019 to Apr. 2021',
				image: 'https://media.licdn.com/dms/image/v2/C4E0BAQGNMFgcATbdTA/company-logo_100_100/company-logo_100_100/0/1631306437825?e=1747872000&v=beta&t=NI0kAaK6O426dIJ5XtrtSqxbf8uVvZmjIJ_QXzKWgk4'
			},
			{
				company: 'Elder Studios',
				role: 'Senior Software Engineer',
				duration: 'Apr. 2016 to Dec. 2018',
				image: 'https://media.licdn.com/dms/image/v2/C4E0BAQHAgQveJUJz0A/company-logo_100_100/company-logo_100_100/0/1630595157627/elder_studios_ltd_logo?e=1747872000&v=beta&t=dXDolZ-Rggqqq2C1MRUIsSo2g21uiyjNG_rXfwkQ714'
			}
		],
		education: {
			image: 'https://media.licdn.com/dms/image/v2/C4E0BAQEnX6Ob8rqI6g/company-logo_100_100/company-logo_100_100/0/1630576130472/university_of_huddersfield_logo?e=1747872000&v=beta&t=WYsGYzZf7k-uKzZj5PGY62zTblnpy1S-iLq5s44WzaA',
			school: 'University of Huddersfield',
			degree: '1st, Computing (BSc) Hons',
			graduationYear: '2012-2016'
		},
		skills: [
			{
				icon: `<i class="text-lg text-primary devicon-amazonwebservices-plain-wordmark"></i>`,
				text: 'AWS'
			},
			{
				icon: `<i class="text-lg text-primary devicon-kubernetes-plain"></i>`,
				text: 'Kubernetes'
			},
			{
				icon: `<i class="text-lg text-primary devicon-java-plain"></i>`,
				text: 'Java'
			},
			{
				icon: `<i class="text-lg text-primary devicon-typescript-plain"></i>`,
				text: 'TypeScript'
			},
			{
				icon: `<i class="text-lg text-primary devicon-python-plain"></i>`,
				text: 'Python'
			},
			{
				icon: `<i class="text-lg text-primary devicon-postgresql-plain"></i>`,
				text: 'Postgresql'
			},
			{
				icon: `<i class="text-lg text-primary devicon-quarkus-plain"></i>`,
				text: 'Quarkus'
			},
			{
				icon: `<i class="text-lg text-primary devicon-spring-plain"></i>`,
				text: 'Spring'
			},
			{
				icon: `<i class="text-lg text-primary devicon-svelte-plain"></i>`,
				text: 'Svelte'
			},
			{
				icon: `<i class="text-lg text-primary devicon-tailwindcss-plain"></i>`,
				text: 'Tailwind'
			},
			{
				icon: `<i class="text-lg text-primary devicon-github-original"></i>`,
				text: 'Github'
			}
		],
		projects: [
			{
				name: 'Jaguar Land Rover',
				technology: 'Java::AWS::Serverless',
				description: 'Tech lead for the new event driven ECU provisioning architecture on JLRs new software defined ' +
					'vehicle platform. Leading JLR by example in the use of serverless technologies.',
				image: 'jlr.png',
				link: 'https://media.jaguarlandrover.com/news/2018/06/jaguar-land-rover-opens-manchester-hub-developing-next-generation-connected-cars'
			},
			{
				name: 'Sainsbury\'s Nectar',
				technology: 'Java::AWS::Kubernetes',
				description: 'A flagship loyalty program for Sainsbury\'s, delievering hyper personalised discounts to ' +
					'customers, with over 2 million active users. Managing iOS, Android, Web and backend infrastructure.',
				image: 'sainsburys.webp',
				link: 'https://www.about.sainsburys.co.uk/news/latest-news/2021/16-09-2021-sainsburys-gets-personal-with-launch-of-tailored-my-nectar-prices'
			},
			{
				name: 'Ram Tracking',
				technology: 'Java::AWS::Fargate',
				description: 'Tech lead on the rebuild of the backend for a GPS fleet tracking system. Re-platformed from ' +
					'on-premise to AWS, with a focus on scalability and stability.',
				image: 'ram.png',
				link: 'https://www.ramtracking.com/interactive-demos/ram-tracking/'
			},
			{
				name: 'Meter Manager',
				technology: 'Java::AWS',
				description: 'A java backend for managing fleets of smart meters, securely connecting to meters, pulling data for windfarms, solar, or billing, processing data in modern dashboards.',
				image: 'mm.png',
				link: 'https://metermanager.co.uk/'
			}
		]
	};

</script>
<div>
	<About data={portfolioContent.about} />
	<Experience data={portfolioContent.experiences} />
	<Education data={portfolioContent.education} />
	<Skills data={portfolioContent.skills} />
	<PersonalProjects data={portfolioContent.projects} />
</div>

