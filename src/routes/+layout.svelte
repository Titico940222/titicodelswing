<script>
	import "../app.css";
	import { onMount } from "svelte";

	let { children } = $props();

	onMount(() => {
		// Añadir clase al body para el fondo estelar
		document.body.classList.add(
			"bg-black",
			"min-h-screen",
			"relative",
			"overflow-x-hidden",
		);
	});
</script>

<svelte:head>
	<meta name="keywords" content="escuela de baila" />
</svelte:head>

<!-- Fondo estelar -->
<div class="fixed inset-0 -z-10">
	<!-- Capa de estrellas grandes -->
	<div
		class="absolute inset-0 bg-[url('/estrellas.jpg')] bg-cover bg-center opacity-30"
	></div>

	<!-- Efecto de brillo sutil -->
	<div
		class="absolute inset-0 bg-gradient-to-b from-amber-900/5 via-transparent to-amber-900/5"
	></div>

	<!-- Efecto de partículas sutiles -->
	<div class="absolute inset-0 overflow-hidden">
		{#each Array(30) as _, i}
			<div
				class="absolute rounded-full bg-amber-300/70 animate-pulse"
				style="
					width: {Math.random() * 2 + 1}px;
					height: {Math.random() * 2 + 1}px;
					left: {Math.random() * 100}%;
					top: {Math.random() * 100}%;
					animation-duration: {Math.random() * 3 + 2}s;
					animation-delay: {Math.random() * 5}s;
				"
			></div>
		{/each}
	</div>
</div>

<!-- Contenido principal -->
<div class="relative z-10">
	{@render children?.()}
</div>
