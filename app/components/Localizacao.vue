<template>
  <section class="localizacao-section">
    <div class="container">
      <!-- Título Principal -->
      <div class="header-section">
        <h2 class="main-title">
          Venha nos <span class="highlight">Visitar</span>
        </h2>
        <p class="subtitle">
          Estamos prontos para atendê-lo com excelência. Agende seu horário ou venha conhecer nosso espaço.
        </p>
      </div>

      <div class="localizacao-content">
        <!-- Lado Esquerdo - Informações de Contato -->
        <div class="localizacao-info">
          <h3 class="section-title">Informações de Contato</h3>
          
          <!-- Endereço -->
          <div class="info-item">
            <div class="info-icon location">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M21 10C21 17 12 23 12 23S3 17 3 10C3 7.61305 3.94821 5.32387 5.63604 3.63604C7.32387 1.94821 9.61305 1 12 1C14.3869 1 16.6761 1.94821 18.364 3.63604C20.0518 5.32387 21 7.61305 21 10Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <path d="M12 13C13.6569 13 15 11.6569 15 10C15 8.34315 13.6569 7 12 7C10.3431 7 9 8.34315 9 10C9 11.6569 10.3431 13 12 13Z" stroke="currentColor" stroke-width="2"/>
              </svg>
            </div>
            <div class="info-content">
              <h4 class="info-label">Endereço</h4>
              <p class="info-text">Rua da Barbearia, 123</p>
              <p class="info-text">Centro - São Paulo, SP</p>
              <p class="info-text">CEP: 01234-567</p>
            </div>
          </div>

          <!-- Telefone -->
          <div class="info-item">
            <div class="info-icon phone">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M22 16.92V19.92C22.0011 20.1985 21.9441 20.4742 21.8325 20.7293C21.7209 20.9845 21.5573 21.2136 21.3521 21.4019C21.1468 21.5901 20.9046 21.7335 20.6407 21.8227C20.3769 21.9119 20.0974 21.9451 19.82 21.92C16.7428 21.5856 13.787 20.5341 11.19 18.85C8.77382 17.3147 6.72533 15.2662 5.18999 12.85C3.49997 10.2412 2.44808 7.27099 2.11999 4.18C2.095 3.90347 2.12787 3.62476 2.21649 3.36162C2.30512 3.09849 2.44756 2.85669 2.63476 2.65162C2.82196 2.44655 3.0498 2.28271 3.30379 2.17052C3.55777 2.05833 3.83233 2.00026 4.10999 2H7.10999C7.59531 1.99522 8.06579 2.16708 8.43376 2.48353C8.80173 2.79999 9.04207 3.23945 9.10999 3.72C9.23662 4.68007 9.47144 5.62273 9.80999 6.53C9.94454 6.88792 9.97366 7.27691 9.8939 7.65088C9.81415 8.02485 9.62886 8.36811 9.35999 8.64L8.08999 9.91C9.51355 12.4135 11.5865 14.4864 14.09 15.91L15.36 14.64C15.6319 14.3711 15.9751 14.1858 16.3491 14.1061C16.7231 14.0263 17.1121 14.0555 17.47 14.19C18.3773 14.5286 19.3199 14.7634 20.28 14.89C20.7658 14.9585 21.2094 15.2032 21.5265 15.5775C21.8437 15.9518 22.0122 16.4296 22 16.92Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <div class="info-content">
              <h4 class="info-label">Telefone</h4>
              <p class="info-text phone-number" @click="ligarTelefone">(11) 99999-9999</p>
              <p class="info-subtext">WhatsApp disponível</p>
            </div>
          </div>

          <!-- Email -->
          <div class="info-item">
            <div class="info-icon email">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M4 4H20C21.1 4 22 4.9 22 6V18C22 19.1 21.1 20 20 20H4C2.9 20 2 19.1 2 18V6C2 4.9 2.9 4 4 4Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                <polyline points="22,6 12,13 2,6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <div class="info-content">
              <h4 class="info-label">Email</h4>
              <p class="info-text">contato@elitebarbershop.com</p>
            </div>
          </div>

          <!-- Horário de Funcionamento -->
          <div class="horario-card">
            <div class="horario-header">
              <div class="horario-icon">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="12" cy="12" r="10" stroke="currentColor" stroke-width="2"/>
                  <polyline points="12,6 12,12 16,14" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </div>
              <h4 class="horario-title">Horário de Funcionamento</h4>
            </div>
            
            <div class="horario-list">
              <div class="horario-item">
                <span class="dia">Segunda a Sexta</span>
                <span class="hora">08:00 - 19:00</span>
              </div>
              <div class="horario-item">
                <span class="dia">Sábado</span>
                <span class="hora">08:00 - 17:00</span>
              </div>
              <div class="horario-item">
                <span class="dia">Domingo</span>
                <span class="hora">09:00 - 15:00</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Lado Direito - Mapa -->
        <div class="localizacao-mapa">
          <div class="mapa-container">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3657.1970467886673!2d-46.65645948451431!3d-23.561684284685976!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce59c8da0aa315%3A0xd59f9431f2c9776a!2sAv.%20Paulista%2C%20900%20-%20Bela%20Vista%2C%20S%C3%A3o%20Paulo%20-%20SP!5e0!3m2!1spt-BR!2sbr!4v1635000000000!5m2!1spt-BR!2sbr"
              width="100%"
              height="100%"
              style="border:0;"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
              title="Localização Barber Brado - Av. Paulista, 900"
            ></iframe>
            
            <!-- Badge de Fácil Acesso -->
            <div class="acesso-badge">
              <div class="badge-icon">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M21 10C21 17 12 23 12 23S3 17 3 10C3 7.61305 3.94821 5.32387 5.63604 3.63604C7.32387 1.94821 9.61305 1 12 1C14.3869 1 16.6761 1.94821 18.364 3.63604C20.0518 5.32387 21 7.61305 21 10Z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </div>
              <div class="badge-content">
                <span class="badge-title">Fácil Acesso</span>
                <span class="badge-subtitle">Centro da cidade</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Função para ligar para o telefone
