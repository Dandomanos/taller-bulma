<template>
	<div class="modal">
		<div class="modal-background"></div>
		<div class="modal-content">
			<!-- <div class="box">
				Mensaje enviado correctamente
			</div> -->
			<div class="notification is-primary">
				Mensaje enviado correctamente
			<a href="" class="delete" @click.prevent="close"></a>
		</div>
	</div>
		
		<!-- <button class="modal-close is-large" @click="close"></button> -->
	</div>
</template>
<script>
export default {
    methods: {
        close(){
            this.$emit('close')
        }
    }
}
</script>

