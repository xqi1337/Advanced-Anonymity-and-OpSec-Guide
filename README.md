# Advanced-Anonymity-and-OpSec-Guide


###
### 
#######################################################################################
# Vorwort ##########################

Starke Anonymität soll Risikogruppen Schutz gegen Repressionen bieten. Es gibt sehr unterschiedliche Gründe, warum man Repressionen befürchten könnte. Minderheiten befürchten Repressionen durch die Majorität. Wer Regeln, Gesetze o.a. staatliche Vorgaben nicht respektieren möchte, muss Repressionen durch den Macht- bzw. Staatsapparat befürchten, wir fürchten in den meisten Fällen die Strafverfolgung durch Ermittlungsbehörden. 

Anonymität erreicht man beim Surfen im Netz, indem man in einer ausreichend großen Anonymitätsgruppe mit identischen Merkmalen untertaucht, so dass einzelne Individuen nicht mehr anhand von Merkmalen wie IP-Adresse, Browsertyp und -eigenschaften usw. unterscheidbar sind. 

Durch starke Anonymisierung ist ein Tracking von einzelnen Individuen zur Erstellung von Persönlichkeitsprofilen  unmöglich, ein positiver Nebeneffekt. 

Die gute Nachricht: Wir wissen seit Edward Snowdens Enthüllungen, das wir nicht paranoid sind! Die schlechte Nachricht: Wir werden alle überwacht. Jetzt und überall. Im folgenden Guide wird beschrieben, welche Schritte notwendig sind, um der Überwachung zu entgehen und unsere Identität online geheim zu halten. In unseren Beispielen gehen wir von Firefox Webbrowser und Thunerbird Mailclient aus.


#######################################################################################
# Grundlagen
#######################################################################################


### Clearnet vs Darknet

Die einen nur wollen sicher ihr Gras zum Eigenkonsum im Darknet bestellen, die anderen möchten unerkannt Waren und Dienstleistungen im Clearnet carden. Um dich richtig zu schützen solltest du vorher wissen was genau du vor hast. Im Darknet kannst du dich recht leicht mit TOR und ein paar anderen Tools gut schützen, im Clearnet sieht die Sache schon anders aus. Dort kann oft kein TOR verwendet werden da die Webseiten und Anbieter Verbindungen erkennen die von TOR-Exitnodes kommen und diese sofort blockieren. 

DHL z.B. sperrt Packstationen meistens nach dem ersten Login von einem TOR-Node da hier automatisch von einem Missbrauch ausgegangen wird (was in 99% der Fälle auch so ist). Will man also im Clearnet arbeiten braucht man eine sichere Verbindung die aber zugleich nicht geblacklisted ist und auch anderweitig keine Aufmerksamkeit aufsich zieht bzw. nicht die Möglichkeiten einschränkt.

Du wirst also mit einem TOR-Browser keinen Erfolg beim Carding haben und mit nur einem sauberen VPN nicht ins Darknet kommen.


### Open Source vs Closed Source

Bei Freier Software wie Linux handelt es sich um Programme, deren Quelltext einsehbar ist und unter bestimmten Lizenzbedingungen verändert und weitergegeben werden darf. Dadurch entsteht die Möglichkeit, den Programmcode zu untersuchen und potentielle Hintertüren zu entdecken. Beim Gegenteil, der proprietären Software, wie z.B. Windows, ist der Quelltext nicht einsehbar, wird aber auf Anfrage von einigen Herstellern zur Verfügung gestellt. Man kann daher nicht 100% sicher sagen was diese Programme im Hintergrund machen. Eine platzierte Spionagesoftware kann daher leicht unerkannt bleiben.

Grundsätzlich ist keine Software vor Infiltrierung durch Dritte geschützt. Bei grossen Projekten wie zum Beispiel dem Linux-Kernel muss der Programmcode durch eine oder sogar mehrere Personen geprüft und freigegeben werden. Erst danach wird er dann veröffentlicht. Dieser Prozess des vorherigen Prüfens heißt Peer Review.

In der Vergangenheit kam es auch im Umfeld Freier Software zu größeren Sicherheitsproblemen, wie zum Beispiel der Heartbleed-Sicherheitslücke, die es Angreifern erlaubte, verschlüsselte HTTPS-Verbindungen abzuhören. Eine Verfügbarkeit des Quelltextes alleine garantiert somit also keine generelle Sicherheit, sie ist aber eine wichtige Voraussetzung, um die Sicherheit von Software zu erhöhen. Daher also das Fazit: Linux ist sicherer als Windows.

Beim Surfen im Internet hinterlässt man eine Vielzahl von Datenspuren, die von Dienst-Anbietern und Ermittlungsbehörden genutzt werden können. In erster Linie dienen sie zur Ermittlung von Vorlieben, um auf den Anwender zugeschnittene Werbung oder Suchergebnisse anzeigen zu können. Gerade bei der Online-Suche kann das schnell zu einer sogenannten Filter Bubble führen. Isst man beispielsweise gerne Asiatisch und hat in der Vergangenheit bei Google nach asiatischen Restaurants gesucht, besteht eine sehr hohe Wahrscheinlichkeit, dass man in Zukunft in erster Linie asiatische Varianten von Restaurants als Suchergebnis erhält. 

Das mag zunächst harmlos klingen, in der Praxis kann das aber bedeuten das uns z.B. die DHL-Webseite anhand der vorher geöffneten Packstation Accounts wiedererkennt und unsere Aktivitäten eindeutig zuzuordnen sind. Oder GMX erkennt das wir heute schon 10 Mailadressen angelegt haben und kann diese Adressen miteinander in Verbindung bringen. Das wollen wir natürlich alles vermeiden.


### Tracker

