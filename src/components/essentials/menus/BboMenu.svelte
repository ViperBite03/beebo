<script lang="ts">
  import BboButton from '../BboButton.svelte'

  let options: string[] = ['Inicio', 'Info', 'Precios', 'Contacto']
</script>

<style lang="scss">
  .menu-container {
    height: fit-content;
    width: 100%;

    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 15px;

    .logo {
      height: 75px;
    }

    .options {
      height: 100%;
      width: fit-content;

      display: flex;
      align-items: center;

      gap: 3px;
    }
  }
</style>

<div class="menu-container">
  <img class="logo" src="/assets/beebo.png" alt="" />

  <div class="options">
    {#each options as option}
      <BboButton label={option} />
    {/each}
  </div>
</div>
