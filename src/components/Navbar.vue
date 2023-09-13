<template>
    <nav class="navbar">
        <ul class="nav-list">
            <li>
                <a class="nav-link" href="">
                    <i class="fas fa-home icon"></i>Home
                </a>
            </li>
            <li>
                <a class="nav-link" href="">
                    <i class="fas fa-suitcase icon"></i>Proyectos
                </a>
            </li>
            <li>
                <a class="nav-link" href="">
                    <i class="fas fa-book icon"></i>Blog
                </a>
            </li>
            <li>
                <a class="nav-link" href="">
                    <i class="fas fa-glasses icon"></i>Recursos
                </a>
            </li>
            <li>
                <a class="nav-link" href="">
                    <i class="fas fa-address-book icon"></i>Contacto
                </a>
            </li>
        </ul>
    </nav>
</template>

<style scoped>
.navbar {
  background-color: transparent;
  /* #18181b */
  padding: 1.3rem 0;
  margin: 0.37rem;
  
}

.nav-list {
  list-style: none;
  display: flex;
  justify-content: space-around;
  align-items: center;

  margin: 0;
  padding: 0;
}

.nav-link {
  font-family: 'Kanit', sans-serif;
  font-family: 'Montserrat', sans-serif;
  font-size:medium;
  color: white;
  text-decoration: none;
  margin: 0 15px;
  position: relative;
  transition: color 0.3s;
  font-size: 1.1rem;
}

.nav-link i {
  margin-right: 5px;
}

.nav-link::before {
  content: "";
  position: absolute;
  bottom: -3px;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: white;
  transform: scaleX(0);
  transform-origin: center;
  transition: transform 0.3s;
}

.nav-link:hover {
  color: #f39c12;

}

.nav-link:hover::before {
  transform: scaleX(1);
  background-color: #f39c12;
}


.icon {
  transition: transform 0.3s ease;
  /* Agrega una transición para la animación */
}

.nav-link:hover .icon {
  transform: rotate(360deg);
  /* Aplica la rotación al icono cuando se hace hover en el enlace */
}
</style>