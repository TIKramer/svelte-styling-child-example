<script lang="ts">
	import Time from 'carbon-icons-svelte/lib/Time.svelte';
	import Tag from './Tag.svelte';
	export let type: 'weekly' | 'monthly' | 'yearly';
  </script>
  
  <Tag title={type} icon={Time} outline />
  