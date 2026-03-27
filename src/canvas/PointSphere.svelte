<script lang="ts">
  import { T } from "@threlte/core";

  const { position } = $props();
</script>

<T.Mesh position={[position.x, 0, position.y]}>
  <T.SphereGeometry args={[0.15, 32, 32]}></T.SphereGeometry>
  <T.MeshBasicMaterial></T.MeshBasicMaterial>
</T.Mesh>
