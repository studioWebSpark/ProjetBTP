<template>
    <div class="flex justify-center mt-5">
        <div class="grid grid-cols-1 gap-4 transition-[grid-template-columns] lg:gap-8 w-full mx-auto px-8">
            <div
                class="h-[700px] w-full rounded-3xl bg-gray-200 relative bg-[url(https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80)] bg-cover bg-center bg-no-repeat">

                <!-- Titre attrayant pour les petits écrans -->
                <h2
                    class="absolute inset-0 flex items-center justify-center text-white text-4xl font-bold text-center lg:hidden">
                    Chaque pièce raconte une histoire : découvrez la vôtre.
                </h2>

                <!-- Conteneur pour la carte de description (masqué sur les petits écrans) -->
                <div class="absolute bottom-10 left-10 items-center hidden lg:flex">
                    <!-- Carte avec effet de flou -->
                    <div class="p-4 bg-opacity-70 backdrop-blur-md rounded-lg shadow-lg">
                        <h3 class="text-lg font-semibold">Transformez vos idées en réalité</h3>
                        <p class="mt-2">Découvrez nos réalisations de chantiers qui allient qualité et innovation.</p>
                        <button class="mt-4 bg-black text-white py-2 px-4 rounded hover:bg-slate-500">En savoir plus</button>
                    </div>

                    <!-- Carte pour afficher une vidéo (supprimée) -->
                    <div class="p-6 rounded-lg shadow-lg bg-opacity-70 backdrop-blur-md">
                        <!-- Vidéo supprimée -->
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>