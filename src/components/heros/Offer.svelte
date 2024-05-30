<script lang="ts">
  import BboCard from '../essentials/BboCard.svelte'
</script>

<style lang="scss">
  .container {
    height: 50vh;

    display: flex;
    justify-content: center;
    align-items: center;
    gap: 50px;
  }
</style>

<div class="container">
  <BboCard pair={0} title="Animations" />

  <BboCard pair={1} title="Value chart" />

  <BboCard pair={2} title="3D" />

  <BboCard pair={3} title="Audio / music" />
</div>
