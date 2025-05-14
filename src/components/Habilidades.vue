<script setup>
const skills = {
  technical: ["HTML5", "CSS", "JavaScript", "Vue.js", "Git", "Figma", "Responsive Design"],
  soft: ["Empatía", "Trabajo en Equipo", "Communication Efectiva", "Aprendizaje Continuo", "Escucha Activa", "Adaptabilidad","Responsabilidad"],
};
</script>

<template>
  <section class="skills-section" id="habilidades">
    <div class="container">
      <h2 class="section-title">Habilidades y Competencias</h2>
      
      <div class="skills-grid">
        <div class="skill-category">
          <h3 class="category-title">
            <span class="icon">💻</span>
            Technical Skills
          </h3>
          <div class="skills-list">
            <span v-for="(skill, index) in skills.technical" :key="'tech-'+index" class="skill-pill">
              {{ skill }}
            </span>
          </div>
        </div>
        
        <div class="skill-category">
          <h3 class="category-title">
            <span class="icon">🧠</span>
            Soft Skills
          </h3>
          <div class="skills-list">
            <span v-for="(skill, index) in skills.soft" :key="'soft-'+index" class="skill-pill soft">
              {{ skill }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skills-section {
  padding: 5rem 1rem;
  background-color: #f8f9fa;
  color: #2d3436;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;
  margin-bottom: 3rem;
  position: relative;
  color: #2d3436;
}

.section-title::after {
  content: '';
  display: block;
  width: 80px;
  height: 4px;
  background: #000000;
  margin: 0.5rem auto 0;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.skill-category {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s ease;
}

.skill-category:hover {
  transform: translateY(-5px);
}

.category-title {
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: #2d3436;
}

.icon {
  font-size: 1.8rem;
}

.skills-list {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
}

.skill-pill {
  background: #dfe6e9;
  color: #2d3436;
  padding: 0.6rem 1.2rem;
  border-radius: 50px;
  font-size: 0.9rem;
  font-weight: 500;
  transition: all 0.3s ease;
}

.skill-pill.soft {
  background: #dfe6e9;
}

.skill-pill:hover {
  background: #0f0f0f;
  color: white;
  transform: scale(1.05);
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }
  
  .skills-grid {
    grid-template-columns: 1fr;
  }
}
</style>