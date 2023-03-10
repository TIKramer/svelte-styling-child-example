<script lang="ts">
	import CheckmarkOutline from 'carbon-icons-svelte/lib/CheckmarkOutline.svelte';
	import WarningAlt from 'carbon-icons-svelte/lib/WarningAlt.svelte';
	import Error from 'carbon-icons-svelte/lib/Error.svelte';
	export let type: 'done' | 'uncompleted' | 'expired';

	$: capitalised = type.charAt(0).toUpperCase() + type.slice(1);

	function getIcon(type: string) {
		let icon = CheckmarkOutline;
		if (type === 'done') {
			icon = CheckmarkOutline;
		} else if (type === 'uncompleted') {
			icon = WarningAlt;
		} else {
			icon = Error;
		}
		return icon;
	}
	$: Icon = getIcon(type);
</script>

<div class="container {type}">
	<Icon class="icon" />
	<span class="text">{capitalised}</span>
</div>

<style>
	.container {
		display: inline-flex;
		align-items: center;
		border-radius: 0.8rem;
		font-size: 0.75rem;
		line-height: 1rem;
		padding: 0.2rem 0.5rem;
	}

	.text {
		margin-left: 0.5rem;
	}

	.done {
		background-color: lightgreen;
		color: white;
	}
	.uncompleted {
		background-color: orange;
		color: white;
	}
	.expired {
		background-color: red;
		color: white;
	}
</style>
