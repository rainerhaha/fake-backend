

Das Wurzel-Verzeichnis des Servers für das Fake-Backend lautet:

https://my-json-server.typicode.com/rainerhaha/fake-backend

Dies musst du im Code des Frontends als String irgendwo angeben.

Dann gibt es weitere Unterverzeichnisse, um auf die Daten zugreifen zu 

können.

Hier gibt es zur Zeit zwei Unterverzeichnisse:

1.) /pcDataSets

2.) /userDataSets


Ein pcDataSet-Objekt repräsentiert einen kompletten Datensatz zu einem Rlab-PC

Unter folgendem Pfad kannst du dir alle vorhandenen Datensätze anzeigen lassen.

Der Datentyp ist eine Liste ( auch als Array bezeichnet ) von Objekten.

https://my-json-server.typicode.com/rainerhaha/fake-backend/pcDataSets/


Per id kannst du auf ein einzelnes Datenobjekt zugreifen:

https://my-json-server.typicode.com/rainerhaha/fake-backend/pcDataSets/1


Du kannst auch nach Datenobjekten mit bestimmten Einträgen filtern:

https://my-json-server.typicode.com/rainerhaha/fake-backend/pcDataSets/?user_principal_name=rainer.witt@gfn.education

oder 

https://my-json-server.typicode.com/rainerhaha/fake-backend/pcDataSets/?server_name=RLAB-Server-1&rlab_pc_ip_addr=100.25.76.2


Als Parameter für die Filterung kannst du alle Einträge verwenden, die in einem pcDataSet-Objekt enthalten sind.



Mit den Daten zu einem Benutzer funktioniert es genauso:

Ein Objekt vom Typ userDataSet repräsentiert einen kompletten Datensatz zu einem Benutzer.

Alle vorhanden Daten-Objekte abrufen:

https://my-json-server.typicode.com/rainerhaha/fake-backend/userDataSets/

Auf einen Benutzer mit einer bestimmten id zugreifen:

https://my-json-server.typicode.com/rainerhaha/fake-backend/userDataSets/3


Die Filterung funktioniert auch genauso wie für pcDataSet-Objekte.