Seit einigen Jahren gibt es die Möglichkeit, einem Webseiten-Betreiber mitzuteilen, dass man nicht verfolgt werden möchte. Im Firefox aktiviert man diese Einstellung, indem man in den „Settings“ unter dem Punkt „Privacy“ die Option „Tell sites that I dont want to be tracked“ wählt. Da es aber bisher weder in Europa noch in den USA einen verbindlichen rechtlichen Rahmen für die Funktion gibt, respektieren nur wenige Seitenbetreiber diese Einstellung.

Im Falle von Betrug gelten diese Richtlinien ohnehin nicht. Die Anti-Fraud-Systeme der einzelnen Webseiten sind sogar extra darauf ausgelegt möglichst viele und möglichst genaue Daten über uns zu sammeln. Auch die Polizei wird versuchen möglichst viele Informationen zu bekommen um uns zu identifizieren. 

Tracker nutzen auf Webseiten eingebundene Elemente, um zu verfolgen, welche Webseiten besucht worden sind. Einen wirksamen Schutz gegen Tracker bietet das Addon Privacy Badger. Er verhindert die Datenübermittlung der Tracker und schaltet somit ihre Funktion aus. Diese Erweiterung wird von der Electronic Frottier Foundation (EFF) entwickelt. Die EFF setzt sich für Grundrechte im Informationszeitalter ein. Die Erweiterung benötigt nach der Installation keine besondere Konfiguration.


### Cookies

Grundsätzlich kann man sagen, dass Cookies weder schlecht noch gefährlich sind. Das sind kleine Dateien, die das Verhalten der Nutzer auf dem eigenen Computer speichern und mit bestimmten Websites interagieren. Sie dienen beispielsweise dazu, eine Sitzung aufrechtzuerhalten. Beim Aufruf einer Webseite kann ein „Cookie“ für die spätere Nutzung gesetzt werden. Beim nächsten Zugriff auf diese Webseite schickt der Browser automatisch den Cookie mit. Der Anbieter kann mit Hilfe des Cookies den Nutzer eindeutig zuordnen. Das wollen wir natürlich nicht, daher schalten wir diese Funktion ab.

Ein besonderer Fall sind Third Party Cookies. Dabei handelt es sich um reguläre Cookies, die aber nicht direkt zur aufgerufenen Webseite gehören. Es wird zum Beispiel ein Facebook-Like-Button in eine Webseite eingebunden. Der Button wird direkt von Facebook geladen und muss nicht angeklickt werden, um den Cookie zu setzen. Der Prozess passiert im Hintergrund.

Wenn man Third-Party-Cookies deaktiviert, werden keine Cookies mehr für Webseiten gesetzt, die nicht direkt aufgerufen worden sind. Die Option zum Deaktivieren von Third-Party-Cookies ist im Firefox etwas versteckt. In den „Privacy“-Einstellungen stellt man zunächst von „Firefox will Remember History“ auf „Use Custom Settings for History“ um. Danach kann man den Punkt „Accept third-party cookies“ auf „Never“ stellen. Firefox bietet ausserdem die Option, alle Cookies beim Beenden des Browsers zu löschen, was wir auch immer tun sollten.


### Adobe Flash

Der Adobe Flash Player hat keine besonders ruhmreiche Vergangenheit, was Sicherheit anbelangt. Der Flash-Player ist durch seine hohe Verbreitung umso verlockender für Angriffe auf die Privatsphäre. Daher sollte man grundsätzlich darauf verzichtet. Viele Dienstanbieter wie YouTube haben auf HTML5-Technologie zum Abspielen von Video- und Audiodateien umgestellt. Apple hat bereit schon 2010, noch unter Steve Jobs Führung, auf Flash in allen seinen Produkten verzichtet. Google hat den hauseigenen Flash-Player Peppermint im Mai 2015 testweise aus Chrome deaktiviert. Mit dem HTML5-basierten Flash-Player Shumway des Mozilla-Projektes ist es möglich, rudimentäre Flash-Inhalte ohne den Adobe Flash Player abspielen zu können. Im Normalfall braucht man Flash auf dem „Arbeitsrechner“ nicht.

Falls man trotzdem noch nicht auf den Adobe Flash Player verzichten kann, sollte man den lokalen Cache deaktivieren. Die Flash-Einstellungen kann man vornehmen, indem man mit der rechten Maustaste auf einen Flash-Inhalt klickt und „Global Settings“ wählt. Unter „Storage“ kann man dann „Block all sites from storing information on this computer“ wählen, um die Cachefunktion abzuschalten.


### NoScript

Das Firefox-Addon NoScript bietet die Möglichkeit, für jede Webseite einzustellen, ob aktive Elemente (sogenannte Skripte) ausgeführt werden sollen. Dabei wird der Ansatz verfolgt, dass standardmäßig alle Skripte verboten sind und pro Webseite freigeschaltet werden müssen. Das ist eine sehr hilfreiche Technik Tracking durch Java zu unterbinden.

Nach der Installation des Add-ons findet man ein entsprechendes Symbol neben der Adressleiste. Sollten auf einer Seite Skripts blockiert worden sein, öffnet sich zusätzlich eine Benachrichtigung im unteren Bereich des Browserfensters. Über einen Klick auf das Symbol öffnet sich eine Liste aller auf der gerade geöffneten Webseite eingebundener Skripte. Angegeben wird jeweils der Name der Webseite, von der versucht wird das Skripte zu beziehen. Besucht man zum Beispiel die Webseite der DHL, wird in der Liste nicht nur „dhl.de“ aufgeführt, sondern auch eine Vielzahl weiterer Webseiten wie zum Beispiel Google, von denen weitere Skripte bezogen werden. In den meisten Fällen kommen diese Skripte von Werbeanbietern oder Analyseseiten und werden zur Identifikation und zum Tracking genutzt.

