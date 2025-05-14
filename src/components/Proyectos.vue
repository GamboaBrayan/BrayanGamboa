<script setup>
const proyectos = [
    {
    nombre: "Vitality",
    descripcion: "Landing Page de un Start up de la universidad sobre recetas saludables.",
    imagen: "/images/vitality.png", 
    enlace: "https://vitality-landing.netlify.app/", 
  },
  {
    nombre: "InfoNow",
    descripcion: "Quieres saber las ultimas noticias de tu interes?",
    imagen: "../images/Api_news.png",
    enlace: "https://apiinfonow.netlify.app/",
  },
];
</script>

<template>
    <div class="proyectos" id="Proyectos">
        <h2>Proyectos</h2>
        <div class="cards-container">
        <div v-for="(proyecto, index) in proyectos" :key="index" class="card">
            <img :src="proyecto.imagen" :alt="proyecto.nombre" class="card-image" v-if="proyecto.imagen" />
            <div class="card-content">
            <h3>{{ proyecto.nombre }}</h3>
            <p>{{ proyecto.descripcion }}</p>
            <a :href="proyecto.enlace" target="_blank" class="card-link" v-if="proyecto.enlace">Ver proyecto</a>
            </div>
        </div>
        </div>  
    </div>
</template> 

<style scoped>
.proyectos {
  padding: 60px 20px;
  text-align: center;
  background-color: #f8f9fa ;
}

h2 {
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;
  margin-bottom: 3rem;
  position: relative;
  color: #2d3436;
}

.cards-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px; /* Espacio entre las cards */
}

.card {
  background-color: #1E1E1E; /* Fondo gris oscuro */
  border-radius: 10px;
  overflow: hidden;
  width: 300px; /* Ancho de cada card */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-10px); /* Efecto de levantar la card */
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
}

.card-image {
  width: 100%;
  height: 200px;
  object-fit: cover; /* Ajusta la imagen al tamaño de la card */
}

.card-content {
  padding: 20px;
  text-align: left;
}

h3 {
  font-size: 1.5em;
  color: #ffffff; /* Color de acento */
  margin-bottom: 10px;
}

p {
  font-size: 1em;
  color: #E0E0E0; /* Letra blanca */
  margin-bottom: 15px;
}

.card-link {
  display: inline-block;
  padding: 10px 20px;
  background-color: #ffffff; /* Color de acento */
  color: #000; /* Texto negro */
  text-decoration: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.card-link:hover {
  background-color: #3aa876; /* Color de acento más oscuro */
}
</style>