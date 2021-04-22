<html>
  <body>
    
    <h4>Versione demo 1.0</h4>
    Stai lavorando o studiando su un testo che non ti appassiona? 
    Questo sito potrebbe aiutarti a trovare l'ispirazione!
    Incolla qui una porzione di testo di qualunque natura (es: una poesia, del codice informatico, un problema di matematica, ...) e avvia il FantaDecoder. 
    Esso elaborerà il testo secondo uno dei suoi algoritmi di decodifica, per arrivare infine a un'immagine ispirazionale. 
    In un certo senso, tale immagine era già contenuta nel testo, in attesa di essere decodificata e scoperta. 
    Questo dimostra come a volte dobbiamo solo cambiare il nostro modo di vedere le cose per iniziare ad apprezzarle.
    <br>
    <br>
    <textarea id="text" placeholder="Inserisci qui il tuo testo"></textarea>
    <br>
    <button>Scegli la decodifica (disabilitato nella demo)</button>
    <br>
    <button onclick="asciiSum()">Scopri l'immagine contenuta</button>
    <p id="image"></p>
    
    <style>
      textarea {
        font-size: 15px;
        width: 100%;
        height: 150px;
      }
      button {
        width: 100%;
      }
    </style>

    <script>
      function asciiSum() {
        var input = document.getElementById("text").value;
        var sum = 0;
        for(i=0; i<input.length; i++){
          sum += input.charCodeAt(i);
        }
        letterNum = sum%21 + 1;
        document.getElementById("image").innerHTML = 
        "<img src=\"butterfly-142506_1280.jpg\"> <br> <button onclick=\"showSteps()\">Mostra passaggi di decodifica</button> <br> <p id=\"steps\"></p>";
      }
      function showSteps() {
        document.getElementById("steps").innerHTML = sum + "<br> + letterNum;
      }
    </script>

  </body>
</html>
