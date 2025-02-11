<script lang="ts">
  import svelteLogo from './assets/svelte.svg'
  import viteLogo from '/vite.svg'
  import Counter from './components/Counter.svelte';
  import ProfilePicture from './components/ProfilePicture.svelte';
  import Menu from './components/Menu.svelte';
  import MainContent from './components/MainContent.svelte';
</script>

<main>
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
    background-color: var(--main-bg-color);
    display: inline-block;
    width: 100%;
  }

  .top-container {
    display: flex;
    
    background-color: var(--main-bg-color);
  }
</style>
