<link rel="stylesheet" href="node_modules/svelte-material-ui/bare.css" />
<script lang="ts">
    import LayoutGrid, {Cell} from '@smui/layout-grid';
    import Textfield from '@smui/textfield';
    import Button from '@smui/button';
    import Tab, {Icon} from '@smui/tab';
    import TabBar from '@smui/tab-bar';
    import {Label} from '@smui/common';
    import { goto } from '$app/navigation';

    let tabs = [{
                  label: 'Home'
                }, 
                {
                  label: 'Practice Email'
                }, 
                {
                  label:'Practice Live Chat'
                }, 
                {
                  label:'Practice Forum Moderation'
                }];
    let active = tabs[0];
  </script>
    <img style='width:200px' src="images/turning_point_logo.png" alt='Error in displaying Logo'/>
  
<div>
    <!-- Note: tabs must be unique. (They cannot === each other.) -->
    <TabBar {tabs} let:tab bind:active>
      <Tab {tab} on:click={() => goto("/SignupPage")}>
        <Label>{tab.label}</Label>
      </Tab>
    </TabBar>
</div>  
