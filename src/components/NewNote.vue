<template>
	<div class="row" style="text-align: center;">
		<form class="new" >
			<div class="col-sm-8 col-xs-12 col-md-6">
				
				<textarea rows="2" v-model="note" style="width: 400px; border: 1px solid black;"></textarea>
				<br>
				<button @click.prevent="createNew" class="btn" >Add Note</button>
				
			</div>
				
			
		</form>
	</div>
</template>

<script>
	 
	 export default {
	 	data: function() {
	 		return {
	 			note: ''
	 		};
	 	},
	 	methods: {
	 	   createNew() {
	 	   	  this.$emit('noteAdded', this.note);
	 	   	  this.note = '';
	 	   }	
	 	}
	 }
	
</script>

<style>
	  .new {
	       position: absolute;
  top: 230px;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;	
	  }
   .btn {
   	float: left;
   	border: 1px solid #ff6464;
   	color: #ff6464;
   	background: transparent;
   }
   .btn:hover{
   	background-color: #ff6464;
   	color: white;
   }
</style>