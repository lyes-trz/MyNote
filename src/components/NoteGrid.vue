<template>
	<div class="row grid">
		<app-note v-for="(note, index) in notes" @click.native="deleteNote(index)">{{ note }}</app-note>
	</div>
</template>

<script>
	 import Note from './Note.vue';
	 export default {
	 	props: ['notes'],
	 	components:{
	 		appNote: Note
	 	},
	 	methods: {
	 		deleteNote(index) {
               this.$emit('noteDeleted', index);
	 		}
	 	}
	 }
	
</script>

<style>
	.grid {
		margin-top: 250px;
	}
</style>