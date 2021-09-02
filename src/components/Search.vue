<template>
    <div  id="search" class="cont-search">
        <i class="fas fa-search"></i>
        Cerca
        <div class="cont-input" id="input-serch">
          <input type="text" class="search" placeholder=" Cerca">
          <i  class="fas fa-times-circle" id="close"></i>
        </div>
    </div>
</template>

<script>
export default {
    name: "search",
    data() {
        
        return {
        }
    },
    props : {


    }
};
</script>

<style lang="scss">
    .cont-search {
      position: relative;
      color: #a9a6a6;
      width: 200px;
      height: 50%;
      background: rgba(var(--b3f,250,250,250),1);
      border: solid 1px rgba(var(--b6a,219,219,219),1);
      border-radius: 2px;
      display: flex;
      justify-content: center;
      align-items: center;

      i {
        font-size: 12px;
      }
      .cont-input {
        visibility: inherit;
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        display: flex;
        align-items: center;

        input {
          height: 100%;
          width: 180px;
          border: none;
          background: rgba(var(--b3f,250,250,250),1);
          font-size: 16px;

          &:focus {
            outline:none;
          }
        }
        i {
          cursor: pointer;

        }
      }

    }
</style>