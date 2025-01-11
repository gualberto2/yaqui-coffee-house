<script lang="ts">
	import image1 from '$lib/images/landing/parallax-image-1.jpg';
	import image2 from '$lib/images/landing/parallax-image-2.jpg';
	import image3 from '$lib/images/landing/parallax-image-3.jpg';
	import image4 from '$lib/images/landing/parallax-image-4.jpg';
	import image5 from '$lib/images/landing/parallax-image-5.jpg';
	import image6 from '$lib/images/landing/parallax-image-6.jpg';
	import image7 from '$lib/images/landing/parallax-image-7.jpg';
	import image8 from '$lib/images/landing/parallax-image-8.jpg';
	import aLittleBitAboutUs from '$lib/images/landing/a-little-bit-about-us.jpg';
	import section1image from '$lib/images/landing/section-1-image.jpg';
	import section1image2 from '$lib/images/landing/section-1-image-2.jpg';
	import section1image3 from '$lib/images/landing/section-1-image-3.jpg';
	import Button from '$lib/components/ui/button/button.svelte';
	import ParallaxScroll from '$lib/components/ui/parallax-scroll/parallax-scroll.svelte';

	const image = [image1, image2, image3, image4, image5, image6, image7, image8];
</script>

<section class="hero-bg flex h-[40rem] flex-col items-center bg-black/60">
	<div class="pt-48">
		<!-- <h1 class="font-hero z-auto mx-auto text-center text-[120px] leading-[90%] text-white">
			Yaqui
		</h1> -->
		<!-- <h2 class=" mx-auto text-center text-4xl font-medium text-white uppercase">Coffee House</h2> -->
		<!-- <div class="flex flex-row items-center justify-center gap-2 pt-5">
			<Button size="lg" class="	bg-amber-600">Order Online</Button>
			<Button size="lg" variant="secondary">Get Directions</Button>
		</div> -->
	</div>
</section>

<section class="mx-auto my-10">
	<div class="my-20 flex flex-col items-center justify-center">
		<h3
			class=" mb-5 text-center text-4xl font-semibold capitalize leading-[125%] tracking-[-0.96px]"
		>
			Visit Us
		</h3>
		<a
			href="https://maps.app.goo.gl/Cz7kFZg73Kx4T1tk6"
			target="_blank"
			rel="noopener noreferrer"
			class="text-md mb-4 cursor-pointer text-center text-lg font-light leading-[150%] tracking-[110%] underline transition duration-150 ease-in-out hover:text-gray-500"
		>
			1930 Avenida Escaya suite 101, Chula Vista, CA 91913
		</a>
		<div class="flex flex-col items-center justify-center gap-1.5 leading-[150%] tracking-[110%]">
			<div class="flex flex-row items-center justify-center gap-2 text-lg font-light">
				<p>M-F</p>
				<p>|</p>
				<p>6am-4pm</p>
			</div>
			<div class="flex flex-row items-center justify-center gap-2 text-lg font-light">
				<p>S-S</p>
				<p>|</p>
				<p>7am-4pm</p>
			</div>
			<div class="flex flex-row items-center justify-center gap-2 text-lg font-light">
				<p>Kitchen</p>
				<p>|</p>
				<p>7am-1pm (Everyday)</p>
			</div>
		</div>
	</div>
	<div
		class="sm: mx-auto flex h-[20rem] w-full flex-row items-center gap-2 px-2 sm:h-[30rem] sm:px-8 md:h-[35rem]"
	>
		<img src={section1image2} alt="" class="h-full w-2/3 object-cover" />
		<div class="flex h-full w-1/3 flex-col gap-2 lg:pb-2">
			<img src={section1image} alt="" class="h-1/2 object-cover" />
			<img src={section1image3} alt="" class="h-1/2 object-cover" />
		</div>
	</div>
	<div class=" my-20 flex flex-col justify-center gap-5 px-8 lg:flex-row">
		<h3 class=" text-center text-4xl font-semibold capitalize leading-[125%] tracking-[-0.96px]">
			Start Your Day Right.
		</h3>
		<p class="max-w-5xl text-lg font-extralight leading-[150%] tracking-[110%]">
			Nestled in the heart of Chula Vista, CA, Yaqui Coffee House exudes warmth and welcomes guests
			with open arms. With its cozy atmosphere, friendly staff, and a menu bursting with
			mouthwatering dishes, it's the perfect place to unwind and savor a delightful meal. Our
			diverse menu caters to every palate, whether you're looking for a leisurely dinner with loved
			ones, a quick lunch catch-up with friends, or a solo meal at the bar. Yaqui Coffee House
			offers a relaxed setting where laughter flows as freely as the conversation. Come as you are,
			and leave with a satisfied heart, a full stomach, and a smile.
		</p>
	</div>

	<div class="mt-12 flex-row px-8 md:flex md:space-x-10">
		<img src={aLittleBitAboutUs} alt="" class=" rounded-sm object-cover md:w-2/3 lg:block" />

		<div class="mt-8 flex flex-col items-center space-y-10">
			<div class="flex flex-col md:space-y-5">
				<div class="flex flex-row items-center">
					<!-- <span class="mr-3 h-28 w-1 rounded-xl bg-[#1e2a4a] sm:h-20 lg:h-28"></span> -->
					<h3 class="text-4xl font-semibold capitalize leading-[125%] tracking-[-0.96px]">
						So Comfortable, You Might Forget You're Not at Home.
					</h3>
				</div>
				<p class="max-w-5xl text-lg font-extralight leading-[150%] tracking-[110%]">
					Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quibusdam voluptates eos autem
					sunt, magnam quae atque similique dolore! Provident aliquam maiores cumque ipsa minus
					adipisci obcaecati mollitia tempora et deserunt?
				</p>
			</div>
			<!-- <div class="flex flex-col md:space-y-5">
				<div class="flex flex-row items-center">
					<span class="mr-3 h-10 w-1 rounded-xl bg-[#1e2a4a]"></span>
					<h3 class=" text-4xl font-medium capitalize leading-[125%] tracking-[-0.96px]">
						A Litte Bit About Us.
					</h3>
				</div>
				<p class="text-normal font-normal leading-[150%]">
					Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quibusdam voluptates eos autem
					sunt, magnam quae atque similique dolore! Provident aliquam maiores cumque ipsa minus
					adipisci obcaecati mollitia tempora et deserunt?
				</p>
				<p
					class="cursor-pointer font-light underline decoration-neutral-800 transition duration-100 ease-in hover:text-neutral-500 hover:decoration-neutral-500"
				>
					Explore our story →
				</p>
			</div> -->
		</div>
	</div>
</section>
