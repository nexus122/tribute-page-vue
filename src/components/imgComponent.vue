<template>
  <div id="img-div">
    <figure>
      <img :src="imgUrl" :alt="caption" id="image"/>
      <figcaption id="img-caption">{{ caption }}</figcaption>
    </figure>
  </div>
</template>

<script>
export default {
  name: "imgComponent",
  props: ["name", "imgUrl", "caption"],
};
</script>

<style scoped>
figcaption {
  background-color: #222;
  color: #fff;
  font: italic smaller sans-serif;
  padding: 3px;
  text-align: center;
}
figure {
  width: 100%;
}

figure img {
  width: 100%;
}
</style>