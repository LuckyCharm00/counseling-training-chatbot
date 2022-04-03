
<link rel="stylesheet" href="node_modules/svelte-material-ui/bare.css" />

<script lang="ts">
  import LayoutGrid, {Cell} from '@smui/layout-grid';
  import Textfield from '@smui/textfield';
  import Button from '@smui/button';
  import {Label} from '@smui/common';
  import { goto } from '$app/navigation';
 
  let username:string = '';
  let password:string = '';

</script>

<!-- Components can be extracted and code better designed later - Linton -->
<LayoutGrid>
    <Cell align="middle" span={4}>
      <div class="padding-cell"></div>
    </Cell>
    <Cell align="middle" span={6}>
      <div class="content-cell">
        <div style="padding-bottom: 50px; padding-top: 100px">
          <img style='width:400px' src="images/turning_point_logo.png" alt='Error in displaying Logo'/>
        </div>
        
        <div style="padding-bottom: 25px">
          <Textfield
            class="shaped-outlined"
            variant="outlined"
            style='min-width: 400px'
            label="Enter Username"
            bind:value={username}
          >
          </Textfield>
        </div>

        <div style="padding-bottom: 25px">
          <Textfield
            class="shaped-outlined"
            variant="outlined"
            style='min-width: 400px'
            label="Enter Password"
            type='password'
            bind:value={password}
          >
          </Textfield>
        </div>
        
        <Button on:click={() => goto("/HomePage")} variant="raised">
          <Label>Log In</Label>
        </Button>

        <Button on:click={() => goto("/SignupPage")} variant="raised">
          <Label>New to Turning Point? Sign Up</Label>
        </Button>

      </div>
    </Cell>
    <Cell align="middle" span={4}>
      <div class="padding-cell"></div>
    </Cell>
</LayoutGrid>