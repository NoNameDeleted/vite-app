<script>
    let { value = "подписаться", onclick} = $props()
</script>

<div>
    <button onclick={onclick}>{value}</button>
    <!-- <input type="button" value={value}> -->
</div>

<style>
    button {
        font-family: "Pixelify Sans", serif;
        font-size: 3vw;
        width: 100%;
        height: 100%;
        background-color: var(--element-color);
        border-color: var(--main-bg-color);
    }
</style>