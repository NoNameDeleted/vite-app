<script>
    import Button from "./Button.svelte";
</script>

<div>
    <Button value={'Подбросить монетку ведьме'}/>
    <Button value={'Подписаться'}/>
    <Button value={'Уйти с территории Ликориса'}/>
</div>

<style>
    div {
        width: 46%;
        background-color: var(--menu-bg-color);
        margin: 2%;
        margin-left: 0%;
        padding: 2%;
        display: grid;
        grid-auto-rows: minmax(1fr, auto);
        row-gap: 4%;
    }
</style>