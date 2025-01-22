<script>
	import { Coffee, Instagram, Facebook, Twitter, Mail, Phone, MapPin } from 'lucide-svelte';
</script>

<footer
	class="sticky top-0 z-50 mx-auto mt-auto flex w-full flex-col bg-[#6a041d] px-5 py-4 text-white"
>
	<div><h2 class="text-xl text-white">Yaqui Coffee House</h2></div>
	<div>Location</div>
</footer>

<footer class="w-full bg-[#1A120B] py-12 text-[#E5E5CB]">
	<div class="mx-auto max-w-7xl px-6">
		<div class="mb-8 flex justify-center">
			<div class="flex items-center gap-2">
				<Coffee size={32} />
				<span class="text-2xl font-semibold">Brew Haven</span>
			</div>
		</div>
		<div class="mb-12 grid grid-cols-1 gap-12 md:grid-cols-3">
			<div class="space-y-4">
				<h3 class="mb-4 text-xl font-semibold">Visit Us</h3>
				<div class="flex items-center gap-2">
					<MapPin size={18} />
					<span>123 Coffee Street, Brewville</span>
				</div>
				<div class="flex items-center gap-2">
					<Phone size={18} />
					<span>(555) 123-4567</span>
				</div>
				<div class="flex items-center gap-2">
					<Mail size={18} />
					<span>hello@brewhaven.com</span>
				</div>
			</div>
			<div>
				<h3 class="mb-4 text-xl font-semibold">Quick Links</h3>
				<ul class="space-y-2">
					<li>
						<a href="/" class="transition-colors hover:text-[#D5CEA3]"> Our Story </a>
					</li>
					<li>
						<a href="/" class="transition-colors hover:text-[#D5CEA3]"> Menu </a>
					</li>
					<li>
						<a href="/" class="transition-colors hover:text-[#D5CEA3]"> Coffee Guide </a>
					</li>
					<li>
						<a href="/" class="transition-colors hover:text-[#D5CEA3]"> Events </a>
					</li>
				</ul>
			</div>
			<div>
				<h3 class="mb-4 text-xl font-semibold">Stay Connected</h3>
				<p class="mb-4">Join our newsletter for brewing tips and special offers!</p>
				<div class="flex gap-2">
					<input
						type="email"
						placeholder="Your email"
						class="rounded border border-[#D5CEA3] bg-[#3C2A21] px-4 py-2 focus:border-[#E5E5CB] focus:outline-none"
					/>
					<button
						class="rounded bg-[#D5CEA3] px-4 py-2 text-[#1A120B] transition-colors hover:bg-[#E5E5CB]"
					>
						Subscribe
					</button>
				</div>
			</div>
		</div>
		<div
			class="flex flex-col items-center justify-between gap-4 border-t border-[#3C2A21] pt-8 md:flex-row"
		>
			<div class="flex gap-6">
				<a href="/" class="transition-colors hover:text-[#D5CEA3]">
					<Instagram size={24} />
				</a>
				<a href="/" class="transition-colors hover:text-[#D5CEA3]">
					<Facebook size={24} />
				</a>
				<a href="/" class="transition-colors hover:text-[#D5CEA3]">
					<Twitter size={24} />
				</a>
			</div>
			<p class="text-sm">© 2023 Brew Haven. All rights reserved.</p>
		</div>
	</div>
</footer>
