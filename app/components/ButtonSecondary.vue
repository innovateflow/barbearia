<template>
  <a 
    v-if="href" 
    :href="href" 
    :target="target"
    class="btn-secondary btn-link"
    role="button"
  >
    <slot>{{ text }}</slot>
  </a>
  <button 
    v-else
    class="btn-secondary" 
    :type="type" 
    @click="handleClick"
  >
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
  },
  href: {
    type: String,
    default: null
  },
  target: {
    type: String,
    default: '_blank'
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
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.btn-secondary.btn-link {
  display: inline-flex;
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