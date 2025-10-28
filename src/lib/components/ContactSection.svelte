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

<!-- Sección Contacto -->
<section id="contacto" class="py-20 relative">
    <!-- Fondo con degradado para mejor legibilidad del texto -->
    <div
        class="absolute inset-0 bg-gradient-to-tl from-black/90 via-gray-900/90 to-black/90 -z-10"
    ></div>
    <div class="container mx-auto px-6">
        <div
            class="max-w-4xl mx-auto bg-gray-900/90 border border-amber-400/30 rounded-lg overflow-hidden shadow-2xl"
        >
            <div class="md:flex">
                <div
                    class="md:w-1/2 bg-gradient-to-br from-amber-500 to-yellow-500 p-8 text-black relative overflow-hidden"
                >
                    <div class="absolute inset-0 opacity-10">
                        <img
                            src="/9.jpeg"
                            alt="Fondo de baile"
                            class="w-full h-full object-cover"
                        />
                    </div>
                    <div class="relative z-10">
                        <h2
                            class="text-3xl font-bold mb-6 font-serif text-black"
                        >
                            Contáctanos
                        </h2>
                        <p class="mb-8 text-gray-900 font-medium">
                            ¿Listo para comenzar tu viaje en el baile? ¡Estamos
                            aquí para ayudarte!
                        </p>

                        <div class="space-y-6">
                            <div class="flex items-center">
                                <div class="bg-black/20 rounded-full mr-4">
                                    <i
                                        class="fas fa-map-marker-alt p-3 text-black"
                                    ></i>
                                </div>
                                <div>
                                    <h3 class="font-bold text-black">
                                        Ubicación
                                    </h3>
                                    <p class="text-gray-900">
                                        Calle 20 # 21-55 La panadería, Pasto -
                                        Nariño
                                    </p>
                                </div>
                            </div>

                            <div class="flex items-start">
                                <div class="bg-black/20 rounded-full mr-4">
                                    <i class="fas fa-phone-alt p-3 text-black"
                                    ></i>
                                </div>
                                <div>
                                    <h3 class="font-bold text-black">
                                        WhatsApp
                                    </h3>
                                    <p class="text-gray-900 font-medium">
                                        320 532 0265
                                    </p>
                                </div>
                            </div>

                            <div class="flex items-start">
                                <div class="bg-black/20 rounded-full mr-4">
                                    <i class="fas fa-envelope p-3 text-black"
                                    ></i>
                                </div>
                                <div>
                                    <h3 class="font-bold text-black">Email</h3>
                                    <p class="text-gray-900">
                                        javiernarvaez1085@gmail.com
                                    </p>
                                </div>
                            </div>

                            <div class="flex space-x-4 pt-4">
                                <a
                                    href="https://instagram.com/titicodelswing_"
                                    class="bg-black hover:bg-gray-900 w-10 h-10 rounded-full flex items-center justify-center text-amber-400 transition-all duration-300 shadow-lg p-2"
                                    aria-label="Instagram"
                                >
                                    <i class="fab fa-instagram"></i>
                                </a>
                                <a
                                    href="https://tiktok.com/@titicodelswing_"
                                    class="bg-black hover:bg-gray-900 w-10 h-10 rounded-full flex items-center justify-center text-amber-400 transition-all duration-300 shadow-lg p-2"
                                    aria-label="TikTok"
                                >
                                    <i class="fab fa-tiktok"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="md:w-1/2 p-8 bg-gray-900/95">
                    <h3 class="text-2xl font-bold text-white mb-6">
                        Envíanos un mensaje
                    </h3>
                    <form
                        class="space-y-4"
                        action="https://formsubmit.co/javiernarvaez1085@gmail.com"
                        method="POST"
                    >
                        <div>
                            <label
                                for="nombre"
                                class="block text-gray-100 mb-2 font-medium"
                            >
                                Nombre
                            </label>
                            <input
                                type="text"
                                id="nombre"
                                name="nombre"
                                class="w-full px-4 py-3 bg-gray-800 border border-gray-600 rounded-md text-white focus:outline-none focus:ring-2 focus:ring-amber-400 focus:border-amber-400 transition-colors"
                                required
                                aria-required="true"
                            />
                        </div>

                        <div>
                            <label
                                for="email"
                                class="block text-gray-100 mb-2 font-medium"
                                >Email</label
                            >
                            <input
                                type="email"
                                id="email"
                                name="email"
                                class="w-full px-4 py-3 bg-gray-800 border border-gray-600 rounded-md text-white focus:outline-none focus:ring-2 focus:ring-amber-400 focus:border-amber-400 transition-colors"
                                required
                                aria-required="true"
                            />
                        </div>

                        <div>
                            <label
                                for="asunto"
                                class="block text-gray-100 mb-2 font-medium"
                                >Asunto</label
                            >
                            <input
                                type="text"
                                id="asunto"
                                name="asunto"
                                class="w-full px-4 py-3 bg-gray-800 border border-gray-600 rounded-md text-white focus:outline-none focus:ring-2 focus:ring-amber-400 focus:border-amber-400 transition-colors"
                                required
                                aria-required="true"
                            />
                        </div>

                        <div>
                            <label
                                for="mensaje"
                                class="block text-gray-100 mb-2 font-medium"
                                >Mensaje</label
                            >
                            <textarea
                                id="mensaje"
                                name="mensaje"
                                rows="4"
                                class="w-full px-4 py-3 bg-gray-800 border border-gray-600 rounded-md text-white focus:outline-none focus:ring-2 focus:ring-amber-400 focus:border-amber-400 transition-colors"
                                required
                                aria-required="true"
                            ></textarea>
                        </div>
                        <input type="hidden" name="_template" value="table" />
                        <input type="hidden" name="_captcha" value="false" />
                        <input type="text" name="_honey" style="display:none" />
                        <input
                            type="hidden"
                            name="_next"
                            value="https://www.titico.online"
                        />

                        <button
                            type="submit"
                            class="w-full bg-gradient-to-r from-amber-500 to-yellow-500 hover:from-amber-600 hover:to-yellow-600 text-black py-3 px-6 rounded-md transition-all duration-300 font-bold shadow-lg hover:shadow-amber-400/25 transform hover:scale-105"
                        >
                            Enviar Mensaje
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </div>
</section>
