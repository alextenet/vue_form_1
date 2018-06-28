<template class="temp">
  <div class="main_form">

    <div class="logo_boot">
      <b-img src="https://getbootstrap.com/docs/4.1/assets/brand/bootstrap-solid.svg" fluid alt="Responsive image" />
    </div>

    <h2>Please sign in</h2>

    <div class="inputs">
        <b-form-input v-model="text1" id="input1" type="text" placeholder="Email address"></b-form-input>
        <b-form-input v-model="text2" id="input2" type="text" placeholder="Password"></b-form-input>
    </div>

    <div class="checkbox1">
        <b-form-checkbox v-model="status" value="accepted" unchecked-value="not_accepted">Remember me</b-form-checkbox>
    </div>

    <div class="row">
        <template v-for="variant in ['primary']">
            <div class="col-md-4 pb-2" v-for="size in ['lg']" :key="`${variant}_${size}`">
                <b-button :size="size" :variant="variant" class="btn">
                    Sign in
                </b-button>
            </div>
        </template>
    </div>

    <div class="mt-3">© 2017-2018 {{file2 && file2.name}}</div>
  </div>
</template>



<script>
  export default {
    data () {
      return {
        text1: '',
        text2: '',
        status: 'not_accepted',
        file2: null
      }
    }
  }
</script>



<style>

.main_form {
  width: 300px;
  margin: 0 auto;

  position: absolute;
  top: 50%;
  left: 50%;
  margin: -210px 0 0 -150px;
}

.logo_boot {
  width: 72px;
  margin: 0 auto;
  margin-bottom: 20px;
}

#input1 {
  height: 45px;
}

#input2 {
  height: 45px;
}

.checkbox1 {
  padding-top: 15px;
  text-align: center;
}

.row {
  padding-top: 30px;
}

h2 {
  text-align: center;
}

.btn {
  text-align: center;
  width: 300px;
}

.mt-3 {
  text-align: center;
  padding-top: 25px;
}



</style>
