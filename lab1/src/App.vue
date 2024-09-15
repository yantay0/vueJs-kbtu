<template>
  <div id="app">
    <header>
      <div class="logo">
        <h1>Mini Blog</h1>
      </div>
      <nav class="navbar">
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Politics</a></li>
          <li><a href="#">Tech</a></li>
          <li><a href="#">Entertainment</a></li>
          <li><a href="#">Travel</a></li>
          <li><a href="#">Sports</a></li>
        </ul>
      </nav>
    </header>

    <!-- Blog Section -->
    <section class="blog-section">
      <div class="blog-post" v-for="(post, index) in posts" :key="index">
        <img :src="post.image" alt="Post image">
        <div class="post-content">
          <h2>{{ post.title }}</h2>
          <p>{{ post.date }}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {
          image: "https://via.placeholder.com/200",
          title: "The AI magically removes moving objects from videos.",
          date: "July 19, 2019",
        },
        {
          image: "https://via.placeholder.com/200",
          title: "The 20 Biggest Fintech Companies In America 2019",
          date: "July 19, 2019",
        },
                {
          image: "https://via.placeholder.com/200",
          title: "The 100 Biggest Fintech Companies In America 2022",
          date: "July 19, 2019",
        },
      ]
    };
  }
};
</script>

<style scoped>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
}

/* Header Styling */
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  background-color: #fff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.logo h1 {
  font-size: 24px;
  margin: 0;
}

.navbar ul {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.navbar ul li {
  margin-left: 20px;
}

.navbar ul li a {
  text-decoration: none;
  color: #333;
  font-size: 16px;
}

.navbar ul li a:hover {
  color: #007bff;
}

.blog-section {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  margin-top: 20px;
}

.blog-post {
  background: #f4f4f4;
  margin: 10px;
  border-radius: 8px;
  overflow: hidden;
  width: 250px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.blog-post img {
  width: 100%;
  height: auto;
}

.post-content {
  padding: 15px;
}

.post-content h2 {
  font-size: 18px;
  margin: 10px 0;
}

.post-content p {
  font-size: 14px;
  color: gray;
}
</style>
