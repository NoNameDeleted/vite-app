<script lang="ts">
    import Button from "./Button.svelte";
    import { popup } from '@telegram-apps/sdk';
    import { openTelegramLink } from '@telegram-apps/sdk';

    function openTGChanel(){
        if (openTelegramLink.isAvailable()) {
            openTelegramLink('https://t.me/just_riiin');
        }
    }
    
    async function openPopup(buttonName: String){
        if (popup.open.isAvailable()) {
        // popup.isOpened() -> false
        const promise = popup.open({
            title: 'Ты нажал кнопку ' + buttonName,
            message: 'Возможно в будущем тут появится функционал',
            buttons: [{ id: 'my-id', type: 'default', text: 'Понятно' }],
        });
        // popup.isOpened() -> true
        const buttonId = await promise;
        // popup.isOpened() -> false
        }
    }
    
</script>

<div>
    <Button value={'Подбросить монетку ведьме'} onclick={() => openPopup('доната')}/>
    <Button value={'Подписаться'} onclick={openTGChanel}/>
    <Button value={'Уйти с территории Ликориса'} onclick={() => openPopup('выхода')}/>
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