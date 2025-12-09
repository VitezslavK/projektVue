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
    <img v-if="photo" :src="photo" />
    <img
      v-else-if="gender === 'female'"
      src="https://phlebotomycareertraining.com/wp-content/uploads/2023/11/default-avatar-photo-placeholder-icon-grey-vector-38519922-e1699300466746-768x768.jpg"
    />
    <img
      v-else
      src="https://connectkaro.org/wp-content/uploads/2019/03/placeholder-profile-male-500x500.png"
    />

    <div class="info">
      <h3>{{ name }}</h3>

      <div class="label-container">
        <Label theme="grey">{{ age }} let</Label>
        <Label v-if="gender === 'male'" theme="blue">
          {{ gender }}
        </Label>
        <Label v-if="gender === 'female'" theme="pink">
          {{ gender }}
        </Label>
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