Einige Darstellungs-Funktionen von Websites sind manchmal per Javascript umgesetzt – z.B Google Captures. Man sollte mit dem Plugin also aufmerksam umgehen. Sollte eine Webseite nicht mehr wie gewünscht dargestellt werden, kann man schrittweise Skripte von fremden Webseiten temporär zulassen, bis der Inhalt wieder korrekt dargestellt wird. Nachdem man so herausgefunden haben, welche Skripte freigeschaltet werden müssen, kann man diese permanent zulassen. Einstellungen bei NoScript gelten immer global. Es ist nicht möglich den Zugriff auf z. B. „googleapis.com“ für eine Webseite zuzulassen, für eine andere aber zu sperren.


### WebRTC

Mit WebRTC kann die lokale IP Adresse des Rechners im LAN und die öffentliche IP Adresse ermittelt werden, wie eine Demonstration von D. Roesler zeigt. Auch VPN-Verbindungen können damit ausgetrickst werden. Außerdem kann das Vorhandensein von Kamera und Mikrofon als Feature im Browser Fingerprint genutzt werden.

Mit dem Plugin Disable WerRTC kann die Übermittlung der Daten abgeschaltet werden.


### Fake User-Agent

Bei jedem Aufruf einer Webseite wird der Name und die Version des Browsers an den Webseitenbetreiber übermittelt, der sogenannte User-Agent-String. Die Informationen umfassen die Geräteart und -typ (PC, Tablet, Smartphone), die verwendete Bildschirmauflösung und das benutzte Betriebssystem sowie auch der auf dem System installierten Schriften, die zum Beispiel mit Hilfe von JavaScript ausgelesen werden können. Anhand dieser Daten kann ein Benutzer schon sehr genau identifiziert und zu mindestens 90% wiedererkannt werden.

Eine mögliche Gegenmaßnahme ist es, den User-Agent-String bei jedem Aufruf einer Webseite zu wechseln. Zu diesem Zweck eignet sich die Erweiterung Secret Agent. Nach der Installation desselbigen kann in den Einstellungen des Add-ons eine Liste der zu verwendenden User-Agent-Strings festgelegt werden. Die Standardliste enthält viele exotische Browser, was dazu führt, dass einige Webseiten nicht mehr korrekt dargestellt werden. Daher empfiehlt es sich, diese Liste zu bereinigen und nur moderne Browser-Varianten zu verwenden. Dazu öffnet man in den Plug-in-Einstellungen das Tab „User Agents“ und bearbeitet den Inhalt der Box „Stealth Mode“.

Der Stealth Mode kann daraufhin im Tab „Entropy“ über den Punkt „Enable Secret Agent’s Stealth Mode“ aktiviert werden. Hier lässt sich auch festlegen, in welchem zeitlichen Abstand der User-Agent-String rotiert werden soll. Alle weiteren Einstellungen des Add-ons können auf den Standardwerten belassen werden. Sollte es Probleme mit der Darstellung einer bestimmten Webseite geben, kann diese in der Host-Whitelist eintragen werden. Etwas störend wirkt die Secret Agent Toolbar. Sie kann bei Bedarf über „View -> Toolbars -> Secret Agent Toolbar“ ausgeblendet werden.


### Referrer

Beim Aufruf eines Links auf einer Webseite wird der Zielseite automatisch über einen sogenannten Referrer im HTTP-Header mitgeteilt, von welcher Seite die Anfrage kam. Hat man z. B. auf Google nach dem Wort „Packstation“ gesucht und klickt auf einen Treffer von DHL, dann bekommt DHL die Information, dass man zuvor auf Google war und dort nach dem Wort „Packstation“ gesucht hat.

Diese Funktion kann für Webseitenbetreiber sehr sinnvoll sein, um Webseiten strukturell besser aufzubauen. Denn damit kann auch ermittelt werden, wie Links am häufigsten aufgerufen werden. Auf der anderen Seite verraten Referrer, welche Suchworte eingegeben wurden, um auf eine Seite zu gelangen.

Da sich ein generelles Deaktivieren negativ auf den Surfkomfort auswirken kann, empfiehlt sich das Zulassen von Referrern innerhalb einer Seite und das Deaktivieren von Referrern beim Wechsel auf eine andere Seite. Leider bietet Firefox selbst diese Einstellmöglichkeit nicht an. Dazu eignet sich die Erweiterung RefControl.

Nach der Installation des Add-ons und dem Neustart des Browsers findet man im „Tools“-Menü einen Eintrag zur Konfiguration der RefControl-Optionen. Dort müssen keine einzelnen Seiten hinzugefügt werden. Stattdessen klickt man neben „Default for sites not listed“ auf „Edit“ und stellt dort „Block“ als Standardaktion ein. Durch das Setzen des Hakens bei „3rd Party requests only“ stellt man sicher, dass die Einstellung nur für den Aufruf neuer Seiten gilt.


### Modus des Browsers

Firefox sollte immer so eingestellt werden dass nach dem Schließen alle Daten über die aktuelle Session gelöscht werden. Unter Settings → Datenschutzeinstellungen können entsprechende Einstellungen gesetzt werden. Haken setzen bei „Die Chronik löschen, wenn Firefox geschlossen wird“ und Cookies nur behalten bis Firefox geschlossen wird. So werden nach dem Schließen immer alle Daten gelöscht und es baut sich keine History auf.


### Suchmaschine

Die Anbieter Google und Bing haben sich bei der Suche im Internet stark durchgesetzt. Damit wissen sie viel über die Vorlieben und das Surfverhalten eines Benutzers. Es gibt alternative Anbieter, die zusichern, keine personenbezogenen Daten zu speichern und weiter zu verarbeiten. Dazu gehören die Suchmaschine DuckDuckGo oder die Schweizer Metasuchmaschine eTools.ch.

StartPage ist eine Suchmaschine, die im Hintergrund auf Google zugreift. Sie ist vollständig lokalisierbar. Es kommt keine personalisierte Suche zum Einsatz, wodurch die Gefahr einer «Filter Bubble» verringert wird.


