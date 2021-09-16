<template>
  <div id="app">
      <Nav></Nav>
      <main>
        <div class="content-main">
          <Main-Left>
            <Main-left-top>
              
            </Main-left-top>
          </Main-Left>
          <Main-Right>

          </Main-Right>
        </div>
      </main>
      <SkeletonLoader></SkeletonLoader>
  </div>
</template>

<script>
import Nav from './components/Nav.vue'
import MainLeft from './components/MainLeft.vue'
import MainRight from './components/MainRight.vue'
import SkeletonLoader from './components/SkeletonLoader.vue'


export default {
  name: 'app',
  data() {
    return {
    }
  },
  components : {
    Nav,
    MainLeft,
    MainRight,
    SkeletonLoader
  },


}
</script>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;

    font-family: 'Roboto', sans-serif;
  }

#app {
  position: relative;
}
// MAIN

  main {
    background: rgba(var(--b3f,250,250,250),1);
    height: 100vh;
    width: 100%;
    display: flex;
    justify-content: center;
    overflow: hidden;
    overflow-y: auto;
    position: relative;
    .content-main {
      width: 60%;
      display: flex;
    }
  }
  
</style>


