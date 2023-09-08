<script setup>
import { ref } from "vue";
import Swal from "sweetalert2";

let email = ref("");
let emailError = ref(false);
const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;

let handleSubmit = () => {
    if (!email.value || !emailRegex.test(email.value)) {
        emailError.value = true;
    } else {
        console.log(emailRegex.test(email.value));
        Swal.fire({
            icon: "success",
            title: "Thank You",
            text: `${email.value} subscribed to our newsletter!`,
        });
    }
};
</script>

<template>
    <!-- Contact Section Start -->
    <div id="kontak" class="bg-theme-primary mt-10">
        <div class="container w-full lg:w-2/5 mx-auto px-5">
            <section class="py-16">
                <h2 class="text-3xl md:text-4xl font-medium text-center text-white mt-9 mb-10 font-theme-heading">Diskon 20% Pembelian Hari Ini</h2>

                <form @submit.prevent="handleSubmit()">
                    <div class="relative flex flex-col items-center lg:flex-row justify-center lg:space-x-3">
                        <Button type="submit" btn-type="secondary">Hubungi Kami</Button>
                    </div>
                </form>
            </section>
        </div>
    </div>
    <!-- Contact Section End -->
</template>
