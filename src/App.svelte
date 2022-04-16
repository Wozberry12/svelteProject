
<script>
    import Accordion from "./components/Accordion.svelte";
    import NavigationBar from "./components/NavigationBar.svelte";
    import Installation from "./components/Installation.svelte";
</script>

<style>
	
</style>

<main class = "main">
    <Accordion>
        <span slot="head"> History of Svelte
        </span>
        <div slot ="details">
            <p>
                Details Are here
            </p>
        </div>
    </Accordion>
    <Accordion>
        <span slot="head"> Software Setup
        </span>
        <div slot ="details">
            <p>
                <Installation />
            </p>
        </div>
    </Accordion>
    <Accordion>
        <span slot="head"> What Makes Svelte Different
        </span>
        <div slot ="details">
            <p>
                Details Are here
            </p>
        </div>
    </Accordion>
    <Accordion>
        <span slot="head"> Code Examples
        </span>
        <div slot ="details">
            <p>
                Details Are here
            </p>
        </div>
    </Accordion>
    <hr>
</main>