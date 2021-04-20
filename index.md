<html>
<body>

Inserisci un ritaglio di codice o un testo qualunque:
<br>
<textarea></textarea>
<br>
<button onclick="myFunction()">Estrai l'immagine contenuta</button>
<p id="demo"></p>

<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "<img src=\"butterfly-142506_1280.jpg\">";
}
</script>

</body>
</html>
