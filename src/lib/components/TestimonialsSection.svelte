<script>
    import { onMount } from "svelte";

    // Props para los datos de los testimonios
    export let testimonios = [];

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

<!-- Sección Testimonios -->
<section id="testimonios" class="py-20 bg-gradient-to-br from-black via-gray-900 to-gray-800">
    <div class="container mx-auto px-6">
        <div class="text-center mb-16" data-aos="fade-up">
            <h2
                class="text-3xl md:text-4xl font-bold text-white mb-4 font-serif"
            >
                Lo que dicen nuestros estudiantes de baile
            </h2>
            <div class="w-24 h-1 bg-gradient-to-r from-amber-400 to-yellow-400 mx-auto mb-6"></div>
        </div>

        <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
            {#each testimonios as testimonio}
                <div
                    class="bg-gray-900 border border-amber-400/20 p-8 rounded-lg shadow-lg hover:shadow-amber-400/10 transition-shadow duration-300"
                    data-aos="fade-up"
                    data-aos-delay={testimonio.id * 100}
                >
                    <div class="flex items-center mb-4">
                        <div class="text-amber-400 text-4xl mr-4">"</div>
                        <p class="text-gray-200 italic">
                            {testimonio.comentario}
                        </p>
                    </div>
                    <div class="flex items-center">
                        <div
                            class="w-12 h-12 bg-gradient-to-br from-amber-400/30 to-yellow-400/30 rounded-full flex items-center justify-center text-amber-400 font-bold text-xl mr-4"
                        >
                            {testimonio.nombre.charAt(0)}
                        </div>
                        <div>
                            <h4 class="font-bold text-white">
                                {testimonio.nombre}
                            </h4>
                            <p class="text-amber-300 text-sm">
                                {testimonio.fecha}
                            </p>
                        </div>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</section>
