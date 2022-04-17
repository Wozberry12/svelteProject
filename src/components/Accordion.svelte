<script>
    import NavigationBar from './NavigationBar.svelte';

    export let isOpen = false;
    //Smoothly opens a tab
    import { slide } from 'svelte/transition';
    //Create clickHandler

    let navItems = NavigationBar.navItems;
    const clickHandler = () =>
        isOpen = !isOpen
</script>


<div class ="accordion">
        <div class="header">
            <div class = "text">
                <slot name = "head">
                </slot>
            </div>
        </div>    
    <button on:click = {clickHandler}>
        Expand
    </button>
    {#if isOpen}
    <div class = "details" transition:slide>
        <slot name="details"></slot>
    </div>
    {/if}
    </div>
<style>

    div.accordion{
        float:left;
        text-align: center;
    }
    div.header{
        width:100%;
        
    }
    div.header .text{
        flex: 1;
        margin-right: 5px;
        font-family:-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        padding-left: 20px;
        padding-right: 20px;
        margin: auto;
        align-items: center;
        height: 100%    
    }
    div.details{
        background-color: rgba(69, 157, 183, 0.2);
        padding:1rem;
        text-align:left;
        flex: 1 1 auto;
    }
    

    
</style>
