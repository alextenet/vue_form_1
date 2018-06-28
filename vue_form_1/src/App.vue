<template class="temp">
  <div>
    <h2>Please sign in</h2>
    <!-- Styled -->
    <b-form-input id="input1" :state="state" v-model.trim="name"></b-form-input>
    <b-form-input id="input1" :state="state" v-model.trim="name"></b-form-input>
    <b-form-checkbox id="checkbox1" v-model="status" value="accepted" unchecked-value="not_accepted">Remember me</b-form-checkbox>

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
      file: null,
      file2: null
    }
  }
}
</script>



<style>

  div {
    width: 300px;
    margin: 0 auto;
    /* margin-top: 400px; */
  }

  h2 {
    text-align: center;
  }

  .btn {
    width: 300px;
    margin-left: -100px;
  }

  .mt-3 {
    text-align: center;
  }

</style>


