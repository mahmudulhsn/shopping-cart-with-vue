

<template>
  <main>
    <div class="flex mt-2 space-x-2">
      <div class="w-3/4">
        <Items />
      </div>

      <div class="w-1/4 border rounded shadow-xl text-center relative h-screen">
        <CartDetails />
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
  }

};
</script>