<script lang="ts">
  import { onMount } from 'svelte'
  import BboButton from '../essentials/BboButton.svelte'
  import Hero from './Hero.svelte'

  let isVisible: boolean = false
</script>

<style lang="scss">
  .container {
    width: 100%;
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

    .hero {
      width: 100%;
      display: none;

      &.active {
        display: block;
      }
    }
  }
</style>

<div class=" container">
  <h1>Who is Beebo? <img src="/assets/underline.png" alt="" /></h1>

  <h2>
    Beebo is a web coder that is always up to date on the crypto world. He loves a good meme coin but likes even more being the first in
    line, helping people have the best look of all solana.
  </h2>

  <BboButton
    label="Click to see Beebo's work!"
    click={() => {
      isVisible = !isVisible
    }}
  />

  <div class="hero" class:active={isVisible}>
    <Hero />
  </div>
</div>
