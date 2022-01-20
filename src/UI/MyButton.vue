<template>
  <button class="btn">
      <slot></slot>
  </button>
</template>

<script>
export default {

}
</script>

<style>
    .btn {
        margin-top: 15px;
        padding: 10px 15px;
        background: teal;
        color: white;
        border: 2px solid teal;
    }
</style>