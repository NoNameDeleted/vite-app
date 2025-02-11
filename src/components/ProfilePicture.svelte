<script>
    import profilePicture from '../assets/profilePicture.png';
</script>

<div>
    <img src={profilePicture} alt="profile pic" />
</div>
                                                                              
<style>
    div {
        width: 46%;
        background-color: var(--pfp-bg-color);
        margin: 2%;
    } 

    img {
        width: 100%;
        transform: scale(0.6);
        image-rendering: pixelated;
    }
</style>