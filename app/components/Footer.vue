<template>
  <footer class="footer-section">
    <div class="container">
      <div class="footer-content">
        <!-- Lado Esquerdo - Nome da Barbearia -->
        <div class="footer-brand">
          <h3 class="brand-name">Barber Brado</h3>
          <p class="brand-tagline">Seu estilo, nossa paixão</p>
        </div>

        <!-- Lado Direito - Redes Sociais -->
        <div class="footer-social">
          <a 
            href="https://instagram.com/barberbrado" 
            target="_blank" 
            class="social-link instagram"
            aria-label="Siga-nos no Instagram"
          >
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <rect x="2" y="2" width="20" height="20" rx="5" ry="5" stroke="currentColor" stroke-width="2"/>
              <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z" stroke="currentColor" stroke-width="2"/>
              <line x1="17.5" y1="6.5" x2="17.51" y2="6.5" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </a>

          <a 
            href="https://facebook.com/barberbrado" 
            target="_blank" 
            class="social-link facebook"
            aria-label="Curta nossa página no Facebook"
          >
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </a>

          <a 
            href="https://youtube.com/@barberbrado" 
            target="_blank" 
            class="social-link youtube"
            aria-label="Inscreva-se em nosso canal do YouTube"
          >
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M22.54 6.42a2.78 2.78 0 0 0-1.94-2C18.88 4 12 4 12 4s-6.88 0-8.6.46a2.78 2.78 0 0 0-1.94 2A29 29 0 0 0 1 11.75a29 29 0 0 0 .46 5.33A2.78 2.78 0 0 0 3.4 19c1.72.46 8.6.46 8.6.46s6.88 0 8.6-.46a2.78 2.78 0 0 0 1.94-2 29 29 0 0 0 .46-5.25 29 29 0 0 0-.46-5.33z" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              <polygon points="9.75,15.02 15.5,11.75 9.75,8.48" fill="currentColor"/>
            </svg>
          </a>
        </div>
      </div>

      <!-- Linha de Copyright -->
      <div class="footer-bottom">
        <p class="copyright">
          © {{ currentYear }} Barber Brado. Todos os direitos reservados.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
// Ano atual para o copyright
const currentYear = new Date().getFullYear()
</script>

<style scoped>
.footer-section {
  background: #1a1a1a;
  color: white;
  padding: 3rem 0 1.5rem;
  margin-top: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 2rem;
  border-bottom: 1px solid #333;
}

/* Lado Esquerdo - Marca */
.footer-brand {
  flex: 1;
}

.brand-name {
  font-size: 2rem;
  font-weight: bold;
  color: #d4af37;
  margin: 0 0 0.5rem 0;
  line-height: 1.2;
}

.brand-tagline {
  font-size: 1rem;
  color: #ccc;
  margin: 0;
  font-style: italic;
}

/* Lado Direito - Redes Sociais */
.footer-social {
  display: flex;
  gap: 1.5rem;
  align-items: center;
}

.social-link {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 48px;
  height: 48px;
  border-radius: 50%;
  transition: all 0.3s ease;
  text-decoration: none;
  border: 2px solid transparent;
}

.social-link:hover {
  transform: translateY(-3px);
  border-color: currentColor;
}

/* Cores específicas para cada rede social */
.social-link.instagram {
  background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
  color: white;
}

.social-link.facebook {
  background: #4267B2;
  color: white;
}

.social-link.youtube {
  background: #FF0000;
  color: white;
}

.social-link:hover {
  transform: translateY(-3px) scale(1.1);
  box-shadow: 0 8px 20px rgba(212, 175, 55, 0.3);
}

/* Linha de Copyright */
.footer-bottom {
  padding-top: 1.5rem;
  text-align: center;
}

.copyright {
  font-size: 0.9rem;
  color: #999;
  margin: 0;
}

/* Responsividade */
@media (max-width: 768px) {
  .footer-section {
    padding: 2rem 0 1rem;
  }
  
  .container {
    padding: 0 1rem;
  }
  
  .footer-content {
    flex-direction: column;
    gap: 2rem;
    text-align: center;
    padding-bottom: 1.5rem;
  }
  
  .footer-brand {
    flex: none;
  }
  
  .brand-name {
    font-size: 1.75rem;
  }
  
  .footer-social {
    gap: 1rem;
  }
  
  .social-link {
    width: 44px;
    height: 44px;
  }
}

@media (max-width: 480px) {
  .brand-name {
    font-size: 1.5rem;
  }
  
  .brand-tagline {
    font-size: 0.9rem;
  }
  
  .footer-social {
    gap: 0.75rem;
  }
  
  .social-link {
    width: 40px;
    height: 40px;
  }
  
  .copyright {
    font-size: 0.8rem;
  }
}
</style>