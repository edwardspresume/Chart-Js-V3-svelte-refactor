<script>
	import Icon from './ChartIcon.svelte';
</script>

<menu class="grid self-start overflow-hidden bg-gray-700 border rounded-xl">
	<button>
		<Icon name="1" />
	</button>

	<button>
		<Icon name="2" />
	</button>

	<button>
		<Icon name="3" />
	</button>

	<button>
		<Icon name="4" />
	</button>

	<button>
		<Icon name="5" />
	</button>

	<button>
		<Icon name="6" />
	</button>

	<button>
		<Icon name="7" />
	</button>

	<button class="hover:bg-slate-950">
		<Icon name="8" />
	</button>
</menu>

<style lang="postcss">
	button {
		@apply p-2 hover:bg-green-800 duration-300 transition-colors;
	}
</style>
