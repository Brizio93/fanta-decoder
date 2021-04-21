<html>
  <body>
    
    <h6>#Versione demo 1.0</h6>
    Stai lavorando o studiando su un testo che non ti ispira? 
    Questo sito potrebbe aiutarti a trovare l'ispirazione!
    Incolla qui il testo, qualunque cosa sia (poesie, procedure informatiche, formule matematiche, ...) e avvia il FantaDecoder. 
    Esso elaborerà il testo secondo uno dei suoi algoritmi di decodifica, per arrivare infine a un'immagine ispirazionale. 
    In un certo senso, tale immagine era già contenuta nel testo, in attesa di essere decodificata e scoperta. 
    Questo dimostra come a volte dobbiamo solo cambiare il nostro modo di vedere le cose per iniziare ad apprezzarle.
    <br>
    <br>
    <textarea id="text" placeholder="Inserisci qui il tuo testo"></textarea>
    <br>
    <button onclick="asciiSum()">Scopri l'immagine contenuta</button>
    <button>Cambia la decodifica</button>
    <p id="outlet"></p>

    <script>
      function asciiSum() {
        var input = document.getElementById("text").value;
        var sum = 0;
        for(i=0; i<input.length; i++){
          sum = sum + input.charCodeAt(i);
        }
        letterNum = sum%21;
        document.getElementById("outlet").innerHTML = 
        "<img src=\"butterfly-142506_1280.jpg\"> <br> <button>Mostra passaggi di decodifica</button> <br> Somma dei valori ASCII presenti = "
        + sum + "<br> Valore alfabetico corrispondente (mod 21) = " + letterNum;
      }
    </script>

  </body>
</html>
