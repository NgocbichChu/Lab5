<template>
    <h2>Bài 1</h2>
    <div class="px-5 w-50 pb-5">
        <p>{{ message }}</p>
        <button class="btn btn-dark" @click="updateMessage">Thay đổi thông điệp</button>
    </div>
</template>
<script setup>
    import { ref } from 'vue';
    const message = ref('Thông điệp ban đầu');
    const updateMessage = () => {
        message.value = 'Thông điệp đã được thay đổi!';
};
</script>
<style>
</style>