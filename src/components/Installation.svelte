<script>


</script>

    <h1>Installing Svelte</h1>
    <ul id="step1">
        <li>
            <p>Open your command prompt and create a new project with </p>
            <div class="codeSnippet">
                <p>
                    mkdir svelte-projects
                </p>
            </div>
        </li>
        <li>
            <p>"Now enter the folder in the command line with 
            <div class = "codeSnippet">
                <p>cd svelte-project</p> 
            </div>
            
        </li>
        <li><p>You need Node.js installed in order to work with Svelete's command line tools. 
                Go to this website to download Node.js for your
                website:
            <a href= "https://nodejs.org/en/" target="_blank" rel="noopener noreferrer"> Node.js </a>
            <br>
                Make sure to download <a href= "https://git-scm.com/" target="_blank" rel="noopener noreferrer"> Git</a> too,
                as it makes it possible to work with pre-defined templates from Svelte's support team.
           </p>
        </li>
        <li>
            <p>Now that you have Git and Node.js downloaded, open a terminal
                in the folder you want to create your Svelte Project. Execute the following
                lines in the terminal
            </p>
            <div class = "codeSnippet">
                <p>
                    npx degit sveltejs/template my-svelte-directory
                    cd my-svelte-directory
                    npm install
                </p>
            </div>
        </li>
        <li>
            <p>
            The previous command created your project inside the directory,
            loaded it up with critical packages, and added files from Github's 
            <a href= "https://github.com/sveltejs/template" target="_blank" rel="noopener noreferrer"> sveltejs/template </a>
            repository.
        </p>
        </li>
        <li>
            <p>
                You can now run Svelte in your terminal using:    </p>
                <div class="codeSnippet">
                    <p>
                        npm run dev
                    </p>
                </div>
        </li>
    </ul>

<style>
    h1{
        text-align:center;
        text-decoration: underline;   
    }
    ul{

        list-style: decimal;
        padding-left: 5px;
        font-size:16px;
    }
    a,a:visited{
        color: crimson;
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