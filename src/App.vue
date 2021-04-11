<template>
  <div id="app">
      <div class="main">  
        <div class="links">
            <a class="link" href="https://github.com/LMArts" target="_blank" rel="noopener noreferrer"><i class="fab fa-github fa-2x hover:text-gray-300"></i></a>
            <a class="link" href="https://linkedin.com/in/leticiamartinsalarcon/" target="_blank" rel="noopener noreferrer"><i class="fab fa-linkedin fa-2x hover:text-gray-300"></i></a>
        </div>
          <h1 class="main-titulo">{{titulo}}</h1>
          <div class="main-button">
              <button v-on:click="showProject = false, showArticle = false" :class="{'active': showArticle == false && showProject == false}">Home</button>
              <button v-on:click="showProject = !showProject, showArticle = false" :class="{'active': showProject == true}">Projetos</button>
              <button v-on:click="showArticle = !showArticle, showProject = false" :class="{'active': showArticle == true}">Artigos</button>
          </div>
          <div class="componente">
            <transition name="fade">
                <div v-if="showProject">
                    <Projects/>
                </div>
            </transition>
            <transition name="fade">
                <div v-if="showArticle">
                    <Articles/>
                </div>
            </transition>
          </div>
      </div>
  </div>
</template>

<script>
    import Articles from './components/Articles.vue';
    import Projects from './components/Projects.vue';
    
    export default {
        name: 'app',
        components:{Projects, Articles},
        data(){
            return{
                titulo: 'Leticia Martins',
                showProject: false,
                showArticle: false
            }
        },
        mounted(){
            const val = document.querySelector("h1");
            const textoLista = val.innerHTML.split('');
            val.innerHTML = '';
            textoLista.forEach((letra, i) => {
            setTimeout(() => val.innerHTML += letra, 150 * i);
            });  
        }
    }
</script>

<style>
#app, .main {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.main-titulo, button, i{
    color: rgba(255, 255, 255, 0.815);
}
.links{
    display: flex;
    justify-content: center;
    width: 100%;
}
.link{
    margin-top: 1em;
    padding: 1em;
}
i:hover {
    color: rgb(255, 255, 255);
}
.main{
    min-height: 100vh;
}
.main-titulo{
    font-size: 1.6em;
    font-weight: bold;
    letter-spacing: 2px;
    margin: 2em auto;
}
.main-button button{
    background-color: transparent;
    font-family: 'Courier New', Courier, monospace;
    border: none;
    outline: none;
    font-size: 1.1em;
    font-weight: 600;
    letter-spacing: 2px;
    cursor: pointer;
    padding: 1em;
}
button:hover{
    color: rgb(255, 255, 255);
}
.componente{
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 1.3em;
    background-color: #353535;
}
.active{
    color: rgba(255, 255, 255, 0.979);
    text-decoration: underline;
}
h1::after{
    content: ' | ';
    margin-left: 1px;
    opacity: 1;
    animation: piscar .7s infinite;
}
@keyframes piscar{
    0%, 100%{
        opacity: 1;
    } 
    50%{
        opacity: 0;
    }
}
@media screen and (min-width:1024px){
    .main-titulo{
        font-size: 2.5em;
    }
    .main-button button{
        font-size: 1.3em;
    }
    .componente{
        width: 60%;
        margin-bottom: 1em;
        border-radius: 10px;
    }

}
</style>
