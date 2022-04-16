<script>
//export let menu = 1;
export let navItems = [
    {
        id: '1',
        name: 'Software Setup'

    },
    {
        id: '2',
        name: 'History of Svelte'

    },
    {
        id: '3',
        name: 'Highlights of Svelte'

    },
    {
        id: '4',
        name: 'Code Snippets'

    }

];
</script>

<style>

</style>

<ul id = "menu">
    {#each navItems as item}
    <li>
        <p>
            {item.name}
        </p> 
    </li>|
    {/each} 
</ul>
<hr id = "navBarLine">


