<template>
    <div>
        <div v-if="cartItemsArray.length > 0">
            <h1 class="text-2xl border-b-2 py-2">Item Lists ({{ cartItemsArray.length }})</h1>
            <div class="cart-item-list pb-8">
                <table class="table-fixed">
                    <thead>
                        <tr>
                            <th class="w-3/5 px-4 py-2">Name</th>
                            <th class="w-1/5 px-4 py-2">Quantity</th>
                            <th class="w-1/5 px-4 py-2">Amount</th>
                            <th class="w-1/5 px-4 py-2"></th>
                        </tr>
                    </thead>
                    <tbody>
                        <CartItems :cartItems="cartItemsArray" @remove="removeCartItem" />
                    </tbody>
                </table>
            </div>

            <div class="inset-x-0 bottom-0 text-xl border-t-2 flex">
                <div class="w-1/2 text-left pl-2 font-bold">Total</div>
                <div class="w-1/2 text-right pr-2">{{ finalTotal }}</div>
            </div>
        </div>
        <div v-else>
            <h1 class="grid place-items-center h-screen text-2xl text-red-500">Please, Add Item to Cart.</h1>
        </div>
    </div>
</template>

<script>
import CartItems from "./CartItems.vue";
export default {
    components: { CartItems },
    data() {
        return {
            cartItemsArray: [],
            finalTotal: 0
        }
    },
    mounted() {
        this.eventBus.on('addItemToCart', (item) => {
            let cartItem = {
                id: item.id,
                name: item.name,
                totalAmount: item.price,
                quantity: 1,
            };

            let tempFinalTotal = cartItem.totalAmount * cartItem.quantity;
            let findItem = this.cartItemsArray.find(element => element.id == cartItem.id);
            if (findItem) {
                this.cartItemsArray.map(element => {
                    if (element.id == cartItem.id) {
                        element.quantity = element.quantity + cartItem.quantity;
                        element.totalAmount = element.totalAmount + tempFinalTotal;
                    }
                })
            } else {
                this.cartItemsArray.push(cartItem)
            }
            this.finalTotal += tempFinalTotal;
        })
    },
    methods: {
        removeCartItem(cartItem) {
            const indexOfObject = this.cartItemsArray.findIndex(object => object.id == cartItem.id);
            this.cartItemsArray.splice(indexOfObject, 1);

            this.finalTotal -= cartItem.totalAmount;

            // return item to the products
            this.eventBus.emit('returnItems', cartItem);
        }
    },


}
</script>
