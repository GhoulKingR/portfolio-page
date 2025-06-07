<script>
	import logo from '$lib/assets/logo.svg';
	import graphicsDesign from '$lib/assets/pattern-graphic-design.svg';
	import uiux from '$lib/assets/pattern-ui-ux.svg';
	import apps from '$lib/assets/pattern-apps.svg';
	import illustrations from '$lib/assets/pattern-illustrations.svg';
	import photography from '$lib/assets/pattern-photography.svg';
	import motionGraphics from '$lib/assets/pattern-motion-graphics.svg';
	import hero from '$lib/assets/image-amy.webp';

	import slide1 from '$lib/assets/image-slide-1.jpg';
	import slide2 from '$lib/assets/image-slide-2.jpg';
	import slide3 from '$lib/assets/image-slide-3.jpg';
	import slide4 from '$lib/assets/image-slide-4.jpg';
	import slide5 from '$lib/assets/image-slide-5.jpg';

	import arrowLeft from '$lib/assets/icon-arrow-left.svg';
	import arrowRight from '$lib/assets/icon-arrow-right.svg';

	/**
	 *
	 * @param {number} n1
	 * @param {number} n2
	 * @returns {number}
	 */
	function mod(n1, n2) {
		'use strict';
		return ((n1 % n2) + n2) % n2;
	}

	const slides = [slide1, slide2, slide3, slide4, slide5];
	let pos = $state(0);
	let toDisplay = $derived.by(() => {
		const left = slides[mod(pos - 1, slides.length)];
		const center = slides[pos];
		const right = slides[mod(pos + 1, slides.length)];
		return [left, center, right];
	});
</script>

<header
	class="flex justify-between mx-[16px] my-[24px] mb-[16px] md:mx-[32px] md:mb-[40px] xl:w-[1110px] xl:mx-auto xl:mt-[32px] xl:mb-[80px]"
>
	<img src={logo} alt="logo" class="w-[48px] h-[48px] md:w-[64px] md:h-[64px]" />
	<button
		class="bg-black pt-[12px] pb-[16px] px-[24px] md:px-[48px] text-white rounded-full font-semibold text-[16px] hover:bg-[#755CDE] cursor-pointer focus:outline-offset-2 focus:outline-2 focus:outline-[#755CDE] focus:bg-[#030303]"
		>Free consultation</button
	>
</header>

