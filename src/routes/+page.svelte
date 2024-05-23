<script>

    // The scripts for the index page go here
    import {Button, TodoItem} from "$lib"

    let count = 0;
    let name = "Olalekan Abdulfatah"
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
    function handleClick2(){
        console.log("eskelebe ti o lebebe")
    }

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
</script>

<!-- then markup for the index page goes here -->
<section>
    <main>
        <h1> Welcome to the index page </h1>
        <p> This is the index page of the SvelteKit app.</p>
        <ul>
            {#each todos as todo (todo.id)}
                <TodoItem {todo} />
            {/each}
        </ul>
    </main>


</section>




<!-- style goes below here -->

<style>
    h1 {
        color: red;
    }
</style>