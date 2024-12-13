<template>
    <section class="mt-20 m-8">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
            <!-- Carte 1 (Nouveautés en carrousel) -->
            <div class="relative overflow-hidden rounded-3xl shadow-lg col-span-1 md:col-span-1 lg:col-span-2 h-96">
                <div class="carousel">
                    <div class="carousel-inner">
                        <div class="carousel-item active">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Nouveauté 1" class="w-full h-full object-cover" />
                        </div>
                        <div class="carousel-item">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Nouveauté 2" class="w-full h-full object-cover" />
                        </div>
                        <div class="carousel-item">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Nouveauté 3" class="w-full h-full object-cover" />
                        </div>
                    </div>
                </div>
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold text-2xl">Nouveautés</h3>
                    <p class="text-white">Découvrez nos dernières réalisations sous forme de carrousel.</p>
                </div>
            </div>

            <!-- Carte 2 (Offre promotionnelle en carrousel) -->
            <div class="relative overflow-hidden rounded-3xl shadow-lg col-span-1 md:col-span-1 lg:col-span-1 h-96">
                <div class="carousel">
                    <div class="carousel-inner">
                        <div class="carousel-item active">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Borne promotionnelle 1" class="w-full h-full object-cover" />
                        </div>
                        <div class="carousel-item">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Borne promotionnelle 2" class="w-full h-full object-cover" />
                        </div>
                        <div class="carousel-item">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Borne promotionnelle 3" class="w-full h-full object-cover" />
                        </div>
                    </div>
                </div>
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Offre Promotionnelle</h3>
                    <p class="text-white">-10 % sur toutes les sélections !</p>
                </div>
            </div>

            <!-- Carte 3 (Actualités en carrousel) -->
            <div class="relative overflow-hidden rounded-3xl shadow-lg col-span-1 md:col-span-1 lg:col-span-1 h-96">
                <div class="carousel">
                    <div class="carousel-inner">
                        <div class="carousel-item active">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Actualité 1" class="h-full object-cover" />
                        </div>
                        <div class="carousel-item">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Actualité 2" class="w-full h-full object-cover" />
                        </div>
                        <div class="carousel-item">
                            <img src="https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80"
                                alt="Actualité 3" class="w-full h-full object-cover" />
                        </div>
                    </div>
                </div>
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Actualités</h3>
                    <p class="text-white">Images en carrousel des dernières actualités.</p>
                </div>
            </div>

            <!-- Section de Statistiques (grande) -->
            <div
                class="col-span-1 md:col-span-1 lg:col-span-2 flex flex-col justify-start items-center p-4 bg-gray-100 rounded-3xl shadow-lg h-96">
                <h3 class="text-xl font-bold mb-4">Statistiques</h3>
                <div class="grid grid-cols-2 gap-6 w-full mt-4">
                    <div class="flex flex-col items-center">
                        <div class="text-4xl font-bold">{{ projectsCount }}</div>
                        <p class="text-sm text-center">Projets Réalisés</p>
                    </div>
                    <div class="flex flex-col items-center">
                        <div class="text-4xl font-bold">{{ quotesCount }}</div>
                        <p class="text-sm text-center">Devis Réalisés</p>
                    </div>
                    <div class="flex flex-col items-center">
                        <div class="text-4xl font-bold">{{ partnersCount }}</div>
                        <p class="text-sm text-center">Partenaires</p>
                    </div>
                    <div class="flex flex-col items-center">
                        <div class="text-4xl font-bold">{{ clientsCount }}</div>
                        <p class="text-sm text-center">Clients Satisfaits</p>
                    </div>
                    <div class="flex flex-col items-center">
                        <div class="text-4xl font-bold">{{ avisclients }}</div>
                        <p class="text-sm text-center">Avis Clients</p>
                    </div>
                    <div class="flex flex-col items-center">
                        <div class="text-4xl font-bold">{{ avisGoogle }}</div>
                        <p class="text-sm text-center">Avis Google</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const projectsCount = ref(0);
const partnersCount = ref(0);
const clientsCount = ref(0);
const avisclients = ref(0);
const avisGoogle = ref(0);
const quotesCount = ref(0);

function animateCount(target, countRef) {
    const duration = 8000; // Durée en millisecondes
    const stepTime = Math.abs(Math.floor(duration / target)); // Temps par étape
    let currentCount = 0;

    const interval = setInterval(() => {
        if (currentCount < target) {
            currentCount++;
            countRef.value = currentCount;
        } else {
            clearInterval(interval);
        }
    }, stepTime);
}

onMounted(() => {
    animateCount(50, projectsCount); // Projets Réalisés
    animateCount(100, quotesCount);      // Devis Réalisés
    animateCount(20, partnersCount);   // Partenaires
    animateCount(50, clientsCount);    // Clients
    animateCount(100, avisclients);  // Clients Avis
    animateCount(100, avisGoogle);  // Clients Google
});
</script>

<style scoped>
.carousel {
    position: relative;
    overflow: hidden;
}

.carousel-inner {
    display: flex;
    transition: transform 0.5s ease;
}

.carousel-item {
    min-width: 100%;
    /* Affiche une image à la fois */
}

.carousel-item img {
    width: 100%;
    height: auto;
}

/* Ajout d'un style pour faire défiler automatiquement */
@keyframes slide {
    0% {
        transform: translateX(0);
    }

    100% {
        transform: translateX(-100%);
    }
}

.carousel-inner {
    animation: slide 12s infinite;
    /* Ajustez la durée pour le défilement */
}
</style>