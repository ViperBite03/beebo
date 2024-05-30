<script lang="ts">
  import BboButton from '@/components/essentials/BboButton.svelte'
</script>

<style lang="scss">
  .hero {
    height: 100dvh;
    padding: 50px 0;
    position: relative;

    display: flex;
    align-items: center;

    h1 {
      font-weight: bolder;
      max-width: 400px;
      font-size: 40px;
      padding-bottom: 50px;
    }
  }
</style>

<div class="g-wrapper hero">
  <div class="text">
    <h1>Beebo is here to help you and your project take off amongst other meme coins.</h1>
    <BboButton label="How Beebo works" />
  </div>
</div>
