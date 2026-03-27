<script lang="ts">
  import { T } from "@threlte/core";
  import Pseudocode from "./components/Pseudocode.svelte";
  import ControlPanel from "./components/ControlPanel.svelte";
  import type { Point } from "./objects/Point";
  import Canvas from "./components/Canvas.svelte";

  const points: Point[] = [];
</script>

<Canvas {points}></Canvas>
<ControlPanel {points}></ControlPanel>
<Pseudocode></Pseudocode>
