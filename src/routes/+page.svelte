<script lang="ts">
	import image1 from '$lib/images/landing/parallax-image-1.jpg';
	import image2 from '$lib/images/landing/parallax-image-2.jpg';
	import image3 from '$lib/images/landing/parallax-image-3.jpg';
	import image4 from '$lib/images/landing/parallax-image-4.jpg';
	import image5 from '$lib/images/landing/parallax-image-5.jpg';
	import image6 from '$lib/images/landing/parallax-image-6.jpg';
	import image7 from '$lib/images/landing/parallax-image-7.jpg';
	import image8 from '$lib/images/landing/parallax-image-8.jpg';
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

<section class="my-10">
	<div
		class="mx-auto flex h-[20rem] w-full max-w-7xl flex-row items-center space-x-2 px-2 sm:h-[30rem] md:h-[35rem]"
	>
		<img src={section1image2} alt="" class="h-full w-2/3 object-cover" />
		<div class="flex h-full w-1/3 flex-col space-y-2">
			<img src={section1image} alt="" class="h-1/2 object-cover" />
			<img src={section1image3} alt="" class="h-1/2 object-cover" />
		</div>
	</div>
	<div>
		<!-- <ParallaxScroll images={image} /> -->
	</div>
</section>
