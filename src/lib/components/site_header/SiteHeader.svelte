<script>
	import ProfileImage from '../ProfileImage.svelte';
	import Logo from './Logo.svelte';
	import SiteNavMenuToggleBtn from './SiteNavMenuToggleBtn.svelte';
</script>

<header class="flex justify-between px-2 py-3 border-b border-white/10">
	<Logo />

	<div class="flex gap-4">
		<ProfileImage />
		<SiteNavMenuToggleBtn />
	</div>
</header>
