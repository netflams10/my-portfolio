<template>
  <div class="container" data-aos="fade-left">
    <HeaderSection />
    <StackSection />
    <ProjectsComponent />
    <ArticleComponent />
    <MyStackComponent />
    <ContactSection />
    <FooterSection />
  </div>
</template>

<script>
  import HeaderSection from './sections/HeaderSection.vue';
  import StackSection from './sections/StackSection.vue';
  import ArticleComponent from './sections/ArticleComponent.vue';
  import ProjectsComponent from './sections/ProjectsComponent.vue';
  import MyStackComponent from './sections/MyStackComponent.vue';
  import ContactSection from './sections/ContactSection.vue';
  import FooterSection from './sections/FooterSection.vue';

  export default {
    name: 'App',
    components: { HeaderSection, StackSection, FooterSection, ContactSection, MyStackComponent, ArticleComponent, ProjectsComponent },
    created () {
      this.$store.dispatch('getData');
    },
  }
</script>

<style lang="scss">
  @import "./assets/sass/index.scss";
</style>
