<template>
    <div>
        <h1 class="text-2xl border-b-2 py-2">Item Lists</h1>
        <div class="cart-item-list pb-8">
            <table class="table-fixed">
                <thead>
                    <tr>
                        <th class="w-3/5 px-4 py-2">Name</th>
                        <th class="w-1/5 px-4 py-2">Quantity</th>
                        <th class="w-1/5 px-4 py-2">Amount</th>
                    </tr>
                </thead>
                <tbody>
                    <CartItems :cartItems="cartItemsList" />
                </tbody>
            </table>
        </div>

        <div class="inset-x-0 bottom-0 text-xl border-t-2 flex">
            <div class="w-1/2 text-left pl-2">Total</div>
            <div class="w-1/2 text-right pr-2">1500.00</div>
        </div>
    </div>
</template>

<script>
import CartItems from "./CartItems.vue";
export default {
    props: {
        cartItemsList: Array,
    },
    components: { CartItems },
}
</script>
