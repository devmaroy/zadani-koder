<template>
  <main>
    <Header />
    <Hero />
    <Info />
    <Steps />
    <MainBanner />
    <BlogPosts />
    <SecondaryBanner />
    <Footer />
  </main>
</template>

<script>
import Header from "~/components/layout/Header";
import Hero from "~/components/sections/Hero";
import Info from "~/components/sections/Info";
import Steps from "~/components/sections/Steps";
import MainBanner from "~/components/sections/MainBanner";
import BlogPosts from "~/components/sections/BlogPosts";
import SecondaryBanner from "~/components/sections/SecondaryBanner";
import Footer from "~/components/layout/Footer";

export default {
  name: "Homepage",
  components: {
    Header,
    Hero,
    Info,
    Steps,
    MainBanner,
    BlogPosts,
    SecondaryBanner,
    Footer,
  },
};
</script>

<style lang="scss" scoped>
.hp {
  text-align: center;
  margin-top: 50px;
}
</style>
