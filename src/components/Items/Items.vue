<template>
    <div class="grid grid-cols-4 gap-4">
        <div class="border p-2 shadow-lg rounded" v-for="(item, index) in itemsArray">
            <SingleItem :item="item" @addItemToCart="addItemToCart" @returnItems="returnItems" />
        </div>
    </div>
</template>

<script>
import SingleItem from '../../components/Items/SingleItem.vue'
export default {
    components: { SingleItem },
    data() {
        return {
            itemsArray: [
                {
                    id: 1,
                    name: "Bashmoti Rice",
                    price: 100.00,
                    stockQuantity: 250,
                    image: './../../assets/img/grocery-items.png'
                },
                {
                    id: 2,
                    name: "Fresh Pineapple",
                    price: 300.00,
                    stockQuantity: 990,
                    image: './../../assets/img/fresh-fruit.png'
                },
                {
                    id: 3,
                    name: "Another Rice",
                    price: 200.00,
                    stockQuantity: 500,
                    image: './../../assets/img/grocery-items.png'
                },
                {
                    id: 4,
                    name: "Another Fruit",
                    price: 150.00,
                    stockQuantity: 200,
                    image: './../../assets/img/fresh-fruit.png'
                },
                {
                    id: 5,
                    name: "Another Fruit 2",
                    price: 160.00,
                    stockQuantity: 350,
                    image: './../../assets/img/fresh-fruit.png'
                },
            ],

        }
    },
    mounted() {
        this.eventBus.on('returnItems', (cartItem) => {
            this.itemsArray.map(element => {
                if (element.id == cartItem.id) {
                    element.stockQuantity = element.stockQuantity + cartItem.quantity;
                }
            })
        })
    },
}
</script>
