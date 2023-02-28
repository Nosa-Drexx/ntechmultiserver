<script>
export default {
  data: () => ({
    name: '',
    email: '',
    subject: '',
    message: ''
  }),
  methods: {
    sumbitForm() {
      console.log(this.name, this.email, this.subject, this.message)
      //Do async thing
    }
  }
}
</script>

<template>
  <section :class="$style.contact" id="contact">
    <div :class="$style['contact-info']">
      <h2 :class="$style.h2">Contact Us</h2>
      <p :class="$style.p">Contact us for free estimate.</p>
      <form :class="$style['contact-form']" @submit.prevent="sumbitForm">
        <div :class="$style['input-required']">
          <input
            name="name"
            type="text"
            v-model="name"
            :class="$style.input"
            id="name"
            placeholder="Name *"
            required="true"
          />
          <input
            name="email"
            type="email"
            v-model="email"
            :class="$style.input"
            id="name"
            placeholder="Email *"
            required="true"
          />
          <input
            name="name"
            type="text"
            v-model="subject"
            :class="$style.input"
            id="name"
            placeholder="Subject"
          />
        </div>
        <div :class="$style['text-area-container']">
          <textarea
            name="message"
            :class="$style['text-area']"
            v-model="message"
            placeholder="Message"
          ></textarea>
          <input type="submit" :class="$style.submit" value="Send" />
        </div>
      </form>
    </div>
  </section>
</template>

<style module>
.contact {
  width: 100%;
  background: var(--blue);
  display: flex;
  justify-content: center;
}
.contact-info {
  width: 100%;
  max-width: 800px;
  padding: 1rem;
  display: flex;
  flex-flow: column nowrap;
  gap: 1rem;
  width: 100%;
}
.h2,
.p {
  margin: 0;
  padding: 0;
  color: var(--white);
}
.input,
.text-area {
  border: 5px solid var(--green);
  font-size: 1.5rem;
  padding: 0.3rem;
  background: var(--white);
  border-radius: 10px;
  width: 100%;
}
.input:hover,
.text-area:hover {
  background: var(--green);
}
.input-required {
  width: 100%;
  display: flex;
  flex-flow: column nowrap;
  gap: 1rem;
}
.contact-form {
  display: flex;
  flex-flow: column nowrap;
  gap: 1rem;
}
.text-area-container {
  width: 100%;
  display: flex;
  flex-flow: column nowrap;
  gap: 1rem;
}
.text-area {
  resize: none;
  padding-top: 1.3rem;
  height: 200px;
}
.submit {
  background: var(--orange);
  padding: 0.5rem;
  font-size: 1.5rem;
  color: var(--white);
  font-weight: bold;
  width: 20%;
  border-radius: 5px;
  align-self: flex-end;
}

@media (min-width: 800px) {
  .contact-form {
    display: flex;
    flex-flow: row nowrap;
    gap: 1rem;
  }
  .input,
  .text-area {
    border: 3px solid var(--green);
  }
  .input-required {
    width: 48%;
  }

  .text-area-container {
    width: 48%;
  }

  .text-area {
    height: 189px;
  }
}
</style>
