<template>
    <tr v-for="(cartItem, index) in  cartItems">
        <td>{{ cartItem.name }}</td>
        <td>{{ cartItem.quantity }}</td>
        <td>{{ cartItem.price }}</td>
    </tr>
</template>

<script>
import CartItem from './CartItem.vue'
export default {
    props: {
        cartItems: Array,
    },
    components: {
        CartItem,
    },
}
</script>
