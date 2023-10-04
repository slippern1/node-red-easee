# node-red-easee
Denne flowen styrer Easee laderobot basert på tid, strømpris og hensyntar effektleddet.
Den kalkulerer også hvor lang tid bilen behøver og lade basert på bilens SOC.

Du må ha en AMS-måler, Powersaver (https://powersaver.no/) og NordPool integrasjonen i Home-Assistant.

1: Endre "Credentials" noden og inneholde ditt epost og passord til din Easee konto; "{\"userName\":\"E-Postadresse\",\"password\":\"PASSORD\"}"

2: Bytt ut "CHANGEME" i alle HTTP nodene med din laderobots serienummer, denne finner du Easee appen -> Laderinnstillinger -> Om.

3: Endre nodene "AMS - Effektledd" og "AMS - Spenning", "AMS - Effektledd".

4: Om du ikke har bilens SOC i Home-Assistant eller Node-Red, kan du slette noden "Ladetid" og alt som omhandler kalkulasjon av ladetiden.

5: Opprette bolsk bryter for som benyttes til Powersaver.

6: Valgfri: Opprett en bolsk bryter i Home-Assistant for manuell overstyring av ladingen: input_boolean.tesla_lading_manuelt
