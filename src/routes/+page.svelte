<script>
	import Button from '$lib/components/ui/button/button.svelte';
	import Todo from './Todo.svelte';
</script>

<div class="mt-2 flex flex-col items-center justify-center">
	<Todo />
	<!-- <Button variant="default" class="bg-green-500">Click me</Button> -->
	<div>
		<a href="/dashboard"> Dashboard </a>
		<a href="/tables"> Tables </a>
	</div>
</div>
