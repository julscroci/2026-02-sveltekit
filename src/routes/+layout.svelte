<script>
	import favicon from '$lib/assets/favicon.svg';

	import "$lib/styles/reset.css";
	import "$lib/styles/tokens.css";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />

	<!-- Satoshi font -->
	<link rel="preconnect" href="https://api.fontshare.com" />
	<link rel="preconnect" href="https://api.fontshare.com" crossorigin />
	<link href="https://api.fontshare.com/v2/css?f[]=satoshi@1,2&display=swap" rel="stylesheet">

	<!-- Inter font -->
	<link rel="preconnect" href="https://rsms.me/">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link rel="stylesheet" href="https://rsms.me/inter/inter.css">
</svelte:head>

{@render children()}
