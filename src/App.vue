<template>
  <div id="app">
    <div class="button-container" >
      <button class="butt button1" @click="currentComponent = 'Component1'">Тест 1</button>
      <button class="butt button2" @click="currentComponent = 'Component2'">Тест 2</button>
      <button class="butt button3" @click="currentComponent = 'Component3'">Тест 3</button>
      <button class="butt button4" @click="currentComponent = 'Component4'">Тест 4</button>
      <button class="butt button5" @click="currentComponent = 'Component5'">Тест 5</button>
    </div>
    <div class="component-container ">
    <component :is="currentComponent"></component>
  </div>
  </div>
</template>

<script>
import Component1 from './TestsHW/Test1strop.vue';
import Component2 from './TestsHW/Test2stropdif.vue'
import Component4 from './TestsHW/Test4Munsberg.vue';
import Component3 from './TestsHW/Test3cudes.vue';
import Component5 from './TestsHW/Test5memory.vue';


export default {
  components: {
    Component1,
    Component2,
    Component3,
    Component4,
    Component5
   

  },
  data() {
    return {
      
      currentIndex: 0, 
      currentComponent: 'Component1', 
      isTimerActive: false, 
      remainingTime: 10, 
      timerInterval: null, 
    };
  },
  methods: {
    
  },
};
</script>

<style>
.butt{
  color: black;
            border: none; 
            padding: 15px 13px; 
            text-align: center; 
            text-decoration: none;
            display: inline-block; 
            font-size: 25px;
            margin: 4px 2px; 
            cursor: pointer; 
            border-radius: 8px; 
            transition: background-color 0.3s; 
}
.button5 {
            background-color: #f2aa4b; 
            
        }
.button4 {
            background-color: #dfab55; 
            
        }
.button3 {
            background-color: #87b17f; 
            
        }
.button2 {
            background-color: #4ab49c; 
            
        }
.button1 {
            background-color: #08b9bc; 
            
        }

.button-container {
  position: fixed; 
  top: 0; 
  left: 0; 
  right: 0; 

  padding: 10px; 
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2); 
  z-index: 1000; 
  display: flex; 
  justify-content: center;
}

.component-container {
  align-items: baseline;
  text-align: center;
}


@media (max-width: 600px) {
.button-container{
 padding: 0%;
}
.fixerr {
  position: fixed; 
  top: 10%;
  left: 0;
  right: 0;
  padding: 10px 0; 
  z-index: 1000; 
}
  .butt {
    padding: 2px 1px; 
    width: 15rem; 
    height: 2rem;/* Кнопки занимают всю ширину */
    font-size: 12px; /* Увеличиваем размер шрифта кнопок */
  }}
</style>