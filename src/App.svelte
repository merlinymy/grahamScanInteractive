<script lang="ts">
  import { T } from "@threlte/core";
  import Pseudocode from "./components/Pseudocode.svelte";
  import ControlPanel from "./components/ControlPanel.svelte";
  import type { Point } from "./objects/Point";
  import Canvas from "./components/Canvas.svelte";

  let points: Point[] = [];
</script>

<div class="appWrap">
  <Canvas {points}></Canvas>
  <div class="controls">
    <ControlPanel bind:points></ControlPanel>
    <Pseudocode></Pseudocode>
  </div>
</div>

<style>
  .appWrap {
    display: flex;
  }
  .controls {
    padding: 1rem;
    flex: 1 1 0;
  }
</style>
