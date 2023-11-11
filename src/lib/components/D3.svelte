<script>
	import Chart from '$lib/components/chart_data/Chart.svelte';
	import ChartLeft from '$lib/components/chart_data/ChartLeft.svelte';
	import ChatBox from '$lib/components/chart_data/ChatBox.svelte';
</script>

<main class="grid grid-cols-[auto,2fr,auto] gap-4 h-[100dvh] px-6 py-20">
	<ChartLeft />
	<Chart />
	<ChatBox />
</main>