const ligarTelefone = () => {
  window.open('tel:+5511999999999', '_self')
}
</script>

<style scoped>
.localizacao-section {
  padding: 5rem 0;
  background: #f5f5f5;
  position: relative;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

/* Header Section */
.header-section {
  text-align: center;
  margin-bottom: 4rem;
}

.main-title {
  font-size: 3rem;
  font-weight: bold;
  color: #2d2d2d;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.highlight {
  color: #d4af37;
}

.subtitle {
  font-size: 1.1rem;
  color: #666;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

/* Content Layout */
.localizacao-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: stretch;
}

/* Lado Esquerdo - Informações */
.localizacao-info {
  background: white;
  border-radius: 20px;
  padding: 2rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
}

.section-title {
  font-size: 1.5rem;
  font-weight: bold;
  color: #2d2d2d;
  margin-bottom: 2rem;
}

.info-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  margin-bottom: 1.5rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid #f0f0f0;
}

.info-item:last-of-type {
  border-bottom: none;
  margin-bottom: 2rem;
}

.info-icon {
  flex-shrink: 0;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
}

.info-icon.location {
  background: #d4af37;
}

.info-icon.phone {
  background: #d4af37;
}

.info-icon.email {
  background: #d4af37;
}

.info-content {
  flex-grow: 1;
}

.info-label {
  font-size: 1rem;
  font-weight: bold;
  color: #2d2d2d;
  margin-bottom: 0.5rem;
}

.info-text {
  font-size: 0.95rem;
  color: #666;
  margin: 0.25rem 0;
  line-height: 1.4;
}

.phone-number {
  color: #2d2d2d;
  cursor: pointer;
  font-weight: 500;
}

.phone-number:hover {
  color: #d4af37;
}

.info-subtext {
  font-size: 0.85rem;
  color: #999;
  font-style: italic;
}

/* Horário Card */
.horario-card {
  background: #f8f9fa;
  border-radius: 15px;
  padding: 1.5rem;
  margin-top: 1rem;
}

.horario-header {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 1rem;
}

.horario-icon {
  width: 24px;
  height: 24px;
  color: #d4af37;
}

.horario-title {
  font-size: 1rem;
  font-weight: bold;
  color: #2d2d2d;
  margin: 0;
}

.horario-list {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.horario-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem 0;
}

.dia {
  font-size: 0.9rem;
  color: #666;
  font-weight: 500;
}

.hora {
  font-size: 0.9rem;
  color: #2d2d2d;
  font-weight: bold;
}

/* Lado Direito - Mapa */
.localizacao-mapa {
  position: relative;
  display: flex;
  flex-direction: column;
}

.mapa-container {
  width: 100%;
  height: 100%;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  position: relative;
  flex: 1;
}

/* Badge de Fácil Acesso */
.acesso-badge {
  position: absolute;
  bottom: 20px;
  left: 20px;
  background: white;
  border-radius: 12px;
  padding: 0.75rem 1rem;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  display: flex;
  align-items: center;
  gap: 0.5rem;
  z-index: 10;
}

.badge-icon {
  width: 20px;
  height: 20px;
  color: #d4af37;
}

.badge-content {
  display: flex;
  flex-direction: column;
}

.badge-title {
  font-size: 0.85rem;
  font-weight: bold;
  color: #2d2d2d;
  line-height: 1;
}

.badge-subtitle {
  font-size: 0.75rem;
  color: #666;
  line-height: 1;
}

/* Responsividade */
@media (max-width: 1024px) {
  .main-title {
    font-size: 2.5rem;
  }
  
  .localizacao-content {
    gap: 2rem;
  }
}

@media (max-width: 768px) {
  .localizacao-section {
    padding: 3rem 0;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  .header-section {
    margin-bottom: 3rem;
  }
  
  .main-title {
    font-size: 2rem;
  }
  
  .subtitle {
    font-size: 1rem;
  }
  
  .localizacao-content {
    grid-template-columns: 1fr;
    gap: 2rem;
    align-items: flex-start;
  }
  
  .localizacao-info {
    padding: 1.5rem;
  }
  
  .localizacao-mapa {
    min-height: 400px;
  }
  
  .mapa-container {
    height: 400px;
  }
  
  .acesso-badge {
    bottom: 15px;
    left: 15px;
    padding: 0.5rem 0.75rem;
  }
}

@media (max-width: 480px) {
  .main-title {
    font-size: 1.75rem;
  }
  
  .localizacao-info {
    padding: 1rem;
  }
  
  .info-icon {
    width: 35px;
    height: 35px;
  }
  
  .horario-card {
    padding: 1rem;
  }
  
  .localizacao-mapa {
    min-height: 350px;
  }
  
  .mapa-container {
    height: 350px;
  }
}
</style>