<script>
let toggle;
let toggleColor = 'yellow'


let beatle = 'George';
let beatles = ['John', 'Paul', 'Ringo', 'George']
let i = 0
setInterval(() => {
  if (i > beatles.length-1){
    i = 0
  }
  beatle = beatles[i]
  i++
}, 1000);

$: {if (i % 2 == 0){
  toggle = 'black'
  toggleColor = 'whiteToggle'
} else {
  toggle = 'white'
  toggleColor = 'blackToggle'
}
}

</script>

<main class = {toggle}>
  <h1 class={toggleColor}>Hello {beatle}.</h1>
</main>

<style>
  main{
    font-family:monospace;
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  h1{
    font-size: 3rem;
  }

  .black{
    background-color: black;
  }

  .white{
    background-color: white;
  }

  .blackToggle{
    color: black;
  }

  .whiteToggle{
    color: white
  }
</style>
