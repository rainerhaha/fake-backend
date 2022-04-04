

Das Wurzel-Verzeichnis des Servers für das Fake-Backend lautet:

http://my-json-server.typicode.com/rainerhaha/fake-backend

Dies musst du im Code des Frontends als String irgendwo angeben.

Dann gibt es weitere Unterverzeichnisse, um auf die Daten zugreifen zu 

können.

Hier gibt es die beiden Unterverzeichnisse:

**1.) /pcDataSets**

**2.) /userDataSets**


Ein pcDataSet-Objekt repräsentiert einen kompletten Datensatz zu einem Rlab-PC

Unter folgendem Pfad kannst du dir alle vorhandenen Datensätze anzeigen lassen.

Der Datentyp ist eine Liste ( wird bei JavaScript auch als Array bezeichnet ) von Objekten.

http://my-json-server.typicode.com/rainerhaha/fake-backend/pcDataSets/


Per id kannst du auf ein einzelnes Datenobjekt zugreifen:

http://my-json-server.typicode.com/rainerhaha/fake-backend/pcDataSets/1


Du kannst auch nach Datenobjekten mit bestimmten Einträgen filtern:

http://my-json-server.typicode.com/rainerhaha/fake-backend/pcDataSets/?user_principal_name=rainer.witz@gfn.education

oder 

http://my-json-server.typicode.com/rainerhaha/fake-backend/pcDataSets/?server_name=RLAB-Server-1&rlab_pc_ip_addr=100.25.76.2


Als Parameter für die Filterung kannst du alle Einträge verwenden, die in einem pcDataSet-Objekt enthalten sind.



Mit den Daten zu einem Benutzer funktioniert es genauso:

Ein Objekt vom Typ userDataSet repräsentiert einen kompletten Datensatz zu einem Benutzer.

Alle vorhandenen Daten-Objekte abrufen:

http://my-json-server.typicode.com/rainerhaha/fake-backend/userDataSets/

Auf einen Benutzer mit einer bestimmten id zugreifen:

http://my-json-server.typicode.com/rainerhaha/fake-backend/userDataSets/3


Die Filterung funktioniert auch genauso wie für pcDataSet-Objekte.

#   

Es gibt noch zwei weitere Schnittstellen, um die Ausführung einer bestimmten Operation anzufordern.

**1.) /pcUserOps:** Hier kann die Ausführung von Operationen angefordert werden, die ein gewöhnlicher Teilnehmer an seinem Rlab-PC ausführen darf.

**2.) /pcSupervisorOps:** Hier kann die Ausführung von Operationen angefordert werden, die ein Supervisor ( z.B. ein Trainer ) an den Rlab-PCs einer bestimmten 

Gruppe ( z.B. die Teilnehmer eines bestimmten Kurses ) von Teilnehmern ausführen darf.


Alle vorhandenen Daten-Objekte abrufen:

http://my-json-server.typicode.com/rainerhaha/fake-backend/pcUserOps/   oder

http://my-json-server.typicode.com/rainerhaha/fake-backend/pcSupervisorOps/

Der Datentyp der Rückgabe ist eine Liste ( wird bei JavaScript auch als Array bezeichnet ) von Objekten.


Die Autorisierung für die Anforderung der Ausführung einer bestimmten User-Operation durchführen:

http://my-json-server.typicode.com/rainerhaha/fake-backend/pcUserOps/1/?upn_req_owner=tony.peters@gfn.education


Die Autorisierung für die Anforderung der Ausführung einer bestimmten Supervisor-Operation durchführen:

http://my-json-server.typicode.com/rainerhaha/fake-backend/pcSupervisorOps/1/

?upn_req_owner=trainer.martens@gfn.education&upn_req_recipient=tony.peters@gfn.education

&gfn_course_name=GFN-Kurs-330&gfn_class_name=GFN-Klasse-2021-10

Hier wird immer zusätzlich auch der user principal name des Teilnehmers sowie der Kurs-Name und der Klassen-Name benötigt.

In der Implementierung können die Daten für gfn_course_name und gfn_class_name auch im Request-Body als JSON-Objekt mit übergeben werden.





