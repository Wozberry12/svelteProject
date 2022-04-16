<script>
    const title = "Svelte";
    const step1 ="Open your command prompt and create a new project with the" 
                +"mkdir svelte-projects";
    const step2 = "Now enter the directory on the command line with"+
                  "cd svelte-project"
    const step3 ="You need Node.js installed in order to work with Svelte's command line tools. Click here: "
</script>

    <h1>{title}</h1>
    <ul id="step1">
        <li>
            <p>
                {step1}
            </p>
        </li>
        <li>
            <p>
                {step2}
            </p>
        </li>
        <li>
            {step3} <a href= "https://nodejs.org/en/" target="_blank" rel="noopener noreferrer"> Download Node.js </a>
        </li>
    </ul>

<style>
    ul#step1{
        list-style: decimal;
    }
</style>