<script lang="ts" setup>
defineProps({
  infoIcon: {
    type: String,
    required: true,
  },
  infoHeader: {
    type: String,
    required: true,
  },
  infoDescription: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="info-block-items-item">
    <div class="info-block-items-item-icon">
      <img :src="infoIcon" alt="" />
    </div>
    <div class="info-block-items-item-text">
      <div class="info-block-items-item-text-header">
        <h4>{{ infoHeader }}</h4>
      </div>
      <div class="info-block-items-item-text-description">
        <p>{{ infoDescription }}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "@/assets/styles/tovw.scss" as *;

.info-block-items-item {
  display: flex;
  align-items: center;
  border-right: 1px solid #b7b9be;
  padding: toVw(10px);
  &-icon {
    margin-right: toVw(30px);
    img {
      width: toVw(66px);
    }
  }
  &-text {
    &-header {
      font-size: toVw(21px);
      padding-bottom: toVw(13px);
      font-weight: 800;
    }
    &-description {
      font-size: toVw(17px);
      color: #b7b9be;
    }
  }
  &:last-child {
    border-right: none;
  }
}
</style>
