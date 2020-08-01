<template>
  <div class="ProyectContainer py-3">
    <div class="proyect_main_container">
        <div class="proyect_container_title text-center">
          <h4 class="proyect_title">Futura Encuesta</h4>
      </div>
      <div class="proyect_container_img">
        <img src="img/Futura.png" alt="" class="img-fluid"/>
      </div>
      
      <nav class="mt-3">
        <div class="nav nav-tabs" id="nav-tab" role="tablist">
          <a
            class="nav-item nav-link "
            id="nav-home-tab"
            data-toggle="tab"
            href="#nav-home"
            role="tab"
            aria-controls="nav-home"
            aria-selected="true"
            >Info</a
          >
          <a
            class="nav-item nav-link"
            id="nav-profile-tab"
            data-toggle="tab"
            href="#nav-profile"
            role="tab"
            aria-controls="nav-profile"
            aria-selected="false"
            >Tecnologias</a
          >
          <a
            class="nav-item nav-link"
            
            href="#nav-contact"
            role="tab"
            aria-controls="nav-contact"
            aria-selected="false"
            >Entrar</a
          >
        </div>
      </nav>
      <div class="tab-content" id="nav-tabContent">
        <div
          class="tab-pane fade"
          id="nav-home"
          role="tabpanel"
          aria-labelledby="nav-home-tab"
        >
          <p class="proyectInfo_description_title">
            Descripción
          </p>
          <p class="proyectInfo_description_text">
            Futura Encuesta es una pagina web la cual su objetivo es recaudar informacion de estudiantes sobre distintos apectos de la Universidad donde estudia y el programa que cursa por medio de una encuesta de 40 preguntas de distintos factores
          </p>
          <p class="proyectInfo_description_title">
            Contribución
          </p>
          <p class="proyectInfo_description_text">
            Forme parte de un equipo de desarollo donde trabaje tanto el frontend como el backend de la pagina
          </p>
        </div>
        <div
          class="tab-pane fade"
          id="nav-profile"
          role="tabpanel"
          aria-labelledby="nav-profile-tab"
        >
          Tab2
        </div>
        <div
          class="tab-pane fade"
          id="nav-contact"
          role="tabpanel"
          aria-labelledby="nav-contact-tab"
        >
          Tab3
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProyectContainer"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ProyectContainer{
    width: 47%;
}
.proyect_main_container{
    width: 100%;
    border: 3px solid gold;
    border-radius: 10px;
    overflow: hidden;
}

.proyect_title{
    color: gold;
}
.nav-tabs .nav-link {
    border: 1px solid #000;
    border-top-left-radius: .25rem;
    border-top-right-radius: .25rem;
    width: 33.3%;
    text-align: center;
    background: #e6dcdc;
    color: #000;
}
.nav-tabs .nav-link.active {
    color: gold;
    background-color: #161616;
    border-color: #dee2e6 #dee2e6 #000;
    border-bottom: none;
    font-weight: 700;
}
.tab-content>.active {
    display: block;
    background: #161616;
    padding: 5px;
}
.proyectInfo_description_title{
    color: gold;
    font-weight: 700;
    margin-bottom: 0;
}
.proyectInfo_description_text{
    color: white;
    font-size: 14px;
}
</style>
