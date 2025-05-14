<template>
    <nav class="navbar">
        <ul class="nav-links">
        <li><a href="#aboutme">Sobre mí</a></li>
        <li><a href="#Proyectos">Proyectos</a></li>
        <li><a href="#habilidades">Habilidades</a></li>
        <li><a href="#contacto">Contacto</a></li>
        <li><a href="/public/cv/CV - Brayan Gamboa.pdf" download class="cv-download-btn" title="Descargar CV">CV</a></li>
        </ul>

    </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen
    },
    closeMenu() {
      this.isMenuOpen = false
    }
  }
}
</script>

<style>
.navbar {
  position: fixed; /* Fija la navbar en la parte superior */
  top: 0;
  left: 0;
  width: 100%;
  background: rgba(0, 0, 0, 0.9);
  padding: 20px 0;
  z-index: 1000; /* Asegura que esté por encima de otros elementos */
}

.nav-links {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center; /* Centra los elementos horizontalmente */
  align-items: center;
}

.nav-links li {
  margin: 0 15px;
}

.nav-links a {
  color: #fff; /* Letra blanca */
  text-decoration: none;
  font-size: 1.1em;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #ffffff; /* Color de acento al hacer hover */
}

.cv-download-btn {
  padding: 8px 15px;
  border-radius: 5px;
  transition: all 0.3s ease;
}

.cv-download-btn:hover {
  color: white;
}

.menu-toggle {
  display: none;
  cursor: pointer;
  padding: 10px 20px;
}

.hamburger {
  width: 25px;
  height: 3px;
  background-color: white;
  position: relative;
  transition: all 0.3s ease;
}

.hamburger:before,
.hamburger:after {
  content: '';
  position: absolute;
  width: 25px;
  height: 3px;
  background-color: white;
  transition: all 0.3s ease;
}

.hamburger:before {
  top: -8px;
}

.hamburger:after {
  top: 8px;
}

.hamburger.active {
  background-color: transparent;
}

.hamburger.active:before {
  transform: rotate(45deg);
  top: 0;
}

.hamburger.active:after {
  transform: rotate(-45deg);
  top: 0;
}

/* Responsive: Tablet (1024px) */
@media (max-width: 1024px) {
  .nav-links li {
    margin: 0 10px;
  }
  
  .nav-links a {
    font-size: 1em;
  }
}

/* Responsive: Mobile (390px) */
@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
    padding: 10px 0;
  }
  
  .menu-toggle {
    display: block;
    align-self: flex-end;
  }
  
  .nav-links {
    width: 100%;
    flex-direction: column;
    max-height: 0;
    overflow: hidden;
    padding: 0;
  }
  
  .nav-links.active {
    max-height: 500px;
    padding: 10px 0;
  }
  
  .nav-links li {
    margin: 10px 0;
    width: 100%;
    text-align: center;
  }
  
  .nav-links a {
    padding: 10px 0;
  }
  
  .cv-download-btn {
    margin-top: 5px;
  }
}
</style>