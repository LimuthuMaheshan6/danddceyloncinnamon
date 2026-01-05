<script lang="ts">
    import {page} from "$app/stores"
    import "./Footer.scss"

    let FooterItems = [
        {path: "/products", name: "Products"},
        {path: "/contact", name: "Contact"},

    ]
</script>



<footer class="bg-[#6d6027]">
    <div class="w-full flex justify-center gap-5   min-md:gap-[60px] flex-wrap">

        <div class="w-[300px] min-md:w-[500px] min-md:h-[250px] flex flex-col justify-center items-center">
            <a href="/">
                <p class="text-white text-[29px]">D&D Ceylon Cinnamon</p>
            </a>
            <p class="text-[#b4b4b4] font-bold text-[15px] text-center">"Helping societies by exporting cinnamon world wide."</p>
        </div>
        <div class=" w-[300px] min-md:h-[250px] flex flex-col items-center justify-center -translate-y-0">
            

            {#each FooterItems as item}
                <a class="hover:text-white text-amber-100" href={item.path}>{item.name}</a>                
            {/each}
        </div>


    </div>

</footer>
