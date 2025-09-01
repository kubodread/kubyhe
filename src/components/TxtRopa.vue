<template>

<div class="cuadroTxt ">
      <div id="container">
          Confección de ropa de
          <div id="flip">
          <div><div>algodón </div></div>
          <div><div>manta</div></div>
          <div><div>lino</div></div>
          </div>
          artesanal y casual
      </div>
</div>



</template>

<script>



export default {
  name: 'TxtRopa',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


a {
  color: #42b983;
}


.cuadroTxt {
  border: solid 1px;
  border-radius: 0.8em;
  background:rgba(201, 201, 201, 0.56);
  padding: 15px;
}



    .figt {
        display: flex;
        align-items: center;
        background-color: lightgray;
        border-radius: 15px;
        padding: 5px;
        mask-image: linear-gradient( #1f2937 90%, transparent );
    }



    #container {
  color:#000000;
  text-transform: uppercase;
  font-size:36px;
  font-weight:bold;
  padding-top:10px;  
  width:100%;
  bottom:45%;
  display:flex;
  flex-wrap: wrap;
  flex-direction: column;
}

#flip {
  height:50px;
  overflow:hidden;
}

#flip > div > div {
  color:#000000;
  padding:4px 12px;
  height:45px;
  margin-bottom:45px;
  border-radius: 15px;
  height: fit-content;
  display:inline-block;
}

#flip div:first-child {
  animation: show 5s linear infinite;
}

#flip div div {
  background:#fffd93;
}
#flip div:first-child div {
  background:#4ec7f3a4;
}
#flip div:last-child div {
  background:#dc143c81;
}

@keyframes show {
  0% {margin-top:-270px;}
  5% {margin-top:-180px;}
  33% {margin-top:-180px;}
  38% {margin-top:-90px;}
  66% {margin-top:-90px;}
  71% {margin-top:0px;}
  99.99% {margin-top:0px;}
  100% {margin-top:-270px;}
}


</style>
