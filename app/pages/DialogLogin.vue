<script setup>
    const modalStore = useModalStore();
</script>

<template>
    <Dialog
        :header="$t('login')"
        v-model:visible="modalStore.displayModal"
        :breakpoints="{ '960px': '75vw', '640px': '90vw' }"
        :style="{ width: '50vw' }"
        :position="position"
        :modal="true"
    >
        <!-- login component form -->
        <FormLogin />

        <!-- footer template -->
        <template #footer>
            <Button
                :label="$t('cancel')"
                icon="pi pi-times"
                @click="modalStore.closeModal()"
                class="p-button-text"
            />
        </template>
    </Dialog>
</template>