
<script>
    import Accordion from "./components/Accordion.svelte";
    //Detail Files in Tutorial
    import Installation from "./components/Installation.svelte";
    import History from "./components/History.svelte";
    import Benefits from "./components/Benefits.svelte";
    import Header from "./components/Header.svelte";
    import CodeSnippets from "./components/CodeSnippets.svelte";
    import Footer from "./components/Footer.svelte";
    import Summary from "./components/Summary.svelte";
    let isOpen = false;

    let navItems = 
    [
        {
            id: '1',
            name: 'Software Setup',
            open: isOpen
        },
        {
            id: '2',
            name: 'History of Svelte',
            open: isOpen
        },
        {
            id: '3',
            name: 'Highlights of Svelte',
            open: isOpen
        },
        {
            id: '4',
            name: 'Code Snippets',
            open: isOpen
        },
        {
            id:'5',
            name:'Moving to Our Web Application',
            open: isOpen
        }
    ];
    
</script>


<main class = "main">
    <Header />
    <div class="clear"><div>
    <div class= "accordContainer">
        <Accordion isOpen = {navItems[0].open}>
            <span slot="head"> {navItems[0].name}
            </span>
            <div slot ="details">
                <p>
                    <Installation />
                </p>
            </div>
        </Accordion>
        <Accordion isOpen = {navItems[1].open}>
            <span slot="head">  {navItems[1].name}
            </span>
            <div slot ="details">
                <p>
                    <History />
                </p>
            </div>
        </Accordion>
        <Accordion isOpen = {navItems[2].open}>
            <span slot="head">  {navItems[2].name}
            </span>
            <div slot ="details">
                <p>
                    <Benefits/>
                </p>
            </div>
        </Accordion>
        <Accordion isOpen = {navItems[3].open}>
            <span slot="head"> {navItems[3].name}
            </span>
            <div slot ="details">
                <p>
                    <CodeSnippets/>
                </p>
            </div>
        </Accordion>

        <Accordion isOpen = {navItems[4].open}>
            <span slot="head"> {navItems[4].name}
            </span>
            <div slot ="details">
                <p>
                    <Summary/>
                </p>
            </div>
        </Accordion>
    
    </div>
    <hr>
<Footer /> 
</main>

<style>
	div.clear{
        clear:both;
    }
    hr{
        width:100%;
    }
   main{
       background-color: #202142;
        height: 100%;
    }
   div.accordContainer{
       position:relative;
       left: 60%;
       top:50%;
       padding:10px;
       transform: translate(-50%,-50%);

   }
</style>

