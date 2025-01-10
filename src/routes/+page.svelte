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
		<h1 class="font-hero z-auto mx-auto text-center text-[120px] leading-[90%] text-white">
			Yaqui
		</h1>
		<h2 class=" mx-auto text-center text-4xl font-medium text-white">Coffee House</h2>
		<div class="flex flex-row items-center justify-center gap-2 pt-5">
			<Button class="	bg-amber-600">Order Online</Button>
			<Button variant="secondary">Get Directions</Button>
		</div>
	</div>
</section>

<section class="mx-auto my-10 max-w-[100rem]">
	<div
		class="sm: mx-auto flex h-[20rem] w-full flex-row items-center gap-2 px-2 sm:h-[30rem] sm:px-8 md:h-[35rem]"
	>
		<img src={section1image2} alt="" class="h-full w-2/3 object-cover" />
		<div class="flex h-full w-1/3 flex-col gap-2 lg:pb-2">
			<img src={section1image} alt="" class="h-1/2 object-cover" />
			<img src={section1image3} alt="" class="h-1/2 object-cover" />
		</div>
	</div>

	<div class="mx-4 mt-12 flex-row sm:mx-8 md:flex md:space-x-10">
		<img src={aLittleBitAboutUs} alt="" class="hidden w-2/3 rounded-sm object-cover lg:block" />

		<div class="mt-4 flex flex-col items-center space-y-10">
			<div class="flex flex-col md:space-y-5">
				<div class="flex flex-row items-center">
					<span class="mr-3 h-28 w-1 rounded-xl bg-[#1e2a4a] sm:h-20 lg:h-28"></span>
					<h3 class=" text-4xl font-medium capitalize leading-[125%] tracking-[-0.96px]">
						So Comfortable, You Might Forget You're Not at Home.
					</h3>
				</div>
				<p class="text-normal font-normal leading-[150%]">
					Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quibusdam voluptates eos autem
					sunt, magnam quae atque similique dolore! Provident aliquam maiores cumque ipsa minus
					adipisci obcaecati mollitia tempora et deserunt?
				</p>
			</div>
			<div class="flex flex-col md:space-y-5">
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
					class="font-light underline decoration-neutral-800 transition duration-100 ease-in hover:text-neutral-500 hover:decoration-neutral-500"
				>
					Explore our story ->
				</p>
			</div>
		</div>
	</div>

	<div class=""></div>
</section>