### HTTPS benutzen

Beim Zugriff auf Webseiten über HTTP werden alle Informationen unverschlüsselt übertragen und können leicht von Dritten analysiert werden. Besonders eine Übertragung von Passwörtern über HTTP ist sehr kritisch.
Um HTTPS für möglichst viele Seiten zu forcieren, bietet sich das Firefox-Add-on HTTPS everywhere der Electronic Frontier Foundation an. Nachdem dessen Installation erfolgt ist und der Browser neu gestartet wurde, findet man neben der Adressleiste ein neues Symbol, über das sich die Erweiterung steuern lässt. Ob die aktuelle Verbindung per HTTPS verschlüsselt ist, kann man anhand des Schlosssymbol in der Adressleiste erkennen.


### VPN

Beim Surfen im Internet kann ein Nutzer eindeutig einem Rechner und einer IP-Adresse zugeordnet werden. Falls möglich, empfiehlt sich immer die Nutzung eines offenen, anonymen WLAN-Zugangs (z. B. in einem Café).  

Ein VPN ist dagegen Pflicht. Der VPN ändert deine IP und verschleiert somit deine reale IP-Adresse. Dazu kommt dass eine VPN-Verbindung immer ein verschlüsselter Tunnel ist, somit kann auch der Betreiber und alle Knotenpunkte über die deine Verbindung geht nichts mitlesen sondern sehen nur den verschlüsselten Tunnel. Bei der Nutzung von Tor ist ein VPN zu empfehlen um den Tor-Traffic im VPN-Tunnel zu verstecken. So wird eine Analyse von Online-Zeiten usw. unterbunden.

Traffic den man nicht sehen kann kann man auch nicht abhören. Also sollte bei einem VPN immer auf starke Verschlüsselung und sicheren Schlüsseltausch achten. Ist der VPN einmal sicher aufgebaut gibt es keine Möglichkeit den Traffic im inneren abzuhören oder zu manipulieren. Stellt der VPN-Client eine Manipulation am Tunnel fest wird der Tunnel abgebrochen und erneut eine sichere Verbindung aufgebaut. 

Passende VPN Angebote findest du in unseren Listings.


### Tor-Netzwerk

Beim sogenannten Onion-Routing werden die Verbindungen über die einzelnen Tor-Knoten, die auf Rechnern in der ganzen Welt laufen, geleitet. Man kann Tor als Client nutzen oder auch selbst einen Knoten anbieten, über den dann andere Teilnehmer anonym surfen können. Die Verbindung zwischen den Knoten wird verschlüsselt. Die einzelnen Teilnehmer haben dabei keinen Einblick in die übermittelten Daten. Am Endpunkt, also am Übergang zum angefragten Zielserver, muss die Verbindung wieder entschlüsselt werden. Dieser Knoten hat Zugriff auf die übertragenen Daten. Es ist also auch hier sehr zu empfehlen, nur verschlüsselte Verbindungen aufzubauen.

Die einfachste Möglichkeit Tor zu nutzen, ist der vom Projekt bereitgestellte Tor-Browser. Dabei handelt es sich um eine modifizierte Firefox-Version, die alle für Tor notwendigen Komponenten bereits enthält.

Alternativ dazu kann man auch eine spezialisierte Linux-Distribution wie zum Beispiel Tails nutzen, die einfach auf einen USB-Stick gespielt und von dort aus gestartet und genutzt werden kann. Tails bietet ausserdem noch einen Windows-Tarnmodus an, in dem sich das System gegenüber Servern im Internet wie ein Windows-Rechner verhält.
Tails eignet sich sehr gut für den Einsatz auf fremden PCs, da es ein abgeschlossenes System ist, das auf dem damit gestarteten Rechner keinerlei Spuren hinterlässt.


#######################################################################################
# Microsoft Windows ist immer unsicher
#######################################################################################

Mit Windows 8.0 hat Microsoft begonnen, dass bei Smartphones akzeptierte Device- based Tracking auch bei PCs einzuführen. Ähnlich wie Google bei Android will Microsoft als einer der fünf größten Datensammler im Internet seine Datenbestände erweitern und besser personalisieren. Das war der Anfang. 
Das Erstellen eines User-Account unter Windows 8.1 wurde ein echtes Dark Pattern. Der Nutzer wird massiv gedrängt, den User-Account auf dem Rechner mit einem Online Konto bei Hotmail oder Windows Live zu verbinden. Nur wenn man in der Eingabemaske falsche Angaben macht, findet man in der Fehlermeldung den unscheinbaren Link für das Erstellen eines User-Account ohne Online Konto bei Microsoft. 
In Windows 10 wurde das Device-based Tracking weiter ausgebaut. Es wird für jeden Account auf dem Rechner eine "Unique Advertising ID" generiert. Diese ID wird auch Dritten zur eindeutigen Identifikation zur Verfügung gestellt.

In der neuen Privacy Policy von Microsoft (April 2018) steht außerdem: 
We will access, disclose and preserve personal data, including your content (such as the content of your emails, other private communications or files in private folders), when we have a good faith belief that doing so is necessary ...
Privaten Daten, die Microsoft in der Standardkonfiguration sammelt: 

# Persönliche Interessen, die sich aus dem Surfverhalten ergeben sowie aus den per Apps gesammelten Daten werden an Microsoft gesendet (eine Sport-App sendet die bevorzugten Teams, eine Wetter-App die häufig angefragten Städte...) 

# Standortdaten aller Geräte mit Windows werden an Microsoft übertragen. Es wird bevorzugt GPS oder die WLANs der Umgebung genutzt, um den Standort so genau wie möglich zu bestimmen. 

# Kontaktdaten der Freunde und Bekannten werden an Microsoft übertragen, wenn man Tools von Microsoft als Adressbuch nutzt. 

