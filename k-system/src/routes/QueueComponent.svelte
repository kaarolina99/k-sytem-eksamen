<script> 


let queueList = [];

export function addToQueue(navnInput, stedInput) {
        queueList.push({navn: navnInput, sted: stedInput})
        console.log("hallo")
    }


</script>

<div class="queueGridContainer">
    <div class="queueGrid">
        <div class="kContainer">
            <h1>Kø</h1>
            <div class="ActiveQueue">
                <div class="queueItems">
                    {#each queueList as person}
                        <div class="queueItem">
                            <p class="navnPosition">Navn: {person.name}<p> 
                            <p class="stedPosition"> Sted: {person.sted}</p>
                        </div>
                    {/each}
                </div>
            </div>
        </div>
    </div>
</div>

<!-- <FormC bind:addToQueue={addToQueue}/> -->


<style>
.queueGridContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 15px;
    overflow: scroll;
}

.queueGrid {
    border: 3px solid #E2BCF6;
    width: 400px;
    height: 400px;
    background-color: #ffb575;
    overflow: scroll;
}

.kContainer {
    text-align: center;
}

.queueItem{
    display: flex;
    justify-content: center;
    align-items: center;
}

.navnPosition{
    margin-right: 20px;
}




</style> 