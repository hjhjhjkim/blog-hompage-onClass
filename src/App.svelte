<script>
  import { Router, Route } from "svelte-routing";
  import Main from "./components/Main.svelte";
  import List from "./components/List.svelte";
  import Detail from "./components/Detail.svelte";
  import Write from "./components/Write.svelte";
</script>

<Router>
  <Route path="/" component={Main} />
  <Route path="/ex" component={Main} />
  <Route path="/list" component={List} />
  <Route path="/detail/:id" component={Detail} let:id />
  <Route path="/write" component={Write} />
</Router>
