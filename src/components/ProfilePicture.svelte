<script>
    import { onMount } from 'svelte';
    import profilePicture from '../assets/profilePicture.png';
    import love from '../assets/love.png'
    import exclamation from '../assets/exclamation.png'

    let emote = $state(true);

    onMount(() => {
		const interval = setInterval(() => {
			emote = !emote;
		}, 1000);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<div>
    <img class="emote" src={emote? love : exclamation} alt="emote">
    <img class="face" src={profilePicture} alt="profile pic" />
</div>
                                                                              
<style>
    div {
        position: relative;
        width: 46%;
        background-color: var(--pfp-bg-color);
        margin: 2%;
    } 

    img {
        image-rendering: pixelated;
    }

    .face {
        width: 100%;
        transform: scale(0.5) ;
        position: relative;
        top: 15%;
    }

    .emote {
        width: 35%;
        position: absolute;
        transform: translate(90%, 35%);
    }
</style>