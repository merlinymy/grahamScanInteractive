<script lang="ts">
  import { Canvas } from "@threlte/core";
  import Scene from "../canvas/Scene.svelte";

  let { points } = $props();
  $inspect(points);
</script>

<div class="canvasWrapper">
  <Canvas>
    <Scene {points}></Scene>
  </Canvas>
</div>

<style>
  .canvasWrapper {
    width: 100%;
    background-color: black;
    flex: 2 1 0;
  }
</style>
