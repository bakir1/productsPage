<template>
 <main id="app">
  <section class="products">
    <Product 
     v-for="product in products"
     :key="product.color"
     :product="product"
    />
  </section>
 </main>
</template>

<script>
import Product from './components/Product';

export default {
  name: 'App',
  components: {
    Product
  },
  data() {
    return {
      products: [
        {
          title: 'Krema 1',
          color: 'pink',
          bgtext: 'Siberian',
          src: require('./assets/sb1.png')
        },
       {
          title: 'Krema 2',
          color: 'green',
          bgtext: 'Siberian',
          src: require('./assets/sb4.png')
        },
       {
          title: 'Krema 3',
          color: 'blue',
          bgtext: 'Siberian',
          src: require('./assets/sb3.png')
        }
      ]
    }
  }
}
</script>

<style>
.{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'montseratt', sans-serif;
}

main {
  width: 100vw;
  min-height: 100vh;
  overflow: hidden;

  background-color: #EEE;
  display: flex;
  justify-content: center;
  align-content: center;
  align-items: center;
}

.products{
  display: flex;
  max-width: 1280px;
  padding: 25px;
  margin: 0 auto;
}

</style>
