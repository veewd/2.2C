<template>
  <div class="web-app-intro">
    <header>
      <h1>{{ pageTitle }}</h1>
    </header>

    <main>
      <section id="welcome">
        <h2>Welcome to Web Applications</h2>
        <p>
          Welcome to this website where we explore the fascinating world of web applications and learn how to build them using Vue 3.
        </p>
        <p>
          Web applications have revolutionized the way we interact with the internet. They provide dynamic and interactive user experiences, making them an essential part of modern web development.
        </p>
        <img src="https://miro.medium.com/v2/resize:fit:786/format:webp/1*GaBtlHe240ZkwlcBrFczgQ.jpeg" alt="Placeholder Image" />
      </section>

      <section id="html">
  <h2>HTML</h2>
  <p>
    HTML (Hypertext Markup Language) is the foundation of web development. It defines the structure and content of web pages, allowing you to create headings, paragraphs, links, images, and more.
  </p>
  <p>
    Understanding HTML is essential for building well-structured web applications.
  </p>
  <img src="https://www.udacity.com/blog/wp-content/uploads/2020/06/HTML_Blog-scaled.jpeg" alt="HTML Image" style="max-width: 100%; height: auto;" />
</section>


<section id="css">
  <h2>CSS</h2>
  <p>
    CSS (Cascading Style Sheets) is used to style web pages, making them visually appealing. With CSS, you can control the layout, colors, fonts, and other design aspects of your web applications.
  </p>
  <p>
    Learning CSS is crucial for creating beautiful and user-friendly web interfaces.
  </p>
  <img src="https://www.oxfordwebstudio.com/user/pages/06.da-li-znate/sta-je-css/sta-je-css.png" alt="CSS Image" style="max-width: 100%; height: auto;" />
</section>


<section id="javascript">
  <h2>JavaScript for Web Design</h2>
  <p>
    JavaScript is a versatile programming language that plays a crucial role in web design. It enables you to create interactive and dynamic web pages by manipulating the Document Object Model (DOM), handling events, and more.
  </p>
  <p>
    In this section, we'll explore how to use JavaScript effectively for enhancing the design and functionality of your web applications.
  </p>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/IPNsAmWe508" frameborder="0" allowfullscreen></iframe>
</section>


      <section id="vue">
  <h2>Vue 3</h2>
  <p>
    Vue 3 is a progressive JavaScript framework that makes it easy to build web applications. It offers powerful features like reactive data binding, component-based architecture, and a robust ecosystem of plugins and libraries.
  </p>
  <p>
    You can get started with Vue 3 by exploring its core documentation:
    <a href="https://v3.vuejs.org" target="_blank" rel="noopener">Vue 3 Docs</a>
  </p>
  <img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/1*UJJ-V7mds_kGpta4aq4BVg.jpeg" alt="Vue Image" style="max-width: 100%; height: auto;" />
</section>

    </main>

    <footer>
      <h3>Useful Links</h3>
      <ul>
        <li><a href="https://v3.vuejs.org" target="_blank" rel="noopener">Vue 3 Documentation</a></li>
        <li><a href="https://github.com/vuejs/vue-next" target="_blank" rel="noopener">Vue 3 GitHub Repository</a></li>
        <li><a href="https://vuejs.org/community" target="_blank" rel="noopener">Vue Community</a></li>
      </ul>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'WebAppIntro',
  data() {
    return {
      pageTitle: 'Web Applications and Vue 3'
    };
  }
}
</script>

<style scoped>
/* Global Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

/* Header Styles */
header {
  background-color: #42b983;
  color: #fff;
  text-align: center;
  padding: 20px 0;
}

/* Main Content Styles */
main {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

section {
  margin-bottom: 40px;
}

h2 {
  font-size: 24px;
  color: #333;
}

p {
  font-size: 16px;
  line-height: 1.5;
  color: #666;
}

/* Footer Styles */
footer {
  background-color: #333;
  color: #fff;
  padding: 20px 0;
  text-align: center;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin-bottom: 10px;
}

a {
  color: #42b983;
  text-decoration: none;
  transition: color 0.3s ease;
}

a:hover {
  color: #2e7d67;
}

/* Additional Styles for the New Sections */
/* You can add specific styles for the new sections if needed */
</style>
