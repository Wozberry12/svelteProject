
<script>
    import Accordion from "./components/Accordion.svelte";
    import NavigationBar from "./components/NavigationBar.svelte";
    //Detail Files in Tutorial
    import Installation from "./components/Installation.svelte";
    import History from "./components/History.svelte";
    import Benefits from "./components/Benefits.svelte";
    import Header from "./components/Header.svelte";
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
        }
    ];
    
</script>


<main class = "main">
    <Header />
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
                Details Are here
            </p>
        </div>
    </Accordion>
    <hr>
</main>

<style>
	
    hr{
        width:100%;
    }
   
</style>

