<script lang="ts">
    let numArray = $state<number[]>([0])
    let len = $derived(numArray.length)

    function add() {
        numArray.push(numArray.length)
    }
</script>
<div class="counter">
    <button onclick={add}>Увеличить</button>
    <div>{numArray}</div>
    <div>{len}</div>
</div>

<style>
    .counter {
        display: flex;
        flex-direction: column;
    }
</style>