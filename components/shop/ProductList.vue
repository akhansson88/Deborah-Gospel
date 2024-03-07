<template>
  <div class="container mx-auto p-6">
    <h3 class="text-xl text-debby-dark font-bold mb-4">Merchandise Store</h3>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
      <ProductItem 
        v-for="product in products" 
        :key="product.id" 
        :product="product"
        @add-to-cart="addToCart"
      />
    </div>
  </div>
</template>

<script>
import ProductItem from '~/components/shop/ProductItem.vue'

export default {
  components: {
    ProductItem
  },
  data() {
    return {
      // Mock data, should be fetched from an API or store
      products: [
        { id: 1, title: 'Single MP3', price: 15.99, image: require('@/assets/img/Izina_Rya_Yesu_AlbumCover.jpg') },
        { id: 2, title: 'T-Shirt', price: 25.99, image: require('@/assets/img/tshirt_gospel.jpg') },
        // ... more products
      ]
    }
  },
  methods: {
    addToCart(product) {
      // Placeholder for cart logic
      console.log('Add to cart', product);
    }
  }
}
</script>
