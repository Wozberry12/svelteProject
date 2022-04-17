<script>
    import Accordion from './Accordion.svelte';
    let lessSvelteCode = "images/svelteLessCode.jpg";
    let reactMoreCode = "images/reactMoreCode.jpg";
</script>
    <h1>What Makes Svelte Special</h1>
    <ul>
        <li>
            Before our group shows off the syntax of Svelte, it is important to understand what makes
            Svelte different.
        </li>
        <li>
            <h3>
                No Virtual DOM
            </h3>
            <p> 
                When using a framework that utilizes a Virtual DOM, everytime your web application
                updates, a new Virtual DOM is created and the old DOM is reconciled against the new one,
                the web application is updated.
                Svelte skips the overhead of this, seeing the Virtual DOM operations as additional work to be done by the web app.
                Svelte is instead a <strong>compiler</strong> that knows at build time,
                rather than run time, what will change in your app. As Richard Harris writes in this
                <a href= "https://svelte.dev/blog/virtual-dom-is-pure-overhead" target="_blank" rel="noopener noreferrer"> article </a>
                , "...you know what would be even faster [than the additional Virtual DOM operations]? Not using them."
            </p>
        </li>
        <li>
            <h3>Simplified Code</h3>
            <p>
                Svelte is built on the premise of brevity and readability. Harris provides
                the example of a user 
                <a href= "https://svelte.dev/blog/write-less-code" target="_blank" rel="noopener noreferrer"> adding two numbers </a>
                in a web application.
                <div class="col1">
                Below is how svelte does it:
                <br>
                <Accordion>
                    <div class = "innerAccord" slot ="details">
                            <img id ="lessCode" src={lessSvelteCode} alt="Much less code."/>
                    </div>
                </Accordion>
            </div>
                <Accordion>
                    <div slot="details">
                        <img id="moreCode" src={reactMoreCode} alt="Much more code."/>
                    </div>
                </Accordion>
        </li>
    </ul>

<style>
    h1{
        text-align:center;
        text-decoration: underline;   
    }
    ul{

        list-style: none;
        padding-left: 5px;
        font-size:16px;
    }
    a,a:visited{
        color: crimson;
    }
    #lessCode{
        width:300px;
        height:150px;
    }
    #moreCode{
        width:400px;
        height:300px;
    }
    div.innerAccord{
       border:black 5px;
       margin:0px;
        
    }
   /* 
    div.codeSnippet{
        background-color: rgba(164, 157, 183, 0.8);
        display: inline-block;
        border-radius: 5px;
        padding: 0.2em 0.3em 0.2em;
        color: crimson;
        font-size: 14px;
        font-family:Arial, Helvetica, sans-serif;
    }*/
</style>