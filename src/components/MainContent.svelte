<script>
  import Button from "./Button.svelte";
  import InTabContent from "./InTabContent.svelte";


</script>

<div class="container">
    <div class="tabs">
        <Button value={'Рина-чан'}/>
        <Button value={'Авто.'}/>
        <Button value={'Проп.'}/>
        <Button value={'История.'}/>
    </div>
    <InTabContent />
</div>


<style>
    .container {
        background-color: var(--menu-bg-color);
        margin: 0% 2% 2%;
        padding: 2% 2% 2%;
    }

    .tabs {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        column-gap: 2%;
    }
</style>