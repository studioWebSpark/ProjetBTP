<template>
    <div class="relative overflow-hidden m-8 mt-20">
        <div class="flex transition-transform duration-800 ease-in-out"
            :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
            <div class="flex-none rounded-3xl shadow-lg relative bg-cover bg-center transition-opacity duration-500 ease-in-out h-96"
                v-for="(testimonial, index) in displayedTestimonials" :key="index"
                :style="{ backgroundImage: `url(${testimonial.image})` }">

                <div class="absolute inset-0 flex flex-col justify-between p-4">
                    <div class="flex justify-between items-center">
                        <div class="flex items-center">
                            <span v-for="star in 5" :key="star" class="text-yellow-500 text-xl"
                                :class="{ 'text-yellow-500': star <= testimonial.rating, 'text-gray-400': star > testimonial.rating }">★</span>
                        </div>
                        <div class="text-right">
                            <h3 class="text-white font-semibold text-lg">{{ testimonial.name }} {{ testimonial.surname
                                }}</h3>
                        </div>
                    </div>
                    <div class="bg-black bg-opacity-50 p-4 rounded-3xl">
                        <p class="text-white text-center">{{ testimonial.comment }}</p>
                    </div>
                </div>
            </div>
        </div>
        <button @click="prev"
            class="absolute top-1/2 left-2 transform -translate-y-1/2 bg-transparent border-none text-2xl cursor-pointer text-white">❮</button>
        <button @click="next"
            class="absolute top-1/2 right-2 transform -translate-y-1/2 bg-transparent border-none text-2xl cursor-pointer text-white">❯</button>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const testimonials = ref([
    { image: 'https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80', rating: 5, comment: 'Un service exceptionnel et une qualité irréprochable ! L’équipe a su répondre à toutes mes attentes et a fait preuve d’un grand professionnalisme tout au long du projet. Je recommande vivement cette entreprise à tous ceux qui recherchent un service de qualité.', name: 'Jean', surname: 'Dupont' },
    { image: 'https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80', rating: 4, comment: 'Je suis très satisfait des résultats obtenus. L’équipe a été à l’écoute de mes besoins et a su apporter des solutions adaptées. Bien que quelques petits ajustements aient été nécessaires, le résultat final est à la hauteur de mes attentes.', name: 'Marie', surname: 'Curie' },
    { image: 'https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80', rating: 5, comment: 'Je recommande vivement cette entreprise ! Leur expertise et leur attention aux détails ont fait toute la différence. Chaque étape du projet a été gérée avec soin, et le résultat final est tout simplement magnifique.', name: 'Paul', surname: 'Martin' },
    { image: 'https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80', rating: 5, comment: 'Professionnels et fiables, l’équipe a su respecter les délais tout en maintenant une qualité de travail exceptionnelle. Je suis très heureux du résultat et je n’hésiterai pas à faire appel à leurs services à l’avenir.', name: 'Sophie', surname: 'Durand' },
    { image: 'https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1770&q=80', rating: 4, comment: 'Une excellente expérience dans l’ensemble. L’équipe a été très réactive et a su s’adapter à mes demandes. Quelques petits détails auraient pu être améliorés, mais je suis globalement très satisfait du service.', name: 'Luc', surname: 'Leroy' },
]);

const currentIndex = ref(0);
const visibleCards = ref(1); // Nombre de cartes visibles (1 carte à la fois)

// Dupliquer les témoignages pour créer un effet de défilement infini
const displayedTestimonials = ref([...testimonials.value, ...testimonials.value, ...testimonials.value]);

const next = () => {
    currentIndex.value = (currentIndex.value + 1) % (displayedTestimonials.value.length);
};

const prev = () => {
    currentIndex.value = (currentIndex.value - 1 + displayedTestimonials.value.length) % displayedTestimonials.value.length;
};

// Fonction pour le défilement automatique
const autoSlide = () => {
    setInterval(() => {
        next();
    }, 12000); // Ajustez le temps ici pour la vitesse de défilement (12 secondes)
};

onMounted(() => {
    autoSlide();
});
</script>

<style scoped>
/* Ajoutez ici des styles personnalisés si nécessaire */
.flex-none {
    width: 100%;
    /* Chaque carte occupe 100% de la largeur du conteneur */
}
</style>