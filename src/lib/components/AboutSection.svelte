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

<!-- Sección Sobre Nosotros -->
<section id="nosotros" class="py-20 relative">
    <!-- Fondo con degradado para mejor legibilidad del texto -->
    <div
        class="absolute inset-0 bg-gradient-to-br from-black/90 via-black/80 to-black/90 -z-10"
    ></div>
    <div class="container mx-auto px-6">
        <div class="text-center mb-16" data-aos="fade-up">
            <h2
                class="text-3xl md:text-4xl font-bold text-white mb-4 font-serif"
            >
                Sobre Nosotros
            </h2>
            <div
                class="w-24 h-1 bg-gradient-to-r from-amber-400 to-yellow-400 mx-auto mb-6"
            ></div>
            <p class="text-lg text-gray-100 max-w-3xl mx-auto leading-relaxed">
                En Titicó del Swing nos apasiona el baile latino y queremos
                compartir esa pasión contigo. Especialistas en la enseñanza de
                ritmos latinos modernos como salsa, merengue y bachata,
                ofrecemos clases de alta calidad para todos los niveles.
            </p>
        </div>

        <div class="grid md:grid-cols-3 gap-8">
            <div
                class="bg-gray-900/80 border border-amber-400/30 p-8 rounded-lg text-center shadow-xl hover:shadow-amber-400/20 hover:translate-y-[-5px] cursor-pointer transition-all ease-in-out duration-300 hover:border-amber-400/50"
                data-aos-delay="100"
            >
                <div
                    class="w-16 h-16 bg-gradient-to-br from-amber-400/40 to-yellow-400/40 rounded-full flex items-center justify-center mx-auto mb-6"
                >
                    <i class="fas fa-heart text-3xl text-amber-300"></i>
                </div>
                <h3 class="text-xl font-bold text-white mb-3">
                    Ritmos Latinos
                </h3>
                <p class="text-gray-200">
                    Nuestros instructores están dedicados a compartir su amor
                    por los ritmos latinos y ayudarte a alcanzar tus metas
                    bailando salsa, merengue y bachata.
                </p>
            </div>

            <div
                class="bg-gray-900/80 border border-amber-400/30 p-8 rounded-lg text-center shadow-xl hover:shadow-amber-400/20 hover:translate-y-[-5px] cursor-pointer transition-all ease-in-out duration-300 hover:border-amber-400/50"
                data-aos-delay="200"
            >
                <div
                    class="w-16 h-16 bg-gradient-to-br from-amber-400/40 to-yellow-400/40 rounded-full flex items-center justify-center mx-auto mb-6"
                >
                    <i class="fas fa-users text-3xl text-amber-300"></i>
                </div>
                <h3 class="text-xl font-bold text-white mb-3">
                    Ambiente Social
                </h3>
                <p class="text-gray-200">
                    Únete a nuestra comunidad de bailarines apasionados por los
                    ritmos latinos y haz nuevos amigos mientras aprendes salsa,
                    merengue y bachata.
                </p>
            </div>

            <div
                class="bg-gray-900/80 border border-amber-400/30 p-8 rounded-lg text-center shadow-xl hover:shadow-amber-400/20 hover:translate-y-[-5px] cursor-pointer transition-all ease-in-out duration-300 hover:border-amber-400/50"
                data-aos-delay="300"
            >
                <div
                    class="w-16 h-16 bg-gradient-to-br from-amber-400/40 to-yellow-400/40 rounded-full flex items-center justify-center mx-auto mb-6"
                >
                    <i class="fas fa-medal text-3xl text-amber-300"></i>
                </div>
                <h3 class="text-xl font-bold text-white mb-3">
                    Instructores Profesionales
                </h3>
                <p class="text-gray-200">
                    Nuestros instructores Javier Iván Narváez (Mercadólogo y
                    Coreógrafo) y Luis Hidalgo (Licenciado en Educación Física)
                    son bailarines profesionales con amplia experiencia en
                    ritmos latinos.
                </p>
            </div>
        </div>
    </div>
</section>
