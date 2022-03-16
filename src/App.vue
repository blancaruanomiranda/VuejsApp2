<template>

    <div class="app">


        <meta charset="UTF-8" />

        <component :is="component" v-bind="{ counter: this.counter, chapter_counter: this.chapter_counter, f_counter: this.f_counter, points: this.points}"></component>
        <button class="start_button" v-if="component == 'Home'" v-on:click="component='instructions'; counter++; chapter_counter++">EMPEZAR </button>
        <button class="start_button" v-if="component == 'Home'" v-on:click="component='final_menu'; counter++"> IR AL MENÚ </button>
        <button class="start_button" v-if="component == 'Home'" v-on:click="component='component1'; counter++; chapter_counter=7"> CAPI 7</button>
        <button class="opacity_animation" id="got_button" v-if="component == 'instructions' && chapter_counter==1" v-on:click="component='instructions2'; counter++"> VALE PERO, DE QUÉ VA LA HISTORIA? </button>
        <button class="opacity_animation" id="got_button" v-if="component == 'instructions2'" v-on:click="component='component1'; counter++"> DALE BRO </button>
        <button id="arrow_button" v-if="component == 'component1' && chapter_counter<7" v-on:click="component='component2'; counter++">
            <span class="icono-flecha"><ion-icon name="arrow-forward-outline"></ion-icon> </span>
        </button>
        <button id="arrow_button" v-if="component == 'component1' && chapter_counter==7" v-on:click="component='instructions'; counter++">
            <span class="icono-flecha"><ion-icon name="arrow-forward-outline"></ion-icon> </span>
        </button>
        <div class="btn-option" v-if="component == 'component2' && chapter_counter<7">
            <div class="button-column">
                <button @click="sumPoints1" id="OPT1" v-if="component == 'component2' && chapter_counter<7" v-on:click="component='answer'; counter++">OPCIÓN 1 </button>
            </div>
            <div class="button-column">
                <button @click="sumPoints2" id="OPT2" v-if="component == 'component2' && chapter_counter<7" v-on:click="component='answer2'; counter++">OPCIÓN 2 </button>
            </div>
        </div>
        <button class="corazon" id="got_button" v-if="component == 'instructions' && chapter_counter==7" v-on:click="component='priv'; counter++"> VAMOS A SOLUCIONAR ESTO </button>
        
        <div class="container" v-if="component == 'priv'">
            <h3>Poner perfil privado</h3>
            <label class="switch">
                <input type="checkbox" @click="delayRedirect(); counter++; f_counter++"/>
                    <span class="slider"></span>
            </label>
        </div>
        <button id="arrow_button" v-if="component == 'answer' | component == 'answer2' && chapter_counter < 7" v-on:click="component='component1'; counter++; chapter_counter++">
            <span class="icono-flecha"><ion-icon name="arrow-forward-outline"></ion-icon> </span>
        </button>
        <button id="arrow_button" v-if="component == 'feedback' && f_counter < 3" v-on:click="component='feedback'; counter++; f_counter++">
            <span class="icono-flecha"><ion-icon name="arrow-forward-outline"></ion-icon> </span>
        </button>
        <button id="got_button" v-if="component == 'feedback' && f_counter == 3" v-on:click="component='final_menu'; counter++"> IR AL MENÚ </button>
        <button id="menu_button" v-if="component == 'final_menu'" v-on:click="component='evaluation'; counter++">EVALUACIÓN</button>
        <button id="menu_button" v-if="component == 'final_menu'" v-on:click="component='tips'; counter++"> CONSEJITOS </button>
        <button id="menu_button" v-if="component == 'final_menu'" v-on:click="component='Home'; counter=0; chapter_counter =0; points=0; f_counter=0"> VOLVER A JUGAR </button>
        <button id="got_button" v-if="component == 'tips'" v-on:click="component='final_menu'; counter++"> VOLVER </button>
        <button id="got_button" v-if="component == 'evaluation'" v-on:click="component='final_menu'; counter++"> VOLVER </button>
        <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>

    </div>

</template>

<script>
    import Home from './components/Home.vue';
    import component1 from './components/component1.vue';
    import component2 from './components/component2.vue';
    import instructions from './components/instructions.vue';
    import instructions2 from './components/instructions2.vue';
    import answer from './components/answer.vue';
    import answer2 from './components/answer2.vue';
    import final_menu from './components/final_menu.vue';
    import tips from './components/tips.vue';
    import evaluation from './components/evaluation.vue';
    import feedback from './components/feedback.vue';
    import priv from './components/private.vue';


    export default {
        name: 'app',
        components: {
            'Home': Home,
            'component1': component1,
            'component2': component2,
            'instructions': instructions,
            'instructions2': instructions2,
            'answer': answer,
            'answer2': answer2,
            'final_menu': final_menu,
            'tips': tips,
            'evaluation': evaluation,
            'feedback': feedback,
            'priv': priv
        },
        data() {
            return {
                counter: 0,
                chapter_counter: 0,
                f_counter: 0,
                i_counter: 0,
                points: 0,
                component: 'Home',
                a: [0, 1, 1, 0, 1, 0],
                a2: [1, 0, 0, 1, 0, 1]
            }
        },
        methods: {
            sumPoints1: function () {
                this.points += this.a[this.chapter_counter-1];
            },
            sumPoints2: function () {
                this.points += this.a2[this.chapter_counter - 1];
            },
            delayRedirect: function () {
                setTimeout(() => {
                    this.component = 'feedback';
                }, 1000);
            }

        }

    };
