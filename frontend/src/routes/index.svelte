<script lang='ts'>
  import HomePage from './HomePage.svelte';
  import LoginPage from './LoginPage.svelte';

  let user = {loggedin: false}
</script>

<!-- Authentication checking should be implemented here - Linton -->
{#if user.loggedin}
<HomePage/>
{:else} 
<LoginPage/>
{/if}