# Inhalte von E-Mails, Instant Messages und Voice/Vidoe Messages (z.B Skype) gehören ebenfalls zu den den Daten, die Microsoft sammelt. 

# Der Windows Defender übermittelt alle installierten Anwendungen. 

# Mit der digitalen Assistentin "Cortana" wird in der Standardkonfiguration eine Art Abhörzentrale eingerichtet, die das Wohnzimmer direkt mit Microsoft verbindet. 

# Mit dem Anniversary Update zum 02. August 2016 wird es fast unmöglich gemacht, die aufdringliche, spionierende "Cortana" abzuschalten, da die digitale Assistentin die komplette Suche bereitstellt (sowohl lokal als auch im Web). 
Das Schreibverhalten wird analysiert und an Microsoft gesendet. Das Profil der typischen Tastenanschläge könnte zukünftig für die Identifikation bei Texteingaben in Webformularen oder Chats genutzt werden (Stichwort: Keystroke Biometrics). 

# Die eindeutige UUID, die Windows bei der Kommunikation mit Microsoft­servern sendet (z.B. bei Softwareupdates), wird vom NSA und GCHQ als Selektor für Taylored Access Operations (TAO) verwendet, um gezielt die Computer von interessanten Personen oder Firmen anzugreifen.
 
# Als besonderes Highlight gehören auch die automatisch generierten Recovery Keys der Festplattenverschlüsselung Bitlocker zu den Daten, die MS in seiner Cloud sammelt und NSA/FBI/CIA zur Verfügung stellt. (Crypto War 3.0?) 

Mit Windows 10 Pro oder Enterprise kann man den Upload des Recovery Key verhindern, indem man den Rechner einmal komplett verschlüsselt (mit Key Upload), dann die Verschlüsselung deaktiviert (damit muss das System wieder komplett entschlüsselt werden), den alten Recovery Schlüssel löscht und nochmal den Rechner komplett verschlüsselt. Erst beim zweiten Versuch wird man gefragt, ob man den Recovery Key evtl. lokal sichern möchte. Das kostet Zeit und ist auch wieder ein echtes Dark Pattern in der Benutzerführung. 

Wenn man es schafft, einen Benutzeraccount ohne Cloud Anbindung einzurichten und in den Einstellungen unter Datenschutz die Privacy Features aktiviert, kann man die Sammelleidenschaft etwas reduzieren aber nicht vollständig abstellen. 

Experten des BSI warnen seit 2013 vor dem Einsatz von Windows 8 in Kombination mit TPM 2.0 und bezeichneten es als inakzeptables Sicherheitsrisiko für Behörden und Firmen. Nutzer eines Trusted-Computing-Systems verlieren nach Ansicht der Experten die Kontrolle über ihren Computer. 
Aus Sicht des BSI geht der Einsatz von Windows 8 in Kombination mit einem TPM 2.0 mit einem Verlust an Kontrolle über das verwendete Betriebssystem und die eingesetzte Hardware einher. Daraus ergeben sich für die Anwender, speziell auch für die Bundesverwaltung und kritische Infrastrukturen, neue Risiken.

Fazit: 

Windows ist also alles andere als sicher und bestimmt nicht gut für unsere Zwecke geeignet. Daher empfehlen wir, wenn es unbedingt Windows sein muss eine ältere Version wie Windows XP oder deren Nachfolger zu benutzten. 



#######################################################################################
#  Anonymisierung von Firefox
#######################################################################################

Mozilla Firefox ist der Webbrowser der Mozilla Foundation und kann durch viele von der Community entwickelte Add-ons und Anpassungen in der Konfiguration zu einem sicheren und privacy-freundlichen Browser aufgewertet werden. Er ist kostenfrei nutzbar und steht auf der Downloadseite für Windows und MacOS bereit. 
→ https://www.mozilla.org/en-US/firefox/all/


### Firefox about:config

Der Konfigurations-Editor listet alle möglichen Firefox Settings die aus den Dateien prefs.js und user.js gelesen werden können. Zusätzlich werden hier die Default-Einstellungen angezeigt. Viele dieser Einstellungen können nur so geändert werden und sind nicht über die üblichen Menüs erreichbar. Mit der Eingabe von "about:config" in der Adressleiste des Firefox kann die Settings-Page aufgerufen werden. Es erscheint eine Warnung die fragt ob man wirklich weiß was man tut. In diesen Settings sollten nur Einstellungen geändert werden deren Auswirkung man sich auch bewusst ist. Andernfalls können schnell weitere Sicherheitslücken entstehen. 

Um einen bestehenden Wert zu ändern musst du einen rechtsklick auf die entsprechende Einstellung machen und dann "Modify" klicken. Alternativ kannst du auch einen Doppelklick machen. Dann kannst du den neuen Wert in das sich öffnende Fenster eintragen. Um nach bestimmten Einstellungen zu suchen kannst du einfach die Suchleiste ganz oben verwenden.

# Nützliche Firefox Mods

media.peerconnection.enabled  =  false
geo.enabled = false
geo.wifi.uri = [leave blank]
network.http.accept.default = text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
network.http.use-cache = false
network.http.keep-alive.timeout = 600
network.http.max-persistent-connections-per-proxy = 16
network.proxy.socks_remote_dns = true
network.cookie.lifetimePolicy = 2
network.http.sendRefererHeader = 0
network.http.sendSecureXSiteReferrer = false
network.protocol-handler.external = false [set the default and all the subsettings to false]
network.protocol-handler.warn-external = true [set the default and all the subsettings to true]
network.http.pipelining = true
network.http.pipelining.maxrequests = 8
network.http.proxy.keep-alive = true
network.http.proxy.pipelining = true
network.prefetch-next = false
browser.cache.disk.enable = false
browser.cache.offline.enable = false
browser.sessionstore.privacy_level = 2
browser.sessionhistory.max_entries = 2
browser.display.use_document_fonts = 0
intl.charsetmenu.browser.cache = ISO-8859-9, windows-1252, windows-1251, ISO-8859-1, UTF-8
dom.storage.enabled = false
extensions.blocklist.enabled = false


