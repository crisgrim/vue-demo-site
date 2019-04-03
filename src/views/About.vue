<template>
  <div>
    <the-menu />
    <the-header title="About me"/>
    <section>
      <img class="about_img" src="@/assets/me.jpg"/>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus tempus lectus at porttitor semper. Duis finibus libero nec nulla bibendum, quis pretium risus accumsan. Pellentesque pellentesque, neque ut posuere laoreet, arcu sem pretium mi, eget hendrerit massa massa sed ipsum. Donec tempor, arcu vitae pellentesque vestibulum, massa dolor dignissim sapien, sed commodo neque mi in turpis. Sed ut nisi efficitur, ullamcorper ante a, efficitur odio. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam rhoncus lacinia orci vel auctor. Mauris imperdiet mattis posuere. In hac habitasse platea dictumst. Sed nec gravida augue. Donec eget sagittis ex. Nulla rutrum est sed tempor sodales. Curabitur rutrum id nisl id porttitor. Nulla at nunc sit amet risus facilisis congue.</p>
    </section>
    <the-footer />
  </div>
</template>

<script>
import TheMenu from '@/components/TheMenu.vue';
import TheHeader from '@/components/TheHeader.vue';
import TheFooter from '@/components/TheFooter.vue';

export default {
  name: 'About',
  components: {
    TheMenu,
    TheHeader,
    TheFooter,
  },
};
</script>

<style>
  .about_img {
    border: 5px solid #ffffff;
    width: 80%;
  }
  section {
    display: block;
    margin: 0 auto;
    width: 80%;
  }
</style>
