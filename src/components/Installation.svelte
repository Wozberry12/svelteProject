<script>
  
    const step3 ="You need Node.js installed in order to work with Svelte's command line tools. Click here: "
</script>

    <h1>Svelte</h1>
    <ul id="step1">
        <li>
            <p>Open your command prompt and create a new project with the mkdir svelte-projects</p>
        </li>
        <li>
            <p>"Now enter the folder in the command line with 
            <p class = "codeSnippet"> 'cd svelte-project'
            </p> 
            
        </li>
        <li><p>You need Node.js installed in order to work with Svelete's command line tools. 
                Go to this website to download Node.js for your
                website:
            <a href= "https://nodejs.org/en/" target="_blank" rel="noopener noreferrer"> Node.js </a>
            <br>
                Make sure to download<a href= "https://git-scm.com/" target="_blank" rel="noopener noreferrer"> Git</a> too,
                as it makes creating Svelte projects from pre-defined templates far easier.
           </p>
        </li>
        <li>
            <p>Now that you have Git and Node.js downloaded, open a terminal
                in the folder you want to create your Svelte Project. Execute the following
                lines in the terminal
            </p>
            <p class = "codeSnippet">
                npx degit sveltejs/template my-svelte-project-name
                cd my-svelte-project-name
                npm install
            </p>
        </li>
    </ul>

<style>
    ul#step1{
        list-style: decimal;
    }
    a,a:visited{
        color: crimson;
    }
    p.codeSnippet{
        background-color: gainsboro;
    }
</style>