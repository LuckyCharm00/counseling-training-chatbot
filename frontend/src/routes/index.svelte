<script>
  import {Router, Route} from 'svelte-routing';
  import LoginPage from './LoginPage.svelte';

</script>

<Router>
  <Route path="/"> <LoginPage/> </Route>
</Router>