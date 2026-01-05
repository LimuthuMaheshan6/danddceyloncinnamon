<script lang="ts">
    let productData = ""
    import { onMount } from "svelte";

interface Products {
    name: string;
    price: string;
    img: string;
}


let productCards= [
    {name: "", price: "", img: ""},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},
    {},


];


function productDataFunc() {
    console.log("Product: ", productData)
}

</script>

<section class="bg-[#441f1f] w-full  pb-[60px]">


<br><br><br>
    
    
        
        <form  class="bg-[#441f1f]  mx-auto flex flex-col items-center" on:submit={() => productDataFunc()}>
            <input type="text"  bind:value={productData}  class="fixed w-64 h-10 bg-amber-200/80 backdrop-blur-2xl rounded-3xl outline-amber-600 border-2 border-amber-900"  placeholder="            Search Cinnamon">
        </form>

        <br><br><br>

        <section class="m-1 flex flex-row justify-center flex-wrap gap-[10px]">

            {#each productCards as item}



               <div class="w-[300px] h-[300px] bg-amber-100 rounded-2xl flex flex-col items-center">
                <img class="h-[250px] w-[250px]" src="" alt="product">
                <p class="name mx-1">Cinnamon Wafers</p>
                <p class="text-[red] mx-1">Rs. 100</p>
               </div>
        
             {/each}
           
        </section>



</section>    