#######################################################################################
#  Festplatten Verschlüsseln
#######################################################################################

Warum überhaupt verschlüsseln? Klare Sache, falls doch mal die Polizei vor der Türe steht werden sie sicher euren Rechner, alle Speichermedien usw beschlagnahmen. Schlecht wenn dann alle eure Geschäfte, Accounts, Daten auf dem Rechner gespeichert sind. Wenn die Platte oder bzw. ein Container gut verschlüsselt ist und das Passwort nicht leicht erraten werden kann kommt nicht mal die CIA an eure Daten ran, versprochen. Zum Verschlüssen benutzen wir Veracrypt.

VeraCrypt ist der offizielle Nachfolger von TrueCrypt, d.h. wer sich schon mit TrueCrypt auskennt wird sich sehr schnell auch in VeraCrypt einarbeiten können. TrueCrypt wurde anhand Sicherheitsmängel eingestellt, VeraCrypt hat diese beseitigt und bietet das Programm kostenlos für Windows, Linux und auch Mac an.

Man kann folgendes damit verschlüsseln:

- Einzene Ordner (Containerdatei erstellen)
- Komplette Partitionen
- Das ganze System
- Versteckte Container in einer verschlüsselten Partition/Container

Was ist ein Container? Man kann sich das so vorstellen wir im realen Leben, das man einen Überseecontainer öffnet, Sachen dort hereinbringt und den Container danach abschließt. Jetzt kommt nur noch derjenige an die Sachen der den richtigen Schlüssel hat. Genauso ist das mit einem VeraCrypt Container. Es wird eine Datei erstellt die xxxMB groß ist, die man öffnen kann, Daten reinkopiert und dann wieder vom PC trennt. Jetzt sieht man nur eine xxxMB große Datei, kann aber nichts damit anfangen.

Ich empfehle nicht unbedingt komplette Partitionen auf externen Datenträgern zu verschlüsseln, denn wenn man diese an das Betriebssystem hängt kommt bei Windows z.B. direkt der Hinweis den Datenträger zu formatieren weil Windows mit dem Dateisystem nichts anfangen kann, ein falscher Klick und die Daten sind im Nirvana. Also lieber eine Containerdatei erstellen.

# Container erstellen

Als erstes starten wir VeraCrypt als Administrator. Das hat den Hintergrund weil ich bei TrueCrypt damals öfters mal Probleme bekam, vielleicht ist es mit VeraCrypt jetzt anders, aber das weiß ich nicht. Folgendes war damals passiert, ich startete TrueCrypt ganz normal, ließ einen 930GB Container erstellen, damit war der PC 8-12 Stunden beschäftigt, am Ende kam dann eine Fehlermeldung weil das Programm keine Administrator Rechte bekam, da war die Arbeit der ganzen Stunden dahin. Startete ich aber direkt als Administrator lief das Programm bis zum Ende ganz normal durch.

- Volumen und auf Neues Volumen erstellen
- Containerdatei erstellen auswählen
- Standard VeryCrypt Volume auswählen
- Speicherort für den Verschlüsselten Container angeben

Jetzt geht es darum den Verschlüsselungsalgorithmus auszuwählen. Hier solltet ihr IMMER eine Kombination wählen. AES - Blowfish z.B. Der Hash Algorithmuss sollte SHA-512 sein.

- Größe des Containers angeben

Jenachdem wieviel Daten ihr speichern wollt reicht oft schon ein kleiner Container mit 500Mb oder 1GB. Diesen könnt ihr dann z.b. einfach auf einen USB-Stick kopieren und eure Daten sicher und verschlüsselt mitnehmen. Der Container kann dann an jedem Rechner auf dem VeraCrypt installiert ist entschlüsselt und verwendet werden. 

- Passwort für den Container vergeben

Im nächsten Fenster haben wir die Auswahl nach einem Dateisystem. NTFS ist ratsam wenn ihr Dateien über 4GB speichern wollt, FAT kann das nicht. 

Jetzt einfach mit dem Mauszeiger im Fenster wild hin und her fahren. Wenn man meint man hat es lange genug gemacht geht man auf Formatieren. Je nach Größe des Containers und Leistung deines Rechners kann das etwas dauern.

Es kommt eine Meldung dass das Volume erstellt wurde. Ein Klick auf "Weiter" und wir sind fertig.

Bevor du wichtige Daten in den Container legst teste bitte ob alles funktioniert und du verstanden hast wie man den Container benutzt. 

# Container öffnen

- Veracrypt starten
- Freien Laufwerksbuchstaben wählen
- Containerdatei auswählen
- Einbinden klicken
- Passwort eingeben
- Der Container ist nun unter dem Laufwerksbuchstaben verfügbar


#######################################################################################
#  Tor-Browser-Bundle | Security STAGE 1
#######################################################################################

Mit wenigen Klicks surfen wir anonym über Tor im Netz – ganz gleich, ob unter Windows, Linux oder OS X. Der Tor-Browser ist die einfachste und schnellste Lösung anonym ins Internet zu kommen.
Der Einstieg in das Anonymisierungs-Netzwerk Tor ist schnell geschafft und nicht komplizierter als eine Firefox-Installation. Das kostenlose Tor-Browser-Bundle bringt alles mit, was wir brauchen: den Tor-Client, der eine Verbindung zum Netzwerk herstellt sowie eine vollständig vorkonfigurierte Firefox-Version namens Tor Browser. Damit wir auch tatsächlich anonym surfen und nicht an eine manipulierte Version des Bundles geraten, sollten man nur direkt beim Tor Project herunterladen. 
Der Tor-Browser ist für Gelegenheits-User gut geeignet und auch völlig ausreichend.


