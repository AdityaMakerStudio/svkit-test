<script lang="ts">
  import type { Hst } from '@histoire/plugin-svelte'
  
  import Button from './button.svelte'

  export let Hst: Hst

  let content = 'Click me!'
</script>
  
<Hst.Story>
  <Hst.Variant  title="default">
    <Button>
    {content}
    </Button>
   
    <svelte:fragment slot="controls">
      <!-- Put controls here -->
    </svelte:fragment>
  </Hst.Variant>
</Hst.Story>
