<template>
  <v-container>
    <v-layout
      text-xs-center
      wrap
    >
      <v-flex xs12>
        <v-img
          src="/logo.png"
          class="my-2"
          contain
          height="200"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <!-- <h1 class="font-weight-bold mb-3">
          Welcome To Cartenz Frontend Web Developer Test
        </h1> -->
        <h2 class="headline font-weight-bold mb-3">
          Disini anda akan di test membuat alikasi CRUD sederhana,
          <br>menggunakan vue.js dan vuetify
        </h2>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">Faktor Penilaian</h2>

        <v-layout justify-center>
          <a
            v-for="(d, i) in harapan"
            :key="i"
            :href="d.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ d.text }}
          </a>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">Limitasi</h2>

        <v-layout justify-center>
          <a
            v-for="(e, i) in caraMengerjakan"
            :key="i"
            :href="e.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ e.text }}
          </a>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">Kerjakan Menggunakan</h2>

        <v-layout justify-center>
          <a
            v-for="(f, i) in appsDigunakan"
            :key="i"
            :href="f.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ f.text }}
          </a>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      appsDigunakan: [
        {
          text: 'Vue.JS',
        },
        {
          text: 'Vuetify',
        }
      ],
      caraMengerjakan: [
        {
          text: 'Tidak boleh akses internet',
        },
        {
          text: 'Dapat dijalankan di chrome',
        }
      ],
      harapan: [
        {
          text: 'Struktur kode',
        },
        {
          text: 'Logika',
        },
        {
          text: 'Reusability Code',
        },
        {
          text: 'Aplikasi dapat di jalankan dengan baik',
        }
      ]
    })
  }
</script>

<style>

</style>
