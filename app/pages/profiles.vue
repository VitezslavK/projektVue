<script setup lang="ts">
const profiles = [
  {
    name: 'Anna Nováková',
    age: 17,
    gender: 'female',
    photo: 'https://randomuser.me/api/portraits/women/45.jpg',
    bio: 'Ráda kreslí, programuje a tráví čas venku se psem. Chce se naučit Vue a dělat vlastní weby.'
  },
  {
    name: 'Petr Dvořák',
    age: 18,
    gender: 'male',
    bio: 'Miluje auta, zajímá se o 3D tisk a občas pomáhá ve školní dílně. Baví ho JavaScript a Arduino.'
  },
  {
    name: 'Lucie Králová',
    age: 16,
    gender: 'female',
    bio: 'Má ráda hudbu a cestování. Učí se HTML a CSS, ale chce pochopit i základy backendu.'
  },
  {
    name: 'Martin Král',
    age: 17,
    gender: 'male',
    photo: 'https://randomuser.me/api/portraits/men/28.jpg',
    bio: 'Hraje florbal a zajímá se o kyberbezpečnost. Chtěl by dělat v IT jako etický hacker.'
  },
  {
    name: 'Tereza Černá',
    age: 18,
    gender: 'female',
    bio: 'Zajímá ji UX design a psychologie uživatelů. Ráda navrhuje rozhraní v Figma a zkouší frontend.'
  },
  {
    name: 'Vitezsklav Kubis',
    age: 17,
    gender: 'male',
    photo: '',
    bio: 'Lol',
  },
]
</script>
<template>
    <profileCard
    v-for="profile in profiles"
    :key=" profile.name "
    :name="profile.name"
    :age="profile.age"
    :gender="profile.gender"
    :bio="profile.bio"
    :photo="profile.photo"
    />
</template>

<style scoped></style>