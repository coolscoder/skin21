<template>
  <div container>
    <div title v-text="head" />
    <div data-link-container>
      <a
        href="#"
        links
        v-for="(link, index) in links"
        v-bind:key="index"
        v-text="link"
      />
    </div>
    <div title foot v-text="foot" />
    <div round />
  </div>
</template>

<script>
  export default {
    name: 'App',
    data: () => ({
      head: "TAMARINA TEAS",
      links: [
        '#SAVAGEX',
        'NEWDROPS',
        'SAVAGE X FIT',
        'X SURVIVORS',
        'MEWDROPS',
        'SAVAGE X FIT',
        'SAVAGE X FIT'
      ],
      foot: "@TAMARINACO",
    }),
  }
</script>

<style>
  body {
    background: #fff;
    color: #fff;
    font-family: Helvetica;
    font-weight: bold;
    text-align: center;
    margin: 0;
  }
  [container] {
    background-color: #ff5b2b;
    border-radius: 20px;
    padding: 3vh 10vw;
    height: 94vh;
    overflow: hidden;
  }
  [title] {
    font-size: 30px;
    height: 12vh;
    color: #ffe231;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  [foot] {
    color: white;
    justify-content: end;
  }
  [data-link-container] {
    background-color: #ff8fe9;
    display: flex;
    flex-direction: column;
    height: 70vh;
    justify-content: space-around;
  }
  [links] {
    color: white;
    font-size: 20px;
    z-index: 2;
  }
  [round] {
    width: 60vw;
    height: 60vw;
    border-radius: 50%;
    background-color: #574dfd;
    position: absolute;
    top: calc(50vh - 30vw);
    left: calc(50% - 30vw);
    z-index: 1;
  }
</style>
