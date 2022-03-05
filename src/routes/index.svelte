<script>
  // Route function import
  import { Router, Route } from "svelte-routing";

  // pages
  import Error from "../pages/Error.svelte";
  import Index from "../pages/Index.svelte";
  import Unilag from "../pages/schools/Unilag.svelte";
  import YabaTech from "../pages/schools/YabaTech.svelte";

  export let url = "";
</script>

<Router {url}>
  <!-- Error Page -->
  <Route path="*" component={Error} />

  <!-- Home Page -->
  <Route path="/" component={Index} />

  <!-- Schools Calculator Pages  -->
  <Route path="/unilag" component={Unilag} />
  <Route path="/yabatech" component={YabaTech} />
</Router>
