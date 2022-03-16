<template>
    <div class="home">
        
        <h1 >¡BIENVENIDO A SOCIALESCAPE!</h1>
       
        <h2> AYUDA A JIMMY A ESCAPAR DEL ACOSADOR </h2>   
        <img src="@/components/static/img/timmy.png" />
    </div>
</template>

<script>
       export default {
        name: 'Home',
        props: {
            msg: String
        }
       
        
    };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
    * {
        padding: 0;
        margin: 0;
    }

    .home {
        padding: 0;
        margin: 0;
        background-color: black;
        background-size: 100% 100%;
        
    }

    h1 {
        margin-top: 15vh;
        margin-left: 7vw;
        
        line-height: 40px;
        justify-content: left;
        font-size: 40px;
        color: #e300ff;
        font-family: 'Press Start 2P', cursive;
        padding: 20px;
    }

    h2 {
        font-size: 20px;
        margin-left: 8vw;
        padding: 10px;
        width: 40%;
        margin-block-start: 70px;
        color: #9f00eb;
        font-family: 'Press Start 2P', cursive;
        line-height: 30px;
    }

   

    img {
        position: fixed;
        right: 50px;
        bottom: 50px;
        height: 50%;
        width: 35%;
    }

   

  

</style>

