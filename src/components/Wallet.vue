<template>
  <span class="navbar-text">
      Wallet: ${{walletAmount}}
    </span>
</template>

<script>

export default {
    props: {
        walletAmount: Number,
    }
}
</script>

<style>

</style>