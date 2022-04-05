
<link rel="stylesheet" href="node_modules/svelte-material-ui/bare.css" />

<script lang="ts">
  import LayoutGrid, {Cell} from '@smui/layout-grid';
  import Textfield from '@smui/textfield';
  import Button from '@smui/button';
  import {Label} from '@smui/common';
  import { goto } from '$app/navigation';
 
  let firstName:string = '';
  let lastName:string = '';
  let emailAddress:string = '';
  let password:string = '';
  let confirmPassword:string = '';

</script>

<!-- Components can be extracted and code better designed later - Linton -->
<LayoutGrid>
    <Cell align="middle" span={4}>
      <div class="padding-cell"></div>
    </Cell>
    <Cell align="middle" span={6}>
      <div class="content-cell">
        <div style="padding-bottom: 50px">
          <img style='width:400px' src="images/turning_point_logo.png" alt='Error in displaying Logo'/>
        </div>
        <div style="padding-bottom: 20px">
        <Label style="font-size: 22px">Sign Up Page</Label>
        </div>
        <div style="padding-bottom: 25px">
          <Textfield
            class="shaped-outlined"
            variant="outlined"
            style='min-width: 400px'
            label="First Name*"
            bind:value={firstName}
          >
          </Textfield>
        </div>

        <div style="padding-bottom: 25px">
          <Textfield
            class="shaped-outlined"
            variant="outlined"
            style='min-width: 400px'
            label="Last Name*"
            bind:value={lastName}
          >
          </Textfield>
        </div>

        <div style="padding-bottom: 25px">
          <Textfield
            class="shaped-outlined"
            variant="outlined"
            style='min-width: 400px'
            label="Email Address*"
            bind:value={emailAddress}
          >
          </Textfield>
        </div>

        <div style="padding-bottom: 25px">
          <Textfield
            class="shaped-outlined"
            variant="outlined"
            style='min-width: 400px'
            label="Enter Password*"
            type='password'
            bind:value={password}
          >
          </Textfield>
        </div>

        <div style="padding-bottom: 25px">
          <Textfield
            class="shaped-outlined"
            variant="outlined"
            style='min-width: 400px'
            label="Confirm Password*"
            type='password'
            bind:value={confirmPassword}
          >
          </Textfield>
        </div>
        <Button on:click={() => goto("/HomePage")} variant="raised" style="display:block">
          <Label>GET STARTED</Label>
        </Button>
      </div>
    </Cell>
    <Cell align="middle" span={4}>
      <div class="padding-cell"></div>
    </Cell>
</LayoutGrid>