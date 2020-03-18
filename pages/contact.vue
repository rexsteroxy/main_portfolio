<template>
  <div class="flex">
    <div class="w-490px flex-grow-0">
      <form class="bg-black shadow p-10 mb-10" @submit.prevent="">
        <p class="text-white text-xl font-bold mb-10">Send a message</p>
        <fe-field
          v-model="form.name"
          label="Your Name"
          type="text"
          class="mb-8"
        />

        <fe-field
          v-model="form.email"
          label="Your Email"
          type="email"
          class="mb-8"
        />

        <fe-field
          v-model="form.message"
          label="Your Message"
          type="textarea"
          class="mb-8"
        />

        <button
          class="uppercase text-white font-black tracking-widest w-full text-center p-3 rounded-full bg-blue"
        >
          Send
        </button>
      </form>

      <google-maps :lat="5.47631" :lng="7.025853" :zoom="4" class="h-300px" />
    </div>

    <div class="flex-1 pl-8">
      <div class="max-w-3/5">
        <h1 class="uppercase text-4xl font-black leading-none mb-10">
          Contact me
        </h1>

        <div class="list-group">
          <div class="list-group-item">
            <p class="item-title">Email</p>
            <p><a href="rexsteroxy22@gmail.com">rexsteroxy22@gmail.com</a></p>
          </div>
          <div class="list-group-item">
            <p class="item-title">Phone</p>
            <p><a href="tel:+2349037096290">+2349037096290</a></p>
          </div>
          <div class="list-group-item">
            <p class="item-title">Address</p>
            <p>
              Orji Opposite Blessed Tansi Catholic Church, Owerri Imo
              state,Nigeria.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Field from '~/components/Field'
import GoogleMaps from '~/components/GoogleMaps'

export default {
  components: {
    FeField: Field,
    GoogleMaps
  },

  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  }
}
</script>
