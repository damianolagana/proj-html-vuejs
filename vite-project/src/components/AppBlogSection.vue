<script >





export default {
  name: "AppBlogSection",
  components: {


  },
  data() {
    return {
      blogs: [
        {
          blogPath: "/img/artist-blog-01-480x325.jpg",
          title: "Brush Strokes Energize Trees in Paintings",
          date: "May 15, 2020",
          views: "688 views"
        },
        {
          blogPath: "/img/artist-blog-02-480x325.jpg",
          title: "Pocket-Sized Notebook Hold Miniature Paintings",
          date: "May 15, 2020",
          views: "603 views"
        },
        {
          blogPath: "/img/artist-blog-03-480x325.jpeg",
          title: " Connection Between Self-Portraits and Identity",
          date: "May 15, 2020",
          views: "397 views"
        }
      ]
    };
  },
  methods: {},

}

</script>

<template>
  <section>
    <div class="container">
      <div class="blogBoxTitle textCenter">
        <h3>ENJOY READING ON MAXCOACH</h3>
        <h1>Latest on <span>Our Blogs</span></h1>
      </div>
      <div class="blogBox">
        <div class="blogCard" v-for="blog in blogs">
          <div>
            <img :src="blog.blogPath" alt="">
          </div>
          <div class="blogInfo">
            <h3>ARTIST</h3>
            <h2>{{ blog.title }}</h2>
          </div>
          <div class="blogIcons">
            <div>
              <font-awesome-icon :icon="['far', 'calendar']" /> {{ blog.date }}
            </div>
            <div>
              <font-awesome-icon :icon="['far', 'eye']" /> {{ blog.views }}
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss";

section {
  background-color: #f8f8f8;
}

.blogBoxTitle {
  line-height: 3rem;
  padding: 3rem 0;


  h3 {
    color: grey;
    font-size: 12px;
  }

  h1 {
    font-size: 40px;

    span {
      color: #20ad96;
      font-weight: 400;
    }
  }
}


.blogBox {
  display: flex;
  padding-bottom: 6rem;
}

.blogCard {
  width: calc(100%/3);
  padding-top: 1rem;

  img {
    width: 100%;
    display: block;
    padding: 0 2rem 2rem 0;
    border-radius: 3%;

  }

  .blogInfo {
    line-height: 2rem;
    padding-bottom: 1.5rem;

    h3 {
      color: grey;
      font-size: 13px;
    }

  }

  .blogIcons {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 65%;
    color: grey;
  }
}
</style>
