<script>
    import Card from "../components/Card.svelte";
    let openedMenu = false;
    let profilePhoto = "https://i.hizliresim.com/lk2ulqn.png";
    let username = "queaxtra";
    let postURL = "https://i.hizliresim.com/bktuto0.png";
    let likeCount = 12631;
    let content = "Fakegram is best 💖";
    let commentsCount = 392;
    let hours = "5d";
    let location = "İstanbul, Türkiye";

    function openMenu() {
        openedMenu = !openedMenu;
    }
</script>

<div>
    <button on:click={openMenu} class="p-2 mx-5 my-5 bg-[#151515] px-5 rounded"><i class="ri-menu-2-line"></i></button>
</div>

{#if openedMenu}
<div class="mx-5 my-2 bg-[#151515] w-60 h-[30rem] rounded flex justify-center text-center">
    <div class="grid grid-cols-1">
        <input type="text" class="w-52 h-8 rounded bg-[#202020] p-5 mt-5" placeholder="Username" bind:value={username}>
        <input type="url" class="w-52 h-8 rounded bg-[#202020] p-5 -mt-7" placeholder="Profile Photo URL" bind:value={profilePhoto}>
        <input type="url" class="w-52 h-8 rounded bg-[#202020] p-5 -mt-7" placeholder="Post Photo URL" bind:value={postURL}>
        <input type="number" min="0" class="w-52 h-8 rounded bg-[#202020] p-5 -mt-7" placeholder="Like Count" bind:value={likeCount}>
        <input type="text" class="w-52 h-8 rounded bg-[#202020] p-5 -mt-7" placeholder="Content" bind:value={content}>
        <input type="number" min="0" class="w-52 h-8 rounded bg-[#202020] p-5 -mt-7" placeholder="Comments Count" bind:value={commentsCount}>
        <input type="text" class="w-52 h-8 rounded bg-[#202020] p-5 -mt-7" placeholder="Hours (s, d, g)" bind:value={hours}>
        <input type="text" class="w-52 h-8 rounded bg-[#202020] p-5 -mt-7" placeholder="Location" bind:value={location}>
    </div>
</div>
{/if}

<Card {profilePhoto} {username} {postURL} {likeCount} {content} {commentsCount} {hours} {location} />