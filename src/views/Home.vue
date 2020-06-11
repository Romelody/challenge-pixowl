<template>
  <div class="Home">
    <Header :tabletView="tabletView" />
    <Banner :tabletView="tabletView" />
    <Features :tabletView="tabletView" />
    <ArtistCreations :tabletView="tabletView" />
    <ArtistQuotes :tabletView="tabletView" />
    <Join v-if="!tabletView" />
    <Footer v-if="!tabletView" />
  </div>
</template>

<script>
import Header from "@/components/Header";
import Banner from "@/components/Banner";
import Features from "@/components/Features";
import ArtistCreations from "@/components/ArtistCreations";
import ArtistQuotes from "@/components/ArtistQuotes";
import Join from "@/components/Join";
import Footer from "@/components/Footer";
export default {
  name: "Home",
  props: {
    msg: String,
    tabletView: Boolean
  },
  components: {
    Features,
    Header,
    Banner,
    ArtistCreations,
    ArtistQuotes,
    Join,
    Footer
  }
};
</script>
