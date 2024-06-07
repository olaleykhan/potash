<script lang="ts">

    console.log("YOU HAVE LOADED STUPID BUTTON")

    function handleClick(){
        console.log("I am being clicked in stupid button: Not so stupid anymore huh?")
    }
</script>

<button on:click on:click={handleClick} on:click >
    <slot> Click me, I do nothing</slot>
   
</button>