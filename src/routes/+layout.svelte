<main>
   
    <nav>
        
        <ul class="nav-list">
            <li class="nav-item"><a href="/">Home</a></li>
            <li class="nav-item"><a href="/noda">Noda</a></li>
            <li class="nav-item"><a href="/noda/page">Noda Page</a></li>  
        </ul>
    </nav>

    <slot/>
</main>

<style>
    nav{
        margin-top: 24px;
    }
    ul.nav-list{
        list-style-type: none;
        display: flex;
        justify-content: space-around;
        padding: 0;
        max-width: 800px;
        margin: 0 auto;
    }

    li.nav-item{
        display: inline;
    }
    li.nav-item a{
        text-decoration: none;
        padding: 8px 24px;;
        border: 1px solid #ccc;
        border-radius: 4px;
        color: #333;
        font-weight: 600;
    }
</style>