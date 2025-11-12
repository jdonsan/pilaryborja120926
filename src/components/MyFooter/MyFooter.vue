<template>
  <footer class="my-footer">
    <p>Desarrollado con <span class="heart">🧡</span> por jdonsan</p>
  </footer>
</template>

<script>
export default {
  name: 'MyFooter'
}
</script>

<style lang="scss" scoped>
.my-footer {
  background-color: $color-1;
  text-align: center;
  padding: 48px 0;

  p {
    font-family: $font-2;
    color: $color-5;
    margin: 0;
    font-size: 14px;
  }

  .heart {
    animation: beat 1s infinite;
    display: inline-block;
    margin: 0 4px;
  }
}

@keyframes beat {
  0%,
  100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
}
</style>
