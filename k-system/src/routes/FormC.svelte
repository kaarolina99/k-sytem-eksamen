<script>
    import QueueComponent from "./QueueComponent.svelte";
    // import {addToQueue} from "./QueueComponent.svelte";


    export let queueList

    let navnInput = "";
    
    let stedInput = "";


        function handleSubmit(event){
            event.preventDefault();
            addToQueue(navnInput, stedInput);
            console.log(queueList)
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
                <form id="queueList" on:submit={handleSubmit}>
                    <label for="Navn"> Navn </label>
                    <br />
                    <input
                        type="text"
                        id="Navn_"
                        name="navn"
                        bind:value={navnInput}
                        on:keydown={handleKeyDown}
                    />
                    <br />
                    <label for="Sted"> Sted </label>
                    <br />
                    <input
                        type="text"
                        id="Sted_"
                        name="sted"
                        bind:value={stedInput}
                        on:keydown={handleKeyDown}
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
        margin-bottom: 25px;
    }
    
    .formsGrid {
        border: 3px solid #E2BCF6;
        width: 400px;
        height: 400px;
        background-color: #ffb575;
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
    
