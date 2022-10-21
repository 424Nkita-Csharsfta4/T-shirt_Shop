<template>
    <Vcatolog/>
    <VCart/>
</template>

<script>
import Vcatolog from './V-catolog.vue'
import VCart from './V-cart.vue'

export default{
 name:'wrapper-main',
 //Выстраивание ииерархии
 components:{
    Vcatolog,
    VCart
},
 data(){//Персональные даные компонента
  return{
    count: 0
  }
 },//Должна обязательно что то возвращять
 
 //computed:{Вычислительные свойства компонента},
 //methods:{},Отлавливает действие пользователя Клики показы модалки скрыти елементов анимация и.тд
 watch:{},//Дает следить за изменениями в компоненте
  mounted(){
    console.log('Hello suka')
  }
}
</script>

<style scoped>
.main-wrappper{
    max-width: 900px;
    margin: 0 auto;
}
</style>