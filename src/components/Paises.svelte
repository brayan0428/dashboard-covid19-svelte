<script>
  export let countries = [];
  countries = countries.filter(c => c.TotalConfirmed > 0);
  let filterCountries = countries;

  function handleFilter(e) {
    const value = e.target.value;
    filterCountries = countries.filter(c =>
      c.Country.toLowerCase().includes(value.toLowerCase())
    );
  }
</script>

<div class="row mb-3">
  <div class="col-md-12">
    <input
      class="form-control"
      placeholder="Buscar pais"
      on:keyup={e => handleFilter(e)} />
  </div>

</div>
<table class="table table-bordered">
  <thead>
    <tr class="text-center">
      <th>Pais</th>
      <th>Confirmados</th>
      <th>Recuperados</th>
      <th>Muertes</th>
    </tr>
  </thead>
  <tbody>
    {#each filterCountries as country}
      <tr>
        <td>{country.Country}</td>
        <td>{country.TotalConfirmed}</td>
        <td>{country.TotalRecovered}</td>
        <td>{country.TotalDeaths}</td>
      </tr>
    {/each}
  </tbody>
</table>
