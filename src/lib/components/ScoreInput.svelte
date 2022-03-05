<script lang="ts">
  export let exam: string = "Jamb";

  export let minValue: number = 180;
  export let maxValue: number = 400;
</script>

<div>
  <label for={exam}>{exam} Score</label>
  <input
    type="number"
    id={exam}
    min={minValue}
    max={maxValue}
    placeholder="Enter your {exam} Score"
    required
  />
</div>
