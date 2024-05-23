<main>
    
    <p> right here appears to be the basic layout of a somewhat Svelty component.</p>
    <nav>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/noda">Noda</a></li>
            <li><a href="/noda/page">Noda Page</a></li>  
        </ul>
    </nav>

    <slot/>
</main>

<style>
    /* global styling */
    main{
        background-color: lightblue;
        height:100vh;
        padding: 2em;
        margin: 0;
        border-radius: 1em;
    }

    p{
        color: pink;
        font-size: larger;
    }
</style>