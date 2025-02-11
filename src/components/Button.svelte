<script>
    let { value = "подписаться"} = $props()
</script>

<div>
    <button>{value}</button>
    <!-- <input type="button" value={value}> -->
</div>

<style>
    button {
        width: 100%;
        height: 100%;
        background-color: var(--element-color);
        border-color: var(--main-bg-color);
    }
</style>