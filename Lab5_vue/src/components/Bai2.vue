<template>
    <h2>Bài 2</h2>
    <div class="px-5">
        <input v-model="userInput" placeholder="Nhập dữ liệu vào đây" />
        <p>Giá trị bạn nhập: {{ userInput }}</p>
    </div>
</template>
<script setup>
import { ref } from 'vue';
const userInput = ref('BichChu DepGai');
</script>
<style>
</style>