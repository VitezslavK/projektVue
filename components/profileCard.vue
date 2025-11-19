<script setup lang="ts">
defineProps<{
  name: string;
    age: number;
    gender: string;
    photo?: string;
    bio: string;
}>();</script>

<template>
<div class="profile-card">
    <img v-if="photo" :src="photo"/>
    <img v-else
    />

    <div class="info">
      <h3>{{name}}</h3>

      <div class="label-container">
        <span>{{age}}let</span>
        <span>{{ gender }}</span>
      </div>

      <p>{{ bio }}</p>
    </div>
  </div>
</template>

<style scoped>
.profile-card {
max-width: 450px;
display: flex;
gap: 20px;
align-items: center;
padding: 20px 24px;
border: 1px solid #e5e7eb;
border-radius: 20px;
background: #ffffff;
box-shadow: 0 8px 24px rgba(0, 0, 0, 0.06);
}

img {
width: 96px;
height: 96px;
border-radius: 9999px;
object-fit: cover;
border: 1px solid #e5e7eb;
}
h3 {
margin: 0 0 8px;
font-size: 1.75rem;
line-height: 2rem;
font-weight: 700;
}

.label-container {
display: flex;
gap: 8px;
margin-bottom: 8px;
}
</style>