<script>
    import { fade } from "svelte/transition";
    import { backInOut } from "svelte/easing";
</script>
<div >
    <p  transition:fade={{delay: 0, duration: 1000, easing:backInOut}}>FASZA</p>
</div>
<style>
    p{
        background-color: aliceblue;
        width: 30%;
        height: 30px;
        border-radius: 15px;
        text-align: center;
        font-size: larger;
        font: bolder;
    }
</style>