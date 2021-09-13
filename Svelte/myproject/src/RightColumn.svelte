<script>
    import LeftColumn from "./LeftColumn.svelte";
    
    $: textPath = "./texts/" + stringCount + ".txt";
    let tcount=24;
    $: stringCount = String(tcount);

 function handleEvent(event) {
    event.preventDefault()
    tcount = (event.detail.counter) -1;
    console.log(tcount);
    stringCount = String(tcount);
    textPath = "./texts/" + stringCount + ".txt";
    
 };
    
</script>


<main>
    <div class="column" style="background-color:white;" >
        <h2> Column 2 </h2>
        
        <br />
        <br />
        <br />
      
        <iframe title= "ocr-text" id="text" src={textPath} on:click={handleEvent} ></iframe>
      
    </div>
</main>

<style>
    .column {
  flex: 60%;
  padding: 10px;
  background-color:#e6f3ff;
  flex-wrap: wrap;
  height: calc(100vh);

}
#try {
  font-size: 20px;
  font-family: monospace;
}
</style>