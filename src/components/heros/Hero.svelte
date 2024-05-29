<script lang="ts"></script>

<style lang="scss">
  .container {
    height: fit-content;
    width: 100%;

    display: flex;
    flex-direction: column;
    align-items: center;

    .triangle {
      height: 35px;
      width: 35px;
      background-color: var(--coral);
      clip-path: polygon(50% 35%, 0% 100%, 100% 100%);
    }

    .page {
      width: 100%;
      height: 250px;
      padding: 50px 75px;
      background-color: var(--coral);
    }
  }
</style>

<div class="container">
  <div class="triangle" />
  <div class="page"></div>
</div>
