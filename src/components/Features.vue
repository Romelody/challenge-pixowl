<template>
  <div id="features">
    <div class="container padding-y">
      <div>
        <h2>VoxEdit features</h2>
        <div class="features-container">
          <Feature
            v-for="feature in features"
            :key="feature.id"
            :titleFeature="feature.titleFeature"
            :textFeature="feature.textFeature"
            :bgImage="feature.bgImage"
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Feature from "./mini-components/Feature";
import image1 from "@/assets/img/feature-01.png";
import image2 from "@/assets/img/feature-02.png";
import image3 from "@/assets/img/feature-03.png";
export default {
  components: {
    Feature
  },
  data() {
    return {
      features: [
        {
          id: 0,
          titleFeature: "Modeler",
          textFeature:
            "Make the most of your creativity! From beginners to experts, anyone can make amazing creations thanks to our robust set of tools and our user-friendly interface.",
          bgImage: image1
        },
        {
          id: 1,
          titleFeature: "Animator",
          textFeature:
            "A game changer in the voxel creation world. With our Skeleton System, VoxEdit allows you to rig and animate anything that you want using the timeline via an easy-to-use keyframing mode.",
          bgImage: image2
        },
        {
          id: 2,
          titleFeature: "Block Editor",
          textFeature:
            "Section to create the fundamental building blocks of the SandBox 3! Each block measures 32 voxels, there are Solid or Liquid blocks with inner properties.",
          bgImage: image3
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
#features {
  background: $medium-grey;
  .features-container {
    display: flex;
    justify-content: space-between;
  }
}
</style>
