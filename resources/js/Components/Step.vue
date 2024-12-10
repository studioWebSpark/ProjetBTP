<template>
    <div class="flex justify-center mt-14">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-4 w-full mx-auto px-8">
            <!-- Carte avec effet de fondu en bas à gauche -->
            <div class="h-[500px] rounded-3xl bg-gray-200 relative bg-[url(https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80)] bg-cover bg-center transition-opacity duration-500 ease-in-out "
                id="image-container">
                <!-- Vous pouvez ajouter un effet de flou ou d'autres éléments ici si nécessaire -->
            </div>

            <!-- Espace pour le texte à droite -->
            <div class="flex flex-col justify-center ">
                <h2 class="text-3xl font-bold mt-4" id="typed-title"></h2>
                <div class="mt-6">
                    <p class="text-gray-600 font-semibold" id="typed-paragraph"></p>
                    <div class="text-gray-600" id="typed-steps"></div>
                </div>
                <!-- Section pour afficher les détails de chaque étape -->
                <div id="steps-container" class="mt-4"></div>
                <button id="back-button" class="mt-4 hidden bg-gray-900 text-white py-2 px-4 rounded">Retour</button>
            </div>
        </div>
    </div>
</template>

<script setup>
import { onMounted } from 'vue';

let stepsDisplayed = false; // Ajout d'une variable pour suivre l'affichage des étapes

const titleText = "Modern Minimalist";
const paragraphText = "Aesthetic furniture where every piece tells a story of style.";
const steps = [
    { icon: '🔍', text: 'Consultation initiale', detail: 'Nous discutons de vos besoins et de vos attentes.', description: 'Cliquez pour plus de détails.' },
    { icon: '🗺️', text: 'Planification du projet', detail: 'Élaboration d’un plan détaillé pour le projet.', description: 'Cliquez pour plus de détails.' },
    { icon: '🔨', text: 'Exécution des travaux', detail: 'Mise en œuvre des travaux selon le plan.', description: 'Cliquez pour plus de détails.' },
    { icon: '🔍', text: 'Inspection finale', detail: 'Vérification de la qualité des travaux réalisés.', description: 'Cliquez pour plus de détails.' },
    { icon: '📦', text: 'Remise du projet', detail: 'Remise des clés et présentation du projet final.', description: 'Cliquez pour plus de détails.' }
];

onMounted(() => {
    const imageContainer = document.getElementById('image-container');
    const typedTitleElement = document.getElementById('typed-title');
    const typedParagraphElement = document.getElementById('typed-paragraph');
    const stepsContainer = document.getElementById('steps-container');

    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting && !stepsDisplayed) { // Vérifie si les étapes n'ont pas encore été affichées
                stepsDisplayed = true; // Marque les étapes comme affichées
                typeText(titleText, typedTitleElement, () => {
                    typeText(paragraphText, typedParagraphElement, () => {
                        displaySteps(steps, stepsContainer);
                    });
                });
            }
        });
    });

    observer.observe(imageContainer);
});

// Fonction pour simuler l'effet d'écriture
function typeText(text, element, callback) {
    let index = 0;
    const typingSpeed = 50; // Vitesse de l'effet d'écriture (en ms)

    function type() {
        if (index < text.length) {
            element.textContent += text.charAt(index);
            index++;
            setTimeout(type, typingSpeed);
        } else if (callback) {
            callback(); // Appelle le callback une fois l'écriture terminée
        }
    }

    type();
}

// Fonction pour afficher les étapes sans les faire disparaître
function displaySteps(steps, stepsContainer) {
    let index = 0;

    function showStep() {
        if (index < steps.length) {
            const step = steps[index];
            const stepCard = document.createElement('div');
            stepCard.className = "p-4 border rounded-lg shadow-lg mb-4 transform scale-75 opacity-0 transition-all duration-500 cursor-pointer";

            // Ajout de l'icône, du texte et de la description
            stepCard.innerHTML = `${step.icon} <strong>${step.text}</strong> - <span class="text-gray-500">${step.description}</span>`;

            // Ajout d'un événement de clic
            stepCard.addEventListener('click', () => {
                updateDisplay(step); // Met à jour l'affichage avec les détails de l'étape
                stepsContainer.innerHTML = ''; // Vide le conteneur des étapes pour ne pas afficher les autres
            });

            // Ajout d'un événement de survol
            stepCard.addEventListener('mouseenter', () => {
                stepCard.classList.add('bg-black', 'text-white');
            });
            stepCard.addEventListener('mouseleave', () => {
                stepCard.classList.remove('bg-black', 'text-white');
            });

            stepsContainer.appendChild(stepCard);

            // Afficher la carte avec effet de zoom
            setTimeout(() => {
                stepCard.classList.remove('opacity-0', 'scale-75');
                stepCard.classList.add('opacity-100', 'scale-100');
            }, 100);

            // Passer à la prochaine étape après 2 secondes
            setTimeout(() => {
                index++;
                showStep();
            }, 900);
        }
    }

    function updateDisplay(step) {
        const typedTitleElement = document.getElementById('typed-title');
        const typedParagraphElement = document.getElementById('typed-paragraph');
        const backButton = document.getElementById('back-button');

        typedTitleElement.textContent = step.text; // Met à jour le titre
        typedParagraphElement.textContent = step.detail; // Met à jour la description
        backButton.classList.remove('hidden'); // Affiche le bouton de retour

        // Ajout d'un événement de clic pour le bouton de retour
        backButton.onclick = () => {
            typedTitleElement.textContent = titleText; // Réinitialise le titre
            typedParagraphElement.textContent = paragraphText; // Réinitialise la description
            backButton.classList.add('hidden'); // Cache le bouton de retour
            stepsContainer.innerHTML = ''; // Réinitialise le conteneur des étapes
            index = 0; // Réinitialise l'index
            showStep(); // Affiche à nouveau les étapes
        };
    }

    showStep(); // Commencer à afficher les étapes
}
</script>