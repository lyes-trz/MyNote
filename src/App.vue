<template>
          <div class="container">
            <app-header :noteCount="notes.length" :maxNotes="maxNotes"></app-header>
            <app-new-note @noteAdded="newNote"></app-new-note>
            <app-note-grid :notes="notes" @noteDeleted="deleteNote"></app-note-grid>
          </div>

</template>

<script>
    import NoteGrid from './components/NoteGrid.vue';
    import NewNote from './components/NewNote.vue';
    import Header from './components/Header.vue';
    export default {
       data: function() {
         return {
            notes: [
              'test note'
            ],
            maxNotes: 10
         }
       },
       methods: {
         newNote(note) {
          if (this.notes.length >= this.maxNotes){
              return alert('Please delete notes first');
          } 
            this.notes.push(note);
         },
         deleteNote(index) {
           this.notes.splice(index, 1);
         }
       },
       components: {
        appNoteGrid: NoteGrid,
        appNewNote: NewNote,
        appHeader: Header
       }
   }
</script>

<style lang="scss">

</style>
