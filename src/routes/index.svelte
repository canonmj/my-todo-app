<script>
	import TodoForm from '../components/TodoForm.svelte';
	import Todo from '../components/Todo.svelte';
	import { todos } from '../stores/todoStore';
</script>

<main>
	<h1 class="mt-12 text-2xl font-bold text-center text-black">My Todos</h1>
	<TodoForm />
	{#each $todos as todo}
		<Todo {todo} />
	{/each}
</main>
