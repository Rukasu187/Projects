<script setup lang="ts">
import { ref } from "vue";
import heroImg from "../assets/hero.png";
import viteLogo from "../assets/vite.svg";
import vueLogo from "../assets/vue.svg";

const count = ref(0);
</script>

<template>
    <section id="center">
        <div class="hero">
            <img :src="heroImg" class="base" width="170" height="179" alt="" />
            <img :src="vueLogo" class="framework" alt="Vue logo" />
            <img :src="viteLogo" class="vite" alt="Vite logo" />
        </div>
        <button
            type="button"
            class="counter hover:cursor-pointer"
            @click="count++"
        >
            Count
        </button>
    </section>

    <div class="ticks"></div>

    <section id="next-steps">
        <div id="docs">
            <svg class="icon" role="presentation" aria-hidden="true">
                <use href="/icons.svg#documentation-icon"></use>
            </svg>
            <h2>Want to reset your Count?</h2>
            <p>reset by pressing the button below</p>
            <button
                type="button"
                class="counter my-4 hover:cursor-pointer"
                @click="count = 0"
            >
                Reset
            </button>
        </div>
        <div v-if="count == 3" id="social">
            <h3 class="text-shadow-white">count is {{ count }} secret</h3>
        </div>
        <div v-else-if="count < 3">
            <p>count is {{ count }} you havent found the secret yet</p>
        </div>
        <div v-else>
            <p>count is {{ count }}</p>
        </div>
    </section>

    <div class="ticks"></div>
    <section id="spacer"></section>
</template>
