<template>
  <main>
    <h2>News</h2>
    <section>
      <w-input v-model="input">Filtrar noticias</w-input>
      <div v-for="post in postsFiltered" :key="post.index">
        <w-card :img="post.img" :title="post.title" :description="post.description" />
      </div>
    </section>
  </main>
</template>

<script>
import { WInput, WCard } from 'vue-library';

export default {
  name: 'Main',
  components: {
    WInput,
    WCard,
  },
  data: () => ({
    input: '',
    posts: [
      {
        img: 'https://dummyimage.com/600x400/b8b8b8/000000.jpg',
        title: 'Title 1',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ut libero orci. Nullam blandit libero mauris, auctor tincidunt nisi fermentum eget. Integer nec ultricies mi. Donec eget ultrices augue.',
      }, {
        img: 'https://dummyimage.com/600x400/b8b8b8/000000.jpg',
        title: 'Probando 2',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ut libero orci. Nullam blandit libero mauris, auctor tincidunt nisi fermentum eget. Integer nec ultricies mi. Donec eget ultrices augue.',
      }, {
        img: 'https://dummyimage.com/600x400/b8b8b8/000000.jpg',
        title: 'Nuevo 3',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ut libero orci. Nullam blandit libero mauris, auctor tincidunt nisi fermentum eget. Integer nec ultricies mi. Donec eget ultrices augue.',
      }, {
        img: 'https://dummyimage.com/600x400/b8b8b8/000000.jpg',
        title: 'Test 4',
        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur ut libero orci. Nullam blandit libero mauris, auctor tincidunt nisi fermentum eget. Integer nec ultricies mi. Donec eget ultrices augue.',
      },
    ],
  }),
  computed: {
    postsFiltered() {
      return this.posts.filter(post => post.title.toLowerCase().includes(this.input.toLowerCase()));
    },
  },
};
</script>

<style scoped>
  main {
    margin: 20px;
    padding: 20px;
  }
  section {
    position: relative;
    overflow: hidden;
  }
</style>
