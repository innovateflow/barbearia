<template>
  <section class="hero-section">
    <div class="container">
      <!-- Lado Esquerdo - Texto de Apresentação -->
      <div class="hero-content">
        <div class="hero-text">
          <h1 class="hero-headline">
            Transforme seu 
            <span class="highlight">Estilo</span>
          </h1>
          <h2 class="hero-subheadline">
            Na melhor barbearia da cidade
          </h2>
          <p class="hero-description">
            Cortes modernos, barba impecável e um atendimento de primeira classe. 
            Experimente o que há de melhor em cuidado masculino.
          </p>
          <div class="hero-actions">
            <ButtonPrimary 
              text="Agendar Horário" 
              @click="handleAgendarClick"
            />
            <ButtonSecondary 
              text="Ver Serviços" 
              @click="handleServicosClick"
            />
          </div>
        </div>
      </div>

      <!-- Lado Direito - Imagem Hero -->
      <div class="hero-image">
        <img 
          src="/images/image-hero.png" 
          alt="Barbearia - Ambiente moderno e profissional" 
          class="hero-img"
          loading="lazy"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
// Importações explícitas dos componentes
import ButtonPrimary from './ButtonPrimary.vue'
import ButtonSecondary from './ButtonSecondary.vue'

// Componente Hero - Primeira seção da página
// Layout responsivo 50/50 com texto à esquerda e imagem à direita

// Funções para lidar com os clicks dos botões
const handleAgendarClick = () => {
  console.log('Botão Agendar Horário clicado')
  // Aqui você pode adicionar a lógica para redirecionar ou abrir modal
}

const handleServicosClick = () => {
  console.log('Botão Ver Serviços clicado')
  // Aqui você pode adicionar a lógica para redirecionar para seção de serviços
}
</script>

<style scoped>
.hero-section {
  min-height: 80vh;
  background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 25%, #4a4a4a 50%, #8b4513 75%, #d4af37 100%);
  display: flex;
  align-items: center;
  margin: 0;
  padding: 4rem 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.hero-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.hero-text {
  color: white;
}

.hero-headline {
  font-size: 3.5rem;
  font-weight: bold;
  line-height: 1.1;
  margin-bottom: 1rem;
}

.highlight {
  background: linear-gradient(135deg, #d4af37, #f1c40f);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-subheadline {
  font-size: 1.5rem;
  font-weight: 600;
  color: #e5e5e5;
  margin-bottom: 1.5rem;
}

.hero-description {
  font-size: 1.1rem;
  line-height: 1.6;
  color: #cccccc;
  margin-bottom: 2.5rem;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.hero-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-img {
  width: 100%;
  height: 500px;
  object-fit: cover;
  border-radius: 12px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.hero-img:hover {
  transform: scale(1.02);
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.4);
}

/* Responsividade */
@media (max-width: 768px) {
  .hero-section {
    min-height: 60vh;
    padding: 2rem 0;
  }
  
  .container {
    grid-template-columns: 1fr;
    gap: 2rem;
    text-align: center;
  }
  
  .hero-headline {
    font-size: 2.5rem;
  }
  
  .hero-subheadline {
    font-size: 1.25rem;
  }
  
  .hero-actions {
    justify-content: center;
  }
  
  .hero-img {
    height: 300px;
  }
}

@media (max-width: 480px) {
  .hero-section {
    min-height: 50vh;
    padding: 1.5rem 0;
  }
  
  .hero-headline {
    font-size: 2rem;
  }
  
  .hero-actions {
    flex-direction: column;
    align-items: center;
  }
  
  .hero-img {
    height: 250px;
  }
}

/* Reset global para remover espaços externos */
:global(body) {
  margin: 0;
  padding: 0;
}

:global(html) {
  margin: 0;
  padding: 0;
}
</style>