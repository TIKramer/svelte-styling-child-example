<script lang="ts">
	import CheckmarkOutline from 'carbon-icons-svelte/lib/CheckmarkOutline.svelte';
	import WarningAlt from 'carbon-icons-svelte/lib/WarningAlt.svelte';
	import Error from 'carbon-icons-svelte/lib/Error.svelte';
	import Tag from './Tag.svelte';
	export let type: 'done' | 'uncompleted' | 'expired';

	let color: string;
	let backgroundColor: string;
	$: {
		if (type === 'done') {
			color = 'white';
			backgroundColor = 'green';
		} else if (type === 'uncompleted') {
			color = 'white';
			backgroundColor = 'orange';
		} else if (type === 'expired') {
			color = 'white';
			backgroundColor = 'red';
		}
	}
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

<Tag title={type} icon={Icon} --background-color={backgroundColor} --color={color} />
