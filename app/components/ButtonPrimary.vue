<template>
  <button class="btn-primary" :type="type" @click="handleClick">
    <slot>{{ text }}</slot>
  </button>
</template>

<script setup>
// Props do componente
const props = defineProps({
  text: {
    type: String,
    default: 'Botão'
  },
  type: {
    type: String,
    default: 'button'
  }
})

// Emits
const emit = defineEmits(['click'])

// Função para lidar com o click
const handleClick = (event) => {
  emit('click', event)
}
</script>

<style scoped>
.btn-primary {
  background: linear-gradient(135deg, #d4af37, #f1c40f);
  color: #1a1a1a;
  padding: 1rem 2rem;
  border: none;
  border-radius: 8px;
  font-weight: bold;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
  width: 100%;
  max-width: 250px;
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(212, 175, 55, 0.3);
}

.btn-primary:active {
  transform: translateY(0);
}

.btn-primary:focus {
  outline: 2px solid #d4af37;
  outline-offset: 2px;
}

/* Responsividade */
@media (max-width: 768px) {
  .btn-primary {
    width: 100%;
    max-width: none;
  }
}
</style>