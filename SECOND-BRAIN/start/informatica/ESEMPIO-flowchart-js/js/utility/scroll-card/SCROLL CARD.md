# codice

```
let circle = document.querySelectorAll(".circle");

let schede = document.querySelectorAll(".scheda");

  

schede[0].classList.add("schedaHide");

schede[2].classList.add("schedaHide");

circle[1].classList.add("circleActive");

  

circle.forEach((pallino, index) => {

  pallino.addEventListener("click", () => {

         // nascondo tutte le schede

    schede.forEach(s => s.classList.add("schedaHide"), console.log("rimosso"));

  

         // disattivo tutti i pallini

    circle.forEach(c => c.classList.remove("circleActive"));

  

         // attivo scheda e pallino cliccati

    let target = schede[index];
  

    target.classList.remove("schedaHide");

    target.classList.add("schedaActive");

    pallino.classList.add("circleActive");

  });

});
```


![[diagramma_flusso.png]]


