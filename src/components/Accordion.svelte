<script>

    export let isOpen = false;
    //Smoothly opens a tab
    import { slide } from 'svelte/transition';
    //Create clickHandler

    const clickHandler = () =>
        isOpen = !isOpen
</script>


<div class ="accordion">
          
    <button class = "btnAccordion" on:click|self = {clickHandler}>
            {#if isOpen == false}
                    <slot name = "head">
                    </slot>
            {:else if isOpen == true}
            Collapse
            {/if}
    
    {#if isOpen}
    <div class = "details" transition:slide>
        <slot name="details"></slot>
    </div>
    {/if}
    </div>
<style>
    button.btnAccordion{
		width: 100%;
		padding:20px;
		display: inline-block;
        font-family: 'Times New Roman', Times, serif;
        font-size: larger;
		justify-content: space-between;
		align-items: center;
		background-color: #a39191;
        position: relative;
    }
    div.accordion{
        float:left;
        align-items: flex-start;
        width:80%;
        padding: 2px;
    }
    div.details{
        background-color: rgba(185, 185, 164, 0.2);
        padding:1rem;
    }
</style>
