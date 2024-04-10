<script>

let queueList = [
    { name: "Karolina", sted: "Amfiet" },
    { name: "Julian", sted: "Utsikten" },
    { name: "Sara", sted: "Blåbås" },
    { name: "Henrik", sted: "Langbord" },
    { name: "Erik", sted: "Grønnbås" },
    { name: "Tidemann", sted: "Amfiet" },
];

</script>


<div class="queueGridContainer">
    <div class="queueGrid">
        <div class="kContainer">
            <h1>Kø</h1>
            <div class="ActiveQueue">
                <div class="queueItems">
                    {#each queueList as person}
                        <div class="queueItem">
                            <p class="nameList">Navn: {person.name}</p> 
                            <p class="place"> Sted: {person.sted}</p>
                        </div>
                    {/each}
                </div>
            </div>
        </div>
    </div>
</div>

<style>
.queueGridContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 15px;
    overflow: scroll;
}

.queueGrid {
    border: 3px solid red;
    width: 400px;
    height: 400px;
    background-color: white;
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

.nameList{
    margin-right: 20px;
}

</style>