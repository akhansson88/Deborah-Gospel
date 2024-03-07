<template>
  <div class="py-8">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-semibold text-debby-dark mb-6">Merchandise</h2>
      <ProductList :products="products" />
    </div>
  </div>
</template>

<script>
import ProductList from '~/components/shop/ProductList.vue';

export default {
  components: {
    ProductList
  },
  data() {
    return {
      // This data will eventually come from an API
      products: [
        {
          id: 1,
          name: 'Deborah T-Shirt',
          price: 20.00,
          image: '~/assets/img/merch/tshirt.jpg',
          // ... more product fields
        },
        // ... more products
      ]
    };
  }
}
</script>
