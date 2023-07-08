<script>
    import { fade } from "svelte/transition";
    let visible = true;
    var a = 0;

    function toreg() {
        window.location.href = "/reg";
        visible = false;
        a = 1;
    }
    function tolog() {
        window.location.href = "/log";
        visible = false;
        a = 1;
    }
</script>


{#if visible}
    <div id="div" >
        <button type="button" on:click={toreg}>REGISZTRÁCIÓ</button>
        <button type="button" on:click={tolog}>BEJELENTKEZÉS</button>
    </div>
{/if}

{#if a === 1}
    <style>
        #div {
            animation: fade-out 500ms;
        }
    </style>
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
