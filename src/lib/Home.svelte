<script>
  import Footer from "../components/Footer.svelte";
</script>

<section class="text-center">
    <h1 class="text-3xl font-extrabold sm:text-5xl mt-32">Fakegram</h1>
    <p class="text-lg relative top-3 opacity-90 sm:text-xl text-gray-700 sm:block p-2">Ready to create a <span class="text-black font-extrabold">fake post</span> for Instagram?</p>
    <a class="inline-block px-8 py-3 text-sm font-medium text-white bg-[#333] drop-shadow-md relative top-7 rounded focus:ring" href="https://github.com/Queaxtra/Fakegram">
        <i class="fa-brands fa-github"></i> Github
    </a>
    <a class="inline-block px-8 py-3 text-sm font-medium text-white bg-[#5865F2] drop-shadow-md relative top-7 rounded focus:ring" href="https://is.gd/unoxdevs">
        <i class="fa-brands fa-discord"></i> Discord
    </a>
</section>

<section>
    <aside class="overflow-hidden sm:grid sm:grid-cols-2 mt-20">
  <div class="p-8 md:p-12 lg:px-16 lg:py-24">
    <div class="max-w-xl mx-auto text-center sm:text-left">
      <h2 class="text-2xl font-bold text-gray-900 md:text-3xl">
        How is it working?
      </h2>
      <p class="text-gray-500 md:mt-4 md:block">
        You can create your own fake post with our system. So how? Click on <b>"Create post"</b> at the top. Then fill in the sections on the side of the page that appears and press the <b>"Create"</b> button. And it finished. Making fake posts is that easy.
      </p>
    </div>
  </div>
  <div class="flex justify-center items-center drop-shadow-md">
    <img src="https://i.hizliresim.com/2tnk4af.jpg" class="rounded object-cover w-80 sm:ml-72 md:ml-2 md:w-96 lg:ml-72" />
  </div>
</aside>
</section>

<Footer />