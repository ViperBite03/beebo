<script lang="ts">
  import BboButton from '../BboButton.svelte'

  let options: string[] = ['Inicio', 'Info', 'Precios', 'Contacto']
</script>

<style lang="scss">
  .menu-container {
    position: fixed;
    width: 100%;
    z-index: 99;

    .g-wrapper {
      height: fit-content;
      width: 100%;

      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-top: 20px;

      .logo {
        height: 50px;
      }

      .options {
        height: 100%;
        width: fit-content;

        display: flex;
        align-items: center;

        gap: 3px;
      }
    }
  }
</style>

<div class="menu-container">
  <div class="g-wrapper">
    <img class="logo" src="/assets/beebo.png" alt="" />

    <div class="options">
      {#each options as option}
        <BboButton label={option} />
      {/each}
    </div>
  </div>
</div>
