<template>
  <div>
    <CharacterRace />
  </div>
</template>

<script>
import CharacterRace from './CharacterRace.vue'
export default {
  name: 'Questionarre',
  components: {
    CharacterRace,
  },
  data() {
    return {
      isFinished: false,
    }
  },

}
</script>