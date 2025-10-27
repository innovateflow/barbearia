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
            <button class="btn-primary">
              Agendar Horário
            </button>
            <button class="btn-secondary">
              Ver Serviços
            </button>
          </div>
        </div>
      </div>

      <!-- Lado Direito - Espaço para Imagem -->
      <div class="hero-image">
        <div class="image-placeholder">
          <div class="placeholder-content">
            <svg class="placeholder-icon" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M4 3a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V5a2 2 0 00-2-2H4zm12 12H4l4-8 3 6 2-4 3 6z" clip-rule="evenodd" />
            </svg>
            <p>Espaço reservado para imagem</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Componente Hero - Primeira seção da página
// Layout responsivo 50/50 com texto à esquerda e imagem à direita
</script>

<style scoped>
.hero-section {
  min-height: 100vh;
  background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 25%, #4a4a4a 50%, #8b4513 75%, #d4af37 100%);
  display: flex;
  align-items: center;
  margin: 0;
  padding: 0;
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
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(212, 175, 55, 0.3);
}

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
}

.btn-secondary:hover {
  background: #d4af37;
  color: #1a1a1a;
  transform: translateY(-2px);
}

.hero-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-placeholder {
  width: 100%;
  height: 500px;
  background: rgba(255, 255, 255, 0.1);
  border: 2px dashed rgba(212, 175, 55, 0.5);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  backdrop-filter: blur(10px);
}

.placeholder-content {
  text-align: center;
  color: rgba(255, 255, 255, 0.7);
}

.placeholder-icon {
  width: 4rem;
  height: 4rem;
  margin-bottom: 1rem;
  opacity: 0.6;
}

.placeholder-content p {
  font-size: 1.1rem;
  font-weight: 500;
}

/* Responsividade */
@media (max-width: 768px) {
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
  
  .image-placeholder {
    height: 300px;
  }
}

@media (max-width: 480px) {
  .hero-headline {
    font-size: 2rem;
  }
  
  .hero-actions {
    flex-direction: column;
    align-items: center;
  }
  
  .btn-primary,
  .btn-secondary {
    width: 100%;
    max-width: 250px;
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