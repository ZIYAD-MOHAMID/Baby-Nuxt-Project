<script setup lang="ts">
const props = defineProps<NameProps>();
interface NameProps {
  name: string;
  index: number;
}

const emit = defineEmits(["remove"]);
const removeName = () => {
  emit("remove", props.index);
};
</script>

<template>
  <div class="card">
    <h4 @click="removeName">{{ name }}</h4>
  </div>
</template>

<style scoped>
.card {
  background-color: #1b3c8a;
  border-radius: 1rem;
  color: #fff;
  cursor: pointer;
  width: 25%;
}
</style>
