<template>
  <b-container class="container main">
    <v-row class="container_form_title">
      <v-col style="text-align:center;">Registra tus datos</v-col>
    </v-row>
    <v-row class="container_form_subtitle">
      <v-col>y pide la cotizacion</v-col>
    </v-row>
    <v-row class="separator">
      <v-col></v-col>
    </v-row>
    <b-form class="container_form" @submit="onSubmit">
      <b-form-group id="InputGroup1"
                    label=""
                    label-for=""
                    description=""
                    class="space">
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
                    description=""
                    class="space">
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
                    description=""
                    class="space">
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
                    description=""
                    class="space">
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
                    description=""
                    class="space">
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
                    description=""
                    class="space">
        <b-form-input id="input3"
                      type="text"
                      v-model="form.typeNeg"
                      required
                      placeholder="TIPO DE NEGOCIO">
        </b-form-input>
        </b-form-group>
        <b-form-group id="InputGroup7"
                    label="COMO TE ENTERASTE?"
                    label-for=""
                    class="space">
        <b-form-select id="exampleInput3"
                      :options="options"
                      required
                      v-model="form.option">
        </b-form-select>
      </b-form-group>
      <!-- checkboxes -->
      <b-form-group id="inputGroup8"
                    label="EQUIPO A COTIZAR"
                    class="inputGroup8 label"
                    >
          <b-form-checkbox-group v-model="form.checked" id="exampleChecks">
            <b-form-checkbox value="CV15">CV15</b-form-checkbox>
            <b-form-checkbox value="CV18">CV18</b-form-checkbox>
            <b-form-checkbox value="RV18">RV18</b-form-checkbox>
            <b-form-checkbox value="RV15">RV15</b-form-checkbox>
          </b-form-checkbox-group>
      </b-form-group>
      <b-row class="inputGroup9">
        
        <b-col class="inputGroup9_col" style="text-align:center;">

          <b-button class="button_submit" type="submit" size="lg" variant="">COTIZAR</b-button>
        </b-col>
      </b-row>
      
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

<style lang="scss">

  .container {
    &_form {
      margin-top: 66px;
      z-index: 5;
    }

    &_form_title {
      display: flex;
      justify-content: center;
      color: white;
      font-size: 2em;
    }

    &_form_subtitle {
      background-color: #6B6B6D;
      color: #D4E68A !important;
      position: absolute;
      left: 0;
      right: 0;
      top: 47px;
      text-align: center;
      z-index: 3;
      padding: 4px 0; 
      margin: 0 -14px;
      font-size: 2em !important;
    }

    .separator {
      position: absolute;
      left: 0;
      right: 0;
      top: 103px;
      z-index: 3;
      padding: 4px 0;
      margin: 0 -14px;
      font-size: 2em !important;
      border-top: 18px solid black;
      border-left: 18px solid transparent;
      border-right: 18px solid transparent;
      color: transparent;
      z-index: -1;
    }
  }

  .form-control {
    border-radius: 0 !important;
    color: black;
  }

  .form-group {
    margin-bottom: 0.2rem !important;
  }

  .space {
    padding: 0 15px !important;
  }

  #InputGroup7 {
    display: flex;
    flex-wrap: nowrap;
    color: white;

    label {
      flex: 1 1 %50 !important;
    }
    
    div {
      flex: 1 1 %50 !important; 
      // flex: 1 !important;
    }
  }
  .inputGroup8 {
    display: flex;
    background-color: #808E99 !important; 
    text-align: center;
    padding: 15px 0;
    margin: 0 !important;
    color: white;
  }

  

  .main {
    background-color: #9FACB3;
    padding: 0 0;
  }

  .inputGroup9 {
    background-color: white;
    padding: 0 0;
    margin: 0px 0;

    &_col {
      padding: 0 0;
    }

  }

  .button_submit {
    margin: 0 auto;
    padding: 24px 199px;
    background-color: #D1E28B !important;
    border-style: none !important;
    border-radius: 0 !important;

    &:hover {
      cursor: pointer;
    }
  }


</style>


