<template>

    <div class="feedback">
        <div class="opacity_animation">
            <p class="a">{{items[f_counter-1].message1}}</p>
            <p class="b">{{items[f_counter-1].message2}}</p>
            <p class="c" v-if="f_counter==1 && points<=3">{{items[f_counter-1].message3}}</p>
            <img id="img1" v-if="f_counter==1 && points<=3" src="@/components/static/img/f1.png" />
            <p class="c" v-if="f_counter==1 && points>3 && points<=5">{{items[f_counter-1].message4}}</p>
            <img id="img2" v-if="f_counter==1 && points>3 && points<=5" src="@/components/static/img/f2.jpg" />
            <p class="c" v-if="f_counter==1 && points>5">{{items[f_counter-1].message5}}</p>
            <img id="img3" v-if="f_counter==1 && points>5" src="@/components/static/img/f3.jpg" />
            <a v-if="f_counter==3" href="https://docs.google.com/forms/d/e/1FAIpQLSeZHZV_2BNeOzCIPn6C6TEgY_sSGiQjv3mHRwn3qB7iZjS4EA/viewform?usp=sf_link" target="_blank">Link al test</a>


        </div>
    </div>
</template>

<script>
    export default {
        name: 'feedback',
        props: {
            counter: Number,
            f_counter: Number,
            points: Number
        },
        data() {
            return {
                items: [
                    {
                        message1: '¡Enhorabuena! Has conseguido alejar definitivamente al acosador. A partir de ahora, tendremos que confiar en Jimmy para que gestione él solito sus redes.',
                        message2: `Durante el juego has tenido que tomar 6 decisiones, y ${this.points} han sido correctas.`,
                        message3: "¡La próxima vez intenta proteger un poco más a Jimmy!",
                        message4: "¡No lo has hecho nada mal! Se te da bien esto de gestionar las redes sociales.",
                        message5: "¡Vaya crack! Si algún día Jimmy se hace famoso, seguro que te querrá contratar como manager para que le lleves las redes."
                      
                    },
                    {
                        message1: 'Todo lo que has visto en esta historia son situaciones que tanto tú como yo nos podemos encontrar en nuestro día a día. Estas situaciones son algunos ejemplos de cómo nos puede afectar nuestra huella digital. ',
                        message2: 'La huella digital son los rastros que dejan todas esas cosas que hacemos en internet. Nuestra huella digital está formada por los sitios web que visitamos, las fotos que publicamos y todos los comentarios o mensajes que mandamos, entre otras cosas. El objetivo de este juego es que veas cómo te pueden afectar tu huella digital  y aprendas de los errores de Jimmy a la hora de publicar cosas en las redes sociales.'
                    },
                    {
                        message1: 'Por último, me gustaría pedirte que vayas al apartado de evaluación que encontrarás en el menú (o si lo prefieres puedes clicar en el link que hay aquí abajo directamente) y completes un pequeño test (se hace súper rápido, lo prometo jeje) y si quieres, visites la sección de consejitos para ver algunas cosillas que puedes hacer para cuidar tu huella digital. También puedes volver a jugar si te apetece.',
                        message2: '¡Gracias por cuidar de Jimmy!'
                    }
                ]
            }
        },
        
        

    };
</script>

<style scoped>
    * {
        padding: 0;
        margin: 0;
        background-color: black;
        background-size: 100% 100%;
    }

    p {
        font-size: 15px;
        text-align: center;
        margin-left: 18vw;
        margin-right: 18vw;
        padding: 20px;
        color: white;
    }
    .a{
        margin-top: 12vh;
    }
    .b{
       
    }
    .c{
     
        
    }
    @keyframes opacity {
        0% {
            opacity: 0;
        }

        50% {
            opacity: 20;
        }

        75% {
            opacity: 50;
        }

        100% {
            opacity: 100;
        }
    }
    .opacity_animation {
        animation-name: opacity;
        animation-duration: 7s;
        animation-iteration-count: 1;
    }
    #img1{
        display: block;
        margin: auto;

    }
    #img2 {
        display: block;
        margin: auto;
        width: 15%;
    }
    #img3 {
        display: block;
        margin: auto;
        width: 15%;
    }

    a {
        justify-content: center;
        display: flex;
        margin-bottom: 6vh;
        margin-top: 2vh;
    }

</style>