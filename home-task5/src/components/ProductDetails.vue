<template>
    <div>
        <div>
            <h1>{{ product.name }}</h1>
            <p>Цена: {{ formattedPrice }}</p>
            <p class="out_of_stock" v-if=!product.available>Out of stock <br>
                <button class="btn product_not">отслеживать</button></p>
             <p class="available" v-else>Available<br><button class="btn" >Купить</button></p>
             
           
        </div>
    </div>
</template>


<script>
export default {
    name: 'ProductDetails',
    props: ['product'],

    data() {
        return {
            available: true
            
        };
    },
    computed: {
        formattedPrice(){
            return this.product.price + " ₽";
        }
    },
};
</script>

<style lang="css" scoped>
.btn{
    margin-top: 6px;
    border-radius: 12px;
    background-color: #7be98f;
}
.product_not{
    
    background-color: #e9b87b;
}
.out_of_stock{
    color: #bd3834;
}
.available{
    color: #13771e;
}

</style>