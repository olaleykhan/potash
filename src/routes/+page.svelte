<script lang="ts">
	import AppetizerGarlic from "$lib/components/AppetizerGarlic.svelte";
    import Count , {alertTotal} from "$lib/components/Count.svelte";

    let x =0;
    let y =0;

    function setY(value: number) {
        y = value;
    }   

    $: iDepentOnY = y;
    $: setY(x);

    function handleClick(){
        console.log(`clicking stipind buttonm ${x++}`)
    }




</script>



<div>
    <Count/>
    <div>
        <style>
            div {
                color: red;
            }
        </style>

        <a href="p/{y}" > hulla{x+y}</a>
    </div>

    <button on:click={()=>alertTotal()}>
        Count
    </button>

    <AppetizerGarlic name="horse 🐴" on:click={handleClick}/>

   


</div>