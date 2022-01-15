<template>
  <div class="row">
    <div class="col-9">
      <h3>Momentenstelling</h3>
      <div class="row">
        <div class="col">
          <h5>component</h5>
          <input id="ship" type="text" class="form-control" disabled name="" value="Ship">
        </div>
        <div class="col">
          <h5>Weight (ton)</h5>
          <input v-model.number="ship__weight" type="text" class="form-control">
        </div>
        <div class="col">
          <h5>VCG (m)</h5>
          <input v-model.number="ship__vcg" type="number" class="form-control">
        </div>
      </div>

      <div class="row">
        <div class="col">
          <input id="ship" type="text" class="form-control"  name="">
        </div>
        <div class="col">
          <input v-model.number="weight_1" type="text" class="form-control">
        </div>
        <div class="col">
          <input v-model.number="vcg_1" type="text" class="form-control">
        </div>
      </div>
    </div>
    <div class="col-3">
      <h3>Informatie</h3>
      <p>{{ ship__weight }}</p>
      <p>{{ ship__vcg}}</p>
      <p>Ship Deplacement: {{ getNewShipDeplacement() }}</p>
      <p>New VCG: {{ getNewVCG() }}</p>
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
      ship__weight: 0,
      ship__vcg: 0,
      weight_1: 0,
      vcg_1: 0,
      ship_deplacement: 0
    }
  },
  methods: {
    getNewShipDeplacement () {
      this.ship_deplacement = this.ship__weight + this.weight_1
      return parseFloat(this.ship_deplacement)
    },
    getNewVCG () {
      var vertMom = this.ship_weight * this.ship__vcg
      console.log(vertMom)
      var vertMom2 = this.weight_1 * this.vcg_1

      var VMoments = (vertMom + vertMom2) / this.getNewShipDeplacement()
      console.log(VMoments)
      return parseFloat(VMoments)
    }
  }
}

</script>
