<template>
  <div class="textTag">
    <div class="textTag__inner" v-for="(item, index) in data" :key="index">
      <h2>{{ item.title }}</h2>
      <div class="textTag__block">
        <span v-for="(icon, index) in item.details" :key="index + 'i'" class="textTag__display">
          <span>
            <v-icon v-if="icon.icon" :name="index" :class="icon.icon" />
            <h5>{{ icon.iconTitle }}</h5>
          </span>

          <span v-if="!icon.icon?.split(' ').includes('last-tag')" class="textTag__dots">
            <v-icon class="fa-solid fa-circle dots"></v-icon>
          </span>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TextTag',
  props: {
    data: Array
  },
  data() {
    return {
    }
  }
}
</script>

<style lang="scss">
.textTag {
  margin: 10px;

  .textTag__inner {
    border-bottom: 1px solid rgb(204, 204, 204);
    text-align: left;

    .textTag__block {
      display: flex;
      margin: 10px 0;
    }

    .textTag__block span {
      display: flex;
    }

    .textTag__block h5 {
      margin: 0 5px;
      color: rgb(90, 90, 90);
      font-weight: 400;
    }

    .textTag__display {
      display: flex;
      align-items: center;
      justify-content: space-around;
      width: 100%;

      .icon-tag {
        font-size: 14px;
      }
    }

    .textTag__dots {
      margin: 0 10px;

      .dots {
        font-size: 6px;
      }
    }
  }

  .textTag__inner h2 {
    font-size: 18px;
    margin: 13px 0;
  }

  .textTag__inner:hover {
    color: rgb(228, 148, 0);
  }
}
</style>
