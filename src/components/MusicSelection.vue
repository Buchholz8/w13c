<template>
  <div>
    <section>
      <h2 v-if="selected === false">Please Select A Song</h2>
      <div v-for="(songs, i) in songs" :key="i">
        <p>{{ songs.title }}</p>
        <p>{{ songs.artist }}</p>
        <img :src="songs.image_url" alt="idk what to put here" />
        <button @click="selected_song" :key="songs.title">play</button>
      </div>
    </section>
    <section>
      <h2>PLaying...</h2>
      <p class="active"></p>
      <p>This is as far as i could make it without having to make each song individually and just hiding the playing tags, i couldnt figure out a way to save what button was pressed , and transfer that to the new tag ,  </p>
    </section>
  </div>
</template>

<script>
export default {
  methods: {
selected_song : function(details) {
  if(this.selected === true){
    this.selected = true
  } else {
    this.selected = !this.selected
  }
details[`target`].getAttriobute(`key`)
let playing = document.querySelector(`.active`)
playing[`innerHTML`] = `key`
}
  },
  data() {
    return {
      selected: false,
      songs: [
        {
          title: `You Proof`,
          artist: `Morgan Wallen`,
          song_id: 1,
          image_url: `data:image/jpeg;base64,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`,
        },
        {
          title: `Thinkin'Bout Me`,
          artist: `Morgan Wallen`,
          song_id: 2,
          image_url: `data:image/jpeg;base64,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`,
        },
      ],
    };
  },
};
</script>

<style scoped>
div {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
</style>