<template>
  <div>
    <!-- Header section -->
    <header class="hero">
      <h1>Welcome to Our E-commerce Site</h1>
      <p>Explore our wide range of products and find great deals.</p>
      <a href="/products" class="cta-button">Shop Now</a>
    </header>

    <!-- Featured products section -->
    <section class="featured-products">
      <h2>Featured Products</h2>
      <div class="product">
        <img src="https://cdn.mos.cms.futurecdn.net/HkdMToxijoHfz4JwUgfh3G-1200-80.jpg.webp" alt="Product 1" />
        <h3>Product Name: PS5</h3>
        <p>Powered by an eight-core AMD Zen 2 CPU and custom AMD Radeon GPU, the PS5 
          is a powerful gaming machine that delivers incredible performance with amazing graphics.
          
        </p>
        <span class="price">$699</span>
      </div>
      <div class="product">
    <img src="https://cdn.theschoollocker.com.au/media/catalog/product/cache/1/image/9df78eab33525d08d6e5fb8d27136e95/m/a/macbook_air_hero_space_gray_pure_front_open_screen_1.jpg" alt="Product 2" />
    <h3>Product Name: MACBOOK AIR</h3>
    <p>The latest MacBook Air features a stunning Retina display with True Tone technology, a backlit Magic Keyboard, Touch ID,
       a 10th-generation Intel Core processor and all-day battery life.
      All in a thin, light and perfectly portable design..</p>
    <span class="price">$1299</span>
  </div>
    </section>

    <!-- About us section -->
    <section class="about-us">
      <h2>About Us</h2>
      <p>We are your trusted source for quality products. Learn more about our mission and values.</p>
      <a href="/about" class="cta-button">About Us</a>
    </section>
  </div>
</template>

<style>
/* Add CSS styles for header section */
.hero {
  background-color: #ff6600; /* Background color */
  color: #fff;
  text-align: center;
  padding: 100px 0;
}

.hero h1 {
  font-size: 36px;
  margin-bottom: 20px;
}

.cta-button {
  display: inline-block;
  padding: 10px 20px;
  background-color: #333; /* Button background color */
  color: #fff;
  text-decoration: none;
  font-weight: bold;
  border-radius: 5px;
}

/* Add CSS styles for featured products section */
.featured-products {
  margin: 50px 0;
}

.product {
  border: 1px solid #ddd;
  padding: 20px;
  text-align: center;
  margin: 10px;
}

.product img {
  max-width: 100%;
}

.price {
  font-size: 24px;
  color: #ff6600;
}

/* Add CSS styles for about us section */
.about-us {
  background-color: #f5f5f5;
  text-align: center;
  padding: 50px 0;
}

.about-us h2 {
  font-size: 28px;
  margin-bottom: 20px;
}
</style>
