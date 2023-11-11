<script context="module">
	import { writable } from 'svelte/store';

	export const isSiteNavMenuOpen = writable(false);
</script>

<script>
	import { navigating } from '$app/stores';

	export let isMainNavMenuOpen = false;

	let SITE_NAV_ID = 'main-nav';

	// Close the site nav menu when navigating
	$: if ($navigating) $isSiteNavMenuOpen = false;
</script>

<button
	aria-controls={SITE_NAV_ID}
	aria-expanded={$isSiteNavMenuOpen}
	aria-label="Toggle Main Navigation"
	on:click={() => ($isSiteNavMenuOpen = !$isSiteNavMenuOpen)}
>
	<div />
	<div />
	<div />
</button>

<style lang="postcss">
	button div {
		@apply bg-white w-7 h-[0.1875rem] rounded transition-transform duration-300 ease-in-out;

		&:not(:last-of-type) {
			margin-block-end: 0.375rem;
		}
	}

	button[aria-expanded='true'] {
		div:nth-child(2) {
			opacity: 0;
		}

		div:nth-child(1) {
			transform: translateY(0.5625rem) rotate(45deg);
		}

		div:nth-child(3) {
			transform: translateY(-0.5625rem) rotate(-45deg);
		}
	}
</style>
