<script lang="ts">
// @ts-nocheck

  import Button from "./Button.svelte";
  import InTabContent from "./InTabContent.svelte";

    let tabsContent = {
        rinaChan: `Ну что попался чертила!
        Я тут главная по пикселям, и ты вообще-то в моих владениях.
        Предлагаю подписаться!
        *Летающая иконка хитро улыбается*`,
        auto: `тут будет автобиография? автомобили? автозаполнение?`,
        prop: `тут будут прописи? пропсы? проповеди?`,
        history: `тут будет история ликориса (наверное)`
    }

    let openedTab = $state('rinaChan')

</script>

<div class="container">
    <div class="tabs">
        <Button value={'Рина-чан'} onclick={() => openedTab='rinaChan'}/>
        <Button value={'Авто.'} onclick={() => openedTab='auto'}/>
        <Button value={'Проп.'} onclick={() => openedTab='prop'}/>
        <Button value={'История.'} onclick={() => openedTab='history'}/>
    </div>
    
    <InTabContent content={tabsContent[openedTab]}/>
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