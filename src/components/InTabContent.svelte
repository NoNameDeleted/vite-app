<script>
    let {content = ""} = $props()
</script>

<div>
    <p>
        {content}
    </p>
</div>

<style>
    p {
        white-space: pre-line;
        margin: 0%;
    }

    div {
        background-color: var(--element-color);
        padding: 1% 2% 2%;
        margin-top: 2%;
        min-height: 20vh;
    }
</style>