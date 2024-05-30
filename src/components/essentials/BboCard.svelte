<script lang="ts">
  export let pair: number = 0
  export let title: string = 'Title'

  const blobs = [
    {
      id: 0,

      color1: 'var(--neonGreen)',
      path1: '20% 0%, 90% 15%, 100% 80%, 65% 100%, 15% 85%, 0 40%',
      top1: '-40',
      left1: '-20',

      color2: 'var(--lilac)',
      path2: '20% 0%, 90% 15%, 100% 80%, 65% 100%, 15% 85%, 0 40%',
      top2: '25',
      left2: '55',
    },
    {
      id: 1,

      color1: 'var(--coral)',
      path1: '10% 15%, 70% 15%, 100% 55%, 65% 100%, 0 70%',
      top1: '10',
      left1: '-25',

      color2: 'var(--bbyBlue)',
      path2: '51% 0, 95% 8%, 94% 96%, 63% 84%, 56% 56%, 25% 51%, 18% 19%',
      top2: '-30',
      left2: '35',
    },
    {
      id: 2,

      color1: 'var(--coral)',
      path1: '20% 0%, 90% 15%, 100% 80%, 65% 100%, 15% 85%, 0 40%',
      top1: '10',
      left1: '-10',

      color2: 'var(--neonGreen)',
      path2: '50% 0, 100% 15%, 90% 80%, 25% 100%, 0 50%',
      top2: '-40',
      left2: '30',
    },
    {
      id: 3,

      color1: 'var(--bbyBlue)',
      path1: '51% 0, 96% 26%, 85% 88%, 34% 90%, 9% 62%, 18% 19%',
      top1: '5',
      left1: '-20',

      color2: 'var(--lilac)',
      path2: '10% 15%, 70% 15%, 100% 55%, 65% 100%, 0 70%',
      top2: '-40',
      left2: '35',
    },
  ]
</script>

<style lang="scss">
  .card {
    border-radius: 8px;
    border-top: 3px solid var(--dark);
    border-left: 3px solid var(--dark);
    box-shadow: 3px 3px 0px 3px var(--dark);

    position: relative;
    overflow: hidden;

    min-height: 125px;
    min-width: 150px;

    width: fit-content;
    height: fit-content;
    padding: 10px 15px;

    display: flex;
    flex-direction: column;
    align-items: center;

    .title {
      font-weight: bolder;
      z-index: 1;
    }

    .blobs {
      height: 100%;
      width: 100%;
      position: absolute;

      .blob {
        filter: url(#round);

        .path {
          position: absolute;
          height: 125px;
          width: 125px;
        }
      }
    }
  }
</style>

<div class="card">
  <span class="title">{title}</span>

  <div class="blobs">
    <div class="blob">
      <div
        class="path"
        style="background-color: {blobs[pair].color1}; clip-path: polygon({blobs[pair].path1}); top: {blobs[pair].top1}px; left: {blobs[
          pair
        ].left1}px;"
      ></div>
    </div>

    <div class="blob">
      <div
        class="path"
        style="background-color: {blobs[pair].color2}; clip-path: polygon({blobs[pair].path2}); top: {blobs[pair].top2}px; left: {blobs[
          pair
        ].left2}px;"
      ></div>
    </div>

    <svg style="visibility: hidden; position: absolute;" width="0" height="0" xmlns="http://www.w3.org/2000/svg" version="1.1">
      <defs>
        <filter id="round">
          <feGaussianBlur in="SourceGraphic" stdDeviation="12" result="blur" />
          <feColorMatrix in="blur" mode="matrix" values="1 0 0 0 0  0 1 0 0 0  0 0 1 0 0  0 0 0 19 -9" result="goo" />
          <feComposite in="SourceGraphic" in2="goo" operator="atop" />
        </filter>
      </defs>
    </svg>
  </div>
</div>
