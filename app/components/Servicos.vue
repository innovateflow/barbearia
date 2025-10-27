<template>
  <section class="servicos-section">
    <div class="container">
      <!-- Header da Seção -->
      <div class="servicos-header">
        <h2 class="servicos-title">Nossos Serviços</h2>
        <p class="servicos-subtitle">
          Cortes modernos e clássicos feitos por profissionais especializados
        </p>
      </div>

      <!-- Grid de Serviços -->
      <div class="servicos-grid">
        <ServicoCard
          v-for="servico in servicos"
          :key="servico.id"
          :titulo="servico.titulo"
          :descricao="servico.descricao"
          :preco="servico.preco"
          :imagem="servico.imagem"
          @agendar="handleAgendar"
        />
      </div>

      <!-- Call to Action -->
      <div class="servicos-cta">
        <p class="cta-text">
          Não encontrou o corte ideal? Nossos profissionais podem criar um estilo personalizado para você!
        </p>
        <ButtonSecondary 
          text="Ver Todos os Serviços" 
          @click="handleVerTodos"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
// Importações explícitas dos componentes
import ServicoCard from './ServicoCard.vue'
import ButtonSecondary from './ButtonSecondary.vue'

// Dados dos serviços
const servicos = ref([
  {
    id: 1,
    titulo: 'Buzz Cut',
    descricao: 'Corte militar clássico, rápido e prático. Ideal para quem busca um visual limpo e profissional.',
    preco: 'R$ 25,00',
    imagem: 'buzz-cut.png'
  },
  {
    id: 2,
    titulo: 'Corte César',
    descricao: 'Estilo romano atemporal com franja curta. Perfeito para rostos quadrados e ovais.',
    preco: 'R$ 30,00',
    imagem: 'corte-cesar.png'
  },
  {
    id: 3,
    titulo: 'Fade Degradê',
    descricao: 'Transição suave entre diferentes alturas. O corte mais moderno e versátil da atualidade.',
    preco: 'R$ 35,00',
    imagem: 'fade-degrade.png'
  },
  {
    id: 4,
    titulo: 'Messy Hair',
    descricao: 'Visual despojado e natural com textura bagunçada. Ideal para um look casual e jovem.',
    preco: 'R$ 32,00',
    imagem: 'messy-hair.png'
  },
  {
    id: 5,
    titulo: 'Pompadour',
    descricao: 'Elegância clássica com volume no topo. O corte dos cavalheiros modernos e sofisticados.',
    preco: 'R$ 40,00',
    imagem: 'pompadour.png'
  },
  {
    id: 6,
    titulo: 'Undercut',
    descricao: 'Lateral raspada com topo volumoso. Contraste marcante para personalidades fortes.',
    preco: 'R$ 38,00',
    imagem: 'undercut.png'
  }
])

// Função para lidar com o agendamento de um serviço específico
const handleAgendar = (servicoData) => {
  console.log('Agendar serviço:', servicoData)
  // Aqui você pode adicionar a lógica para abrir modal de agendamento ou redirecionar
}

// Função para ver todos os serviços
const handleVerTodos = () => {
  console.log('Ver todos os serviços')
  // Aqui você pode adicionar a lógica para ir para página de serviços completa
}
</script>

<style scoped>
.servicos-section {
  padding: 5rem 0;
  background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 50%, #1a1a1a 100%);
  margin: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.servicos-header {
  text-align: center;
  margin-bottom: 3rem;
}

.servicos-title {
  font-size: 2.5rem;
  font-weight: bold;
  color: #ffffff;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.servicos-subtitle {
  font-size: 1.2rem;
  color: #cccccc;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

.servicos-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-bottom: 4rem;
}

.servicos-cta {
  text-align: center;
  padding: 2rem;
  background: rgba(212, 175, 55, 0.15);
  border-radius: 16px;
  border-left: 4px solid #d4af37;
}

.cta-text {
  font-size: 1.1rem;
  color: #e5e5e5;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

/* Responsividade */
@media (max-width: 992px) {
  .servicos-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }
}

@media (max-width: 768px) {
  .servicos-section {
    padding: 4rem 0;
  }
  
  .servicos-title {
    font-size: 2rem;
  }
  
  .servicos-subtitle {
    font-size: 1.1rem;
  }
  
  .servicos-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
    margin-bottom: 3rem;
  }
  
  .servicos-cta {
    padding: 1.5rem;
  }
  
  .cta-text {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .servicos-section {
    padding: 3rem 0;
  }
  
  .servicos-title {
    font-size: 1.75rem;
  }
  
  .servicos-header {
    margin-bottom: 2rem;
  }
  
  .servicos-grid {
    margin-bottom: 2rem;
  }
  
  .servicos-cta {
    padding: 1rem;
  }
}
</style>