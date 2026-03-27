<script lang="ts">
  import Button from "./Button.svelte";
  import { Point } from "../objects/Point";

  let pointsCount = $state(10);
  let { points = $bindable() } = $props();

  function generateRandomPoints(numPoints: number) {
    points = []; // Clear the existing points
    for (let i = 0; i < numPoints; i++) {
      const x = Math.round(Math.random() * 10);
      const y = Math.round(Math.random() * 10);
      points.push(new Point(x, y));
    }
  }
  function generateCollinearPoints() {
    points.push();
  }
</script>

<div class="examples">
  <div class="randomPoints">
    <input type="number" bind:value={pointsCount} min="3" max="100" />
    {#if pointsCount < 3 || pointsCount > 100}
      <p>Please enter a number between 3 and 100.</p>
    {:else}
      <Button
        buttonName="Generate {pointsCount} random points"
        onclick={() => generateRandomPoints(pointsCount)}
      ></Button>
    {/if}
    <Button buttonName="Collinear Edgecase" onclick={generateCollinearPoints}
    ></Button>
    {#if points.length > 0}
      <p>Current Points: {points}</p>
    {/if}
  </div>
</div>
