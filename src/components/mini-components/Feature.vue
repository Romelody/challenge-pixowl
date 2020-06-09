<template>
  <div id="feature">
    <div class="text-component">
      <h3>
        <strong>{{ titleFeature }}Modeler</strong>
      </h3>
      <p>
        {{ textFeature }}Make the most of your creativity! From beginners to
        experts, anyone can make amazing creations thanks to our robust set of
        tools and our user-friendly interface.
      </p>
    </div>
  </div>
</template>
<style lang="scss" scoped>
#feature {
  background-image: url(../../assets/img/feature-01.png);
  background-repeat: no-repeat;
  background-size: 400px 410px;
  width: 400px;
  height: 410px;
  .text-component {
    padding: 40px;
    color: $white;
    h3 {
      font-weight: 500;
      text-align: center;
      margin-bottom: 15px;
      strong {
      }
    }
    p {
      text-align: center;
      letter-spacing: 0px;
    }
  }
}
</style>
