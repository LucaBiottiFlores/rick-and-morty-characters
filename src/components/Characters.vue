<template>
    
    <div id="Characters">
        <div class="characterListContainer d-flex flex-column flex-wrap">
          <div class="character d-flex flex-wrap my-3 mx-3" v-for="(character, index) in characters" :key="index">
              <img class="characterImg" v-bind:src="character.src">
              <p class="characterText my-auto mx-4"> {{ character.name }} </p>
          </div>
        </div>
    </div>

</template>

<script>
export default {
    name: 'Characters',
    data: () => ({
        characters: [
            {name: "Rick Sanchez", src:"https://rickandmortyapi.com/api/character/avatar/1.jpeg"},
            {name: "Morty Smith", src:"https://rickandmortyapi.com/api/character/avatar/2.jpeg"},
            {name: "Summer Smith", src:"https://rickandmortyapi.com/api/character/avatar/3.jpeg"},
            {name: "Beth Smith", src:"https://rickandmortyapi.com/api/character/avatar/4.jpeg"},
            {name: "Jerry Smith", src:"https://rickandmortyapi.com/api/character/avatar/5.jpeg"},
        ]
    }),
}
</script>

<style>
    .characterImg {
        width: 150px;
        border-radius: 50%;
    }
    .characterText {
        font-size: 30px;
        color: green;
    }
    .characterListContainer {
        margin-bottom: 200px;
    }
</style>