<main class="mb-[8px] md:mb-[24px] xl:mb-[48px]">
	<section
		class="text-center mb-[40px] md:mb-[64px] xl:mb-[80px] xl:w-[1110px] mx-[16px] md:mx-[32px] xl:mx-auto"
	>
		<h1
			class="text-[#030303] font-semibold text-[40px] leading-[120%] mb-[20px] md:text-[56px] md:leading-[130%] md:w-[538px] md:mx-auto xl:w-[762px]"
		>
			Design solutions made easy
		</h1>
		<p class="text-[#6a6662] font-normal text-[18px] leading-[28px] md:w-[596px] md:mx-auto">
			With over ten years of experience in various design disciplines, I’m your one-stop shop for
			your design needs.
		</p>
	</section>

	<section
		class="grid grid-cols-2 md:grid-rows-3 md:grid-cols-4 xl:grid-cols-6 xl:grid-rows-2 gap-[20px] mb-[64px] md:mb-[80px] xl:mb-[120px] xl:w-[1110px] mx-[16px] md:mx-[32px] xl:mx-auto"
	>
		<div class="col-span-2 md:row-span-2 p-[20px] bg-[#755cde] rounded-[8px]">
			<img
				src={graphicsDesign}
				alt="Graphics Design"
				class="ml-auto mb-[101px] w-[128px] h-[192px]"
			/>
			<div class="text-white font-medium text-[24px] leading-[130%]">Graphics Design</div>
		</div>
		<div class="p-[20px] bg-[#ec9b56] rounded-[8px]">
			<img src={uiux} alt="UI/UX" class="w-[64px] h-[64px] ml-auto mb-[47px]" />
			<div class="text-white font-medium text-[24px] leading-[130%]">UI/UX</div>
		</div>
		<div class="p-[20px] bg-[#f39e9e] rounded-[8px]">
			<img src={apps} alt="Apps" class="w-[64px] h-[64px] ml-auto mb-[47px]" />
			<div class="text-white font-medium text-[24px] leading-[130%]">Apps</div>
		</div>
		<div class="col-span-2 p-[20px] bg-[#e16b5b] rounded-[8px]">
			<img src={illustrations} alt="Illustrations" class="ml-auto mb-[27px] w-[128px] h-[64px]" />
			<div class="text-white font-medium text-[24px] leading-[130%]">Illustrations</div>
		</div>
		<div class="col-span-2 p-[20px] bg-[#61c4b7] rounded-[8px]">
			<img src={photography} alt="Photography" class="ml-auto mb-[27px] w-[160px] h-[64px]" />
			<div class="text-white font-medium text-[24px] leading-[130%]">Photography</div>
		</div>
		<div class="col-span-2 p-[20px] bg-[#552049] rounded-[8px]">
			<img
				src={motionGraphics}
				alt="Motion Graphics"
				class="ml-auto mb-[27px] w-[128px] h-[64px]"
			/>
			<div class="text-white font-medium text-[24px] leading-[130%]">Motion Graphics</div>
		</div>
	</section>

	<section
		class="text-center mb-[64px] md:mb-[80px] xl:flex items-center xl:mb-[120px] xl:w-[1110px] mx-[16px] md:mx-[32px] xl:mx-auto"
	>
		<img
			src={hero}
			alt="hero"
			class="w-[300px] h-[300px] mx-auto mb-[24px] xl:w-[445px] xl:h-[445px] xl:mr-[125px] xl:mb-[0px]"
		/>

		<div class="xl:text-left">
			<h1 class="text-[#030303] text-[40px] leading-[130%] font-semibold mb-[20px]">
				I’m Amy, and I’d love to work on your next project
			</h1>
			<p class="text-[#6a6662] text-[18px] font-normal leading-[150%] mb-[32px]">
				I love working with others to create beautiful design solutions. I’ve designed everything
				from brand illustrations to complete mobile apps. I’m also handy with a camera!
			</p>
			<button
				class="bg-[#e16b5b] py-[16px] px-[48px] text-white font-semibold text-[16px] leading-[150%] rounded-full cursor-pointer hover:bg-[#F6A560] focus:outline-offset-2 focus:outline-2 focus:outline-[#F6A560] focus:bg-[#F6A560]"
				>Free consultation</button
			>
		</div>
	</section>

	<section class="mb-[64px] overflow-x-hidden pb-[4px]">
		<h1
			class="text-[#030303] font-semibold text-[40px] leading-[120%] mb-[40px] w-fit mx-auto xl:mb-[48px]"
		>
			My work
		</h1>

		<div class="mb-[40px] xl:mb-[48px]">
			<div class="relative flex justify-center space-x-[20px] xl:space-x-[32px]">
				<img src={toDisplay[0]} alt="slide 1" class="rounded-[8px] w-[70%] h-auto" />
				<img src={toDisplay[1]} alt="slide 2" class="rounded-[8px] w-[70%] h-auto" />
				<img src={toDisplay[2]} alt="slide 3" class="rounded-[8px] w-[70%] h-auto" />
			</div>
		</div>

		<div class="w-fit mx-auto grid grid-cols-2 gap-[16px]">
			<button
				class="w-[48px] h-[48px] md:w-[64px] md:h-[64px] bg-[#030303] flex justify-center items-center rounded-full hover:bg-[#755CDE] cursor-pointer focus:outline-offset-2 focus:outline-2 focus:outline-[#755CDE] focus:bg-[#030303]"
				onclick={() => {
					pos = mod(pos - 1, slides.length);
				}}><img src={arrowLeft} alt="left" class="w-[15px] h-[16px]" /></button
			>
			<button
				class="w-[48px] h-[48px] md:w-[64px] md:h-[64px] bg-[#030303] flex justify-center items-center rounded-full hover:bg-[#755CDE] cursor-pointer focus:outline-offset-2 focus:outline-2 focus:outline-[#755CDE] focus:bg-[#030303]"
				onclick={() => {
					pos = mod(pos + 1, slides.length);
				}}><img src={arrowRight} alt="right" class="w-[15px] h-[16px]" /></button
			>
		</div>
	</section>

	<section
		class="text-center bg-[#030303] px-[16px] py-[40px] rounded-[10px] xl:w-[1110px] mx-[16px] md:mx-[32px] xl:mx-auto xl:flex xl:space-x-[208px] xl:items-center xl:px-[64px] xl:py-[81.5px]"
	>
		<div class="xl:w-[540px] xl:text-left">
			<h1
				class="text-[#fff7f0] text-[40px] font-semibold leading-[120%] mb-[24px] md:leading-[130%]"
			>
				Book a call with me
			</h1>
			<p class="text-[#fff7f0] font-normal text-[18px] leading-[150%] mb-[40px]">
				I’d love to have a chat to see how I can help you. The best first step is for us to discuss
				your project during a free consultation. Then we can move forward from there.
			</p>
		</div>
		<button
			class="bg-[#e16b5b] py-[16px] px-[48px] text-white font-semibold text-[16px] leading-[150%] rounded-full cursor-pointer hover:bg-[#F6A560] focus:outline-offset-2 focus:outline-2 focus:outline-[#F6A560] focus:bg-[#F6A560]"
			>Free consultation</button
		>
	</section>
</main>

<footer
	class="flex justify-between mx-[16px] my-[24px] mb-[16px] md:mx-[32px] xl:w-[1110px] xl:mx-auto xl:mb-[48px]"
>
	<img src={logo} alt="logo" class="w-[48px] h-[48px] md:w-[64px] md:h-[64px]" />
	<button
		class="bg-black pt-[12px] pb-[16px] px-[24px] md:px-[48px] text-white rounded-full font-semibold text-[16px] hover:bg-[#755CDE] cursor-pointer focus:outline-offset-2 focus:outline-2 focus:outline-[#755CDE] focus:bg-[#030303]"
		>Free consultation</button
	>
</footer>
