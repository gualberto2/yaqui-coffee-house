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
	import ParallaxScroll from '$lib/components/ui/parallax-scroll/parallax-scroll.svelte';
	import { onMount } from 'svelte';
	import collageImage1 from '$lib/images/landing/collagePics/image1.jpg';
	import collageImage2 from '$lib/images/landing/collagePics/image2.jpg';
	import collageImage3 from '$lib/images/landing/collagePics/image3.jpg';
	import collageImage4 from '$lib/images/landing/collagePics/image4.jpg';
	import collageImage5 from '$lib/images/landing/collagePics/5image.jpg';
	import collageImage6 from '$lib/images/landing/collagePics/6.jpg';
	import collageImage7 from '$lib/images/landing/collagePics/7.jpg';
	import collageImage8 from '$lib/images/landing/collagePics/8.jpg';
	import collageImage9 from '$lib/images/landing/collagePics/9.jpg';
	import collageImage10 from '$lib/images/landing/collagePics/10.jpg';
	import collageImage11 from '$lib/images/landing/collagePics/11.jpg';
	import collageImage12 from '$lib/images/landing/collagePics/12.jpg';
	import collageImage13 from '$lib/images/landing/collagePics/13.jpg';
	import collageImage14 from '$lib/images/landing/collagePics/14.jpg';
	import collageImage15 from '$lib/images/landing/collagePics/15.jpg';
	import collageImage16 from '$lib/images/landing/collagePics/16.jpg';
	import collageImage17 from '$lib/images/landing/collagePics/17.jpg';
	import collageImage18 from '$lib/images/landing/collagePics/18.jpg';
	import giftcard from '$lib/images/gift-card.jpeg';
	import Button from '$lib/components/ui/button/button.svelte';
	import { Car, Gift, MapPin, ShoppingBag } from 'lucide-svelte';

	const collagePics = [
		collageImage1,
		collageImage2,
		collageImage3,
		collageImage4,
		collageImage5,
		collageImage6,
		collageImage10,
		collageImage8,
		collageImage9,
		collageImage7,
		collageImage11,
		collageImage12,
		collageImage13,
		collageImage18,
		collageImage14,
		collageImage17,
		collageImage16,
		collageImage15
	];

	onMount(() => {
		(window as any).hbspt.forms.create({
			portalId: '48887664',
			formId: '86c54468-9174-49c3-a719-0ee8edfcd045',
			target: '#contact-form'
		});
	});

	const image = [image1, image2, image3, image4, image5, image6, image7, image8];
</script>

<svelte:head>
	<title>Yaqui Coffee House</title>
	<meta name="Yaqui Coffee House" content="The Heart of Sonora" />
</svelte:head>
<section class="relative flex h-[30rem] items-center overflow-hidden sm:min-h-screen">
	<video
		title="Gumlet Video Player - Yaqui Coffee House"
		autoPlay
		src="https://video.gumlet.io/67e177ee68c224a51551c6bf/67e1793068c224a51551cfaf/download.mp4"
		loop
		muted
		playsinline
		class="relative z-30 h-full w-full object-cover"
	></video>
	<!-- <iframe
		loading="lazy"
		title="Gumlet video player"
		src="https://play.gumlet.io/embed/67e1793068c224a51551cfaf?preload=true&autoplay=true&loop=true&background=true&disable_player_controls=true"
		style="border:none; position: absolute; top: 0; left: 0; height: 100%; width: 100%;"
		allow="accelerometer; gyroscope; autoplay; encrypted-media; picture-in-picture; fullscreen;"
	>
	</iframe> -->

	<!-- Foreground (zoomed out) video -->
</section>

<section
	class="mx-auto my-32 flex max-w-6xl flex-col gap-10 px-8 lg:flex-row"
	id="our-story-section"
>
	<img
		src={aLittleBitAboutUs}
		alt=""
		class=" max-h-[24rem] rounded-sm object-cover lg:block lg:w-2/3"
	/>

	<div class="mt-8 flex flex-col items-center">
		<div class="flex flex-col md:space-y-5">
			<div class="flex flex-row items-center">
				<!-- <span class="mr-3 h-28 w-1 rounded-xl bg-[#1e2a4a] sm:h-20 lg:h-28"></span> -->
				<h3 class="-[-0.96px] text-4xl font-semibold leading-[125%] text-neutral-900">
					So Comfortable, You Might Forget You're Not at Home
				</h3>
			</div>
			<p class="max-w-5xl text-xl font-extralight leading-[150%] text-neutral-700">
				Yaqui Coffee House started with a deep love for coffee in my hometown in the state of
				Sonora, Mexico, also home of the indigenous Yaqui tribe. This concept brings the perfect
				fusion of specialty coffee and dynamic recipes inspired in every step of my journey. At
				Yaqui Coffee House, our culture and motto is to “Never serve anything we are not proud of”.
			</p>
		</div>
	</div>
</section>

