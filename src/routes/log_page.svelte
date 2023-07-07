<script>
	import { fade } from "svelte/transition";
    import Home from "./home_page.svelte";
    import { backInOut } from "svelte/easing";
    let visible = true;
    let ns = 0;
    function log() {
        //window.location.href = "/home";
        visible = false;
    }
</script>


{#if visible}
    <div class="text-column" id="div" transition:fade={{delay: 0, duration: 1000, easing:backInOut}}>
        <h1>BEJELENTKEZÉS</h1>

        <form action="">

            <label for="username">FELHASZNÁLÓNÉV</label>
            <input type="text" name="username">

            

            <label for="password">JELSZÓ</label>
            <input type="password" name="password">

            
            <button type="button" on:click={log} >BEJELENTKEZÉS</button>
            

        </form>
</div>
{/if}

{#if !visible}
    <Home/>
{/if}

<style>
    button{
        position: relative;
        left:50%;
        top: 15px;
    }
</style>