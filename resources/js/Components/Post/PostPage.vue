<template>
  <jet-form-section @submitted="submitForm">
    <template #title>{{ this.post.name }}</template>

    <template #description> Information de l'article </template>

    <template #form>
      <!-- Name -->
      <div class="col-span-6 sm:col-span-4 title">
        {{ this.post.name }}
      </div>

      <!-- Content -->
      <div class="col-span-6 sm:col-span-4">
        <jet-label for="content" value="Contenu" />
        {{ this.post.content }}
      </div>
    </template>
  </jet-form-section>
</template>

<script>
import JetActionMessage from "@/Jetstream/ActionMessage";
import JetButton from "@/Jetstream/Button";
import JetFormSection from "@/Jetstream/FormSection";
import JetInput from "@/Jetstream/Input";
import JetInputError from "@/Jetstream/InputError";
import JetLabel from "@/Jetstream/Label";
import JetSecondaryButton from "@/Jetstream/SecondaryButton";

export default {
  props: ["errors", "post"],

  components: {
    JetActionMessage,
    JetButton,
    JetFormSection,
    JetInput,
    JetInputError,
    JetLabel,
    JetSecondaryButton,
  },
  data() {
    return {
      form: this.$inertia.form({
        name: this.post ? this.post.name : "",
        content: this.post ? this.post.content : "",
      }),
    };
  },

  methods: {},
};
</script>

<style>
.title {
  font-size: 35px;
}
</style>