<section class="mx-auto my-10">
	<div
		class=" felt-texture my-20 flex flex-col justify-center bg-yaqui-primary py-10 text-white sm:flex-row"
	>
		<div class="flex flex-col justify-center gap-10 sm:flex-row sm:gap-20">
			<div class="text-center sm:text-start">
				<h2 class="text-5xl">Ready For Yaqui?</h2>
				<p class="text-xl">Choose an option...</p>
			</div>
			<div class="flex flex-col items-center gap-4">
				<Button
					variant="secondary"
					size="lg"
					href="https://order.toasttab.com/online/yaqui-coffee-house-chula-vista"
					target="_blank">Order Delivery <Car /></Button
				>
				<Button
					variant="secondary"
					size="lg"
					href="https://order.toasttab.com/online/yaqui-coffee-house-chula-vista"
					target="_blank">Order Pickup <ShoppingBag /></Button
				>
				<Button
					variant="secondary"
					size="lg"
					href="https://maps.app.goo.gl/Cz7kFZg73Kx4T1tk6"
					target="_blank">Get Directions <MapPin /></Button
				>
			</div>
		</div>
	</div>

	<div>
		<div class="my-10 flex flex-col items-center justify-center gap-1.5 p-1.5 sm:flex-row">
			<h3 class=" -[-0.96px] text-center text-4xl font-semibold">Start Your Day Right</h3>
			<p class="-[1.1px] max-w-5xl text-xl font-thin">Enjoy what Sonora has to offer</p>
		</div>
	</div>

	<div class="min-h-screen">
		<ParallaxScroll images={collagePics} />
	</div>

	<!-- <div
		class="sm: mx-auto mt-48 flex h-[20rem] w-full flex-row items-center gap-2 px-2 sm:h-[30rem] sm:px-8 md:h-[45rem]"
	>
		<img src={section1image} alt="" class="h-full w-2/3 object-cover" />
		<div class="flex h-full w-1/3 flex-col gap-2 lg:pb-2">
			<img src={section1image2} alt="" class="h-1/2 object-cover" />

			<img src={section1image3} alt="" class="h-1/2 object-cover" />
		</div>
	</div> -->

	<section id="gift-cards" class="gift-card-texture w-full bg-[#8B6F5C] px-4 py-8 text-white">
		<div class=" mb-5 mt-2 flex flex-col items-center justify-center gap-1.5 p-1.5 sm:flex-row">
			<h3 class=" -[-0.96px] text-center text-4xl font-semibold">Gift Cards</h3>
			<p class="-[1.1px] max-w-5xl text-xl font-thin">
				Share the warmth of Yaqui House Coffee with someone special.
			</p>
		</div>
		<a
			href="https://www.toasttab.com/yaqui-coffee-house-chula-vista/giftcards"
			target="_blank"
			class="mx-auto flex max-w-6xl flex-row items-center justify-center gap-2 px-8 py-2 text-xl font-medium uppercase text-[#8B6F5C] transition-colors duration-300"
		>
			<img
				src={giftcard}
				alt="Yaqui House Coffee Gift Card"
				class="h-1/2 w-1/2 cursor-pointer rounded-lg object-contain shadow-md transition duration-150 ease-out hover:shadow-2xl"
			/>
		</a>
		<div class="flex w-full flex-row items-center justify-center space-y-8">
			<div class="mt-8">
				<a
					href="https://www.toasttab.com/yaqui-coffee-house-chula-vista/giftcards"
					target="_blank"
					class="flex items-center gap-2 rounded-full bg-[#E8D5C4] px-8 py-2 text-xl font-medium uppercase text-[#8B6F5C] transition-colors duration-300 hover:bg-white"
				>
					<Gift class="h-5 w-5" />
					Purchase
				</a>
			</div>
		</div>
	</section>

	<div class="my-20 flex flex-col items-center justify-center" id="location-section">
		<h3
			id="hours-section"
			class=" -[-0.96px] mb-5 text-center text-4xl font-semibold leading-[125%]"
		>
			Visit Us
		</h3>
		<a
			href="https://maps.app.goo.gl/Cz7kFZg73Kx4T1tk6"
			target="_blank"
			rel="noopener noreferrer"
			class="text-md -[1.1px] mb-4 flex cursor-pointer flex-row items-center px-1.5 text-center text-2xl font-light underline transition duration-150 ease-in-out hover:text-primary/80"
		>
			1930 Avenida Escaya suite 101, Chula Vista, CA 91913
		</a>
		<div class="-[1.1px] flex flex-col items-center justify-center gap-1.5 text-2xl leading-[150%]">
			<div class="flex flex-row items-center justify-center gap-2 font-light">
				<p>CLOSED MONDAYS</p>
			</div>
			<div class="flex flex-row items-center justify-center gap-2 font-light">
				<p>T-F</p>
				<p>|</p>
				<p>6am-4pm</p>
			</div>
			<div class="flex flex-row items-center justify-center gap-2 font-light">
				<p>S-S</p>
				<p>|</p>
				<p>7am-4pm</p>
			</div>
			<div class="flex flex-row items-center justify-center gap-2 font-light">
				<p>Kitchen</p>
				<p>|</p>
				<p>7am-1pm (Everyday)</p>
			</div>
		</div>
	</div>
</section>

<div id="contact-form-section" class="arches-texture mt-20 bg-yaqui-foreground py-10">
	<div class="mb-5 text-center text-white">
		<h4 class=" -[-0.96px] text-center text-4xl font-semibold leading-[125%] text-white">
			Get In Touch
		</h4>
	</div>
	<div class="mx-auto max-w-2xl rounded-xl bg-white p-4 text-white">
		<div id="contact-form" class="px-2 text-white"></div>
	</div>
</div>
