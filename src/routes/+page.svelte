<script>
	import Button from '$lib/components/ui/button/button.svelte';
	import Todo from './Todo.svelte';
</script>

<h1 class="flex justify-center bg-green-500 py-4 text-3xl font-bold text-white">
	Welcome to Liveqeue
</h1>

<div class="mt-2 flex flex-col items-center justify-center">
	<Todo />
	<!-- <Button variant="default" class="bg-green-500">Click me</Button> -->
</div>
