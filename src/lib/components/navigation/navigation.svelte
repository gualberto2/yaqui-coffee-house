<script lang="ts">
	import logo from '$lib/images/logo.png';
	import * as Sheet from '$lib/components/ui/sheet/index.js';
	import { Instagram, Menu, Phone, User } from 'lucide-svelte';
	import Button from '../ui/button/button.svelte';

	const links = [
		{ name: 'Our Mission', href: '#our-story-section' },
		{ name: 'Contact', href: '#contact-form-section' },
		{ name: 'Location', href: '#location-section' },
		{ name: 'Hours', href: '#hours-section' },
		{
			name: 'Gift Cards',
			href: '#gift-cards'
		},
		{
			name: 'Account',
			href: 'https://www.toasttab.com/yaqui-coffee-house-chula-vista/rewardsSignup',
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
					link.name === 'Our Mission' ||
					link.name === 'Location' ||
					link.name === 'Hours' ||
					link.name === 'Gift Cards'
						? scrollToSection
						: null}
				>
					{link.name}
				</a>
			{/each}
		</div>
		<div class="flex flex-row items-center gap-5">
			<div class="flex cursor-pointer flex-row items-center justify-center gap-4 hover:underline">
				<a
					aria-label="Instagram Redirect Button"
					target="_blank"
					href="https://www.instagram.com/yaquihouse/"
				>
					<Instagram size={26} />
				</a>
				<a aria-label="Phone Call Button" href="tel:+16194003538">
					<Phone size={26} />
				</a>
				<a
					aria-label="Toast Account Redirect Button"
					target="_blank"
					href="https://www.toasttab.com/yaqui-coffee-house-chula-vista/rewardsSignup"
				>
					<User size={27} />
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
							target={link.target ? link.target : '_self'}
							class="w-full cursor-pointer rounded-2xl py-3 text-center text-3xl font-medium
						text-neutral-800 transition duration-150 ease-in hover:bg-neutral-300"
							on:click={link.name === 'Contact' ||
							link.name === 'Our Mission' ||
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
					target="_blank"
					href="https://www.instagram.com/yaquihouse/"
					class="cursor-pointer rounded-2xl p-2 text-center text-xl font-medium
				text-neutral-800 transition duration-150 ease-in hover:bg-neutral-300"
				>
					<Instagram size={40} />
				</a>
				<a
					aria-label="Yelp Link Button"
					href="tel:+16194003538"
					class="cursor-pointer rounded-2xl p-2 text-center text-xl font-medium
			text-neutral-800 transition duration-150 ease-in hover:bg-neutral-300"
				>
					<Phone size={40} />
				</a>
				<a
					aria-label="Toast User Account Link"
					target="_blank"
					href="https://www.toasttab.com/yaqui-coffee-house-chula-vista/rewardsSignup"
					class="cursor-pointer rounded-2xl p-2 text-center text-xl font-medium
			text-neutral-800 transition duration-150 ease-in hover:bg-neutral-300"
				>
					<User size={40} />
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
		class="absolute right-5 flex flex-row items-center text-center text-2xl uppercase "
		href="https://order.toasttab.com/online/yaqui-coffee-house-chula-vista"
		target="_blank">Order</Button
	>
</nav>
