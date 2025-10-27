<template>
  <div class="servico-card">
    <div class="servico-image">
      <img 
        :src="imageSrc" 
        :alt="`Corte ${titulo} - Barbearia`" 
        class="servico-img"
        loading="lazy"
      />
    </div>
    
    <div class="servico-content">
      <h3 class="servico-titulo">{{ titulo }}</h3>
      <p class="servico-descricao">{{ descricao }}</p>
      
      <div class="servico-footer">
        <div class="servico-preco">{{ preco }}</div>
        <ButtonPrimary 
          text="Agendar" 
          @click="handleAgendarClick"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
// Importação explícita do componente
import ButtonPrimary from './ButtonPrimary.vue'

// Props do componente
const props = defineProps({
  titulo: {
    type: String,
    required: true
  },
  descricao: {
    type: String,
    required: true
  },
  preco: {
    type: String,
    required: true
  },
  imagem: {
    type: String,
    required: true
  }
})

// Computed para gerar o caminho da imagem
const imageSrc = computed(() => `/images/${props.imagem}`)

// Emits
const emit = defineEmits(['agendar'])

// Função para lidar com o click do botão agendar
const handleAgendarClick = () => {
  emit('agendar', {
    titulo: props.titulo,
    preco: props.preco,
    imagem: props.imagem
  })
}
</script>

<style scoped>
.servico-card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.servico-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.servico-image {
  position: relative;
  width: 100%;
  aspect-ratio: 1 / 1;
  overflow: hidden;
}

.servico-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.servico-card:hover .servico-img {
  transform: scale(1.05);
}

.servico-content {
  padding: 1.5rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.servico-titulo {
  font-size: 1.25rem;
  font-weight: bold;
  color: #2d2d2d;
  margin-bottom: 0.75rem;
  line-height: 1.3;
  text-align: center;
}

.servico-descricao {
  font-size: 0.95rem;
  color: #666;
  line-height: 1.5;
  margin-bottom: 1.5rem;
  text-align: center;
  flex-grow: 1;
}

.servico-footer {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.servico-preco {
  font-size: 1.4rem;
  font-weight: bold;
  color: #d4af37;
  margin: 0;
  flex: 0 0 70%;
  text-align: left;
}

.servico-footer :deep(.btn-primary) {
  flex: 0 0 30%;
  width: auto !important;
  max-width: none !important;
  min-width: auto;
  padding: 0.5rem 0.75rem !important;
  font-size: 0.875rem !important;
  white-space: nowrap;
}

/* Responsividade */
@media (max-width: 768px) {
  .servico-content {
    padding: 1.25rem;
  }
  
  .servico-titulo {
    font-size: 1.1rem;
  }
  
  .servico-descricao {
    font-size: 0.9rem;
  }
  
  .servico-preco {
    font-size: 1.25rem;
  }
  
  .servico-footer {
    flex-direction: column;
    gap: 0.75rem;
    align-items: stretch;
  }
  
  .servico-preco {
    flex: none;
    text-align: center;
  }
  
  .servico-footer :deep(.btn-primary) {
    flex: none;
    width: 100% !important;
  }
}

@media (max-width: 480px) {
  .servico-content {
    padding: 1rem;
  }
  
  .servico-titulo {
    font-size: 1rem;
  }
  
  .servico-descricao {
    font-size: 0.85rem;
  }
  
  .servico-preco {
    font-size: 1.1rem;
  }
}
</style>