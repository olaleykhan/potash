<script lang="ts" >
    export let todo;
  import { createEventDispatcher } from 'svelte';

  
  const dispatch = createEventDispatcher<{
    delete:number;
    alert:string;

  }>();

  function handleClick(id:number){
    //   console.log("I am being deleted.... id: ", id)
      dispatch('delete', id)
    }

</script>

<li>
    <input type="checkbox" bind:checked={todo.completed}>
    <span>{todo.text}</span>
    <button on:click={() => handleClick(todo.id) }>{todo.completed? "Delete": "Remove"}</button>
</li>