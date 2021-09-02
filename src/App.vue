<template>
  <div id="app">
    <div id="nav" class="navigatore">
      <div class="container-nav">
        <div class="logo">
          <img src="@/assets/logo.png" alt="logo instagram">
        </div>
        <Search></Search>
        <nav>
          <ul>
            <li><i class="fas fa-home"></i></li>
            <li><i class="far fa-paper-plane"></i></li>
            <li><i class="far fa-compass"></i></li>
            <li><i class="far fa-heart"></i></li>
            <li><img src="@/assets/profile.jpg" alt="foto profilo"></li>
          </ul>
        </nav>
      </div>
    </div>
    <main>

    </main>
  </div>
</template>

<script>
import Search from "@/components/Search.vue"

export default {
  name: 'app',
  data() {
    return {
    }
  },
  components : {
    Search
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
  .navigatore {
    width: 100%;
    border-bottom: 1px solid rgba(var(--b6a,219,219,219),1);
    display: flex;
    justify-content: center;

    .container-nav {
      width: 60%;
      height: 54px;
      display: flex;
      justify-content: space-between;
      align-items: center;


      .logo {
        margin-left: 10px;
        height: 65%;
        width: 120px;
        img {
          height: 100%;
        }
      }

      nav {
        margin-right: 10px;
        ul {
          list-style: none;
          display: flex;
          align-items: center;
          li {
            padding: 3px;
            margin: 0 5px;
            i {
              font-size: 22px;
              cursor: pointer;
            }
            img {
              width: 25px;
              border-radius: 50%;
            }
          }
        }
      }
    }
  }

  main {
    background: rgba(var(--b3f,250,250,250),1);
    height: calc(100vh - 55px);
  }
</style>


