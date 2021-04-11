<template>
    <div id="projeto">
       <p class="msg-inicial">Seja bem-vindo(a)! Nesta seção você pode conferir alguns de meus principais projetos. 
        A maioria dos códigos fonte estão disponíveis em meu Github.</p>
       <div class="bloco-principal">
           <h2 class="bloco-titulo">Destaques</h2>
           <div class="bloco">
               <img src="../assets/img/bicycle.png" alt="Bicicleta"/>
               <div class="sub-bloco">
                    <h3><a class="link-item" href="https://lmarts.github.io/website-bicicletaria/" target="_blank" rel="noopener noreferrer">Ciclo Terra Preta</a></h3>
                    <p>HTML &#8226; CSS &#8226; Bootstrap</p>
                    <p>Website para bicicletaria</p>
               </div>
           </div>
           <div class="bloco">
               <img src="../assets/img/book.png" alt="Bicicleta"/>
               <div class="sub-bloco">
                    <h3><a class="link-item" href="http://177.107.76.214/~camarabp/" target="_blank" rel="noopener noreferrer">Centro de Memória</a></h3>
                    <p>HTML &#8226; CSS &#8226; JavaScript &#8226; Bootstrap &#8226; PHP &#8226; MySQL</p>
                    <p>Acervo digital da Câmara Municipal de Bragança Paulista</p>
               </div>
           </div>
           <div class="bloco">
               <img src="../assets/img/netflix.png" alt="Bicicleta"/>
               <div class="sub-bloco">
                    <h3><a class="link-item" href="https://lmarts.github.io/Clone-Netflix/" target="_blank" rel="noopener noreferrer">Clone Netflix</a></h3>
                    <p>HTML &#8226; CSS &#8226; JavaScript</p>
                    <p>Clone básico do site da Netflix</p>
               </div>
           </div>
           <h2 class="bloco-titulo">#ImersãoAlura</h2>
           <div class="bloco">
               <div class="sub-bloco">
                    <h3><a class="link-item" href="https://editor.p5js.org/L_Martins/full/DpFmx9lIG" target="_blank" rel="noopener noreferrer">RexGame</a></h3>
                    <p>p5.js Web</p>
                    <p>Reboot do jogo do dinossauro do Google</p>
               </div>
           </div>
           <h2 class="bloco-titulo">Outros Projetos</h2>
           <div class="bloco">
                <div>
                    <ul>
                        <li class="item"><a class="link-item" href="https://leticiamartins-portfolio.web.app/" target="_blank" rel="noopener noreferrer">Este portfólio</a> - Meu website pessoal (Vue Js)</li>
                        <li class="item"><a class="link-item" href="https://github.com/LMArts/FindKid" target="_blank" rel="noopener noreferrer">FindKid</a> - Aplicativo para auxiliar na identificação e localização de crianças perdidas em locais aglomerados (React Native, Node Js)</li>
                        <li class="item"><a class="link-item" href="https://lmarts.github.io/Clone-Instagram/" target="_blank" rel="noopener noreferrer">Clone Instagram</a> - Clone da página inicial do Instagram (HTML, CSS)</li>
                        <li class="item"><a class="link-item" href="https://lmarts.github.io/Pixel-Art-Game/" target="_blank" rel="noopener noreferrer">Pixel Art</a> - Um joguinho sobre pintar quadradinhos (HTML, CSS, JavaScript)</li>
                        <li class="item"><a class="link-item" href="https://github.com/LMArts/Projeto-DSW" target="_blank" rel="noopener noreferrer">Website em React Js</a> - Sistema de cadastro simples (React Js, Node Js)</li>
                    </ul>
                </div>
           </div>
       </div>
    </div>
</template>

<script>
export default {
    name: 'projeto'
}
</script>

<style>
#projeto{
    color: rgba(255, 255, 255, 0.815);
    padding: 1em;
}
.msg-inicial{
    font-size: 1.1em;
    text-align: justify;
    line-height: 1.8em;
}
.bloco{
    display: flex;
    align-items: center;
}
.sub-bloco{
    margin-left: 1em;
}
.link-item{
    color: rgba(255, 255, 255, 0.815);
    font-weight: bolder;
    text-decoration: none;
    padding: 0;
}
.link-item:hover{
    color: rgb(255, 255, 255);
    text-decoration: underline;
}
.item{
    padding-bottom: 1em;
    line-height: 1.8em;
}
</style>