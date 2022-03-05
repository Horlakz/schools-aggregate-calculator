<script lang="ts">
  import logo from './assets/svelte.png'

  import Router from './routes/index.svelte'
</script>

<svelte:head>
 <link rel="icon" href={logo}>

 <title>Calculate Your Aggregate Score</title>
</svelte:head>

<Router />

