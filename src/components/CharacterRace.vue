<template>
  <div>
    <h1>Character Race</h1>
    <select name="characterRaces" id="">
      <option 
        :value="race.name" 
        v-for="race in characterRaces"
        :key="race.index"
      >
        {{ race.name }}
      </option>
    </select>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'CharacterRace',
  data() {
    return {
      apiResponse: [],
      characterRaces: [],
    }
  },
  async mounted() {
    const apiResponse = await axios.get('https://www.dnd5eapi.co/api/races')
    console.log(apiResponse);
    this.characterRaces = apiResponse.data.results
  },
}
</script>