<template >
    <div class="container w-50 py-5">
        <h2>Tạo bài viết mới</h2>
        <input v-model="title" placeholder="Tiêu đề bài viết">
        <input v-model="author" placeholder="Tên tác giả">
        <textarea v-model="content" placeholder="Nội dung"></textarea>
        <button class="btn btn-primary" @click="submitPost">Đăng bài</button>
    </div>
</template>
<script setup>
import { ref } from 'vue'

// Sử dụng defineEmits để emit sự kiện
const emit = defineEmits(['add-post'])

const title = ref('')
const content = ref('')
const author = ref('')

function submitPost() {
  if (title.value && content.value && author.value) {
    const newPost = {
      title: title.value,
      content: content.value,
      author: author.value
    }

    // Gửi sự kiện 'add-post' với dữ liệu của bài viết
    emit('add-post', newPost)

    // Reset fields
    title.value = ''
    content.value = ''
    author.value = ''
  }
}
</script>

<style >
    input,textarea{
        display: block;
        width: 100%;
        margin: 10px 0;
        padding: 10px;
        border-radius: 5px;
        border: 1px solid #ddd;
    }
    
</style>