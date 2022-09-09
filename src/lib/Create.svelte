<script>
    import Card from "../components/Card.svelte";
    let profilephoto = "";
    let username = "queaxtra";
    let posturl = "";
    let likecount = 0
    let content = "Fakegram is best 💖";
    let commentscount = 0
    let day = 0
    let verifyuser = false;
</script>

<div class="w-72 h-[100vh] bg-gray-200">
    <details class="group w-60 bg-gray-100 rounded relative top-5 left-1/2 -translate-x-1/2 drop-shadow-md">
        <summary class="flex items-center px-4 py-2 text-gray-500 rounded-lg cursor-pointer">
            <i class="fa-solid fa-image"></i>
            <span class="ml-3 text-sm font-medium">Profile Photo</span>
            <span class="ml-auto transition duration-300 shrink-0 group-open:-rotate-180">
                <i class="fa-solid fa-caret-down"></i>
            </span>
        </summary>
        <nav class="w-52 mt-1.5 flex ml-auto mr-auto left-0 right-0 flex-col bg-gray-100 rounded">
          <div class="flex items-center py-2 text-gray-500 rounded-lg">
            <i class="fa-solid fa-pencil"></i>
            <span class="ml-3 text-sm font-medium">
                <input type="text" class="bg-gray-200 w-44 rounded p-1" bind:value={profilephoto} placeholder="Enter a image URL">
            </span>
          </div>
        </nav>
    </details>

    <details class="group w-60 bg-gray-100 rounded relative top-5 left-1/2 -translate-x-1/2 drop-shadow-md my-3">
        <summary class="flex items-center px-4 py-2 text-gray-500 rounded-lg cursor-pointer">
            <i class="fa-solid fa-user-tag"></i>
            <span class="ml-3 text-sm font-medium">Username</span>
            <span class="ml-auto transition duration-300 shrink-0 group-open:-rotate-180">
                <i class="fa-solid fa-caret-down"></i>
            </span>
        </summary>
        <nav class="w-52 mt-1.5 flex ml-auto mr-auto left-0 right-0 flex-col bg-gray-100 rounded">
          <div class="flex items-center py-2 text-gray-500 rounded-lg">
            <i class="fa-solid fa-pencil"></i>
            <span class="ml-3 text-sm font-medium">
                <input type="text" class="bg-gray-200 w-44 rounded p-1" bind:value={username}>
            </span>
          </div>
        </nav>
    </details>

    <details class="group w-60 bg-gray-100 rounded relative top-5 left-1/2 -translate-x-1/2 drop-shadow-md my-3">
        <summary class="flex items-center px-4 py-2 text-gray-500 rounded-lg cursor-pointer">
            <i class="fa-solid fa-image"></i>
            <span class="ml-3 text-sm font-medium">Post</span>
            <span class="ml-auto transition duration-300 shrink-0 group-open:-rotate-180">
                <i class="fa-solid fa-caret-down"></i>
            </span>
        </summary>
        <nav class="w-52 mt-1.5 flex ml-auto mr-auto left-0 right-0 flex-col bg-gray-100 rounded">
          <div class="flex items-center py-2 text-gray-500 rounded-lg">
            <i class="fa-solid fa-pencil"></i>
            <span class="ml-3 text-sm font-medium">
                <input type="url" class="bg-gray-200 w-44 rounded p-1" placeholder="Enter a image URL" bind:value={posturl}>
            </span>
          </div>
        </nav>
    </details>

    <details class="group w-60 bg-gray-100 rounded relative top-5 left-1/2 -translate-x-1/2 drop-shadow-md my-3">
        <summary class="flex items-center px-4 py-2 text-gray-500 rounded-lg cursor-pointer">
            <i class="fa-solid fa-heart"></i>
            <span class="ml-3 text-sm font-medium">Like Count</span>
            <span class="ml-auto transition duration-300 shrink-0 group-open:-rotate-180">
                <i class="fa-solid fa-caret-down"></i>
            </span>
        </summary>
        <nav class="w-52 mt-1.5 flex ml-auto mr-auto left-0 right-0 flex-col bg-gray-100 rounded">
          <div class="flex items-center py-2 text-gray-500 rounded-lg">
            <i class="fa-solid fa-pencil"></i>
            <span class="ml-3 text-sm font-medium">
                <input type="number" min="0" class="bg-gray-200 w-44 rounded p-1" bind:value={likecount}>
            </span>
          </div>
        </nav>
    </details>

    <details class="group w-60 bg-gray-100 rounded relative top-5 left-1/2 -translate-x-1/2 drop-shadow-md my-3">
        <summary class="flex items-center px-4 py-2 text-gray-500 rounded-lg cursor-pointer">
            <i class="fa-solid fa-wand-magic-sparkles"></i>
            <span class="ml-3 text-sm font-medium">Content</span>
            <span class="ml-auto transition duration-300 shrink-0 group-open:-rotate-180">
                <i class="fa-solid fa-caret-down"></i>
            </span>
        </summary>
        <nav class="w-52 mt-1.5 flex ml-auto mr-auto left-0 right-0 flex-col bg-gray-100 rounded">
          <div class="flex items-center py-2 text-gray-500 rounded-lg">
            <i class="fa-solid fa-pencil"></i>
            <span class="ml-3 text-sm font-medium">
                <input type="text" class="bg-gray-200 w-44 rounded p-1" bind:value={content}>
            </span>
          </div>
        </nav>
    </details>

    <details class="group w-60 bg-gray-100 rounded relative top-5 left-1/2 -translate-x-1/2 drop-shadow-md my-3">
        <summary class="flex items-center px-4 py-2 text-gray-500 rounded-lg cursor-pointer">
            <i class="fa-solid fa-comments"></i>
            <span class="ml-3 text-sm font-medium">Comments Count</span>
            <span class="ml-auto transition duration-300 shrink-0 group-open:-rotate-180">
                <i class="fa-solid fa-caret-down"></i>
            </span>
        </summary>
        <nav class="w-52 mt-1.5 flex ml-auto mr-auto left-0 right-0 flex-col bg-gray-100 rounded">
          <div class="flex items-center py-2 text-gray-500 rounded-lg">
            <i class="fa-solid fa-pencil"></i>
            <span class="ml-3 text-sm font-medium">
                <input type="number" min="0" class="bg-gray-200 w-44 rounded p-1" bind:value={commentscount}>
            </span>
          </div>
        </nav>
    </details>

    <details class="group w-60 bg-gray-100 rounded relative top-5 left-1/2 -translate-x-1/2 drop-shadow-md my-3">
        <summary class="flex items-center px-4 py-2 text-gray-500 rounded-lg cursor-pointer">
            <i class="fa-solid fa-earth"></i>
            <span class="ml-3 text-sm font-medium">Day</span>
            <span class="ml-auto transition duration-300 shrink-0 group-open:-rotate-180">
                <i class="fa-solid fa-caret-down"></i>
            </span>
        </summary>
        <nav class="w-52 mt-1.5 flex ml-auto mr-auto left-0 right-0 flex-col bg-gray-100 rounded">
          <div class="flex items-center py-2 text-gray-500 rounded-lg">
            <i class="fa-solid fa-pencil"></i>
            <span class="ml-3 text-sm font-medium">
                <input type="number" min="0" class="bg-gray-200 w-44 rounded p-1" bind:value={day}>
            </span>
          </div>
        </nav>
    </details>
    
    <details class="group w-60 bg-gray-100 rounded relative top-5 left-1/2 -translate-x-1/2 drop-shadow-md my-3">
        <summary class="flex items-center px-4 py-2 text-gray-500 rounded-lg cursor-pointer">
            <i class="fa-solid fa-user-check"></i>
            <span class="ml-3 text-sm font-medium">Verify User</span>
            <span class="ml-auto transition duration-300 shrink-0 group-open:-rotate-180">
                <i class="fa-solid fa-caret-down"></i>
            </span>
        </summary>
        <nav class="w-52 mt-1.5 flex ml-auto mr-auto left-0 right-0 flex-col bg-gray-100 rounded">
          <div class="flex items-center py-2 text-gray-500 rounded-lg">
            <i class="fa-regular fa-hand-pointer relative -top-0.5"></i>
            <span class="-ml-16 text-sm font-medium">
                <input type="checkbox" min="0" class="bg-gray-200 w-44 rounded p-1" bind:checked={verifyuser}>
                {#if verifyuser}
                    <span class="-ml-20 relative -top-0.5 text-sm font-medium">Verified User</span>
                {:else}
                    <span class="-ml-20 relative -top-0.5 text-sm font-medium">Not Verified</span>
                {/if}
            </span>
          </div>
        </nav>
    </details>
</div>

<Card {profilephoto} {username} {posturl} {likecount} {content} {commentscount} {day} {verifyuser} />