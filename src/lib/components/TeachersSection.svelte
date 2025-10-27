<script>
    import { onMount } from "svelte";

    // Props para los datos de los profesores
    export let profesores = [];

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

<!-- Sección Profesores -->
<section id="profesores" class="py-20 relative">
    <!-- Fondo con degradado para mejor legibilidad del texto -->
    <div
        class="absolute inset-0 bg-gradient-to-tr from-black/90 via-gray-900/90 to-black/90 -z-10"
    ></div>
    <div class="container mx-auto px-6">
        <div class="text-center mb-16" data-aos="fade-up">
            <h2
                class="text-3xl md:text-4xl font-bold text-white mb-4 font-serif"
            >
                Nuestros Instructores
            </h2>
            <div
                class="w-24 h-1 bg-gradient-to-r from-amber-400 to-yellow-400 mx-auto mb-6"
            ></div>
            <p class="text-lg text-gray-100 max-w-3xl mx-auto leading-relaxed">
                Conoce a nuestro equipo de instructores profesionales
                especializados en ritmos latinos como salsa, merengue y bachata.
            </p>
        </div>

        <div class="grid md:grid-cols-2 gap-12 max-w-4xl mx-auto">
            {#each profesores as profesor}
                <div
                    class="flex flex-col md:flex-row items-center bg-gray-900/80 border border-amber-400/30 rounded-lg overflow-hidden shadow-xl hover:shadow-amber-400/20 hover:translate-y-[-5px] cursor-pointer transition-all ease-in-out duration-300 hover:border-amber-400/50"
                    data-aos-delay={profesor.id * 100}
                >
                    <div class="w-full md:w-1/3 h-64 md:h-full">
                        <img
                            src={profesor.foto}
                            alt={`Foto de ${profesor.nombre}`}
                            class="w-full h-full object-cover"
                            loading="lazy"
                        />
                    </div>
                    <div class="p-6 w-full md:w-2/3">
                        <h3 class="text-2xl font-bold text-white mb-2">
                            {profesor.nombre}
                        </h3>
                        <p class="text-amber-300 mb-3 font-medium">
                            {profesor.especialidad}
                        </p>
                        <p class="text-gray-200 text-sm mb-4">
                            <span class="font-semibold text-amber-200"
                                >Experiencia:</span
                            >
                            {profesor.experiencia}
                        </p>
                        <div class="flex space-x-3">
                            <a
                                href="https://instagram.com/titicodelswing_"
                                class="bg-amber-400/20 hover:bg-amber-400 text-amber-300 hover:text-black w-10 h-10 rounded-full flex items-center justify-center transition-all duration-300"
                                aria-label="Perfil de Instagram"
                            >
                                <i class="fab fa-instagram text-xl"></i>
                            </a>
                            <a
                                href="https://tiktok.com/@titicodelswing_"
                                class="bg-amber-400/20 hover:bg-amber-400 text-amber-300 hover:text-black w-10 h-10 rounded-full flex items-center justify-center transition-all duration-300"
                                aria-label="Perfil de TikTok"
                            >
                                <i class="fab fa-tiktok text-xl"></i>
                            </a>
                        </div>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</section>