#######################################################################################
#  Tails auf USB-Stick | Security STAGE 2
#######################################################################################

Tails ist ein Live-Betriebssystem, das darauf ausgerichtet ist unsere Privatsphäre und Anonymität zu bewahren. Es hilft uns dabei, das Internet so gut wie überall und von jedem Computer aus anonym zu nutzen, ohne dabei Spuren zu hinterlassen, sofern wir dies nicht ausdrücklich wünschen.

Tails beinhaltet verschiedene Programme, die im Hinblick auf die Sicherheit vorkonfiguriert wurden: einen Webbrowser, einen Instant-Messaging-Client, ein E-Mail-Programm, ein Office-Paket, einen Bild- und Audioeditor usw.

### Tails USB-Stick erstellen

Die Installation von Tails lässt sich auch als Laie im IT-Bereich bewerkstelligen. Sie können Tails über Windows, Mac Os X, DEBIAN/UBUNTU oder LINUX (Red Hat, FEDORA,...) installieren. Natürlich handeln sie eigenverantwortlich.

Für die Installation benötigen wir folgendes:

- Einen Computer mit Internetzugang 
- Zwei USB-Sticks mit mindestens 4GB Speicher 
- Einen weiteren Computer, Smartphone oder Drucker, für die weiteren Schritte der Installation
- Ca. zwei Stunden Zeit
Zwei USB-Sticks sind nötig, weil man zunächst eine Vorab-Version von Tails auf dem einem Stick installieren muss und erst im nächsten Schritt über diesen ersten Stick die finale Version von Tails auf den zweiten Stick installiert.
Eine sehr ausführliche Installationsanleitung finden sie auf der unten verlinkten Herstellerwebseite. Ich gebe an dieser Stelle nur einen kurzen Überblick über den Installationsvorgang.

# Download von Tails
Als erstes muss die Installationsdatei von der Herstellerwebseite geladen werden. Achte darauf, dass es sich auch wirklich um die originale Webseite handelt. 
→ https://tails.boum.org/index.de.html

Nach ein paar Angaben über ihr verwendetes Betriebssystem und die bevorzugte Installationsweise (du kannst Tails auch von einer bereits bestehenden Tails-Installation aus installieren), starte den Download der Installationsdatei. Dabei kann es notwendig sein, im Vorfeld ein Firefox-Plugin zu installieren, das den Download der Tails-ISO verifiziert.

# Tails auf dem USB-Stick installieren

Im nächsten Schritt müssen wir ein Programm (Universal USB Installer) laden, das es erlaubt, die eben geladene Tails-ISO auf dem ersten USB-Stick zu installieren. Diesen Stick können wir jetzt schon mit dem Computer verbinden.

Nach dem Download des USB-Installers starten wir diesen durch einen Doppelklick. Eventuell wirst du von deinem Betriebssystem noch nach einer Bestätigung gefragt, ob du dieses Programm wirklich starten willst. Bestätige dies und lese im Anschluss die Lizenzvereinbarung des USB-Installers durch und bestätige diese.

Nun müssen wir in einem Dropdown-Menü die Linux-Destribution Tails auswählen (ist ziemlich weit unten im Menü), als Quelle das zuvor geladene ISO-Image und als Ziel den ersten USB-Stick. Außerdem müssen wir bei „Format“ ein Häkchen setzen, durch das wir bestätigen, dass der USB-Stick formatiert werden darf (ACHTUNG! Alle Daten auf dem Stick werden dabei gelöscht.)

Nun müssen wir nur noch die Installation von Tails bestätigen und im Anschluss den Universal USB-Installer schließen. Auf dem ersten USB-Stick befindet sich jetzt die Vorab-Version von Tails.
Jetzt müssen wir den Computer über den USB-Stick neu starten. Im Vorfeld sollten sie diese Webseite auf einem anderen Gerät (Computer, Tablet, Handy,...) aufrufen, bzw. die weiteren Schritte der Installation ausdrucken oder notieren.

Je nach Hersteller des Computers kann es nötig sein, den Computer in einem anderen Modus (Boot-Menu) zu starten, über den man dem Computer vorgeben muss, über den USB-Stick zu starten. Wenn wir die Tastenkombination dafür nicht kennen, können wir versuchen folgende Tasten während des Startvorgangs zu betätigen: Esc, F12, F10, F9, F8 oder F2. Bei meinem PC sind es zum Beispiel Del oder F2. Damit kommt man in das Boot-Menu und zur Möglichkeit, über den USB-Stick zu starten. Daneben lässt sich die Reihenfolge von den zu bootenden Laufwerken verändern und speichern. Man kann z.B. USB → HDD → CD einstellen, wenn immer als erstes versucht werden soll, über den Stick zu starten, falls ein USB-Stick am Computer angeschlossen ist. Ist keiner angeschlossen, so startet das System über die Festplatte.

Wenn sie es geschafft haben, das System über den USB-Stick zu starten, erscheint ein kleines Auswahlfenster. Hier bestätigen sie mit der Return-Taste den ersten Punkt (Live). Im Anschluss wählen sie noch die bevorzugte Sprache aus. Wir haben nun die Vorabversion von Tails erfolgreich installiert.

# Tails auf zweitem USB-Stick installieren

Im Anschluss müssen wir die endgültige Version von Tails auf dem zweiten USB-Stick installieren. Dazu schließen wir den zweiten Stick am Computer an, gehen in Tails auf Anwendungen → Tails → Tails Installer und wählen Install by Cloning aus.

Wähle den zweiten USB-Stick als Target Device und klicke auf Install Tails, um die Installation auf dem zweiten Stick zu starten. Es folgt eine Warnmeldung, dass alle Daten auf dem zweiten Stick gelöscht werden. Bestätige diese, wenn wir damit einverstanden sind. Die endgültige Version von Tails wird jetzt auf dem zweiten USB-Stick installiert.

