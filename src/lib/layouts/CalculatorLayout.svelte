<script>
  import BaseLayout from "./BaseLayout.svelte";
</script>

<BaseLayout>
  <!-- Page Heading -->
  <h2>Calculate your Aggregate Score</h2>
  <p>
    To see the requirements for your score,
    <a href="google.com" target="_blank">click here</a>
  </p>
  <form on:submit|preventDefault>
    <slot />

    <!-- Calculator Button -->
    <div>
      <button type="button"> Calculate </button>
    </div>

    <!-- Result Display -->
    <span>Your Aggregate Score is </span>
  </form>
</BaseLayout>

<style lang="scss">
  button {
    cursor: pointer;
  }
</style>
