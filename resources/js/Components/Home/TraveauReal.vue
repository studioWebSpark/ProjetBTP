<template>
    <section class="mt-14 m-8 ">
        <h2 class="text-2xl font-bold mb-4">Travaux Réalisés</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
            <!-- Carte 1 (plus grande) -->
            <div
                class="overflow-hidden rounded-3xl shadow-lg col-span-1 md:col-span-2 lg:col-span-2 relative bg-[url(https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80)] bg-cover bg-center transition-opacity duration-500 ease-in-out ">
                <!-- Hauteur augmentée -->
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Mondrian</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
            <!-- Carte 2 -->
            <div class="relative overflow-hidden rounded-3xl shadow-lg">
                <img src="https://example.com/image2.jpg" alt="Nirnia" class="w-full h-96 object-cover" />
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Nirnia</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
            <!-- Carte 3 -->
            <div class="relative overflow-hidden rounded-3xl shadow-lg">
                <img src="https://example.com/image3.jpg" alt="Artex" class="w-full h-96 object-cover" />
                <div class="absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Artex</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
            <!-- Carte 4 -->
            <div
                class="overflow-hidden rounded-3xl shadow-lg col-span-1 md:col-span-2 lg:col-span-2 relative bg-[url(https://images.unsplash.com/photo-1604014237800-1c9102c219da?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80)] bg-cover bg-center transition-opacity duration-500 ease-in-out ">

                <div class=" absolute bottom-0 left-0 right-0 bg-black bg-opacity-50 p-4">
                    <h3 class="text-white font-semibold">Brera</h3>
                    <a href="#" class="text-white">→</a>
                </div>
            </div>
          
            
            
        </div>
    </section>
</template>