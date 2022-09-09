<script>
    import Footer from "./Footer.svelte";
    export let profilephoto;
    export let username;
    export let posturl;
    export let likecount;
    export let content;
    export let commentscount;
    export let day;
    export let verifyuser;

    $: if (username.length > 15) {
        alert("Username must be less than 15 characters");
    }
</script>

{#if profilephoto && username && posturl}
<div class="relative w-96 h-[30rem] bg-white left-1/2 -translate-x-1/2 -mt-[50rem] rounded">
    <div>
        <img src={profilephoto} class="absolute ml-3 mt-2 w-10 h-10 rounded-full">
    </div>
    <h2 class="absolute ml-16 mt-4 text-sm font-extrabold">
        {username}
        {#if verifyuser}
        <span class="absolute text-lg mx-1 -mt-1 material-symbols-outlined text-blue-500">verified</span>
        {/if}
    </h2>
    <div class="float-right">
        <p class="absolute -ml-10 mt-4 text-xl font-extrabold"><i class="fa-solid fa-ellipsis"></i></p>
    </div>
    <hr class="relative top-14">
    <div>
        <img src="{posturl}" class="relative left-1/2 -translate-x-1/2 top-[3.7rem]">
        <div>
            <div class="relative top-[4.5rem]">
                <div class="float-left mx-3">
                    <svg color="#262626" fill="#262626" height="24" role="img" viewBox="0 0 24 24" width="24"><path d="M16.792 3.904A4.989 4.989 0 0121.5 9.122c0 3.072-2.652 4.959-5.197 7.222-2.512 2.243-3.865 3.469-4.303 3.752-.477-.309-2.143-1.823-4.303-3.752C5.141 14.072 2.5 12.167 2.5 9.122a4.989 4.989 0 014.708-5.218 4.21 4.21 0 013.675 1.941c.84 1.175.98 1.763 1.12 1.763s.278-.588 1.11-1.766a4.17 4.17 0 013.679-1.938m0-2a6.04 6.04 0 00-4.797 2.127 6.052 6.052 0 00-4.787-2.127A6.985 6.985 0 00.5 9.122c0 3.61 2.55 5.827 5.015 7.97.283.246.569.494.853.747l1.027.918a44.998 44.998 0 003.518 3.018 2 2 0 002.174 0 45.263 45.263 0 003.626-3.115l.922-.824c.293-.26.59-.519.885-.774 2.334-2.025 4.98-4.32 4.98-7.94a6.985 6.985 0 00-6.708-7.218z"></path></svg>
                </div>
                <div class="float-left">
                    <svg color="#262626" fill="#262626" height="24" role="img" viewBox="0 0 24 24" width="24"><path d="M20.656 17.008a9.993 9.993 0 10-3.59 3.615L22 22z" fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="2"></path></svg>
                </div>
                <div class="float-left mx-3">
                    <svg color="#262626" fill="#262626" height="24" role="img" viewBox="0 0 24 24" width="24"><line fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="2" x1="22" x2="9.218" y1="3" y2="10.083"></line><polygon fill="none" points="11.698 20.334 22 3.001 2 3.001 9.218 10.084 11.698 20.334" stroke="currentColor" stroke-linejoin="round" stroke-width="2"></polygon></svg>
                </div>
                <div class="float-right mr-3">
                    <svg color="#262626" fill="#262626" height="24" role="img" viewBox="0 0 24 24" width="24"><polygon fill="none" points="20 21 12 13.44 4 21 4 3 20 3 20 21" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></polygon></svg>
                </div>
                <p class="relative -left-[6.5rem] text-sm font-extrabold top-8">{likecount > 1000 ? likecount.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",") : likecount} likes</p>
                <p class="relative -left-[6.5rem] text-sm font-extrabold top-10">{username} <span class="font-medium">{content}</span></p>
                <p class="relative left-4 text-sm text-gray-500 top-12 opacity-90">See all {commentscount} reviews</p>
                <p class="relative left-4 text-[13px] text-gray-500 top-14 opacity-90">{day} days ago</p>
            </div>
        </div>
    </div>
    <hr class="relative top-36 w-[23rem] left-1/2 -translate-x-1/2">
    <div class="float-left mx-3 relative top-40">
        <svg color="#262626" fill="#262626" height="24" role="img" viewBox="0 0 24 24" width="24"><path d="M15.83 10.997a1.167 1.167 0 101.167 1.167 1.167 1.167 0 00-1.167-1.167zm-6.5 1.167a1.167 1.167 0 10-1.166 1.167 1.167 1.167 0 001.166-1.167zm5.163 3.24a3.406 3.406 0 01-4.982.007 1 1 0 10-1.557 1.256 5.397 5.397 0 008.09 0 1 1 0 00-1.55-1.263zM12 .503a11.5 11.5 0 1011.5 11.5A11.513 11.513 0 0012 .503zm0 21a9.5 9.5 0 119.5-9.5 9.51 9.51 0 01-9.5 9.5z"></path></svg>
        <p class="relative text-sm text-gray-500 -top-[21px] left-8">Add comment...</p>
    </div>
    <div class="float-right relative top-[11.7rem] mr-16 opacity-60">
        <p class="relative text-sm text-blue-500 font-extrabold -top-[21px] left-8">Share</p>
    </div>
</div>
{:else}
<!--  -->
{/if}

<style>
    .material-symbols-outlined {
        font-variation-settings:
        'FILL' 1,
        'wght' 400,
        'GRAD' 0,
        'opsz' 48
}
</style>