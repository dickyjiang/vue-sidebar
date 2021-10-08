<template>
  <div class="bg-white h-screen">
    <Navbar/>
    <div class="border-black">
        <div class="pl-4 py-2 mb-4 border-b border-black text-black text-4xl font-semibold">
          <h1>Controlled</h1>
          <h1>Tab</h1>
        </div>
        <div class="pl-4">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta eius alias soluta a est officiis. Asperiores nesciunt odit nostrum quam accusantium atque necessitatibus. Deleniti natus quasi dolor aperiam accusamus eaque ducimus, cupiditate enim perferendis! Ipsum quo nesciunt, nihil natus temporibus voluptate, asperiores tempora vitae voluptatem exercitationem at fuga quae delectus unde sit quaerat debitis veniam quos nisi. Quasi, ipsa corrupti? Quo culpa debitis doloribus sunt temporibus alias suscipit esse dignissimos, explicabo sit laudantium necessitatibus ipsa sint, enim, consequatur cupiditate facilis quibusdam tenetur est hic id repellendus vel dolor molestias? Ullam repellat aliquam ex qui molestias? Aspernatur, dolores. Excepturi, dicta minima.</p>
        </div>
    </div>

  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue'

export default {
  name: 'Home',
  components: { Navbar
  }
}
</script>
