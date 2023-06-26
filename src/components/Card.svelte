<script lang="ts">
    export let profilePhoto: string;
    export let username: string;
    export let postURL: string;
    export let likeCount: number;
    export let content: string;
    export let commentsCount: number;
    export let hours: string;
    export let location: string;
</script>

<div class="ml-auto mr-auto left-0 right-0 w-96 bg-white rounded mt-40 md:mt-32 lg:mt-32">
    <img class="absolute w-12 mx-3 py-2" src={profilePhoto} alt="Profile Image">
    <div>
        <p class="flex ml-20 py-3 text-sm font-bold text-gray-700">{username} <span class="ml-1 text-gray-500 font-normal">• {hours}</span></p>
        <p class="relative ml-20 -top-3 text-xs text-black/50">{location}</p>
    </div>
    <img src={postURL} alt="Post Image">
    <div class="flex relative m-2">
        <svg aria-label="Like" color="rgb(0,0,0)" fill="rgb(0,0,0)" height="24" role="img" viewBox="0 0 24 24" width="24"><title>Like</title><path d="M16.792 3.904A4.989 4.989 0 0 1 21.5 9.122c0 3.072-2.652 4.959-5.197 7.222-2.512 2.243-3.865 3.469-4.303 3.752-.477-.309-2.143-1.823-4.303-3.752C5.141 14.072 2.5 12.167 2.5 9.122a4.989 4.989 0 0 1 4.708-5.218 4.21 4.21 0 0 1 3.675 1.941c.84 1.175.98 1.763 1.12 1.763s.278-.588 1.11-1.766a4.17 4.17 0 0 1 3.679-1.938m0-2a6.04 6.04 0 0 0-4.797 2.127 6.052 6.052 0 0 0-4.787-2.127A6.985 6.985 0 0 0 .5 9.122c0 3.61 2.55 5.827 5.015 7.97.283.246.569.494.853.747l1.027.918a44.998 44.998 0 0 0 3.518 3.018 2 2 0 0 0 2.174 0 45.263 45.263 0 0 0 3.626-3.115l.922-.824c.293-.26.59-.519.885-.774 2.334-2.025 4.98-4.32 4.98-7.94a6.985 6.985 0 0 0-6.708-7.218Z"></path></svg>
        <svg class="mx-3" aria-label="Comment" color="rgb(0,0,0)" fill="rgb(0,0,0)" height="24" role="img" viewBox="0 0 24 24" width="24"><title>Comment</title><path d="M20.656 17.008a9.993 9.993 0 1 0-3.59 3.615L22 22Z" fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="2"></path></svg>
        <svg aria-label="Share" color="rgb(0,0,0)" fill="rgb(0,0,0)" height="24" role="img" viewBox="0 0 24 24" width="24"><title>Share</title><line fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="2" x1="22" x2="9.218" y1="3" y2="10.083"></line><polygon fill="none" points="11.698 20.334 22 3.001 2 3.001 9.218 10.084 11.698 20.334" stroke="currentColor" stroke-linejoin="round" stroke-width="2"></polygon></svg>
        <svg class="float-right ml-60" aria-label="Save" color="rgb(0,0,0)" fill="rgb(0,0,0)" height="24" role="img" viewBox="0 0 24 24" width="24"><title>Save</title><polygon fill="none" points="20 21 12 13.44 4 21 4 3 20 3 20 21" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></polygon></svg>
    </div>
    <div>
        <p class="m-2 font-bold text-sm text-black">{likeCount > 1000 ? likeCount.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",") : likeCount} likes</p>
        <p class="text-black m-2 relative -top-1 text-sm">{username} <span class="text-black/70">{content}</span></p>
        <p class="text-black/50 m-2 relative -top-2 text-sm">see all {commentsCount} comment</p>
        <p class="text-black/50 m-2 relative -top-3 text-sm">Add a comment... <span class="float-right"><svg aria-label="İfade Simgesi" class="relative top-1.5 opacity-50" color="rgb(0,0,0)" fill="rgb(0,0,0)" height="13" role="img" viewBox="0 0 24 24" width="13"><title>İfade Simgesi</title><path d="M15.83 10.997a1.167 1.167 0 1 0 1.167 1.167 1.167 1.167 0 0 0-1.167-1.167Zm-6.5 1.167a1.167 1.167 0 1 0-1.166 1.167 1.167 1.167 0 0 0 1.166-1.167Zm5.163 3.24a3.406 3.406 0 0 1-4.982.007 1 1 0 1 0-1.557 1.256 5.397 5.397 0 0 0 8.09 0 1 1 0 0 0-1.55-1.263ZM12 .503a11.5 11.5 0 1 0 11.5 11.5A11.513 11.513 0 0 0 12 .503Zm0 21a9.5 9.5 0 1 1 9.5-9.5 9.51 9.51 0 0 1-9.5 9.5Z"></path></svg></span></p>
    </div>
</div>