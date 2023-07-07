<script lang="ts">
    import { fade } from "svelte/transition";
    import Log from "./log_page.svelte";
    import Reg from "./reg_page.svelte";
    import { backInOut } from "svelte/easing";
    let visible = true;
    let ns = 0;    

    function toreg() {
        //window.location.href = "/reg";
        //var string="<Reg/>";
        //console.log("<Reg/>");
        ns = 1;
        visible = false;
        
    }
    function tolog() {
        //indow.location.href = "/log";
        ns = 2;
        visible = false;
        //console.log("<Log/>");
		
    }
	
</script>
<div id="ht"></div>
<div id="ht2"></div>

{#if visible}
    <div id="div"   in:fade={{delay: 0, duration: 1000, easing:backInOut}} 
                    out:fade={{delay: 0, duration: 1000, easing:backInOut}} >
        <button type="button" on:click={toreg} >REGISZTRÁCIÓ</button>
        <button type="button" on:click={tolog} >BEJELENTKEZÉS</button>
    </div>
{/if}

{#if ns === 1}
            <Reg/>
{:else if ns === 2}
            <Log/>
{/if}




<style>
	
    

    button {
        position: relative;
        transform-origin: center;
        margin-top: 20px;
        width: 30%;
        height: 50px;
        opacity: 1;
    }
</style>
