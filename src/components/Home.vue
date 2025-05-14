<script setup>
const nombre = "Brayan Gamboa Delgado";
const descipcion = "Soy un estudiante de la carrera de Ingeniería de Software entre los ciclos 7mo y 8vo con enfoque en desarrollo front-end. He trabajado en proyectos universitarios donde he adquirido experiencia utilizando tecnologías como HTML, CSS, JavaScript y frameworks como Angular y Vue. Además, he complementado mi formación con cursos especializados en desarrollo web a través de plataformas como Google.";
</script>

<template>
  <div class="home" id="aboutme">
    <video src="../assets/background.mp4" autoplay muted loop></video>
    <div class="content-wrapper">
      <div class="text-content">
        <h1>{{ nombre }}</h1>
        <p>{{ descipcion }}</p>
      </div>
      <div class="image-content">
        <img src="../assets/me.png" alt="Foto perfil" class="foto-perfil">
        <div class="social-icons">
          <a href="https://github.com/GamboaBrayan" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-github"></i>
          </a>
          <a href="https://www.linkedin.com/in/brayan-gamboa-delgado/" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-linkedin"></i>
          </a>
          <a href="https://www.instagram.com/brayan.sgd/" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-instagram"></i>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.home {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  overflow: hidden;
}

.content-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  max-width: 1200px;
  width: 100%;
  align-items: center;
}

.text-content {
  color: white;
}

.image-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.home h1 {
  color: white;
  font-size: 2.8rem;
  margin-bottom: 20px;
  line-height: 1.2;
}

.home p {
  font-size: 1.1rem;
  line-height: 1.6;
  margin-bottom: 30px;
}

.foto-perfil {
  width: 100%;
  max-width: 350px;
  height: auto;
  aspect-ratio: 7/8;
  border-radius: 50%;
  border: 3px solid #ffffff;
  object-fit: cover;
}

video {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  z-index: -1;
  object-fit: cover;
}

.social-icons {
  display: flex;
  gap: 20px;
  margin-top: 30px;
  justify-content: center;
  width: 100%;
}

.social-icons a {
  color: #ffffff;
  font-size: 1.7rem;
  transition: color 0.3s ease;
}

.social-icons a:hover {
  transform: scale(1.1);
}

.social-icons a:hover:nth-child(1) { color: #000; }
.social-icons a:hover:nth-child(2) { color: #0077b5; }
.social-icons a:hover:nth-child(3) { color: #e1306c; }

/* Responsive: Tablet (1024px) */
@media (max-width: 1024px) {
  .content-wrapper {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 30px;
  }
  
  .home h1 {
    font-size: 2.4rem;
  }
  
  .home p {
    font-size: 1rem;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
  }
  
  .image-content {
    order: -1;
  }
  
  .foto-perfil {
    max-width: 300px;
  }
}

/* Responsive: Mobile (390px) */
@media (max-width: 390px) {
  .home {
    padding: 40px 20px;
  }
  
  .home h1 {
    font-size: 1.8rem;
  }
  
  .home p {
    font-size: 0.95rem;
  }
  
  .foto-perfil {
    max-width: 250px;
  }
  
  .social-icons a {
    font-size: 1.5rem;
  }
  
  .content-wrapper {
    gap: 20px;
  }
}

/* Asegúrate de tener Font Awesome incluido en tu proyecto */
</style>