<template>
  <header>
    <div class="link">
      <nuxt-link v-scroll-to="'#top'" to>
        Top
      </nuxt-link>
      <nuxt-link v-scroll-to="'#about'" to>
        About
      </nuxt-link>
      <nuxt-link v-scroll-to="'#skills'" to>
        Skills
      </nuxt-link>
      <div class="clear" />
    </div>
  </header>
</template>

<script>
export default {
  name: 'MyHeader',
}
</script>

<style>

header {
  width: 100%;
  text-align: center;
  background-color: white;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.2);
  position: fixed;
  top: 0;
  z-index: 10;
}

a {
  height: 50px;
  line-height: 50px;
  transition: all 0.3s;
  cursor: pointer;
  font-size: 18px;
  color: #343434;
  text-decoration: none;
  width: 150px;
  display: inline-block;

  &:hover {
    background-color: darken(white, 5%);
  }

  &:link {
    color: #343434;
  }
}

.clear {
  clear: left;
}
/* タブレット */
@media (max-width: 1250px) {
  a {
    width: 30%;
    height: 60px;
    line-height: 60px;
  }
}

/* スマートフォン */
@media (max-width: 670px) {
  a {
    width: 40%;
    height: 35px;
    line-height: 35px;
  }
}
</style>