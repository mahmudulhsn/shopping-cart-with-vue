<template>
    <div>
        <div class="img">
            <img class="w-full" :src="item.image" alt="">
        </div>
        <div class="product-details text-center mb-5">
            <h4 class="text-2xl">{{ item.name }}</h4>
            <h3 class="text-xl"><strong>Price: </strong> {{ item.price }}</h3>
            <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-5 rounded shadow-2xl">
                Add To Cart
            </button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        item: Object,
    },

}
</script>