Nach der erfolgreichen Installation können wir den Computer runter fahren und den ersten Stick entfernen. Starte nun den Computer von dem zweiten USB-Stick, so wie wir es bereits erfolgreich mit dem ersten Stick gemacht haben.

# Tails auf USB-Stick oder Speicherkarte oder sogar DVD?

Wer Tails auf einem USB-Stick oder einer Speicherkarte nutzt, hat den Vorteil, dass Daten direkt auf dem Datenträger (Stick oder Karte) gespeichert werden können. Dafür hat es den Nachteil, dass das System über Schadsoftware geändert werden kann. Wer ein absolut sicheres System wünscht, sollte Tails auf einer DVD installieren. Dadurch wird erreicht, dass das System nicht mehr geändert werden kann. Wer Daten über Tails speichern möchte, kann immer noch einen Datenträger über das System auswählen, und die Daten darauf speichern, was aber doch sehr umständlich sein kann.

Wir können die Benutzeroberfläche von Tails so einstellen, dass sie der von Windows XP ähnelt. Dazu müssen wir in Tails unter „System → Einstellungen → Erscheinungsbild“ die Windows XP Benutzeroberfläche auswählen und bestätigen. Das machst die Nutzung für viele User einfacher.


#######################################################################################
#  Hochsicheres Whonix System | Security STAGE 3
#######################################################################################

Whonix ist eine Debian-basierende Linux-Distribution, die auf Privatsphäre, Sicherheit und Anonymität im Internet Wert legt. Um dies zu erreichen, setzt Whonix insbesondere auf die Nutzung des Tor-Netzwerks. 

Das Betriebssystem besteht aus zwei virtuellen Maschinen, einer Workstation und einem Gateway für das Tor-Netzwerk. Jegliche Netzwerkkommunikation wird durch das Tor-Netzwerk geleitet. Updates werden via Tor mit dem Debian apt-get-Paketmanager eingespielt. VirtualBox, Qubes OS und KVM werden als Virtualisierungssoftware unterstützt. Die Desktop-Umgebung ist KDE. Installer werden für Windows, Linux, macOS und Qubes OS angeboten.

Wir richten zusammen das Whonix Grundsystem ein, so dass wir zukünftig von Anfang anonym online unterwegs sind. Dazu nutzen wir einerseits die kostenlose Software VirtualBox. Andererseits aber auch das kostenlose Betriebssystem Whonix sowie ein VPN.


### Benötigte Software

Hier die Software in einer Liste, die du benötigst, um garantiert anonym surfen zu können:
- VirtualBox: Die kostenlose Virtualisierungssoftware ist ungemein leistungsstark und für nahezu jedes Betriebssystem erhältlich. Lade die aktuellste Version hier herunter und installiere VirtualBox anschließend.

- Whonix: Ein Linux-Derivat, das extra dafür geschaffen ist, um anonym surfen zu können. Grundsätzlich besteht Whonix aus zwei Komponenten. Wir benötigen allerdings lediglich das sogenannte „Gateway“. Lade das Image für VirtualBox herunter.

Du benötigst außerdem ein beliebiges weiteres Betriebssystem das Disk-Image. Im Idealfall sollte es eine ISO von Windows 7 oder höher sein. Windows wird nach wie vor von den meisten Anwendern genutzt und gilt als recht einfach zu bedienen. Es hat zwar gewisse Schwächen. Allerdings verfügt es auch über die höchste Kompatibilität. So oder so lässt sich damit vor allem das Grundsystem besonders einfach einrichten. 


### Installation

Bevor man Whonix benutzt ist es sinnvoll zu verstehen wie Whonix überhaupt funktioniert. Whonix besteht aus zwei Teilen. Der erste Teil ist das Gateway welches ein TOR-Relay zur Verfügung stellt. Der zweite Teil ist die Workstation, also die Maschine auf der wir später arbeiten können.

Beide Teile laufen nur als VM (Virtuelle Maschine) auf einem Host. Der Host kann sowohl Windows, Linux oder ein OSX sein. Um VM laufen lassen zu können benötigt der Host das Programm "Virtual Box".

-> https://www.virtualbox.org/wiki/Downloads

Dazu laden wir uns noch die beiden Whonix VMs runter. Je nachdem welches Host-System ihr habt, beide VMs downloaden. Sowohl das Gateway als auch die Workstation.

-> https://www.whonix.org/wiki/Download

Nachdem ihr Virtual Box installiert habt könnt ihr die beiden Whonix VMs importieren. Virtual Box öffnen und folgendes tun:

- Klick File > Import Appliance…
- Klick “Choose” und wähle die Whonix-Gateway.ova File.
- Klick next und dann “Import” ohne Einstellungen zu ändern.
- Warten bis der Import komplett ist.
- Diese Schritte für die Whonix-Workstation.ova File wiederholen.
- Jetzt kann man Whonix-Gateway und Whonix-Workstation starten.

Der default Username ist: user
Der default Passwort ist: changeme

Beim ersten Start müsst ihr durch einen kurzen Setup-Prozess der aber selbstklärend und einfach ist. Danach sollte Whonix nach Updates suchen und diese ggf. installieren.

Passwörter sollten nach der Installation geändert werden. Ganz einfach ein Terminal öffnen und folgendes eingeben. "passwd user", dann ein neues Passwort vergeben.

Gearbeitet wird NUR in der Whonix Workstation. Das Gateway MUSS immer laufen da die Workstation sonst keine Verbindung zum TOR-Netzwerk aufbauen kann.


#######################################################################################
# Finish
#######################################################################################

Das waren die Grundlagen in der Online-Sicherheit. Hat dir der Guide gefallen, dann freuen wir uns über gutes Feedback von dir. Hast du etwas nicht verstanden oder hast Verbesserungsvorschläge dann schreib uns eine Nachricht. Wir freuen uns über jeden Input mit dem wir unsere Produkte verbessern können.

