<template>
    <section class="topo-do-site">
        <div class="interface">
            <div class="flex">
                <div class="txt-topo-site">
                    <h1 id="txt-apresentação">Olá eu sou o Juliano <span>.</span> &#x1F44B; </h1>
                    <p>Tenho 22 anos, sou estudante de programação e futuro engenheiro.</p>
                    
                    <div class="btn-contato">
                        <a href="#"><button>Entre em contato</button></a>
                    </div>
                    
                </div>
                <div class="img-topo-site">
                    <img src="../assets/juliano.png" alt="">
                </div>
            </div>
        </div>
    </section>

</template>
<script>
export default{
    name:'ApresentacaoJu',
}

</script>

<style>
section.topo-do-site{
    padding: 40px 4%;

}
section.topo-do-site .flex{
    align-items: center;
    justify-content: center;
    gap: 90px;
    
    
}
.topo-do-site h1{
    color: white;
    font-size: 45px;
    line-height: 40px;
}
.topo-do-site .txt-topo-site h1 span{
    color: aquamarine;
}
.topo-do-site .txt-topo-site p{
    color: white;
    margin: 40px 0;
}
.topo-do-site .img-topo-site img{
    position: relative;
    animation: flutuar 2s ease-in-out infinite alternate;
}
@keyframes flutuar{
    0%{
        top: 0;
    }
    100%{
        top: 30px;
    }
}
#txt-apresentação {
    border-right: .15em solid black;
    font-size: 2em;
    white-space: nowrap;
    overflow: hidden;
    width: 21ch;
    animation: typing 8s steps(21) infinite, blink-caret .75s step-end infinite;
  }
  
  @keyframes typing {
    0% { width: 0; }
    50% { width: 20ch; }
    100% { width: 0; }
  }
  
  @keyframes blink-caret {
    from, to { border-color: transparent; }
    50% { border-color: black; }
  }
  
  
@media screen and (max-width: 1020px) {
    .flex{
        flex-direction: column;
        text-align: center;
    }
    
    section.topo-do-site .flex{
        align-items: center;
        gap: 40px;

    }
    section.topo-do-site{
        padding: 20% 8%;
    
    }
    .topo-do-site .img-topo-site{
        width: 100%;
    }
    section.topo-do-site .flex{
        flex-direction: column-reverse;
        
    }
    
    
}


</style>