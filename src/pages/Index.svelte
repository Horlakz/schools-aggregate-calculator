<script lang="ts">
  // Svelte imports
  import { Link } from "svelte-routing";

  // imports
  import BaseLayout from "../lib/layouts/BaseLayout.svelte";
</script>

<BaseLayout>
  <h2>list of schools</h2>
  <ul>
    <li><Link to="/unilag">University Of Lagos(UNILAG)</Link></li>
    <li><Link to="/yabatech">Yaba College of Education(YABATECH)</Link></li>
  </ul>
</BaseLayout>

<style>
</style>
