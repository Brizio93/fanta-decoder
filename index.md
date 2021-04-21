<html>
<body>

Stai lavorando o studiando su un testo che non ti ispira? Forse semplicemente non lo guardi nel modo giusto. Questo sito potrebbe aiutarti a trovare l'ispirazione. Incolla qui il testo, qualunque cosa sia (poesie, procedure informatiche, formule matematiche, ...) e avvia il FantaDecoder. Esso elaborerà il testo secondo uno dei suoi algoritmi di decodifica, per arrivare infine a un'immagine ispirazionale. In un certo senso, tale immagine era già contenuta nel testo, in attesa di essere decodificata e scoperta. Questo dimostra come a volte dobbiamo solo cambiare il nostro modo di vedere le cose per iniziare ad apprezzarle.
<br>
<br>
<textarea id="text" placeholder="Inserisci qui il tuo testo"></textarea>
<br>
<button onclick="myFunction()">Scopri l'immagine contenuta</button>
<button>Cambia la decodifica</button>
<p id="demo"></p>

<script>
function myFunction() {
  var x = document.getElementById("text").value;
  document.getElementById("demo").innerHTML = "<img src=\"butterfly-142506_1280.jpg\"> <br> <button>Mostra passaggi di decodifica</button>" + x;
}
</script>

</body>
</html>
