<template>
<TheNavbar />
 <div>
  <TheHeader />

    <main>
      <p>Find gorgeous spots to visit this summer by simply searching for them on our website.</p>
      </main>
  </div>
  <caption-content>
    <template #content>
      <img 
      src="https://images.pexels.com/photos/846265/pexels-photo-846265.jpeg?cs=srgb&dl=pexels-the-happiest-face-%29-846265.jpg&fm=jpg"
      />
      <ProductCard />
    </template>
    <ImageProduct/>
    <CardDesign/>
    <CardTag/>
    <CaptionContent/>
    <CardTitle/>
    <ClickButton/>
    <CardSize/>
    <ProductCard/>
    <ProductPrice/>
    
        <div>
      <card-design v-for="product in products" :key="product.id">
        <image-product :url="product.image" />
        <product-header>{{ product.title }}</product-header>
        <product-info>{{ product.info }}</product-info>
        <product-price>{{ product.price }}</product-price>
        <product-size>{{ product.size }}</product-size>
        <product-tag v-if="product.tags">{{ product.tags }}</product-tag>
        <product-action>Add to Cart</product-action>
      </card-design>
    </div>
  </caption-content>
      <TheFooter />
</template>
      
<script setup>
import TheFooter from './components/ui/TheFooter.vue'
import TheNavbar from './components/ui/TheNavbar.vue'
import ImageProduct from './components/product/ImageProduct.vue'
import CardDesign from './components/product/CardDesign.vue'
import CaptionContent from './components/product/CaptionContent.vue'
import CardSize from './components/product/CardSize.vue'
import CardTitle from './components/product/CardTitle.vue'
import ClickButton from './components/product/ClickButton.vue'
import ProductPrice from './components/product/ProductPrice.vue'
import TheHeader from './components/ui/TheHeader.vue'


const products = [
  {
    title: "Nike Air Jordan",
    info: "These shoes are super comfortable and stylish",
    price: "$185",
    size: "6-14",
    image: require(`./assets/images/nike-air-jordan.png`),
    tags: "Red, Black, White, Blue, Green",

  },
  {
    title: "Adidas Backpack",
    info: "Great Backpack for summer hiking",
    price: "$85",
    size: "S,M,L",
    image: require(`./assets/images/adidas-backpack.jpeg`),
    tags: "Red, Black, White",
  },

  {

    title: "Adidas Crewneck",
    info: "Very comfortable Adidas Sweatshirt/Crewneck",
    price: "$105",
    size: "S,M,L",
    image: require(`./assets/images/adidas-crewneck.jpeg`),
    tags: "Red, Black, White, pink,",

  }
]
</script>
<style>

#app {

  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
  color: red;
  background: black;
}

</style>