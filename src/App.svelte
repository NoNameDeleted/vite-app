<script lang="ts">
  import ProfilePicture from './components/ProfilePicture.svelte';
  import Menu from './components/Menu.svelte';
  import MainContent from './components/MainContent.svelte';
  import { init } from '@telegram-apps/sdk';
  import { isTMA } from '@telegram-apps/bridge';

  async function checkTG(){
    if (await isTMA()) {
      console.log('It\'s Telegram Mini Apps');
      isTG = 'It\'s Telegram Mini Apps'
      init();
    }
    else{
      console.log('It\'s NOT Telegram Mini Apps');
      isTG = 'It\'s NOT Telegram Mini Apps'
    }
  }

  let isTG = $state('not seted')

  checkTG()
</script>

<main>
  <!-- {isTG} -->
  <div class="top-container">
    <ProfilePicture />
    <Menu />
  </div>
    <MainContent />
  
</main>

<style>
  :root {
    --main-bg-color: #f68187;
    --pfp-bg-color: #5d5d5d;
    --menu-bg-color: #571c27;
    --element-color: #f6ca9f;
  }

  main {
    font-family: "Pixelify Sans", serif;
    font-size: 3vw;
    background-color: var(--main-bg-color);
    display: inline-block;
    width: 100%;
  }

  .top-container {
    display: flex;
    
    background-color: var(--main-bg-color);
  }
</style>
