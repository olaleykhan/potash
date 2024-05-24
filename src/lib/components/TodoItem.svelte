<script lang="ts" >
    export let todo;
  import { createEventDispatcher, afterUpdate } from 'svelte';

  
  const dispatch = createEventDispatcher();

  function handleDelete(id:string){
    //   console.log("I am being deleted.... id: ", id)
      dispatch('delete', {id})
    }

    afterUpdate(() => {
        console.log("I am being updated.... awnnn")
    })
</script>

<li>
    <input type="checkbox" bind:checked={todo.completed}>
    <span>{todo.text}</span>
    <button on:click={() => handleDelete(todo.id) }>{todo.completed? "Delete": "Remove"}</button>
</li>