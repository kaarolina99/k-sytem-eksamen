<script>
import QueueComponent from "./QueueComponent.svelte";

export let queueList 

let navnInput

let stedInput

function printConsoleLog(){
    console.log(navnInput, stedInput)
}

function handleKeyDown(event){
    if (event.keyCode === 13) {
        console.log("Enter key was pressed");
    }
}

</script>



<QueueComponent data={queueList}></QueueComponent>

<div class="formsGridContainer">
    <div class="formsGrid">
        <div class="sContainer">
            <h1>Skriv deg opp i kø</h1>
            <form id="queueData" on:submit={printConsoleLog}>
                <label for="Navn"> Navn </label>
                <br />
                <input
                    on:keydown={handleKeyDown}
                    type="text"
                    id="Navn_"
                    name="Navn"
                    bind:value={
                        navnInput
                    }
                />
                <br />
                <label for="Sted"> Sted </label>
                <br />
                <input
                on:keydown={handleKeyDown}
                    type="text"
                    id="Sted_"
                    name="Sted"
                    bind:value={
                        stedInput
                    }
                />
                <br /><br />
                <input type="Submit" value="Submit">
            </form>
        </div>
    </div>
</div>



<style>
.formsGridContainer {
    display: flex;
    justify-content: center;
    align-items: center;
}

.formsGrid {
    border: 3px solid red;
    width: 400px;
    height: 400px;
    background-color: white;
}

.sContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    height: 100%;
}

</style>

<!-- onKeyDown={handleKeyDown} -->