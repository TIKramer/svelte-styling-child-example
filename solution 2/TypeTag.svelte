<script lang="ts">
	import Tag from './Tag.svelte';

	export let type: 'air' | 'water' | 'fire';
	let color: string;
	let backgroundColor: string;
	$: {
		if (type === 'air') {
			color = 'white';
			backgroundColor = 'lightblue';
		} else if (type === 'water') {
			color = 'white';
			backgroundColor = 'blue';
		} else if (type === 'fire') {
			color = 'white';
			backgroundColor = 'red';
		}
	}
</script>

<Tag title={type} --color={color} --background-color={backgroundColor} />
