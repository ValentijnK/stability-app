<template>
  <div class="row">
    <div class="row">
      <div class="col">
        <h3>Hold Calculator</h3>
      </div>
    </div>
    <div class="col-3">
      <h5>Stowage factor of bulk cargo?</h5>
      <input v-model.number="StowageFactor" class="form-control">
    </div>
    <div class="col-2">
      <h5>How much cargo in tons?</h5>
      <input v-model.number="CargoAmount" class="form-control">
    </div>
    <div class="col-4">
      <div class="row">
        <div class="col">
          <h5>Length</h5>
          <input v-model.number="HoldLength" type="text" class="form-control">
        </div>
        <div class="col">
          <h5>Breadth</h5>
          <input v-model.number="HoldBreadth" type="text" class="form-control">
        </div>
        <div class="col">
          <h5>Height</h5>
          <input v-model.number="HoldHeight" type="number" class="form-control">
        </div>
      </div>
    </div>
    <div class="col-3">
      <h3>Informatie</h3>
      <p>Hold (m3): {{ calculateHold() }}</p>
      <p>Cargo in m3: {{ calculateCargo() }}</p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  },
  data () {
    return {
      StowageFactor: 0,
      CargoAmount: 0,
      HoldLength: 0,
      HoldBreadth: 0,
      HoldHeight: 0
    }
  },
  methods: {
    calculateHold () {
      return this.HoldLength * this.HoldBreadth * this.HoldHeight
    },
    calculateCargo () {
      return this.StowageFactor * this.CargoAmount
    }
  }
}

</script>
