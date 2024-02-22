<script>
	import logo1 from '$lib/images/logos/3m.svg';
	import logo2 from '$lib/images/logos/barstool-store.svg';
	import logo3 from '$lib/images/logos/budweiser.svg';
	import logo4 from '$lib/images/logos/buzzfeed.svg';
	import logo5 from '$lib/images/logos/forbes.svg';
	import logo6 from '$lib/images/logos/macys.svg';
	import logo7 from '$lib/images/logos/menshealth.svg';
	import logo8 from '$lib/images/logos/mrbeast.svg';

	import { onMount } from 'svelte';
	/**
	 * @type {any[]}
	 */
	let slides = [];
	onMount(() => {
		slides = [
			logo1,
			logo2,
			logo3,
			logo4,
			logo5,
			logo6,
			logo7,
			logo8,
			logo1,
			logo2,
			logo3,
			logo4,
			logo5,
			logo6,
			logo7,
			logo8
		];
	});
</script>

<div class="logos">
	<div class="logos-slide">
		{#each slides as logo}
			<img src={logo} alt="" />
		{/each}
	</div>
	<div class="logos-slide">
		{#each slides as logo}
			<img src={logo} alt="" />
		{/each}
	</div>
</div>

<style>
	@keyframes slide {
		from {
			transform: translateX(0);
		}
		to {
			transform: translateX(-100%);
		}
	}

	.logos {
		overflow: hidden;
		padding: 60px 0;
		background: white;
		white-space: nowrap;
		position: relative;
	}

	.logos-slide {
		overflow: hidden;

		display: inline-flex;
		animation: 5s slide infinite linear;
	}

	.logos-slide img {
		height: 50px;
		margin: 0 40px;
	}

	/* @media (max-width: 768px) {
		.logos-slide img {
			height: 30px;
			margin: 0 20px;
		}
	} */
</style>
