<script>
    export let todo;
    // export let dispatch;
</script>

<li>
    <input type="checkbox" bind:checked={todo.completed}>
    <span>{todo.text}</span>
    <button on:click={() => {
        // dispatch('delete', todo.id)
        console.log("I am being clicked to delete todo.... awnnn")
    }}>{todo.completed? "Delete": "Remove"}</button>
</li>