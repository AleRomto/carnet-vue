<template>
  <div class="carnet">
    <aside>
      <div>
        <span>CEDULA DE INDENTIDAD</span>
        <img width="40" :src="flagImage" alt="Bandera de Chile" />
      </div>
      <img :src="photo" alt="Foto del titular" />
      <p>{{ run }}</p>
    </aside>

    <main>
      <header>
        <p>REPUBLICA DE CHILE</p>
        <span>SERVICIO DE REGISTRO CIVIL E IDENTIFICACIÓN</span>
      </header>
      <section>
        <article>
          <header>APELLIDOS</header>
          <span>{{ apellidos }}</span>
        </article>
        <article>
          <header>NOMBRES</header>
          <span>{{ nombres }}</span>
        </article>
        <div class="grid-2-colums">
          <article>
            <header>NACIONALIDAD</header>
            <span>{{ nacionalidad }}</span>
          </article>
          <article>
            <header>SEXO</header>
            <span>{{ sexo }}</span>
          </article>
        </div>
        <div class="grid-2-colums">
          <article>
            <header>FECHA DE NACIMIENTO</header>
            <span>{{ fechaNacimiento }}</span>
          </article>
          <article>
            <header>NÙMERO DOCUMENTO</header>
            <span>{{ numeroDocumento }}</span>
          </article>
        </div>
        <div class="grid-2-colums">
          <article>
            <header>FECHA DE EMISIÒN</header>
            <span>{{ fechaEmision }}</span>
          </article>
          <article>
            <header>FECHA DE VENCIMIENTO</header>
            <span>{{ fechaVencimiento }}</span>
          </article>
        </div>
        <article>
          <header>FIRMA DEL TITULAR</header>
          <span>{{ firma }}</span>
        </article>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  name: 'CarnetIdentidad',
  data() {
    return {
      flagImage: '/chile_bandera.png', 
      photo: '/grace_hopper.jpg', 
      run: '22.222.222-2',
      apellidos: 'HOPPER',
      nombres: 'GRACE MURRAY',
      nacionalidad: 'ESTADOUNIDENSE',
      sexo: 'F',
      fechaNacimiento: '09 DIC 1906',
      numeroDocumento: '222.222.222',
      fechaEmision: '01 ENE 2025',
      fechaVencimiento: '01 ENE 2030',
      firma: 'Grandma COBOL',
    };
  },
};
</script>


<style scoped>
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60vh;
  font-size: 9px;
}

.carnet {
  width: 450px;
  height: 260px;
  background: #c8deed;
  border-radius: 20px;
  display: grid;
  grid-template-columns: 30% 1fr;
  padding: 15px;
  box-shadow: 0px 0px 10px 2px black;
}

aside div {
  display: flex;
  font-size: 12px;
  padding-bottom: 16px;
}

aside > img {
  margin-top: 10px;
  width: 100%;
}

aside p {
  text-align: center;
  font-size: 12px;
  font-weight: bold;
  font-family: 'Roboto', sans-serif;
}

main {
  padding: 0px 12px;
}

main article {
  margin: 4px 0px;
}

main article header {
  font-weight: bold;
  color: #0235a4;
  font-size: 8px;
  font-family: 'Roboto', sans-serif;
}

main header p {
  font-size: 18px;
  font-family: 'Roboto', sans-serif;
  margin: 0;
  font-weight: bold;
  color: #0235a4;
}

main header span {
  font-size: 8px;
  color: #399be1;
}

main section {
  margin-top: 8px;
}

main section article span {
  font-size: 12px;
  font-weight: 500;
  font-family: 'Roboto', sans-serif;
}

main section .grid-2-colums {
  display: grid;
  grid-template-columns: 50% 50%;
}
</style>
