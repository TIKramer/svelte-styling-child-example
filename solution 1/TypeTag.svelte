<script lang="ts">
	export let type: 'air' | 'water' | 'fire';
	$: capitalised = type.charAt(0).toUpperCase() + type.slice(1);
</script>

<div class="container {type}">
	{capitalised}
</div>

<style>
	.container {
		border-radius: 25px;
		display: inline;
		white-space: nowrap;
		border-radius: 0.8rem;
		font-size: 0.75rem;
		line-height: 1rem;
		padding-left: 0.5rem;
		padding-right: 0.5rem;
		padding-top: 0.2rem;
		padding-bottom: 0.2rem;
	}

    .air {
        background-color: lightblue;
        color: white;
    }
    .water {
        background-color: blue;
        color: white;
    }
    .fire {
        background-color: red;
        color: white;
    }
</style>
