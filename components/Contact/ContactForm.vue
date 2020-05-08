<template lang="pug">
  v-row(justify='center')
    v-dialog(v-model='value'
            persistent 
            max-width='600px')
      v-card
        v-card-title
          span.headline.center Contact me!
        v-card-text
          //- (@submit="onSubmit")
          v-form
            v-text-field( v-model='name'
                          :value="name"
                          @input="setName($event)"
                          :error-messages="nameErrors"
                          :counter='20'
                          label='Name*'
                          hint='Write your complet name'
                          outlined
                          )
            v-text-field( v-model='email'
                          :value="email"
                          @input="setEmail($event)"
                          :error-messages="emailErrors"
                          label='E-mail*'
                          outlined
                          )
            v-select( v-model='subject'
                      :items="['Bodas', 'Publicidad', 'Editoriales de moda']" 
                      :value="subject"
                      @input="setSubject($event)"
                      :error-messages="subjectErrors"
                      label='Subject*'
                      outlined
                      )
            v-select( v-model='interest'
                      :items="['MakeUp', 'Peinado', 'Maquillaje y Peinado']"
                      :value="interest"
                      @input="setInterest($event)"
                      :error-messages="interestErrors"
                      label='Interest*'
                      outlined
                      )
            v-textarea( v-model='content'
                        :value="interest"
                        @input="setInterest($event)"
                        :error-messages="interestErrors"
                        label='Interest*'
                        outlined
                        )
          small *indicates required field
          v-card-actions
            v-spacer
            v-btn(color='#2e5665'
                  @click='$emit("input", false)'
                  outlined) Close
            v-btn(color='#2e5665'
                  @click='onSubmit'
                  :disabled="$v.$invalid"
                  outlined) Send
                  //- type="submit"
</template>

<script>
// hsla(7, 24%, 86%, 1) hsla(27, 33%, 74%,0.8)
// border: 10px dotted 	hsla(27, 33%, 74%,0.8);
import { validationMixin } from "vuelidate";
import { required, maxLength, email } from "vuelidate/lib/validators";

export default {
  mixins: [validationMixin],
  data() {
    return {
      name: "",
      email: "",
      subject: "",
      interest: "",
      content: ""
    };
  },
  props: {
    value: {
      type: Boolean,
      default: false
    }
  },
  validations: {
    name: { required, maxLength: maxLength(20) },
    email: { required, email },
    subject: { required },
    interest: { required },
    content: { maxLength: maxLength(100) }
  },
  computed: {
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Name must be at most 20 characters long");
      !this.$v.name.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    },
    subjectErrors() {
      const errors = [];
      if (!this.$v.subject.$dirty) return errors;
      !this.$v.subject.required && errors.push("Subject is required");
      return errors;
    },
    interestErrors() {
      const errors = [];
      if (!this.$v.interest.$dirty) return errors;
      !this.$v.interest.required && errors.push("Interest is required");
      return errors;
    },
    contentErrors() {
      const errors = [];
      if (!this.$v.content.$dirty) return errors;
      !this.$v.content.maxLength &&
        errors.push("Content must be at most 100 characters long");
      return errors;
    }
  },
  methods: {
    onSubmit() {
      this.sendMyEmail();
      this.sendClientEmail();
      this.clear();
      // nuria@nuriariobo.es
      // Host: "smtp.ionos.es",
      // Username: "nuria@nuriariobo.es",
      // Password: "Nuriariobomola93!", riobonuria@gmail.com
    },
    setName(value) {
      this.name = value;
      this.$v.name.$touch();
    },
    setEmail(value) {
      this.email = value;
      this.$v.email.$touch();
    },
    setSubject(value) {
      this.subject = value;
      this.$v.subject.$touch();
    },
    setInterest(value) {
      this.interest = value;
      this.$v.interest.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = "";
      this.email = "";
      this.subject = null;
      this.interest = null;
      this.content = "";
    },
    sendMyEmail() {
      Email.send({
        SecureToken: "a8d676fb-a071-4f99-b726-81f23407070a",
        To: "riobonuria@gmail.com",
        From: "nuria@nuriariobo.es",
        Subject: `${this.subject}`,
        Body:
          "<html><h2>La clienta: " +
          `${this.name}` +
          "</h2>" +
          "<br>Ha hecho una solicitud solicitud para: " +
          "<strong> " +
          `${this.interest}` +
          " de " +
          `${this.subject}` +
          "</strong>" +
          ". Incluyendo el siguiente mensaje: " +
          "<br>" +
          "<em>“" +
          `${this.content}` +
          "”</em>" +
          "<br>" +
          "<br><strong>Contacta con ella!!!</strong></br>"
      })
        .then(message => {
          this.$emit("input", false);
        })
        .catch(e => console.log(e));
    },
    sendClientEmail() {
      Email.send({
        SecureToken: "a8d676fb-a071-4f99-b726-81f23407070a",
        To: this.email,
        From: "nuria@nuriariobo.es",
        Subject: `${this.subject}`,
        Body:
          "<html><h2>NURIA RIOBÓ MUAH</h2>" +
          "<strong>Bienvenida " +
          `${this.name}` +
          ",</strong>" +
          "<br>" +
          "<br>Muchas gracias por contactar.</br>" +
          "<br>He recibido tu solicitud para " +
          `${this.interest}` +
          " de " +
          `${this.subject}` +
          ". Me pondré en contacto contigo lo antes posible." +
          "<br>" +
          "<br>Un saludo</br>" +
          "<br>" +
          "<br><em>Nuria Riobó</em></br></html>"
        // Attachments: [
        //   {
        //     name: "kkkk.png",
        //     data: "~/assets/images/kkkk.png"
        //   }
        // ]
      })
        .then(message => alert("Mail sent successfully"))
        .catch(e => console.log(e));
    }
  }
};
</script>

<style scoped>
.center {
  margin: 0 auto;
}
</style>
