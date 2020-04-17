<script>
  import Estadisticas from "./components/Estadisticas.svelte";
  import Paises from "./components/Paises.svelte";

  import { onMount } from "svelte";
  let data = {};
  const URL_API = "https://api.covid19api.com/summary";
  let errorPeticion = false;
  onMount(async () => {
    try {
      const response = await fetch(URL_API);
      data = await response.json();
    } catch (err) {
      errorPeticion = true;
    }
  });
</script>

<div class="container mt-5">

  <!-- Page Heading -->
  <div class="d-sm-flex align-items-center justify-content-between mb-4">

    <div>
      <h1 class="h3 mb-0 text-gray-800">Dashboard Covid-19</h1>
      <h6>
        <b>
          <i>Designed by Brayan Llanos</i>
        </b>
      </h6>
    </div>
  </div>
  <Estadisticas {...data.Global} />
  {#if data.Countries}
    <Paises countries={data.Countries} />
  {/if}
  {#if !data.Countries && !errorPeticion}
    <h3>Cargando datos...</h3>
  {/if}
  {#if errorPeticion}
    <div class="row">
      <div class="col-md-12">
        <div class="alert alert-danger" role="alert">
          <h3 class="alert-heading font-weight-bold">Error</h3>
          <p>
            Ups! Ocurrio un error al realizar la solicitud, por favor recargue
            la pagina
          </p>
        </div>
      </div>
    </div>
  {/if}
</div>
