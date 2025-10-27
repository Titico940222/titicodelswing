<script>
    import { onMount } from "svelte";

    // Inicialización de AOS (Animate On Scroll)
    onMount(() => {
        import("aos").then((AOS) => {
            AOS.init({
                duration: 800,
                easing: "ease-in-out",
                once: true,
            });
        });
        AOS.refresh();
    });
</script>

<!-- Hero Section -->
<section id="inicio" class="pt-32 pb-20 md:pt-40 md:pb-32 relative">
    <!-- Fondo con degradado para mejor legibilidad del texto -->
    <div
        class="absolute inset-0 bg-gradient-to-b from-black/90 via-black/75 to-black/90 -z-10"
    ></div>
    <!-- Efecto de partículas -->
    <div class="absolute inset-0 overflow-hidden opacity-20">
        <div
            class="absolute w-4 h-4 bg-amber-400 rounded-full animate-pulse"
            style="top: 20%; left: 25%;"
        ></div>
        <div
            class="absolute w-6 h-6 bg-orange-300 rounded-full animate-pulse"
            style="top: 60%; left: 70%;"
        ></div>
        <div
            class="absolute w-3 h-3 bg-yellow-500 rounded-full animate-pulse"
            style="top: 80%; left: 30%;"
        ></div>
        <div
            class="absolute w-5 h-5 bg-orange-500 rounded-full animate-pulse"
            style="top: 30%; left: 80%;"
        ></div>
    </div>

    <div class="container mx-auto px-6 relative z-10">
        <div class="flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-12 md:mb-0" data-aos="fade-right">
                <h1
                    class="text-4xl md:text-6xl font-bold text-white mb-6 font-serif"
                >
                    Baila al ritmo de la <span
                        class="bg-gradient-to-r from-amber-400 via-yellow-300 to-amber-400 bg-clip-text text-transparent drop-shadow-lg"
                        >Salsa</span
                    >
                </h1>
                <p class="text-xl text-gray-100 mb-8 max-w-lg leading-relaxed">
                    Descubre la magia del baile latino en nuestra academia.
                    Clases de salsa, merengue y bachata para todos los niveles
                    en un ambiente divertido y profesional.
                </p>
                <div
                    class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4"
                >
                    <a
                        href="#contacto"
                        class="bg-gradient-to-r from-amber-400 to-yellow-400 hover:from-amber-500 hover:to-yellow-500 text-black px-8 py-4 rounded-md text-lg text-center transition-all duration-300 font-bold shadow-lg hover:shadow-amber-400/25 transform hover:scale-105"
                    >
                        ¡Empieza Ahora!
                    </a>
                    <a
                        href="#clases"
                        class="border-2 border-amber-400 text-white hover:bg-amber-400 hover:text-black px-8 py-4 rounded-md text-lg font-semibold text-center transition-all duration-300 shadow-lg hover:shadow-amber-400/50"
                    >
                        Ver Clases
                    </a>
                </div>
            </div>
            <div class="md:w-1/2" data-aos="fade-left">
                <div class="relative">
                    <div
                        class="w-full h-96 rounded-lg overflow-hidden shadow-2xl border-4 border-amber-400/30"
                    >
                        <img
                            src="/1.jpeg"
                            alt="Bailarines de salsa en acción"
                            class="w-full h-full object-cover"
                            loading="eager"
                        />
                    </div>
                    <div
                        class="absolute -bottom-6 -right-6 w-36 h-36 bg-gradient-to-br from-amber-500 to-yellow-300 rounded-full flex items-center justify-center text-black font-bold text-base transform rotate-12 shadow-2xl border-4 border-white"
                    >
                        <span class="text-center px-2 text-gray-50"
                            >¡Diviértete<br />bailando!</span
                        >
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
