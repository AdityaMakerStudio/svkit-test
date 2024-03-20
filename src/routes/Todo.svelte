<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';

	interface Todo {
		text: string;
		completed: boolean;
	}

	let todos: Todo[] = [];
	let newTodo = '';

	function addTodo() {
		if (newTodo.trim() !== '') {
			todos = [...todos, { text: newTodo, completed: false }];
			newTodo = '';
		}
	}

	function toggleTodo(index: number) {
		todos = todos.map((todo, i) => {
			if (i === index) {
				return { ...todo, completed: !todo.completed };
			}
			return todo;
		});
	}

	function deleteTodo(index: number) {
		todos = todos.filter((_, i) => i !== index);
	}
</script>

<main>
	<h1 class="mb-2 text-xl font-semibold">Todo App</h1>
	<div>
		<input
			bind:value={newTodo}
			on:keydown={(e) => e.key === 'Enter' && addTodo()}
			placeholder="Add a new todo"
			class="rounded-md border-2 border-slate-400 p-2"
		/>
		<Button variant="default" class="bg-green-500 hover:bg-green-700" on:click={addTodo}
			>Add Todo</Button
		>
	</div>
	<ul class="my-2 rounded-md bg-green-200 px-1">
		{#each todos as todo, index (index)}
			<li class:completed={todo.completed}>
				<input type="checkbox" checked={todo.completed} on:change={() => toggleTodo(index)} />
				<span>{todo.text}</span>
				<Button
					variant="secondary"
					size="default"
					class="bg-red-500 hover:bg-red-700 "
					on:click={() => deleteTodo(index)}>Delete</Button
				>
			</li>
		{/each}
	</ul>
</main>

<style>
	.completed {
		text-decoration: line-through;
		color: #aaa;
	}
</style>
