<template>
  <b-container class="container">
    <b-form @submit="onSubmit">
      <b-form-group id="InputGroup1"
                    label=""
                    label-for=""
                    description="">
        <b-form-input id="input1"
                      type="text"
                      v-model="form.name"
                      required
                      placeholder="NOMBRE">
        </b-form-input>
      </b-form-group>
      <b-form-group id="InputGroup2"
                    label=""
                    label-for=""
                    description="">
        <b-form-input id="input2"
                      type="text"
                      v-model="form.lastName"
                      required
                      placeholder="APELLIDOS">
        </b-form-input>
      </b-form-group>
      <b-form-group id="InputGroup3"
                    label=""
                    label-for=""
                    description="">
        <b-form-input id="input3"
                      type="text"
                      v-model="form.tel"
                      required
                      placeholder="TELEFONO">
        </b-form-input>
      </b-form-group>
      <b-form-group id="InputGroup4"
                    label=""
                    label-for=""
                    description="">
        <b-form-input id="input3"
                      type="email"
                      v-model="form.email"
                      required
                      placeholder="EMAIL">
        </b-form-input>
      </b-form-group>
      <b-form-group id="InputGroup5"
                    label=""
                    label-for=""
                    description="">
        <b-form-input id="input3"
                      type="text"
                      v-model="form.city"
                      required
                      placeholder="CIUDAD">
        </b-form-input>
      </b-form-group>
      <b-form-group id="InputGroup6"
                    label=""
                    label-for=""
                    description="">
        <b-form-input id="input3"
                      type="text"
                      v-model="form.typeNeg"
                      required
                      placeholder="TIPO DE NEGOCIO">
        </b-form-input>
        </b-form-group>
        <b-form-group id="InputGroup7"
                    label="Como nos encontraste"
                    label-for="">
        <b-form-select id="exampleInput3"
                      :options="options"
                      required
                      v-model="form.option">
        </b-form-select>
      </b-form-group>
      <!-- checkboxes -->
      <b-form-group id="inputGroup8"
                    label="EQUIPO A COTIZAR">
        
          <b-form-checkbox-group v-model="form.checked" id="exampleChecks">
            <b-form-checkbox value="CV15">CV15</b-form-checkbox>
            <b-form-checkbox value="CV18">CV18</b-form-checkbox>
            <b-form-checkbox value="RV18">RV18</b-form-checkbox>
            <b-form-checkbox value="RV15">RV15</b-form-checkbox>
          </b-form-checkbox-group>
      </b-form-group>
      <b-button type="submit" variant="">COTIZAR</b-button>
      
    </b-form>
  </b-container>
</template>


<script>
export default {
  data () {
    return {
      form: {
        name: '',
        lastName: '',
        tel: '',
        email: '',
        city: '',
        typeNeg: '',
        option: 'Redes Sociales',
        checked: ''
      },
      options: [
        { text: 'Redes Sociales', value: 'socialNetworks' },
        { text: 'Publicidad', value: 'publicidad' },
        { text: 'Otro', value: 'Otro' }
      ]
    }
  }
}
</script>

<style>

</style>


