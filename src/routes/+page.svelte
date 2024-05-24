<script lang="ts" >

    // The scripts for the index page go here
    import type {ComponentEvents} from 'svelte'
    import {Button, TodoItem} from "$lib"
	import type { H } from "vitest/dist/reporters-yx5ZTtEV.js";

    let count = 0;
    let name = "Olalekan Abdulfatah"
    let todoInput = "";
    let todos = [
        {
            id: 1,
            text: "Learn Svelte",
            done: true
        },
        {
            id: 2,
            text: "Learn SvelteKit",
            done: false
        },
        {
            id: 3,
            text: "Build something awesome",
            done: false
        }
    ]
    function handleClick(){
        console.log("I am being clicked.... awnnn")
        if(count>0){
            // this is actually not going to work at all since the onclick method has the once modifier
            alert("I am sorry, I can't work anymore. I am tired.")
            return;
        }
        count++;
        console.log("I work normally as I am humanly expected to do.")
 
    }
    
//     const handleOnChange = (event: Event) => {
//     const target = event.target as HTMLInputElement;
//     todoInput = target.value;
//   };

  function handleDelete(event: ComponentEvents<TodoItem>['delete']){
      console.log("I am being deleted.... id: ", event)
    //   TODO: terrible typescript support. improve typing support in project
      const id = event.detail ;
      todos = todos.filter(todo => todo.id !== id)
    }

//     function handleRemoveTodo(id) {
//     dispatch('removetodo', {
//       id
//     });
//   }


    function handleSumbit(){
        console.log("I am being submitted.... awnnn")

        console.log("todos are: ",todos)
        const todo = {
            id: todos.length + 1,
            text: todoInput,
            done: false
        }
        todos = [...todos, todo];
        todoInput = "";
    }


</script>

<!-- then markup for the index page goes here -->
<section>
    <main>
        <h1> Welcome to the index page </h1>
        <p> This is the index page of the SvelteKit app.</p>
        <ul>
            {#each todos as todo (todo.id)}
                <TodoItem {todo} on:delete={handleDelete} />
            {/each}
        </ul>

        <form on:submit|preventDefault={handleSumbit}>
            <input type="text" on:input={handleOnChange} placeholder="Enter your todo" bind:value={todoInput} />
            <Button >Click me</Button>
        </form>
    </main>


</section>




<!-- style goes below here -->

<style>
    h1 {
        color: red;
    }
</style>