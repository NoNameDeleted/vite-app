<script>
    import Button from "./Button.svelte";
    import { popup } from '@telegram-apps/sdk';

    async function openPopup(){
        if (popup.open.isAvailable()) {
        // popup.isOpened() -> false
        const promise = popup.open({
            title: 'Hello!',
            message: 'Here is a test message.',
            buttons: [{ id: 'my-id', type: 'default', text: 'Default text' }],
        });
        // popup.isOpened() -> true
        const buttonId = await promise;
        // popup.isOpened() -> false
        }
    }
    
</script>

<div>
    <Button value={'Подбросить монетку ведьме'} onclick={openPopup}/>
    <Button value={'Подписаться'} onclick={openPopup}/>
    <Button value={'Уйти с территории Ликориса'} onclick={openPopup}/>
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