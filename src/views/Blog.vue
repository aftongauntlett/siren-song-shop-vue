<template>
  <b-container>
    <Header />
    <div class="pt-5">
      <ul class="flex-container">
        <BlogContent
          class="flex-item mb-5 mx-4"
          v-for="item in items"
          :key="item.name"
          :item="item"
        />
      </ul>
    </div>
  </b-container>
</template>

<script>
import Header from "../components/Header.vue";
import BlogContent from "../components/BlogContent.vue";
export default {
  components: { BlogContent, Header },
  data() {
    return {
      items: [
        {
          image: "magical-book.jpg",
          name: "Blog Example Title",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?",
        },
        {
          image: "magical-book.jpg",
          name: "Blog Example Title",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?",
        },
        {
          image: "magical-book.jpg",
          name: "Blog Example Title",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?",
        },
        {
          image: "magical-book.jpg",
          name: "Blog Example Title",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?",
        },
        {
          image: "magical-book.jpg",
          name: "Blog Example Title",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque? Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?",
        },
        {
          image: "magical-book.jpg",
          name: "Blog Example Title",
          description:
            "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?",
        },
        {
          image: "magical-book.jpg",
          name: "Blog Example Title",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?",
        },
        {
          image: "magical-book.jpg",
          name: "Blog Example Title",
          description:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere minus autem provident, ut nisi vitae qui, cupiditate aliquam fuga eius iste quo beatae illum dicta sequi vel deserunt. Sit, doloremque?",
        },
      ],
    };
  },
};
</script>

<style scoped>
.flex-container {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  padding: 25px;
  list-style: none;
}

.flex-item {
  background: unset;
  min-width: 350px;
  max-width: 475px;
  margin-top: 10px;
  box-shadow: 1px 1px 20px 10px #3b525557;
}

.about-section {
  padding: 20px;
  max-width: 700px;
  margin: auto;
}
</style>
