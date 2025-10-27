<script>
    import { onMount } from "svelte";

    // Props para los datos de las clases
    export let clases = [];

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

<!-- Sección Clases -->
<section id="clases" class="py-20 relative">
    <!-- Fondo con degradado para mejor legibilidad del texto -->
    <div
        class="absolute inset-0 bg-gradient-to-bl from-black/90 via-gray-900/90 to-black/90 -z-10"
    ></div>
    <div class="container mx-auto px-6">
        <div class="text-center mb-16" data-aos="fade-up">
            <h2
                class="text-3xl md:text-4xl font-bold text-white mb-4 font-serif"
            >
                Nuestros Grupos de Baile
            </h2>
            <div
                class="w-24 h-1 bg-gradient-to-r from-amber-400 to-yellow-400 mx-auto mb-6"
            ></div>
            <p class="text-lg text-gray-100 max-w-3xl mx-auto leading-relaxed">
                Ofrecemos grupos especializados para todas las edades y niveles,
                desde principiantes hasta profesionales en ritmos latinos como
                salsa, merengue y bachata.
            </p>
        </div>

        <div class="grid md:grid-cols-3 gap-8">
            {#each clases as clase}
                <div
                    class="bg-gray-900/80 border border-amber-400/30 rounded-lg overflow-hidden shadow-xl hover:shadow-amber-400/20 transform hover:scale-102 cursor-pointer transition-all ease-in-out duration-300"
                    data-aos-delay={clase.id * 100}
                >
                    <div class="h-48 overflow-hidden relative">
                        <img
                            src={clase.imagen}
                            alt={clase.titulo}
                            class="w-full h-full object-cover"
                            loading="lazy"
                        />
                        <div
                            class="absolute inset-0 bg-gradient-to-t from-gray-900 via-transparent to-transparent"
                        ></div>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">
                            {clase.titulo}
                        </h3>
                        <p class="text-gray-200 mb-4">{clase.descripcion}</p>
                        <div class="flex items-center text-amber-300 mb-2">
                            <i class="fas fa-users mr-2"></i>
                            <span>{clase.edades}</span>
                        </div>
                        <div class="flex items-center text-amber-300 mb-2">
                            <i class="far fa-clock mr-2"></i>
                            <span>{@html clase.horario}</span>
                        </div>
                        <div class="flex items-center text-green-300 mb-2">
                            <i class="fas fa-dollar-sign mr-2"></i>
                            <span>Mensualidad: {clase.mensualidad}</span>
                        </div>
                        <div class="flex items-center text-blue-300 mb-4">
                            <i class="fas fa-tag mr-2"></i>
                            <span>Inscripción: {clase.inscripcion}</span>
                        </div>
                        {#if clase.nota}
                            <div
                                class="bg-gradient-to-r from-amber-400/30 to-yellow-400/30 border border-amber-400/60 text-amber-200 px-3 py-2 rounded text-sm mb-4 font-medium"
                            >
                                <i class="fas fa-info-circle mr-1"></i>
                                {clase.nota}
                            </div>
                        {/if}
                        <a
                            href="#contacto"
                            class="inline-block w-full bg-gradient-to-r from-amber-500 to-yellow-500 hover:from-amber-600 hover:to-yellow-600 text-black text-center py-3 px-4 rounded-md transition-all duration-300 font-bold shadow-lg hover:shadow-amber-400/25 transform hover:scale-102 cursor-pointer"
                        >
                            Inscribirse
                        </a>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</section>
