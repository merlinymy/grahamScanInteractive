<script lang="ts">
  import { Canvas } from "@threlte/core";
  import Scene from "../canvas/Scene.svelte";

  const points = $props();
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
  }
</style>
