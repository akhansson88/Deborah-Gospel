<template>
  <div class="rounded-lg shadow-lg bg-white max-w-sm">
    <img :src="product.image" :alt="product.title" class="rounded-t-lg w-full"/>
    <div class="p-6">
      <h5 class="text-gray-900 text-xl font-medium mb-2">{{ product.title }}</h5>
      <p class="text-gray-600 text-base mb-4">
        {{ product.description }}
      </p>
      <p class="text-gray-900 text-xl font-semibold mb-4">{{ product.price | currency }}</p>
      <button @click="$emit('add-to-cart', product)" class="bg-debby-skyblue text-white p-3 rounded-lg w-full">Add to Cart</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true
    }
  },
  filters: {
    currency(value) {
      return `$${value.toFixed(2)}`;
    }
  }
}
</script>
