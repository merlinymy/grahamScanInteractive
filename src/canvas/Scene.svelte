<script lang="ts">
  import { T } from "@threlte/core";
  import { OrbitControls } from "@threlte/extras";
  import { Point } from "../objects/Point";
  import PointSphere from "./PointSphere.svelte";

  let { points } = $props();
</script>

<T.PerspectiveCamera makeDefault position={[5, 5, 5]}>
  <OrbitControls></OrbitControls>
</T.PerspectiveCamera>
{#each points as point}
  <PointSphere position={{ x: point.x, y: point.y }}></PointSphere>
{/each}
<T.GridHelper></T.GridHelper>
<T.AxesHelper></T.AxesHelper>
