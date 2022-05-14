

<template>
  <main>
    <div class="flex mt-2 space-x-2">
      <div class="w-3/4">
        <Items :items="itemsArray" />
      </div>

      <div class="w-1/4 border rounded shadow-xl text-center relative h-screen">
        <CartDetails :cartItemsList="cartItemsArray" />
      </div>

    </div>
  </main>
</template>

<script>
import Items from "./../components/Items/Items.vue";
import CartDetails from "../components/Cart/CartDetails.vue";
export default {
  components: {
    Items,
    CartDetails
  },
  data() {
    return {
      itemsArray: [
        {
          id: 1,
          name: "Bashmoti Rice",
          price: 100.00,
          image: './../../assets/img/grocery-items.png'
        },
        {
          id: 2,
          name: "Fresh Pineapple",
          price: 300.00,
          image: './../../assets/img/fresh-fruit.png'
        },
        {
          id: 3,
          name: "Another Rice",
          price: 200.00,
          image: './../../assets/img/grocery-items.png'
        },
        {
          id: 4,
          name: "Another Frout",
          price: 150.00,
          image: './../../assets/img/fresh-fruit.png'
        },
        {
          id: 5,
          name: "Another Frout 2",
          price: 160.00,
          image: './../../assets/img/fresh-fruit.png'
        },
      ],
      cartItemsArray: [
        {
          id: 1,
          name: "Bashmoti Rice",
          quantity: 2,
          price: 100.00,
        },
        {
          id: 2,
          name: "Fresh Pineapple",
          quantity: 2,
          price: 300.00,
        },
        {
          id: 3,
          name: "Another Rice",
          quantity: 1,
          price: 200.00,
        },
        {
          id: 4,
          name: "Another Frout",
          quantity: 8,
          price: 150.00,
        },
        {
          id: 5,
          name: "Another Frout 2",
          quantity: 1,
          price: 160.00,
        },
      ]
    }
  },
};
</script>