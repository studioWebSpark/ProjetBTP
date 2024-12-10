<template>
    <header class="relative py-4 md:py-6 ">
        <div class="px-4 mx-auto max-w-7xl sm:px-6 lg:px-8">
            <div class="relative flex items-center justify-between">
                <div class="flex-shrink-0">
                    <a href="#" title=""
                        class="flex rounded outline-none focus:ring-1 focus:ring-gray-900 focus:ring-offset-2">
                        <img class="w-auto h-8"
                            src="https://d33wubrfki0l68.cloudfront.net/682a555ec15382f2c6e7457ca1ef48d8dbb179ac/f8cd3/images/logo.svg"
                            alt="" />
                    </a>
                </div>

                <div class="flex lg:hidden">
                    <button type="button" class="text-gray-900">
                        <svg class="w-7 h-7" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                                d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>

                <div
                    class="hidden lg:absolute lg:inset-y-0 lg:flex lg:items-center lg:justify-center lg:space-x-12 lg:-translate-x-1/2 lg:left-1/2">
                    <a href="#" title=""
                        class="text-base font-medium text-gray-900 transition-all duration-200 rounded focus:outline-none font-pj hover:text-opacity-50 focus:ring-1 focus:ring-gray-900 focus:ring-offset-2">
                        Experts </a>

                    <a href="#" title=""
                        class="text-base font-medium text-gray-900 transition-all duration-200 rounded focus:outline-none font-pj hover:text-opacity-50 focus:ring-1 focus:ring-gray-900 focus:ring-offset-2">
                        Community Groups </a>

                    <a href="#" title=""
                        class="text-base font-medium text-gray-900 transition-all duration-200 rounded focus:outline-none font-pj hover:text-opacity-50 focus:ring-1 focus:ring-gray-900 focus:ring-offset-2">
                        Support </a>
                </div>

                <div class="hidden lg:flex lg:items-center lg:justify-center lg:space-x-10">
                    <a href="#" title=""
                        class="text-base font-medium text-gray-900 transition-all duration-200 rounded focus:outline-none font-pj hover:text-opacity-50 focus:ring-1 focus:ring-gray-900 focus:ring-offset-2">
                        Login </a>

                    <a href="#" title=""
                        class="px-5 py-2 text-base font-semibold leading-7 text-gray-900 transition-all duration-200 bg-transparent border border-gray-900 rounded-xl font-pj focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-900 hover:bg-gray-900 hover:text-white focus:bg-gray-900 focus:text-white"
                        role="button">
                        Join community
                    </a>
                </div>
            </div>
        </div>
    </header>
    <div class="flex justify-center mt-5">
        <div class="grid grid-cols-1 gap-4 transition-[grid-template-columns] lg:gap-8 w-full mx-auto px-8">
            <div
                class="h-[700px] w-full rounded-3xl bg-gray-200 relative bg-[url(https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80)] bg-cover bg-center bg-no-repeat">

                <!-- Conteneur pour la carte de description et la vidéo -->
                <div class="absolute bottom-10 left-10 flex items-center">
                    <!-- Carte avec effet de flou -->
                    <div class="p-4 bg-opacity-70 backdrop-blur-md rounded-lg shadow-lg">
                        <h3 class="text-lg font-semibold">Description de la carte</h3>
                        <p class="mt-2">Ceci est une description de la carte. Vous pouvez ajouter plus <br>
                            d'informations
                            ici.</p>
                        <button class="mt-4 bg-black text-white py-2 px-4 rounded hover:bg-slate-500">En savoir
                            plus</button>
                    </div>

                    <!-- Tiret -->
                    <div class="mx-4 h-36 border-l border-black"></div>

                    <!-- Carte pour afficher une vidéo -->
                    <div class="p-6 rounded-lg shadow-lg bg-opacity-70 backdrop-blur-md">
                        <iframe class="w-full h-32" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0"
                            allowfullscreen></iframe>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <Step />

    <section class="mt-10">
        <h2 class="text-2xl font-bold mb-4">Travaux Réalisés</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
            <!-- Carte 1 (plus grande) -->
            <div
                class="overflow-hidden rounded-lg shadow-lg col-span-1 md:col-span-2 lg:col-span-2 relative bg-[url(https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80)] bg-cover bg-center transition-opacity duration-500 ease-in-out ">
                <!-- Hauteur augmentée -->
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Mondrian</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
            <!-- Carte 2 -->
            <div class="relative overflow-hidden rounded-lg shadow-lg">
                <img src="https://example.com/image2.jpg" alt="Nirnia" class="w-full h-96 object-cover" />
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Nirnia</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
            <!-- Carte 3 -->
            <div class="relative overflow-hidden rounded-lg shadow-lg">
                <img src="https://example.com/image3.jpg" alt="Artex" class="w-full h-96 object-cover" />
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Artex</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
            <!-- Carte 4 -->
            <div
                class="overflow-hidden rounded-lg shadow-lg col-span-1 md:col-span-2 lg:col-span-2 relative bg-[url(https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80)] bg-cover bg-center transition-opacity duration-500 ease-in-out ">

                <div class=" absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Brera</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
            <!-- Carte 5 -->
            <div
                class="overflow-hidden rounded-lg shadow-lg col-span-1 md:col-span-2 lg:col-span-2 relative bg-[url(https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80)] bg-cover bg-center transition-opacity duration-500 ease-in-out ">
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Alea Pro</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
            <!-- Carte 6 -->
            <div class="relative overflow-hidden rounded-lg shadow-lg">
                <img src="https://example.com/image6.jpg" alt="Nirnia" class="w-full h-96 object-cover" />
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Nirnia</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
        </div>
    </section>



</template>

<script setup>
import Step from '../Components/Step.vue'; // Chemin relatif vers le composant
</script>

<style>
/* Ajoutez des styles personnalisés ici si nécessaire */
</style>
