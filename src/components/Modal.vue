<template>
	<div class="modal">
		<div class="modal-background"></div>
		<div class="modal-content">
			<div class="box">
				Mensaje enviado correctamente
			</div>
		</div>
		<button class="modal-close is-large" @click="close"></button>
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

