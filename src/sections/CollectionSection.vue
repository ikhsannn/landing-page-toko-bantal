<script setup>
import collections from "../data/collection";
</script>

<template>
    <!-- Collection Section Start -->
    <div id="koleksi-section" class="container mx-auto px-5 md:w-4/5">
        <section class="py-16 pt-18">
            <div class="w-4/5 md:w-3/5 mx-auto">
                <h2 class="text-3xl md:text-4xl font-theme-heading font-medium text-center">Koleksi Kami</h2>
                <p class="text-theme-grayish-blue text-center text-lg font-theme-content mt-7">Tidur telentang, menyamping, atau memeluk bantal, tersedia bantal tidur yang dibuat khusus untuk kamar tidur Anda. Pilih dari rangkaian bantal bulu angsa, memory foam, atau poliester dengan ketebalan bervariasi untuk mendukung gaya tidur Anda.</p>
            </div>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mt-12">
                <div v-for="(collections, index) in collections" :key="collections.id" :class="[index === 0 ? '' : '', index === 1 ? '' : '', index === 2 ? '' : '']" class="shadow-lg rounded-lg">
                    <div class="flex justify-center mt-12">
                        <img :src="collections.icon" alt="Browser Logo" />
                    </div>
                    <h3 class="text-2xl font-theme-heading font-medium text-center mt-6">{{ collections.title }}</h3>
                    <p class="text-md font-theme-content text-theme-grayish-blue text-center mt-3">{{ collections.subTitle }}</p>
                    <h3 class="text-2xl font-theme-heading font-medium text-center mt-3 mb-8">{{ collections.harga }}</h3>
                </div>
            </div>
        </section>
    </div>
    <!-- Collection Section End -->
</template>
