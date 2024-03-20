<script lang="ts">
  import type { Hst } from '@histoire/plugin-svelte'
  
  import alert-dialog-action from './alert-dialog-action.svelte'

  export let Hst: Hst
</script>
  
<Hst.Story>
  <Hst.Variant title="Default">
    <alert-dialog-action />

    <svelte:fragment slot="controls">
      <!-- Put controls here -->
    </svelte:fragment>
  </Hst.Variant>
</Hst.Story>
