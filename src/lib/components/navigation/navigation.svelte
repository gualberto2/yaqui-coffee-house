<script lang="ts">
	import logo from '$lib/images/logo.png';
	import * as Sheet from '$lib/components/ui/sheet/index.js';
	import { Instagram, Menu, Phone } from 'lucide-svelte';
	import Button from '../ui/button/button.svelte';

	const links = [
		{ name: 'Our Story', href: '#our-story-section' },
		{ name: 'Contact', href: '#contact-form-section' },
		{ name: 'Location', href: '#location-section' },
		{ name: 'Hours', href: '#hours-section' },
		{
			name: 'Menu',
			href: 'https://order.toasttab.com/online/yaqui-coffee-house-chula-vista',
			target: '_blank'
		}
	];

	function scrollToSection(event) {
		event.preventDefault();
		const targetId = event.currentTarget.getAttribute('href').substring(1);
		const targetElement = document.getElementById(targetId);
		if (targetElement) {
			targetElement.scrollIntoView({ behavior: 'smooth' });
		}
	}
</script>

<nav class="mx-10 hidden flex-row items-center justify-between py-3 lg:flex">
	<div class="">
		<a href="/" class="duration-400 flex h-32 items-center justify-center overflow-hidden">
			<img src={logo} alt="Logo" class="duration-400 h-full object-cover transition-[height]" />
		</a>
	</div>
	<div class="g items-cente flex flex-row gap-5">
		<div class="flex flex-row items-center gap-5">
			{#each links as link}
				<a
					href={link.href}
					target={link.target ? link.target : '_self'}
					class="cursor-pointer text-2xl text-neutral-800 underline-offset-1 hover:underline"
					on:click={link.name === 'Contact' ||
					link.name === 'Our Story' ||
					link.name === 'Location' ||
					link.name === 'Hours'
						? scrollToSection
						: null}
				>
					{link.name}
				</a>
			{/each}
		</div>
		<div class="flex flex-row items-center gap-5">
			<div class="flex cursor-pointer flex-row items-center justify-center gap-4 hover:underline">
				<a target="_blank" href="https://www.instagram.com/yaquihouse/">
					<Instagram />
				</a>
				<a href="tel:+16194003538" class="flex items-center gap-2">
					<Phone size={18} />
				</a>
			</div>
		</div>
		<Button
			size="lg"
			variant="default"
			class="ml-6 uppercase"
			href="https://order.toasttab.com/online/yaqui-coffee-house-chula-vista"
			target="_blank">Order Online</Button
		>
	</div>
</nav>

<nav class="relative flex flex-row items-center justify-center px-6 py-2 lg:hidden">
	<Sheet.Root>
		<Sheet.Trigger class="absolute left-5 block  "><Menu class="h-8 w-8" /></Sheet.Trigger>
		<Sheet.Content side="left" size="lg" class=" w-full space-y-10">
			<div class="mt-20 flex w-full flex-col items-center justify-center gap-5 px-10">
				{#each links as link}
					<Sheet.Close
						autofocus={false}
						class="flex w-full flex-col items-center justify-center gap-5  uppercase"
					>
						<a
							href={link.href}
							class="w-full cursor-pointer rounded-2xl py-3 text-center text-3xl font-medium
						text-neutral-800 transition duration-150 ease-in hover:bg-neutral-300"
							on:click={link.name === 'Contact' ||
							link.name === 'Our Story' ||
							link.name === 'Location' ||
							link.name === 'Hours'
								? scrollToSection
								: null}
						>
							{link.name}
						</a>
					</Sheet.Close>
				{/each}
			</div>
			<div class="flex flex-row items-center justify-center gap-8">
				<a
					aria-label="Instagram Link Button"
					href="/"
					class="cursor-pointer rounded-2xl p-2 text-center text-xl font-medium
				text-neutral-800 transition duration-150 ease-in hover:bg-neutral-300"
				>
					<Instagram class="h-10 w-10" />
				</a>
				<a
					aria-label="Yelp Link Button"
					href="/"
					class="cursor-pointer rounded-2xl p-2 text-center text-xl font-medium
			text-neutral-800 transition duration-150 ease-in hover:bg-neutral-300"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="40"
						height="40"
						fill="currentColor"
						class="bi bi-yelp"
						viewBox="0 0 16 16"
					>
						<path
							d="m4.188 10.095.736-.17.073-.02A.813.813 0 0 0 5.45 8.65a1 1 0 0 0-.3-.258 3 3 0 0 0-.428-.198l-.808-.295a76 76 0 0 0-1.364-.493C2.253 7.3 2 7.208 1.783 7.14c-.041-.013-.087-.025-.124-.038a2.1 2.1 0 0 0-.606-.116.72.72 0 0 0-.572.245 2 2 0 0 0-.105.132 1.6 1.6 0 0 0-.155.309c-.15.443-.225.908-.22 1.376.002.423.013.966.246 1.334a.8.8 0 0 0 .22.24c.166.114.333.129.507.141.26.019.513-.045.764-.103l2.447-.566zm8.219-3.911a4.2 4.2 0 0 0-.8-1.14 1.6 1.6 0 0 0-.275-.21 2 2 0 0 0-.15-.073.72.72 0 0 0-.621.031c-.142.07-.294.182-.496.37-.028.028-.063.06-.094.089-.167.156-.353.35-.574.575q-.51.516-1.01 1.042l-.598.62a3 3 0 0 0-.298.365 1 1 0 0 0-.157.364.8.8 0 0 0 .007.301q0 .007.003.013a.81.81 0 0 0 .945.616l.074-.014 3.185-.736c.251-.058.506-.112.732-.242.151-.088.295-.175.394-.35a.8.8 0 0 0 .093-.313c.05-.434-.178-.927-.36-1.308M6.706 7.523c.23-.29.23-.722.25-1.075.07-1.181.143-2.362.201-3.543.022-.448.07-.89.044-1.34-.022-.372-.025-.799-.26-1.104C6.528-.077 5.644-.033 5.04.05q-.278.038-.553.104a8 8 0 0 0-.543.149c-.58.19-1.393.537-1.53 1.204-.078.377.106.763.249 1.107.173.417.41.792.625 1.185.57 1.036 1.15 2.066 1.728 3.097.172.308.36.697.695.857q.033.015.068.025c.15.057.313.068.469.032l.028-.007a.8.8 0 0 0 .377-.226zm-.276 3.161a.74.74 0 0 0-.923-.234 1 1 0 0 0-.145.09 2 2 0 0 0-.346.354c-.026.033-.05.077-.08.104l-.512.705q-.435.591-.861 1.193c-.185.26-.346.479-.472.673l-.072.11c-.152.235-.238.406-.282.559a.7.7 0 0 0-.03.314c.013.11.05.217.108.312q.046.07.1.138a1.6 1.6 0 0 0 .257.237 4.5 4.5 0 0 0 2.196.76 1.6 1.6 0 0 0 .349-.027 2 2 0 0 0 .163-.048.8.8 0 0 0 .278-.178.7.7 0 0 0 .17-.266c.059-.147.098-.335.123-.613l.012-.13c.02-.231.03-.502.045-.821q.037-.735.06-1.469l.033-.87a2.1 2.1 0 0 0-.055-.623 1 1 0 0 0-.117-.27Zm5.783 1.362a2.2 2.2 0 0 0-.498-.378l-.112-.067c-.199-.12-.438-.246-.719-.398q-.644-.353-1.295-.695l-.767-.407c-.04-.012-.08-.04-.118-.059a2 2 0 0 0-.466-.166 1 1 0 0 0-.17-.018.74.74 0 0 0-.725.616 1 1 0 0 0 .01.293c.038.204.13.406.224.583l.41.768q.341.65.696 1.294c.152.28.28.52.398.719q.036.057.068.112c.145.239.261.39.379.497a.73.73 0 0 0 .596.201 2 2 0 0 0 .168-.029 1.6 1.6 0 0 0 .325-.129 4 4 0 0 0 .855-.64c.306-.3.577-.63.788-1.006q.045-.08.076-.165a2 2 0 0 0 .051-.161q.019-.083.029-.168a.8.8 0 0 0-.038-.327.7.7 0 0 0-.165-.27"
						/>
					</svg>
				</a>
			</div>
		</Sheet.Content>
	</Sheet.Root>
	<a
		href="/"
		class="duration-400 flex h-20
		   items-center justify-center overflow-hidden transition-[height]"
	>
		<img src={logo} alt="Logo" class="duration-400 h-full object-cover transition-[height]" />
	</a>
	<Button
		size="default"
		class="absolute right-5 block pb-1 text-center uppercase "
		href="https://order.toasttab.com/online/yaqui-coffee-house-chula-vista"
		target="_blank">Order</Button
	>
</nav>
