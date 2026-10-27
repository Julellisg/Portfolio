<script lang="ts">
	import './layout.css';
	import favicon from '#lib/assets/jg-icon.png';
	import type { LayoutProps } from './$types';

	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>Julian Ellis Geronimo</title>
	<meta name="description" content="Web developer and generalist who learns by building—from clones to new ideas. Passionate about the web and using AI to build faster." />
</svelte:head>

{@render children()}