<style>
  .wrapper {
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    display: grid;
    justify-items: center;
    align-items: center;
    background: black;
  }
</style>
<script>
  import { Animated, PixelMap } from 'svelte-animated-pixels';
  const FRAMES = [
    `
    . x . . . . . x .
    . . x . . . x . .
    . . x x x x x . .
    . x x x x x x x .
    . x x x x x x x .
    . . x x x x x . .
    . x . . . . . x .
    . . x . . . x . .
    `,
    `
    . . . x . x . . .
    . . x . . . x . .
    . . x x x x x . .
    . x x x x x x x .
    . x x x x x x x .
    . . x x x x x . .
    . . x x . x x . .
    . . . . . . . . .
    `
  ];
</script>

<div class="wrapper">
  <Animated frames={FRAMES} let:using={{ map }}>
    <PixelMap scale={5} {map} />
  </Animated>
</div>