<template>
  <button class="btn-secondary" :type="type" @click="handleClick">
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
.btn-secondary {
  background: transparent;
  color: white;
  padding: 1rem 2rem;
  border: 2px solid #d4af37;
  border-radius: 8px;
  font-weight: bold;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
  width: 100%;
  max-width: 250px;
}

.btn-secondary:hover {
  background: #d4af37;
  color: #1a1a1a;
  transform: translateY(-2px);
}

.btn-secondary:active {
  transform: translateY(0);
}

.btn-secondary:focus {
  outline: 2px solid #d4af37;
  outline-offset: 2px;
}

/* Responsividade */
@media (max-width: 768px) {
  .btn-secondary {
    width: 100%;
    max-width: none;
  }
}
</style>