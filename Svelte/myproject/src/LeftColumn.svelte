<script>
    //export let imagePathLeft="./images/Sanskrit-Sahitya-Kaumudi-025.jpg";
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
    $: imagePath = "./images/Sanskrit-Sahitya-Kaumudi-0" + stringCount + ".jpg";
    export let count =25;
    $: stringCount = String(count);
    console.log(imagePath);

    function loadPrevImage() {
        count = count- 1;
        stringCount = String(count);
        imagePath = imagePath;
    };
    
    function loadNextImage() {
        count = count+ 1;
        stringCount = String(count);
        imagePath = imagePath;
        dispatch({counter: count});
    };


</script>


    <div class="column">
        <h2>Column 1</h2>
          <button id="button-left" class="button" on:click={loadPrevImage} >
            <div class="button__arrow button__arrow--left"></div>
  
            Back
            ...
          </button>
          <br />
          
          
          <img id="image" src={imagePath} >
           
          <br />
  
          <button class="button" id="button-right" on:click={loadNextImage}>
  
            Next
            ...
            <div class="button__arrow button__arrow--right"></div>
          </button>
  
      </div>


<style>
    .column {
  flex: 60%;
  padding: 10px;
  background-color:#e6f3ff;
  flex-wrap: wrap;
  height: calc(100vh);

}

#image {
   width: 90%;
   height: 80%;

}

</style>