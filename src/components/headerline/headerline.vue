<template>
  <div class="c-headerline">
    <div class="x-container">
      <div class="headerline">
        <slot name="headerline" />
      </div>
      <div class="content"  v-if="$slots.content">
        <slot name="content" />
      </div>
    </div>
  </div>
</template>

<style lang='scss' src='./headerline.scss' scoped>

</style>