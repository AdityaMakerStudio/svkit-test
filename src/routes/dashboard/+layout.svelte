<script>
   import Sidebar from "$lib/components/Sidebar.svelte";
   import Button from "$lib/components/ui/button/button.svelte";
</script>
  
  <div class="container">
    <Sidebar />
  
    <main>
      <Button variant="default" class="bg-green-500"  >
        Click me 
      </Button>
      <slot />
    </main>
  </div>
  
  <style>
    .container {
      display: flex;
      height: 100%;
      margin: auto;
      justify-content: center;
      align-items: center;
      width: 30rem;
      margin-top: 2rem;
    }
  
    main {
      flex-grow: 1;
      padding: 20px;
    }
  </style>