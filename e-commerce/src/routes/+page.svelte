<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="flex flex-col justify-center items-center flex-1.5">

	<h1 class="w-full text-center text-4xl md:text-6xl">
		<span class="welcome block relative">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" class="absolute w-full h-full top-0 block" />
			</picture>
		</span>
		Welcome to your new<br />SvelteKit app
	</h1>

	<h2 class="text-lg md:text-xl mt-4">
		try editing <strong class="font-semibold">src/routes/+page.svelte</strong>
	</h2>

	<Counter />
</section>
