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
	<!-- Primary Meta Tags -->
	<meta charset="UTF-8" />
	<meta
		name="viewport"
		content="width=device-width, initial-scale=1.0, maximum-scale=5.0"
	/>
	<meta http-equiv="X-UA-Compatible" content="ie=edge" />
	<meta name="theme-color" content="#000000" />

	<!-- SEO Meta Tags -->
	<title>Titico del Swing | Escuela de Baile Profesional</title>
	<meta
		name="description"
		content="Escuela de baile profesional con los mejores instructores y clases para todos los niveles. Aprende diferentes estilos de baile en un ambiente divertido y profesional."
	/>
	<meta
		name="keywords"
		content="escuela de baile, clases de baile, baile latino, salsa, bachata, kizomba, tango, baile deportivo, clases de baile para principiantes, academia de baile, baile en pareja, bailes latinos, ritmos latinos, aprender a bailar"
	/>
	<meta name="author" content="Titico del Swing" />
	<meta
		name="robots"
		content="index, follow, max-snippet:-1, max-image-preview:large, max-video-preview:-1"
	/>
	<link rel="canonical" href="https://www.titico.online/" />

	<!-- Open Graph / Facebook / Google -->
	<meta property="og:locale" content="es_ES" />
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://www.titico.online/" />
	<meta
		property="og:title"
		content="Titico del Swing | Escuela de Baile Profesional"
	/>
	<meta property="og:site_name" content="Titico del Swing" />
	<meta
		property="og:description"
		content="Aprende a bailar con los mejores instructores. Clases para todos los niveles y estilos. Únete a nuestra comunidad de baile hoy mismo."
	/>
	<meta property="og:image" content="https://www.titico.online/favicon.png" />
	<meta property="og:image:width" content="512" />
	<meta property="og:image:height" content="512" />
	<meta
		property="og:image:alt"
		content="Titico del Swing - Clases de baile profesionales"
	/>

	<!-- Favicon -->
	<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
	<link rel="icon" type="image/png" sizes="32x32" href="/favicon.png" />
	<link rel="icon" type="image/png" sizes="16x16" href="/favicon.png" />
	<link rel="manifest" href="/site.webmanifest" />
	<link rel="mask-icon" href="/safari-pinned-tab.svg" color="#000000" />

	<!-- PWA / Mobile -->
	<meta name="mobile-web-app-capable" content="yes" />
	<meta name="apple-mobile-web-app-title" content="Titico del Swing" />
	<meta
		name="apple-mobile-web-app-status-bar-style"
		content="black-translucent"
	/>
	<meta name="apple-mobile-web-app-capable" content="yes" />

	<!-- Additional Meta Tags -->
	<meta name="format-detection" content="telephone=yes" />
	<meta name="msapplication-TileColor" content="#000000" />
	<meta name="msapplication-config" content="/browserconfig.xml" />
	<meta name="revisit-after" content="7 days" />
	<meta name="rating" content="general" />
	<meta name="geo.region" content="CO" />
	<meta name="geo.placename" content="Pasto" />

	<!-- Preconnect to external domains -->
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />

	<!-- Structured Data / Schema.org -->
	<script type="application/ld+json">
		{
			"@context": "https://schema.org",
			"@type": "DanceSchool",
			"name": "Titico del Swing",
			"description": "Escuela de baile profesional con los mejores instructores y clases para todos los niveles.",
			"url": "https://www.titico.online",
			"logo": "https://www.titico.online/favicon.png",
			"telephone": "+57 320 532 0265",
			"address": {
				"@type": "PostalAddress",
				"streetAddress": "Calle 20 # 21-55",
				"addressLocality": "Pasto",
				"postalCode": "520003",
				"addressCountry": "CO"
			},
			"openingHoursSpecification": [
				{
					"@type": "OpeningHoursSpecification",
					"dayOfWeek": [
						"Monday",
						"Tuesday",
						"Wednesday",
						"Thursday",
						"Friday"
					],
					"opens": "16:00",
					"closes": "22:00"
				},
				{
					"@type": "OpeningHoursSpecification",
					"dayOfWeek": "Saturday",
					"opens": "10:00",
					"closes": "20:00"
				}
			],
			"sameAs": [
				"https://www.instagram.com/titicodelswing_/",
				"https://www.tiktok.com/@titicodelswing_"
			]
		}
	</script>
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
