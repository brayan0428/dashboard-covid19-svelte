<script>
  export let TotalConfirmed = 0;
  export let TotalRecovered = 0;
  export let TotalDeaths = 0;
</script>

<div class="row">

  <!-- Earnings (Monthly) Card Example -->
  <div class="col-xl-4 col-md-6 mb-4">
    <div class="card border-left-primary shadow h-100 py-2">
      <div class="card-body">
        <div class="row no-gutters align-items-center">
          <div class="col mr-2">
            <div
              class="text-xs font-weight-bold text-primary text-uppercase mb-1">
              Total Casos Confirmados
            </div>
            <div class="h5 mb-0 font-weight-bold text-gray-800">
              {TotalConfirmed}
            </div>
          </div>
          <div class="col-auto">
            <i class="fas fa-check-circle fa-2x" />
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Earnings (Monthly) Card Example -->
  <div class="col-xl-4 col-md-6 mb-4">
    <div class="card border-left-success shadow h-100 py-2">
      <div class="card-body">
        <div class="row no-gutters align-items-center">
          <div class="col mr-2">
            <div
              class="text-xs font-weight-bold text-success text-uppercase mb-1">
              Total Recuperados
            </div>
            <div class="h5 mb-0 font-weight-bold text-gray-800">
              {TotalRecovered}
            </div>
          </div>
          <div class="col-auto">
            <i class="fas fa-users fa-2x" />
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Earnings (Monthly) Card Example -->
  <div class="col-xl-4 col-md-6 mb-4">
    <div class="card border-left-danger shadow h-100 py-2">
      <div class="card-body">
        <div class="row no-gutters align-items-center">
          <div class="col mr-2">
            <div
              class="text-xs font-weight-bold text-danger text-uppercase mb-1">
              Total Muertes
            </div>
            <div class="h5 mb-0 font-weight-bold text-gray-800">
              {TotalDeaths}
            </div>
          </div>
          <div class="col-auto">
            <i class="fas fa-cross fa-2x" />
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
