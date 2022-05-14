<template>
    <tr v-for="(cartItem, index) in  cartItems">
        <td>{{ cartItem.name }}</td>
        <td>{{ cartItem.quantity }}</td>
        <td>{{ cartItem.price }}</td>
    </tr>
</template>

<script>
export default {
    props: {
        cartItems: Array,
    },

}
</script>
