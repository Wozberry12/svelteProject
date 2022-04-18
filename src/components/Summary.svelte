<script>
   const codeSnippet = "{#each Array for item(item.id)}"

</script>
    <ul>
        <h1>Conclusion: Moving to Our Web Application</h1>
        <li>
            <p>
                Our web application predominantly utilizes components and props from Svelte,
                as it made our code far more brief and readable.
            </p>
       </li>
       <br>
       <li>
           <p>Also using two-way binding properties for text-inputs and their respective variables,
                also further shortened the length of the code. The most important function provided by Svelte,
                however, was the ability to use an each loop within the HTML, allowing for creating iterative
                HTML documents.
                <div class="codeSnippet">
                    <p>{codeSnippet}</p>
                </div>
            <p>
                Once you understand the each loop above, you will be able to write a project like ours!
            </p>
       </li>
    </ul>

<style>
    h1{
        text-align:center;
        text-decoration: underline;   
    }
    ul{
        text-align: left;
        list-style: none;
        padding-left: 5px;
        font-size:16px;
    }
   

    div.codeSnippet{
        background-color: rgba(164, 157, 183, 0.8);
        display: inline-block;
        border-radius: 5px;
        padding: 0.2em 0.3em 0.2em;
        color: crimson;
        font-size: 14px;
        font-family:Arial, Helvetica, sans-serif;
    }
</style>