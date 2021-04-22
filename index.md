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
    <textarea id="text" placeholder="Inserisci qui il tuo testo (minimo 50 caratteri)"></textarea>
    <br>
    <button>Scegli la decodifica (disabilitato nella demo)</button>
    <br>
    <button onclick="asciiSum()">Scopri l'immagine contenuta</button>
    <img id=imageOut>
    <p id="textOut"></p>

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
      var sum;
      var letterNum;
      const dictionary = [
        "A come Alba", "B come Barca", "C come Coralli", "D come Donna", "E come Elefante", "F come Farfalla", "G come Gatto",
        "H come Hamburger", "I come Iridescenza", "L come Lucertola", "M come Montagne", "N come Nettare", "O come Olio", "P come Piante",
        "Q come Quaglia", "R come Rosa", "S come Sorgente", "T come Torta", "U come Uva", "V come Vitamine", "Z come Zenzero"
      ]
      function asciiSum() {
        var input = document.getElementById("text").value;
        if(input.length<50) {
          document.getElementById("imageOut").src = "images/Error.jpg";
          document.getElementById("textOut").innerHTML = "";
        }
        else {
          sum = 0;
          for(i=0; i<input.length; i++){
            sum += input.charCodeAt(i);
          }
          if(sum%100==0) {
            document.getElementById("imageOut").src = "images/Golden.jpg";
            document.getElementById("textOut").innerHTML = "";
          }
          else {
            letterNum = sum%21 + 1;
            imageRef = "images/" + dictionary[letterNum-1] + ".jpg";
            document.getElementById("imageOut").src = imageRef;
            document.getElementById("textOut").innerHTML = 
            "<button onclick=\"showSteps()\">Mostra passaggi di decodifica</button> <br> <p id=\"steps\"></p>";
          }
        }
      }
      function showSteps() {
        document.getElementById("steps").innerHTML = "Somma dei valori ASCII presenti = " + sum + "<br> Valore alfabetico (somma mod 21 + 1) = " + letterNum
        + "<br> Lettera corrispondente: " + dictionary[letterNum-1];
      }
    </script>

  </body>
</html>
