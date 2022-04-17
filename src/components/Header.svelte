<script>
    let svelteLogo = 'images/svelteLogo.png';
</script>

<header>
    <div class = "colLeft">
    <h1>
        Svelte: Simplifying Reactive Development
    </h1>
    </div>
    <div class= "colRight">
        <img src = {svelteLogo} alt="Svelte Logo"/>
    </div>
    <div class = "clear"></div>
    <p>
        By Will Oswald, Marco Kosasih, and Ben Kamide
    </p>

    
</header>

<style>
    div.clear {
        clear: both;
    }
    .colLeft{
        margin-top: 5%;
        width:70%;
        float: left;
        
    }
    .colRight{
        width: 20%;
        float: right;
    }
    header{
        text-align: center;
        padding:1em;
        margin: 0 auto;
    }

    h1{
        color: orangered;
        text-transform: capitalize;
        font-weight:300;
        font-size:3em;
        width: 100%;
        height:100%;
        border: 5px black solid;
    }
    p{
        color: orangered;
        text-transform: capitalize;
    }
    img{
        width: 100%;
        height: 100%;
    }
</style>