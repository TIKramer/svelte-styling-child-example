<script lang="ts">
	import Time from 'carbon-icons-svelte/lib/Time.svelte';
	export let type: 'weekly' | 'monthly' | 'yearly';
	$: capitalised = type.charAt(0).toUpperCase() + type.slice(1);
</script>

<div class="container {type}">
    <Time class="icon" />
    <span class="text">{capitalised}</span>
</div>


<style>
    .container {
		outline: 1px solid;
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

  
</style>
