<template>
    <div class="v-catolog-wrapper">
        
        <img class="v-catalog-item__image" src="https://img.joomcdn.net/cf004abcfc15260ee63c14b661fd613fba6ed508_original.jpeg " alt="img">

       <p class="catolog_item_name">{{product_data.name}}</p>
       <p class="catolog_item_price">{{product_data.price}} Р.</p>
       <button class="catolog_item_add_to_card-btn btn" @click="sendDataToParent">Add to card</button>
    </div>
</template>

<script>

export default{
    name:"V-catolog-item",
    props:{
        product_data:{
            type:Object,
            default(){
                return{

                }
            }
        }
    },
    data(){
        return{}
    },
    computed:{
      

    },
    methods:{
        sendDataToParent(){
            this.$emit( 'sendArticle',this.product_data.article)
        }
    }
}
</script>



<style >

.v-catolog-wrapper{
    flex-basis: 25%;
    box-shadow: 0 0 8px 0 #e0e0e0;
    padding:4*2;
    margin-bottom: 8*2;
 
}
.v-catalog-item__image{
    width: 300px;
    height: 300px;
}
</style>