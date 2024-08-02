# Guia de Documentació del Projecte

Us proporciono una guia completa sobre com documentar l'aplicació, que consta de dos components principals: el scrapper web i el mòdul d'interacció amb l'API de Uber.

## Estructura de la Documentació

La documentació s'ha d'organitzar en les següents seccions per a cada component:

1. **Visió General**
2. **Procés Pas a Pas**
3. **Flux de Dades**
4. **Documentació de les Funcions Principals**

### 1. Documentació del Scrapper Web

#### Visió General

Proporcioneu una breu visió general de la finalitat i la funcionalitat del scrapper web.

#### Procés Pas a Pas

Describiu cada pas del procés de scrapping amb detall. Per exemple:
- **Inicialització:** Descriviu com s'inicialitza el scrapper, incloent-hi qualsevol configuració o paràmetres.
- **Obtenció de Dades:** Expliqueu com el scrapper obté dades dels llocs web objectiu.
- **Processament de Dades:** Detalleu com es processen i es transformen les dades brutes.
- **Gestió d'Errors:** Descriviu com es gestionen els errors i excepcions durant el procés de scrapping.

#### Flux de Dades

Describiu com es mouen les dades a través del scrapper web. Incloeu el següent:
- **Font de Dades:** Especifiqueu els llocs web objectiu des dels quals es scrapen les dades.
- **Processament:** Expliqueu com es processen les dades i quines transformacions s'apliquen.
- **Emmagatzematge:** Detalleu on i com s'emmagatzemen les dades després de processar-les.

#### Documentació de les Funcions Principals

Documenteu cada funció principal amb la següent informació:
- **Nom de la Funció:** `fetchDataFromWebsite()`
- **Finalitat:** Obtenir dades brutes del lloc web especificat.
- **Paràmetres d'Entrada:** URL del lloc web objectiu.
- **Sortida:** Contingut HTML brut del lloc web.
- **Descripció:** Aquesta funció pren l'URL d'un lloc web com a entrada, fa una sol·licitud HTTP per obtenir el contingut i retorna l'HTML brut.

### 2. Documentació del Mòdul d'Interacció amb l'API

#### Visió General

Proporcioneu una breu visió general de la finalitat i la funcionalitat del mòdul d'interacció amb l'API.

#### Procés Pas a Pas

Describiu cada pas del procés d'interacció amb l'API amb detall. Per exemple:
- **Inicialització:** Descriviu com s'inicialitza el mòdul d'interacció amb l'API, incloent-hi qualsevol configuració o paràmetres.
- **Enviament de Sol·licituds:** Expliqueu com l'aplicació envia sol·licituds a l'API.
- **Gestió de Respostes:** Detalleu com es gestionen i es processen les respostes de l'API.
- **Gestió d'Errors:** Descriviu com es gestionen els errors i excepcions durant les interaccions amb l'API.

#### Flux de Dades

Describiu com s'envien i es reben les dades de l'API. Incloeu el següent:
- **Sol·licituds a l'API:** Expliqueu com es preparen i s'envien les dades a l'API.
- **Respostes de l'API:** Descriviu com es gestionen i es processen les respostes de l'API.
- **Utilització de les Dades:** Detalleu com s'utilitzen les dades processades dins de l'aplicació.

#### Documentació de les Funcions Principals

Documenteu cada funció principal amb la següent informació:
- **Nom de la Funció:** `sendDataToAPI()`
- **Finalitat:** Enviar dades processades a l'API especificada.
- **Paràmetres d'Entrada:** Dades a enviar i punt final de l'API.
- **Sortida:** Resposta de l'API.
- **Descripció:** Aquesta funció pren les dades processades i el punt final de l'API com a entrades, envia una sol·licitud HTTP a l'API i retorna la resposta.

## Exemple

A continuació, es mostra un exemple de com hauria de ser la documentació per a una funció en cada component:

### Exemple de Funció del Scrapper Web

**Nom de la Funció:** `fetchDataFromWebsite()`
- **Finalitat:** Obtenir dades brutes del lloc web especificat.
- **Paràmetres d'Entrada:** `string $url` - L'URL del lloc web objectiu.
- **Sortida:** `string` - El contingut HTML brut del lloc web.
- **Descripció:** Aquesta funció pren l'URL d'un lloc web com a entrada, fa una sol·licitud HTTP per obtenir el contingut i retorna l'HTML brut.
- **Ús Exemple:**
  ```php
  $htmlContent = fetchDataFromWebsite('https://example.com');
  ```

### Exemple de Funció del Mòdul d'Interacció amb l'API

**Nom de la Funció:** `sendDataToAPI()`
- **Finalitat:** Enviar dades processades a l'API especificada.
- **Paràmetres d'Entrada:** `array $data` - Les dades a enviar; `string $apiEndpoint` - El punt final de l'API.
- **Sortida:** `array` - La resposta de l'API.
- **Descripció:** Aquesta funció pren les dades processades i el punt final de l'API com a entrades, envia una sol·licitud HTTP a l'API i retorna la resposta.
- **Ús Exemple:**
  ```php
  $apiResponse = sendDataToAPI($data, 'https://api.example.com/endpoint');
  ```

## Exemple de Diagrama de Flux

A continuació es mostra un exemple de diagrama de flux per il·lustrar el flux de dades tant per al scrapper web com per al mòdul d'interacció amb l'API:

```
Scrapper Web:
  +-----------------------+
  | Inicialitza el Scrapper|
  +----------+------------+
             |
             v
  +----------+------------+
  | Obté Dades de l'URL   |
  +----------+------------+
             |
             v
  +----------+------------+
  | Processa Dades Brutes |
  +----------+------------+
             |
             v
  +----------+------------+
  | Emmagatzema Dades Processades|
  +-----------------------+

Mòdul d'Interacció amb l'API:
  +-----------------------+
  | Inicialitza el Mòdul d'API |
  +----------+------------+
             |
             v
  +----------+------------+
  | Prepara Dades per a l'API |
  +----------+------------+
             |
             v
  +----------+------------+
  | Envia Dades a l'API    |
  +----------+------------+
             |
             v
  +----------+------------+
  | Gestiona Resposta de l'API |
  +----------+------------+
             |
             v
  +-----------------------+
  | Utilitza Dades Processades |
  +-----------------------+
```