</script>

<style>

    * {
        margin: 0px;
        padding: 0px;
        background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(28,0,38,1) 73%, rgba(53,0,59,1) 100%);
        animation: gradient 15s ease infinite;
        background-attachment: fixed;
        text-align: justify;
        line-height: 20px;
        overflow-x: hidden;
        font-family: "Lucida Console", "Courier New", monospace;
       
        
    }
    .app{
        height: 100vh;
    }
    h3{
        color: white;
        background: transparent;
        
    }
  
    button {
        display: inline-block;
        cursor: pointer;
        font-size: 16px;
        line-height: 20px;
        font-weight: 600;
        border-radius: 25px;
        padding: 13px 23px;
        border: 1px solid mediumpurple;
        background: transparent;
        color: mediumpurple;
        transition-duration: 0.2s;
        z-index: 1;
    }

        button:hover {
            background: mediumpurple;
            color: black;
            box-shadow: 0 0 5px mediumpurple, 0 0 25px mediumpurple, 0 0 50px mediumpurple, 0 0 100px mediumpurple;
        }

   

    #got_button {
        display: block;
        margin: auto;
  
    }
  
    #next_button {
        display: block;
        margin: auto;
    }
    @keyframes opacity {
        0% {opacity: 0;}
        50% {
            opacity: 60;
        }
        75% {
            opacity: 70;
        }
        100% {
            opacity: 100;
        }
    }
    .opacity_animation {
        animation-name: opacity;
        animation-duration: 5s;
        animation-iteration-count: 1;
    }
    
    
    #menu_button {
        display: block;
        margin: auto;
        margin-bottom: 18px;
        width: 190px;
        text-align: center;
    }
    .start_button {
        margin-left:8vw;
        margin-top:12vh;
        position: relative;
       
    }
       
    #arrow_button {
        display: block;
        margin: auto;
        margin-top: 20px;
        border: 1px solid mediumpurple;
        width: 120px;
       
    }
        #arrow_button:hover {
            background-color: transparent;
            border: 1px solid mediumpurple;
            color: mediumpurple;
            box-shadow: 0 0 5px mediumpurple, 0 0 25px mediumpurple, 0 0 50px mediumpurple, 0 0 100px mediumpurple;
        }
    .icono-flecha {
        display: block;
        text-align: center;
        align-items: center;
        height: 80%;
        background: transparent;
        font-size: 22px;
        color: mediumpurple;

    }
        .icono-flecha:hover {
            
            background-color: transparent;
            
            color: mediumpurple;
            box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
        }
    
    #flecha{
        height: 20%;
        width: 70%;
        display: block;
        margin: auto;
    }



    .btn-option {
        display: flex;
    }
    .button-column {
        flex: 50%;
        padding: 5px;
        text-align: center;
    }
    .btn-option #OPT1 {
        margin-left: 18vw;
        
    }
    .btn-option #OPT2 {
        margin-right: 18vw;
       
    }

    @keyframes latidos {
        from {
            transform: none;
        }

        50% {
            transform: scale(1.1);
        }

        to {
            transform: none;
        }
    }

    .corazon {
        display: inline-block;
        text-shadow: 0 0 10px #222,1px 1px 0 #450505;
        animation: latidos 1s infinite;
        transform-origin: center;
    }

    .container{
        display: flex;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
        background: transparent;
        align-items: center;
    }
    .switch{
        position: relative;
        display: inline-block;
        width: 110px;
        height: 60px;
        margin: 0 10px;
        background: transparent;
    }
    .slider{
        position: absolute;
        cursor: pointer;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: #ccc;
        transition: .4s;
        border-radius: 34px;
        border: 1px solid mediumpurple;
    }
    .switch input{display:none}

    .slider:before{
        position: absolute;
        content: "";
        height: 50px;
        width: 50px;
        left: 5px;
        bottom: 5px;
        background: white;
        transition: .4s;
        border-radius: 50px;
    }
    input:checked + .slider{
        background: mediumpurple;
    }
    input:checked + .slider:before {
        transform: translateX(50px);
    }


  
    
    
                
                
</style>

