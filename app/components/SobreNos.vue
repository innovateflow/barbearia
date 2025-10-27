<template>
  <section class="sobre-nos-section">
    <div class="container">
      <!-- Lado Esquerdo - Conteúdo Sobre a Barbearia -->
      <div class="sobre-content">
        <h2 class="sobre-title">Sobre Nossa Barbearia</h2>
        <h3 class="sobre-subtitle">Tradição e modernidade em cada corte</h3>
        
        <div class="sobre-text">
          <p>
            Há mais de 15 anos, nossa barbearia combina técnicas tradicionais com tendências 
            modernas para oferecer a melhor experiência em cuidados masculinos da região.
          </p>
          
          <p>
            Nossos profissionais são especializados em cortes clássicos e contemporâneos, 
            barba, bigode e tratamentos capilares. Utilizamos apenas produtos de alta qualidade 
            e equipamentos de última geração.
          </p>
          
          <p>
            Mais que um simples corte de cabelo, oferecemos um momento de relaxamento e 
            cuidado pessoal em um ambiente acolhedor e profissional.
          </p>
        </div>

        <div class="sobre-stats">
          <div class="stat-item">
            <span class="stat-number">15+</span>
            <span class="stat-label">Anos de experiência</span>
          </div>
          <div class="stat-item">
            <span class="stat-number">5000+</span>
            <span class="stat-label">Clientes satisfeitos</span>
          </div>
          <div class="stat-item">
            <span class="stat-number">100%</span>
            <span class="stat-label">Dedicação e qualidade</span>
          </div>
        </div>

        <div class="sobre-actions">
          <ButtonPrimary 
            text="Conheça Nossa Equipe" 
            @click="handleEquipeClick"
          />
        </div>
      </div>

      <!-- Lado Direito - Imagem da Frente -->
      <div class="sobre-image">
        <img 
          src="/images/frente.png" 
          alt="Frente da nossa barbearia - ambiente moderno e acolhedor" 
          class="frente-img"
          loading="lazy"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
// Importação explícita do componente
import ButtonPrimary from './ButtonPrimary.vue'

// Componente Sobre Nós - Segunda seção da página
// Layout responsivo 50/50 com conteúdo à esquerda e imagem à direita

// Função para lidar com o click do botão
const handleEquipeClick = () => {
  console.log('Botão Conheça Nossa Equipe clicado')
  // Aqui você pode adicionar a lógica para redirecionar para página da equipe
}
</script>

<style scoped>
.sobre-nos-section {
  padding: 4rem 0;
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
  margin: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: stretch;
}

.sobre-content {
  display: flex;
  flex-direction: column;
}

.sobre-title {
  font-size: 2.5rem;
  font-weight: bold;
  color: #2d2d2d;
  margin-bottom: 0.5rem;
  line-height: 1.2;
}

.sobre-subtitle {
  font-size: 1.25rem;
  color: #8b4513;
  font-weight: 600;
  margin-bottom: 2rem;
  font-style: italic;
}

.sobre-text {
  margin-bottom: 2.5rem;
}

.sobre-text p {
  font-size: 1.1rem;
  line-height: 1.7;
  color: #555;
  margin-bottom: 1.5rem;
}

.sobre-stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-bottom: 2.5rem;
  padding: 2rem;
  background: rgba(212, 175, 55, 0.1);
  border-radius: 12px;
  border-left: 4px solid #d4af37;
}

.stat-item {
  text-align: center;
}

.stat-number {
  display: block;
  font-size: 2rem;
  font-weight: bold;
  color: #d4af37;
  margin-bottom: 0.5rem;
}

.stat-label {
  font-size: 0.9rem;
  color: #666;
  font-weight: 500;
}

.sobre-actions {
  display: flex;
  justify-content: flex-start;
}

.sobre-image {
  display: flex;
  justify-content: center;
  align-items: stretch;
  height: 100%;
}

.frente-img {
  width: 100%;
  height: 100%;
  max-width: 500px;
  object-fit: cover;
  border-radius: 12px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.frente-img:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.2);
}

/* Responsividade */
@media (max-width: 768px) {
  .sobre-nos-section {
    padding: 3rem 0;
  }
  
  .container {
    grid-template-columns: 1fr;
    gap: 3rem;
    text-align: center;
    align-items: center;
  }
  
  .sobre-image {
    align-items: center;
    height: auto;
  }
  
  .frente-img {
    height: auto;
    aspect-ratio: 3 / 4;
  }
  
  .sobre-title {
    font-size: 2rem;
  }
  
  .sobre-subtitle {
    font-size: 1.1rem;
  }
  
  .sobre-stats {
    grid-template-columns: 1fr;
    gap: 1rem;
    padding: 1.5rem;
  }
  
  .stat-number {
    font-size: 1.75rem;
  }
  
  .sobre-actions {
    justify-content: center;
  }
  
  .frente-img {
    max-width: 380px;
  }
}

@media (max-width: 480px) {
  .sobre-nos-section {
    padding: 2rem 0;
  }
  
  .container {
    gap: 2rem;
  }
  
  .sobre-title {
    font-size: 1.75rem;
  }
  
  .sobre-text p {
    font-size: 1rem;
  }
  
  .sobre-stats {
    padding: 1rem;
  }
  
  .stat-number {
    font-size: 1.5rem;
  }
  
  .stat-label {
    font-size: 0.8rem;
  }
  
  .frente-img {
    max-width: 320px;
  }
}
</style>