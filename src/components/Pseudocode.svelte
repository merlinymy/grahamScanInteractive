<script lang="ts"></script>

<div class="pseudocode">
  <ol>
    <li>
      <p>
        let p<sub>0</sub> be the point in <b>Q</b> with the minimum y-coordinate,
        or the left-most such point in case of a tie
      </p>
    </li>
    <li>
      <p>
        let [p<sub>1</sub>, p<sub>2</sub>, ..., p<sub>m</sub>] be the remaining
        points in <b>Q</b>, sorted by polar angle in counterclockwise order
        around p<sub>0</sub> (if more than one point has the same angle, remove
        all but the one that is farthest from p<sub>0</sub>)
      </p>
    </li>
    <li>
      <p><b>if</b> m {"<"} 2</p>
    </li>
    <li>
      <p class="indented"><b>return</b> "convex hull is empty"</p>
    </li>
    <li><p><b>else</b> let <b>S</b> be an empty stack</p></li>
    <li>
      <p class="indented">
        <b>S</b>.push(p<sub>0</sub>, p<sub>1</sub>, p<sub>2</sub>)
      </p>
    </li>
    <li><b>for</b> i = 3 <b>to</b> m</li>
    <li>
      <p class="indented">
        <b>while</b> the angle formed by the last point in stack, the second to
        last point in stack, and p<sub>i</sub> makes a nonleft turn
      </p>
    </li>
    <li><p class="double-indented"><b>S</b>.pop()</p></li>
    <li>
      <p class="indented"><b>S</b>.push(p<sub>i</sub>)</p>
    </li>
    <li><p class="indented"><b>return S</b></p></li>
  </ol>
</div>

<style>
  .indented {
    margin-left: 1rem;
  }
  .double-indented {
    margin-left: 2rem;
  }
</style>
