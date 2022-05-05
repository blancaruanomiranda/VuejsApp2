<template>
    
    <div class="component2">


        <h1>CAPÍTULO {{chapter_counter}}</h1>

        <p id="normal" v-if="chapter_counter!=6"> {{items[chapter_counter-1].message1}}</p>
        <p id="normal" v-if="chapter_counter!=6"> {{items[chapter_counter-1].message2}}</p>


        <component :is="component" v-bind="{ counter: this.counter, chapter_counter: this.chapter_counter }"></component>


        <div class="image-wrapper" v-if="chapter_counter==1">
            <div class="column">
                <img id="imgOPT1" src="@/components/static/img/img1_A.jpg" style="width:50%" />
            </div>
            <div class="column">
                <img id="imgOPT2" src="@/components/static/img/img1_B.jpg" style="width:50%" />
            </div>
        </div>
        <div class="image-wrapper2" v-if="chapter_counter==2">
            <div class="column2">
                <img id="OPT1-2" src="@/components/static/img/img2_A.jpeg" style="width:50%" />
            </div>
            <div class="column2">
                <img id="OPT2-2" src="@/components/static/img/img2_B.jpeg" style="width:50%" />
            </div>
        </div>
        <div class="image-wrapper2" v-if="chapter_counter==3">
            <div class="column2">
                <img id="OPT1-2" src="@/components/static/img/img3_A.jpg" style="width:50%" />
            </div>
            <div class="column2">
                <img id="OPT2-2" src="@/components/static/img/img3_B.jpg" style="width:50%" />
            </div>
        </div>
        <div class="image-wrapper" v-if="chapter_counter==4">
            <div class="column">
                <img id="imgOPT1" src="@/components/static/img/img4_A.jpeg" style="width:55%" />
            </div>
            <div class="column">
                <img id="imgOPT2" src="@/components/static/img/img4_B.jpeg" style="width:60%" />
            </div>
        </div>
        <div class="image-wrapper2" v-if="chapter_counter==5">
            <div class="column2">
                <img id="OPT1-2" src="@/components/static/img/img5_A.jpeg" style="width:50%" />
            </div>
            <div class="column2">
                <img id="OPT2-2" src="@/components/static/img/img5_B.jpg" style="width:50%" />
            </div>
        </div>
        <div v-if="chapter_counter==6">
            <p id="normal">Justo cuando Jimmy acaba de colgar la foto de sus apuntes, le llega una notificación de un mensaje. La persona que le manda el mensaje no tiene foto de perfil y se llama rodasoca_al_reves. El mensaje dice lo siguiente: <em>"Hola Jimmy!! ¡Cuánto tiempo hermano!  Te acuerdas de mí? Soy David, jugábamos juntos a basket jaja me das tu email y tu número de teléfono para que hablemos y quedemos un día ?”</em></p>
            <p id="normal"> ¿Qué debría hacer Jimy?</p>
        </div>
        <div class="image-wrapper" v-if="chapter_counter==6">

            <div class="column">
                <p id="textA">Jimmy no tiene ni idea de quién es este tío. Nunca ha jugado a baloncesto con un tal David. Aún así, le pica la curiosidad y le pasa el email y el número para averiguarlo.</p>

            </div>
            <div class="column">
                <p id="textB">Jimmy no lo duda ni un segundo y bloquea al usuario. Sabe que nunca ha jugado a baloncesto con ningún David, así que chao. </p>
            </div>
        </div>

        



    </div>
</template>

<script>
    import answer from './answer.vue';
    export default {
        name: 'component2',
        components: {
            'answer': answer
        },
        props: {
            counter: Number,
            chapter_counter: Number,
        },
        data() {
            return {
                component: 'Home',
                items: [
                    {
                        message1: 'Son las 11 de la mañana de un viernes. Es la hora del patio. Jimmy y sus amigos se sientan en las gradas, como siempre, mientras se comen sus bocatas. Hoy es un día especial: los padres de Jimmy por fin le dejan hacerse un perfil en las redes sociales. Los amigos de Jimmy le explican que lo primero que tienes que hacer al crearte un perfil es escoger el nombre de usuario, la foto de perfil y añadir una pequeña biografía para que la gente te pueda conocer un poco más. ',
                        message2: 'Escoge un perfil para Jimmy:'
                    },
                    {
                        message1: 'Después de todo el día en el insti, por fin es la hora de volver a casa. Jimmy tiene muchas ganas de llegar y estirarse en el sofá para ver el debate de la Isla de las Tentaciones de la noche anterior mientras se toma un ColaCao. Jimmy tiene tantas ganas de llegar a su casa que cuando por fin está delante de la puerta decide compartirlo en su perfil.',
                        message2: '¿Qué historia debería compartir Jimmy?'
                    },
                    {
                        message1: 'Tras una tarde chill en el sofá, Jimmy se pone su mejor outfit para ir a cenar con sus amigos. Van a celebrar el cumpleaños de Marc, el pequeño del grupo. En ese grupo es tradición que el cumpleañero escoja dónde quiere cenar, así que como Marc es muy fan de las hamburguesas con patatas, van a la mejor hamburguesería de la ciudad.',
                        message2: '¿Qué historia debería compartir Jimmy?'
                    },
                    {
                        message1: 'Al día siguiente, los panas comentan por WhatsApp la noche anterior. Aunque se lo pasaron genial, porque lo importante es la compañía, tuvieron algún problemilla con los camareros. Jimmy decide buscar el perfil de la hamburguesería y dejarles un comentario en su última publicación para quejarse.',
                        message2: '¿Qué comentario debería escribir Jimmy?'
                    },
                    {
                        message1: 'Se acercan los exámenes finales. Jimmy decide aprovechar todo el finde para estudiar. Las primeras tres horas son bastante productivas y Jimmy está a tope estudiando mates, pero al final acaba con la cabeza como un bombo. Jimmy coge el móvil y le hace una foto a sus apuntes, para compartir el sufrimiento con sus seguidores.',
                        message2: '¿Qué foto debería compartir Jimmy?'
                    },
                    {
                        message2: ''
                    },
                    {
                        message1: 'THIS IS CHAPTER 7'
                    }
                ]
            }
        }
    };
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
    *{
        box-sizing:border-box;
        margin:0;
    }
    .component2{
       
        margin:0px;
    }
    h1 {
        margin-top: 5vh;
        margin-left: 6vw;
        font-size: 30px;
        color: #9f00eb;
        padding: 20px;
        font-family: 'Press Start 2P', cursive;
    }

    p {
        font-size: 15px;
        margin-left: 7vw;
        margin-bottom: 5vh;
        margin-right: 8vw;
        color: white;
    }


    .image-wrapper {
        display: flex;
    }

    .column {
        flex: 50%;
        padding: 5px;
        text-align: center;
    }
    #imgOPT1{
        margin-left: 18vw;
        
    }
    #imgOPT2 {
        margin-right: 18vw;
       
    }
    .image-wrapper2 {
        display: flex;
        
    }
    .column2 {
        flex: 50%;
        padding: 5px;
        text-align: center;
    }
    #OPT1-2 {
        margin-left: 18vw;
        
    }

    #OPT2-2 {
        margin-right: 18vw;
        
    }

    

    .text-wrapper {
        display: flex;
        justify-content: space-between;
        margin-inline: 70px;
        
    }

    #textA {
        color: #00fff0;
        border: 1px solid white;
        padding: 20px;
        margin-left: 10vw;
        
    }
    #textB {
        color: #00fff0;
        border: 1px solid white;
        padding: 20px;
        margin-right: 10vw;
    }
    #normal{

    }
    
    
   

    

    



    

   

   
</style>