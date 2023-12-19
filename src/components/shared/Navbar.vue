<template>
  <nav class="nav">
    <div class="nav__upper">
      <div class="d-flex align-center ga-2">
        <img
          style="transform: rotate(45deg)"
          src="../../assets/icons/diamond-ring.svg"
          alt=""
          width="20"
        />
        <p class="text-18 letter-spacing-9">SHOP WEDDINGS</p>
      </div>
      <div class="nav__upper__logo">
        <img src="../../assets/logo.png" alt="logo" />
      </div>
      <div class="d-flex align-center">
        <div class="search">
          <v-form @submit.prevent class="d-flex align-center">
            <v-text-field
              placeholder="search"
              variant="underlined"
              style="width: 150px"
              class="text-11"
            ></v-text-field>
            <v-btn type="submit" variant="plain" :slim="true" min-width="20">
              <img src="../../assets/icons/search.svg" width="20" />
            </v-btn>
          </v-form>
        </div>
        <div class="country px-3 mx-1 cursor-pointer">
          <img src="../../assets/icons/bd.png" width="24" alt="" />
        </div>
        <div class="profile px-3 mx-1 cursor-pointer">
          <img src="../../assets/icons/profile.svg" width="20" alt="" />
        </div>
        <div class="bookmark px-3 mx-1 cursor-pointer">
          <img src="../../assets/icons/bookmark.svg" width="20" alt="" />
        </div>
        <div class="shopping-bag pl-3 ml-1 cursor-pointer">
          <img src="../../assets/icons/shopping-bag.svg" alt="" width="24" />
          <div
            class="shopping-bag__counter rounded-circle bg-black d-flex align-center justify-center"
          >
            <p>0</p>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import flag from '../../assets/icons/bd.png'
export default {
  name: 'Navbar',
  data: function () {
    return {
      flag: flag
    }
  }
}
</script>

<style lang="scss" scoped>
.nav {
  border-bottom: 1px solid #eee;
  &__upper {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    height: 70px;
    padding: 0px 22px;
    //background-color: gray;

    &__logo {
      width: 105px;
      height: 40px;
      position: absolute;
      left: 50%;
      transform: translateX(-50%);

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }

    .shopping-bag {
      position: relative;
      &__counter {
        width: 15px;
        height: 15px;
        position: absolute;
        bottom: -12%;
        right: -12%;
        p {
          display: inline-block;
          font-size: 9px;
          line-height: 7px;
        }
      }
    }
  }
}
</style>
