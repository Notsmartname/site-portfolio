<template>
  <div class="line">
  </div>
</template>

<script setup>

</script>

<style>
.line {
  position: relative;
  left: 470px;
  width: 1px;
  min-height: 100%;
  background: rgba(238, 238, 238, 0.10);
  z-index: -999;
}

.line::after {
  position: absolute;
  content: '';
  background: url(/images/elem-line.svg);
  top: 864px;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 96px;
  height: 96px;
  fill: rgba(57, 62, 70, 0.75);
  backdrop-filter: blur(4px);
}
</style>