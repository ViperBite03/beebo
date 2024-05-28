<script lang="ts">
  import BboButton from '../essentials/BboButton.svelte'
</script>

<style lang="scss">
  .container {
    height: 100dvh;
    position: relative;

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 35px;

    h1 {
      font-size: 40px;
      font-weight: 600;
      position: relative;

      img {
        position: absolute;
        bottom: 0;
        right: 5px;
        width: 150px;
        z-index: -1;
      }
    }

    h2 {
      max-width: 750px;
      font-size: 20px;
      text-align: justify;
    }
  }
</style>

<div class="g-wrapper container">
  <h1>Who is Beebo? <img src="/assets/underline.png" alt="" /></h1>

  <h2>
    Beebo is a web coder that is always up to date on the crypto world. He loves a good meme coin but likes even more being the first in
    line, helping people have the best look of all solana.
  </h2>

  <BboButton label="Click to see Beebo's work!" />
</div>
