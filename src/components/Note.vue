<template>
	<div class="col-sm-6 col-md-4 col-lg-3">
		<div class="note">
			  <slot></slot>
		</div>
	</div>
</template>

<script>
	 export default {
	 	props: ['notes']
	 }
	
</script>

<style>
	.note {
		border: 1px solid black;
		padding: 15px;
		cursor: pointer;
		font-size: 15px;
		text-align: center;
		margin-bottom: 10px;

	}
	.note:hover {
		background-color: #ff6464;
		border-color: #ff6464;
		color: white;
	}

</style>