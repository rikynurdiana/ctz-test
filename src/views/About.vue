<template>
  <div class="container">
    <h2>Terdapat data berbentuk biodata dengan field berikut</h2>
    <ol>
      <li>nama (input text)</li>
      <li>jenis kelamin (select option)</li>
      <li>umur (input number)</li>
      <li>hoby (multiple select)</li>
      <li>alamat (input text area)</li>
    </ol>

    <br>
    <hr>
    <br>

    <h2>Soal</h2>
    <ol>
      <li>Buatlah table untuk menampilkan data-data tersebut</li>
      <li>Buatlah dialog untuk mengisi form pada action create, edit, dan view data</li>
      <li>Buatlah alert untuk setiap action create, edit dan delete yang disubmit</li>
    </ol>

    <br>
    <hr>
    <br>

    <p>Tampilkan hasil kerja anda di halaman ‘Jawaban’</p>
    <h2>Notes</h2>
    <ol>
      <li>Simpan data hasil crate ke dalam memory (jika halaman di refresh, data akan hilang)</li>
      <li>Jika dapat menggunakan vuex untuk store data akan mendapatkan nilai tambahan</li>
      <li>Untuk penempatan design yang rapih mendapat nilai tambahan</li>
      <li>Semua components yang dibutuhkan untuk mengerjakan sudah disiapkan dan tinggal digunakan (terlampir di bawah)</li>
    </ol>

    <br>
    <hr>
    <br>

    <h2>Komponen yang dapat digunakan :</h2>
    <strong>input text</strong>
    <v-text-field label="inpu text"></v-text-field>

    <br>

    <strong>select option</strong>
    <v-select :items="['1']" label="select option"></v-select>

    <br>

    <strong>multiple select</strong>
    <v-select :items="['1','2','3']" label="multiple" multiple></v-select>

    <br>

    <strong>text area</strong>
    <v-textarea label="text area" value="" rows="1"></v-textarea>

    <br>

    <strong>button</strong><br>
    <v-btn color="success">Success</v-btn>
    <v-btn color="error">Error</v-btn>
    <v-btn color="warning">Warning</v-btn>
    <v-btn color="info">Info</v-btn>

    <br>
    <br>

    <strong>dialog</strong><br>
    <v-dialog
      v-model="dialog"
      width="500"
    >
      <v-btn
        slot="activator"
        color="red lighten-2"
        dark
      >
        Click Me
      </v-btn>

      <v-card>
        <v-card-title
          class="headline grey lighten-2"
          primary-title
        >
          Privacy Policy
        </v-card-title>

        <v-card-text>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            flat
            @click="dialog = false"
          >
            I accept
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>

    <br><br>

    <strong>table</strong><br>
    <v-data-table
      :headers="headers"
      :items="desserts"
      class="elevation-1"
    >
      <template slot="items" slot-scope="props">
        <td>{{ props.item.name }}</td>
        <td>{{ props.item.calories }}</td>
      </template>
    </v-data-table>

  </div>
</template>

<script>
  import c from '@/const'

  export default {
    data () {
      return {
        dialog: '',
        headers: c.header,
        desserts: c.desserts,
      }
    }
  }
</script>