<template>
  <div class="contact-container">
    <h1>Contáctame</h1>
    
    <div class="contact-info">
      <div class="contact-item">
        <span class="icon">📧</span>
        <a href="Brayangamboa620@gmail.com" class="contact-link">Brayangamboa620@gmail.com</a>
      </div>
      <div class="contact-item">
        <span class="icon">📱</span>
        <a href="https://wa.me/+51934504275?text=Hola,%20estoy%20interesado%20en%20contactarte.%20Soy..." class="contact-link">+51 934 504 275</a>
      </div>

      <div class="contact-item">
        <span class="icon">📍</span>
        <span>Lima, Perú</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage'
}
</script>

<style>
.contact-container {
  max-width: 100%;
  margin: 0 auto;
  padding: 2rem;
  text-align: center;
  background-color: #f8f9fa;
}

h1 {
  justify-content: center;
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;
  margin-bottom: 3rem;
  position: relative;
  color: #2d3436;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.contact-item {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  font-size: 1.1rem;
  color: black;
}

.icon {
  font-size: 1.5rem;
}

.contact-link {
  color: #3498db;
  text-decoration: none;
  transition: color 0.3s;
}

.contact-link:hover {
  color: #2980b9;
  text-decoration: underline;
}

/* Responsive: Mobile (390px) */
@media (max-width: 390px) {
  .contact-container {
    padding: 1rem;
  }
  
  h1 {
    font-size: 1.8rem;
    margin-bottom: 1.5rem;
  }
  
  .contact-info {
    gap: 1rem;
  }
  
  .contact-item {
    font-size: 1rem;
    flex-direction: column;
    text-align: center;
    padding: 0.8rem 0.5rem;
    gap: 0.5rem;
  }
  
  .icon {
    font-size: 1.5rem;
  }
  
  .contact-link {
    font-size: 0.95rem;
  }
}
</style>