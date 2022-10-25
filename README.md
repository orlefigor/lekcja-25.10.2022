<!DOCTYPE html>
<html>
  <head>
    <title>cus</title>
  </head>
  <body>
    <script>
      let licz = 0;
      let NP = 0;
      let P = 0;
      let zera = 0;
      const tabS = [];
      const tabP = [];
      const tabN = [];
      const tab0 = [];
      while (licz < 10 || licz > 20) {
        licz = parseInt(prompt("podaj ilosc liczb(od 10 do 20):"));
      }
      for (let i = 0; i < licz; i++) {
        let zm = undefined;
        while (isNaN(zm)) {
          zm = parseInt(prompt("podaj liczbe:"));
        }
        tabS[i] = zm;
        if (zm == 0) {
          tab0[zera] = zm;
          zera++;
        } else if (zm % 2 == 0) {
          tabP[P] = zm;
          P++;
        } else if (zm % 2 != 0) {
          tabN[NP] = zm;
          NP++;
        }
      }
      console.log(tabS);
      //   document.write("zera:");
      //   document.write(tab0);
      //   document.write("<br>");
      //   document.write("parzyste:");
      //   document.write(tabP);
      //   document.write("<br>");
      //   document.write("nieparzyste:");
      //   document.write(tabN);
      //   document.write("<br>");

      //------------------------sort parzyste-----------------------
      for (let j = 0; j < tabP.length - 1; j++) {
        let n = 0;
        for (let z = 0; z < tabP.length - 1; z++) {
          if (tabP[n] > tabP[n + 1]) {
            let sort = undefined;
            sort = tabP[n];
            tabP[n] = tabP[n + 1];
            tabP[n + 1] = sort;
            n++;
          } else {
            n++;
          }
        }
      }
      document.write("<br>");
      document.write("sort parzyste:");
      document.write(tabP);
      document.write("<br>");
      //--------------------------------------------------------
      //------------------------sort nieparzyste-----------------------
      for (let j = 0; j < tabN.length - 1; j++) {
        let n = 0;
        for (let z = 0; z < tabN.length - 1; z++) {
          if (tabN[n] > tabN[n + 1]) {
            let sort = undefined;
            sort = tabN[n];
            tabN[n] = tabN[n + 1];
            tabN[n + 1] = sort;
            n++;
          } else {
            n++;
          }
        }
      }
      document.write("<br>");
      document.write("sort nieparzyste:");
      document.write(tabN);
      document.write("<br>");
      //--------------------------------------------------------
      //------------------------sort calosci-----------------------
      for (let j = 0; j < tabS.length - 1; j++) {
        let n = 0;
        for (let z = 0; z < tabS.length - 1; z++) {
          if (tabS[n] > tabS[n + 1]) {
            let sort = undefined;
            sort = tabS[n];
            tabS[n] = tabS[n + 1];
            tabS[n + 1] = sort;
            n++;
          } else {
            n++;
          }
        }
      }
      document.write("<br>");
      document.write("sort wszystkie:");
      document.write(tabS);
      document.write("<br>");
      //--------------------------------------------------------
      document.write("<br>");
      document.write("najwieksze nieparzyste:");
      document.write(tabN[tabN.length - 1]);
      document.write("<br>");
      document.write("<br>");
      document.write("najmniejsze nieparzyste:");
      document.write(tabN[0]);
      document.write("<br>");
      document.write("<br>");
      document.write("najwieksze parzyste:");
      document.write(tabP[tabP.length - 1]);
      document.write("<br>");
      document.write("<br>");
      document.write("najmniejsze parzyste:");
      document.write(tabP[0]);
      document.write("<br>");
      document.write("<br>");
      document.write("zero wystapilo:");
      document.write(tab0.length);
      document.write("razy");
      document.write("<br>");
      document.write("<br>");
      document.write("najwieksze ogulnie:");
      document.write(tabS[tabS.length - 1]);
      document.write("<br>");
      document.write("<br>");
      document.write("najmniejsze ogulnie:");
      document.write(tabS[0]);
      document.write("<br>");
    </script>
  </body>
</html>
