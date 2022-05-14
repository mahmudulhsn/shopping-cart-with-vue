<script setup>
import TheWelcome from "@/components/TheWelcome.vue";
</script>

<template>
  <main>
    <div class="flex mt-2 space-x-2">
      <div class="w-3/4">
        <div class="grid grid-cols-4 gap-4">
          <!-- single item starts -->
          <div class="border p-2 shadow-lg rounded">
            <div class="img">
              <img class="w-full" src="./../../assets/img/grocery-items.png" alt="">
            </div>
            <div class="product-details text-center mb-5">
              <h4 class="text-2xl">Basmoti Rice</h4>
              <h3 class="text-xl"><strong>Price: </strong> 300.00 BDT</h3>
              <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-5 rounded shadow-2xl">Add
                To
                Cart</button>
            </div>
          </div>
          <!-- single item ends -->

          <!-- single item starts -->
          <div class="border p-2 shadow-lg rounded">
            <div class="img">
              <img class="w-full" src="./../../assets/img/fresh-fruit.png" alt="">
            </div>
            <div class="product-details text-center">
              <h4 class="text-2xl">Fresh Pineapple</h4>
              <h3 class="text-xl"><strong>Price: </strong> 300.00 BDT</h3>
              <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-5 rounded">Add To
                Cart</button>
            </div>
          </div>
          <!-- single item ends -->

          <!-- single item starts -->
          <div class="border p-2 shadow-lg rounded">
            <div class="img">
              <img class="w-full" src="./../../assets/img/grocery-items.png" alt="">
            </div>
            <div class="product-details text-center">
              <h4 class="text-2xl">Another Rice</h4>
              <h3 class="text-xl"><strong>Price: </strong> 200.00 BDT</h3>
              <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-5 rounded">Add To
                Cart</button>
            </div>
          </div>
          <!-- single item ends -->

          <!-- single item starts -->
          <div class="border p-2 shadow-lg rounded">
            <div class="img">
              <img class="w-full" src="./../../assets/img/grocery-items.png" alt="">
            </div>
            <div class="product-details text-center">
              <h4 class="text-2xl">Another Rice</h4>
              <h3 class="text-xl"><strong>Price: </strong> 200.00 BDT</h3>
              <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-5 rounded">Add To
                Cart</button>
            </div>
          </div>
          <!-- single item ends -->

          <!-- single item starts -->
          <div class="border p-2 shadow-lg rounded">
            <div class="img">
              <img class="w-full" src="./../../assets/img/grocery-items.png" alt="">
            </div>
            <div class="product-details text-center">
              <h4 class="text-2xl">Another Rice</h4>
              <h3 class="text-xl"><strong>Price: </strong> 200.00 BDT</h3>
              <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-5 rounded">Add To
                Cart</button>
            </div>
          </div>
          <!-- single item ends -->

          <!-- single item starts -->
          <div class="border p-2 shadow-lg rounded">
            <div class="img">
              <img class="w-full" src="./../../assets/img/grocery-items.png" alt="">
            </div>
            <div class="product-details text-center">
              <h4 class="text-2xl">Another Rice</h4>
              <h3 class="text-xl"><strong>Price: </strong> 200.00 BDT</h3>
              <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-5 rounded">Add To
                Cart</button>
            </div>
          </div>
          <!-- single item ends -->

          <!-- single item starts -->
          <div class="border p-2 shadow-lg rounded">
            <div class="img">
              <img class="w-full" src="./../../assets/img/grocery-items.png" alt="">
            </div>
            <div class="product-details text-center">
              <h4 class="text-2xl">Another Rice</h4>
              <h3 class="text-xl"><strong>Price: </strong> 200.00 BDT</h3>
              <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 mt-5 rounded">Add To
                Cart</button>
            </div>
          </div>
          <!-- single item ends -->
        </div>
      </div>

      <div class="w-1/4 border rounded shadow-xl text-center relative h-screen">
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
              <tr>
                <td>Basmoti Rice </td>
                <td>1</td>
                <td>300.00</td>
              </tr>
              <tr>
                <td>Fresh Pineapple</td>
                <td>2</td>
                <td>600.00</td>
              </tr>
              <tr>
                <td>Another Rice</td>
                <td>3</td>
                <td>600.00</td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="inset-x-0 bottom-0 text-xl border-t-2 flex">
          <div class="w-1/2 text-left pl-2">Total</div>
          <div class="w-1/2 text-right pr-2">1500.00</div>
        </div>
      </div>

    </div>
  </main>
</template>
