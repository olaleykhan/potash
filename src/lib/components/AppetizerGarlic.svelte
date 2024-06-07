<script lang="ts">
	import StupidButton from "./StupidButton.svelte";


    export let name = "horse 🐴";   //  🐴;

    // $: name = name.toUpperCase();
    
    console.log(" PROPS FROM  appetizer: ",$$props);

    function handleClick(){
        console.log("I am being clicked in middle child component. Inam supposed tl snathcj it ")
    }

</script>


<div>
    <h1>
        {`Hello ${name} World!  in apetiz `}
    </h1>
    <p>
        This is an appetizer garlic.
    </p>

    <StupidButton on:click={handleClick} on:click > I am stupid</StupidButton>

    laughing emoji is:  😂
</div>