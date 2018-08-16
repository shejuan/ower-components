<template>
  <div class="sj-loading-wrapper">
    <div class="sj-cssload-container" 
      :style="{
        height: diam + size * 2 + 'px'
      }">
      <div class="sj-cssload-speeding-wheel"
        :style="{
          width: `${diam}px`,
          height: `${diam}px`,
          border: `${size}px solid ${color}`,
          'border-left-color': 'transparent',
          'border-right-color': 'transparent'
        }"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'loading',
  props: {
    color: {
      type: String,
      default: '#2a8ee3'
    },
    diam: {
      type: Number,
      default: 50
    },
    size: {
      type: Number,
      default: 3
    }
  }
};
</script>

<style lang="less" rel="stylesheet/less"  scoped>
.sj-cssload-container {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  width: 100%;
  margin: auto;
  text-align: center;
}

.sj-cssload-speeding-wheel {
  margin: 0 auto;
  border-radius: 50%;
  animation: cssload-spin 575ms infinite linear;
}

@keyframes cssload-spin {
  100% {
    transform: rotate(360deg);
  }
}
</style>