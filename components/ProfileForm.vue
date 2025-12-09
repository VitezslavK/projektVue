<script setup lang="ts">
    const newProfile = ref({
        name: "",
        age: 0,
        gender: "",
        bio: "",
    });
</script>
<template>
  <form class="profile-form">
    <input v-model="newProfile.name" type="text" placeholder="Jméno" />

    <input v-model.number="newProfile.age" type="number" placeholder="Věk" />

    <select v-model="newProfile.gender">
      <option value="male">male</option>
      <option value="female">female</option>
    </select>

    <textarea v-model="newProfile.bio" placeholder="Krátký popis"></textarea>

    <button type="submit">Přidat profil</button>
  </form>
</template>
<style scoped>
    .profile-form {
  max-width: 450px;
  display: flex;
  flex-direction: column;
  gap: 12px;
  padding: 20px 24px;
  border: 1px solid #e5e7eb;
  border-radius: 16px;
  background: #ffffff;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.06);
}

input,
select,
textarea {
  padding: 10px 12px;
  border-radius: 8px;
  border: 1px solid #d1d5db;
  background: #f9fafb;
  font-size: 1rem;
}

textarea {
  min-height: 80px;
  resize: vertical;
}

button {
  padding: 12px;
  border-radius: 8px;
  background: #3b82f6;
  color: white;
  border: none;
  cursor: pointer;
  font-weight: 600;
  transition: background 0.15s;
}

button:hover {
  background: #2563eb;
}
</style>