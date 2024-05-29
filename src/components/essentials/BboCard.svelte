<script lang="ts"></script>

<style lang="scss">
  .card {
    border-top: 3px solid var(--dark);
    border-left: 3px solid var(--dark);
    border-radius: 8px;

    min-height: 100px;
    min-width: 75px;

    width: fit-content;
    height: fit-content;

    box-shadow: 3px 3px 0px 3px var(--dark);
  }
</style>

<div class="card">
  <slot />
</div>
