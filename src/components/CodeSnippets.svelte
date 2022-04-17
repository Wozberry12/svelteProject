<script>
    import SpecialButton from './SpecialButton.svelte';

    const reactiveExample = "$: doubled = number * 2";
    const scriptTag = "< script > Insert all JavaScript Here< /script >\n";
    const styleTag = "< style >Insert all CSS here< /style >\n";
    
    const importComponent = "<ComponentName />";
    const setMeOutside = "<ComponentName setMeOutside = {'This value is given to the component'}/>"
</script>

    <h1>Examples of Code</h1>
    <ul>    
        <li>
            <h3>Reactive Assignments</h3>
            <p>
                Svelte will automatically update the DOM whenever <strong>any</strong>
                component's state changes. Svelte has a built in reactive operator that
                recomputes values whenever any relevant part changes. Take a look at the below code:
            <div class="codeSnippet">
                {reactiveExample}
            </div>
            <p>The "$:" signifies this as reactive declaration. Whenever the "count" variable updates,
                    the double variable will also update. This is a very simple example, but this button became
                    binded to an update in only one line of code.
                    <SpecialButton/>
            </p>    
        </li>
        <li>
            <h3>Props and Components</h3>
            <p>
                Svelte is built upon the idea of reusable and modular code. When designing this website,
                our group would load components into modules,vastly shortening not only the time it takes 
                to write the code,but the amount of lines in the code.
            </p>
            <p>All Svelte components will be composed using the following template</p>
            <div class="codeSnippet">
                <p>
                    {scriptTag}
                    <br><br>
                    Insert Html Here
                    <br><br>
                    {styleTag}
                </p>
            </div>
        </li>    
        <li>
            <p>Next you import the component into the desired module, inside the script section:</p>
            <div class="codeSnippet">
                <p>
                    import ComponentName from './pathOfComponent/Component.svelte';
                </p>
            </div>
            <p>Now whenever you need to access the component you can put it wherever it is needed within
                the main application. This can be on any line in your source code! It is inserted like so:
                <div class="codeSnippet">
                    {importComponent}
                </div>
                This will run <strong>ALL</strong> the code from the imported component. This mean you have full control
                of where the JavaScript, HTML, and CSS will be executed in a component based on where it is injected.
                But what if you need to pass in a value into a component from an external module? This is where
                Svelte Props come in!
        </li>
        <li>
            <h3>
                Props in Svelte
            </h3>
            <p>
                In order to pass a value into an external component, you must
                declare the variable with a name identical to the variable you wish to utilize
                within the component. Next, within the component, you are accessing
                you must add the <code>export</code> keyword in front of the variable:
                <div class= "codeSnippet">
                    export let setMeOutside;
                </div>
                <p>
                    The <code>export</code> keyword lets the compiler know this variable can be set
                    outside of this component. Now return to the application using the component.
                    Declare a variable in the script section with the same name, then pass it into the 
                    component like so:
                    <div class= "codeSnippet">
                        let setMeOutside;
                        <br><br>
                        {setMeOutside}
                </div>
        </li>
    </ul>

<style>
    h1{
        text-align:center;
        text-decoration: underline;   
    }
    h3{
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