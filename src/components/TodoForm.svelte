<script>
	import { addTodo } from '../stores/todoStore';
	let todo = '';
	const handleSubmit = () => {
		addTodo(todo);
		todo = '';
	};
</script>

<form on:submit|preventDefault={handleSubmit} class="my-6">
	<div class="flex flex-col text-sm mb-2">
		<label for="todo" class="font-bold mb-2">
			<input
				type="text"
				bind:value={todo}
				name="todo"
				placeholder="Wattacha gotta do?"
				class="w-full appearance-none shadow-sm border border-gray-200 p-2 foucs:outline-none foucus:border-gray-500 rounded-lg"
			/>
		</label>
	</div>
	<button
		type="submit"
		class="w-full shadow-sm bg-blue-500 hover:bg-blue-600 text-white py-2 px-4 rounded-lg"
		>보내기</button
	>
</form>
