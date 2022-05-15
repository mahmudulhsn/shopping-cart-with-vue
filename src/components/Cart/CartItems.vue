<template>
    <tr v-for="(cartItem, index) in  cartItems">
        <td>{{ cartItem.name }}</td>
        <td>{{ cartItem.quantity }}</td>
        <td>{{ cartItem.totalAmount }}</td>
        <td class="text-red-600 font-bold text-xl cursor-pointer" @click="removeFromCart(cartItem)">X</td>
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
