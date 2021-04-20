<html>
<body>

In prima elementare ci siamo innamorati della lettura.
Semplici parole scritte che evocano vivide immagini nella mente.
Crescendo, abbiamo affrontato testi e linguaggi via via più complessi.
E se vi dicessi che anche i files tecnici contengono immagini altrettanto belle?
Ma certo, tutto dipende dalla codifica con cui vengono letti!
<br>
<br>
FantaDecoder implementa alcune decodifiche che permettono di leggere un'immagine a partire da una qualsiasi sequenza di caratteri. 
In fondo possiamo dire che quelle immagini erano da sempre contenute in quei testi, e aspettavano solo di essere decodificate.
<br>
<br>
<textarea placeholder="Inserisci qui il tuo testo"></textarea>
<br>
<button onclick="myFunction()">Scopri l'immagine contenuta</button>
<button>Cambia la decodifica</button>
<p id="demo"></p>

<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "<img src=\"butterfly-142506_1280.jpg\"> <br> <button>Mostra passaggi di decodifica</button>";
}
</script>

</body>
</html>
