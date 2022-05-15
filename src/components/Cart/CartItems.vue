<template>
    <tr v-for="(cartItem, index) in  cartItems">
        <td>{{ cartItem.name }}</td>
        <td>{{ cartItem.quantity }}</td>
        <td>{{ cartItem.totalAmount }}</td>
        <td><span
                class="text-white font-bold text-xl cursor-pointer bg-red-600 rounded-full px-3 py-1 hover:bg-red-900 duration-300"
                @click="removeFromCart(cartItem)">X</span>
        </td>
    </tr>
</template>

<script>
export default {
    props: {
        cartItems: Array,
    },
    methods: {
        removeFromCart(cartItem) {
            this.$emit('remove', cartItem);
        }
    },

}
</script>
