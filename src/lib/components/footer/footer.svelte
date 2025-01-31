<script lang="ts">
	import { Coffee, Instagram, Facebook, Twitter, Mail, Phone, MapPin } from 'lucide-svelte';

	const links = [
		{
			name: 'Menu',
			href: 'https://order.toasttab.com/online/yaqui-coffee-house-chula-vista',
			target: '_blank'
		},
		{ name: 'Our Story', href: '#our-story-section' },
		{ name: 'Hours', href: '#hours-section' },
		{ name: 'Location', href: '#location-section' },
		{ name: 'Contact', href: '#contact-form-section' }
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

<!-- bg-[#1A120B] py-12 text-[#E5E5CB] -->
<!-- bg-[#6a041d] text-[#E5E5CB]-->

<footer class="w-full bg-yaqui-foreground py-12 text-white">
	<div class="mx-auto max-w-7xl px-6">
		<div class="mb-8 flex justify-center">
			<a href="/" class="flex items-center gap-2">
				<Coffee size={32} />
				<span class=" text-4xl font-semibold">Yaqui Coffee House</span>
			</a>
		</div>
		<div class="mb-12 flex flex-col justify-center gap-12 md:flex-row md:gap-20 lg:gap-32">
			<div class="space-y-4">
				<h3 class="mb-4 text-3xl font-semibold">Visit Us</h3>
				<a
					href="https://maps.app.goo.gl/Cz7kFZg73Kx4T1tk6"
					target="_blank"
					rel="noopener noreferrer"
					class="flex items-center gap-2 text-xl transition-colors"
				>
					<MapPin size={18} />
					<span class="">1930 Avenida Escaya suite 101,<br /> Chula Vista, CA 91913</span>
				</a>
				<a href="tel:+16194003538" class="flex items-center gap-2">
					<Phone size={18} />
					<span class="text-xl">(619) 400-3538</span>
				</a>
				<div class="flex cursor-pointer items-center gap-2">
					<Mail size={18} />
					<span class="text-xl">info@yaquicoffeehouse.com</span>
				</div>
			</div>
			<div>
				<h3 class="mb-4 text-3xl font-semibold">Quick Links</h3>
				<ul class="flex flex-col space-y-2">
					{#each links as link}
						<a
							href={link.href}
							target={link.target ? link.target : '_self'}
							class="text-xl transition-colors hover:text-[#D5CEA3]"
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
				</ul>
			</div>
			<div>
				<h3 class="mb-4 text-3xl font-semibold">Stay Connected</h3>
				<p class="mb-4 text-xl">Join our newsletter for brewing tips and special offers!</p>
				<div class="flex flex-col gap-2 sm:flex-row">
					<input
						type="email"
						placeholder="Your email"
						class="rounded border border-[#E90C3C] bg-[#27020A] px-4 py-2 uppercase placeholder:uppercase focus:border-[#C20A32] focus:outline-none"
					/>
					<button
						class="rounded bg-white px-4 py-2 uppercase text-[#1A120B] transition-colors hover:bg-[#E5E5CB]"
					>
						Subscribe
					</button>
				</div>
			</div>
		</div>
		<div
			class="flex flex-col items-center justify-between gap-4 border-t border-white pt-8 md:flex-row"
		>
			<div class="flex gap-6">
				<a href="/" class="transition-colors hover:text-[#D5CEA3]">
					<Instagram size={24} />
				</a>
				<a
					target="_blank"
					href="https://www.facebook.com/people/YAQUI-Coffee-House/61566139258989/?mibextid=wwXIfr"
					class="transition-colors hover:text-[#D5CEA3]"
				>
					<Facebook size={24} />
				</a>
				<a href="/" class="transition-colors hover:text-[#D5CEA3]">
					<Twitter size={24} />
				</a>
			</div>
			<p class="text-lg">© 2025 Yaqui Coffee House. All rights reserved.</p>
		</div>
	</div>
</footer>

<style>
	a {
		cursor: pointer;
	}
</style>
