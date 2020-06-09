<template>
  <div class="Home">
    <Header />
    <Banner />
    <Features />
    <ArtistCreations />
    <ArtistQuotes />
    <Join />
    <Footer />
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
    msg: String
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
