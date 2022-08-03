# Organization

Describes the organization entity
-  `id`: Organization Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `legalName`: Organization's legal name
   -  Attribute type: **Property**. [Organization](https://schema.org/Organization)
   -  Required
-  `taxId`: The organization's tax number
   -  Attribute type: **Property**. [taxID](https://schema.org/taxID)
   -  Required
-  `ssnId`: The organization's social security number
   -  Attribute type: **Property**. 
   -  Required
-  `caeId`: The organization's economic activity code
   -  Attribute type: **Property**. 
   -  Optional
-  `address`: The company's headquarters address
   -  Attribute type: **Property**. [address](https://schema.org/address)
   -  Optional
-  `email`: Contact email address
   -  Attribute type: **Property**. [email](https://schema.org/email)
   -  Required
-  `telephone`: Mobile or telephone contact
   -  Attribute type: **Property**. [telephone](https://schema.org/telephone)
   -  Optional
-  `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon
   -  Attribute type: **GeoProperty**. 
   -  Optional



# Project

Contains the information of a project
-  `id`: Projects id Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Project name
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Required
-  `category`: Movel type
   -  Attribute type: **Property**. 
   -  Optional
-  `status`: Indicates the actual workers station * `waiting` - Projects budget approved * `working` - Projects parts are already in the factorys floor * `finished` - Projects parts are all done * `assembly` - Projects parts are being assembled in the test zone * `expedition` - The request from a client is already out from the factory. One of : `Waiting`, `working`, `finished`, `assembly`, `expedition`.
   -  Attribute type: **Property**. 
   -  Optional
-  `nestingTag`: Identification of the final tag to past in wood part originated on nesting station
   -  Attribute type: **Relationship**. 
   -  Optional
-  `producedBy`: Identification of the operators giveName that are working in specific project Name
   -  Attribute type: **Relationship**. 
   -  Optional
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Optional
-  `acessories`: Identification of all nedded acessories for specific project
   -  Attribute type: **Relationship**. 
   -  Optional
-  `part`: Identification of the parts for a specific project comming from cut list
   -  Attribute type: **Relationship**. 
   -  Optional
-  `assemblyBy`: Identification assembled parts belong to some project made for some worker
   -  Attribute type: **Relationship**. 
   -  Optional
-  `expedition`: Identification the addres that will recieve the oreder name
   -  Attribute type: **Relationship**. 
   -  Optional



# Owner

Identifies a clinet (Owner of a project)
-  `id`: Client Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `clientTypeInstitution`: Type of client -> True identifies an institutional client. False identifies a singular client
   -  Attribute type: **Property**. 
   -  Optional
-  `legalName`: Institution legal name
   -  Attribute type: **Property**. [Organization](https://schema.org/Organization)
   -  Optional
-  `givenName`: Client first name
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `familyName`: Client last name
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `taxId`: Client/Institution Tax ID
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Required
-  `address`: The client's address
   -  Attribute type: **Property**. [address](https://schema.org/address)
   -  Required
-  `email`: Contact email address
   -  Attribute type: **Property**. [email](https://schema.org/email)
   -  Required
-  `telephone`: Mobile or telephone contact
   -  Attribute type: **Property**. [telephone](https://schema.org/telephone)
   -  Required
-  `buysTo`: Identification the addres that will recieve the oreder name
   -  Attribute type: **Relationship**. 
   -  Optional



# Worker

Identifies a worker within an organization
-  `id`: Worker Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `givenName`: Worker first name
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Required
-  `familyName`: Worker last name
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `taxId`: Worker Tax ID
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `ssnId`: Worker Social Security Number ID
   -  Attribute type: **Property**. 
   -  Optional
-  `functionPerformed`: Indicates the actual worker's station * `CNC` - CNC Operator * `Nesting` - Nesting Operator * `Manual-Cut` - Manual Cut Operator * `Assembly` - Assembly Operator * `Manager` - Factory manager * `Designer` - Designer Department * `Budgeting` - Badgeting Department * `Warehouse` - Warehouse Department (consumables and wood's stock) * `Other` - Other Operation, like merchandise distributor. One of : `CNC`, `Nesting`, `Manual Cut`, `Assembly`, `Manager`, `Designer`, `Budgeting`, `Warehouse`, `Other`.
   -  Attribute type: **Property**. 
   -  Optional
-  `workerShif`: Defines the possibilities of working hours * `Morning` - Shift from 8am until 5pm * `Afternoon` - Shift from 5pm until 0am * `Night` - Shift from 0am until 8am. One of : `Morning`, `Afternoon`, `Night`.
   -  Attribute type: **Property**. 
   -  Optional
-  `hasOrganization`: Identification of the Organization where the Worker is currently employed.
   -  Attribute type: **Relationship**. 
   -  Optional
-  `assemblyFor`: Identification of the project what the assembly refers of
   -  Attribute type: **Relationship**. 
   -  Optional



# Consumable

Describes a consumable list associated with a project
-  `id`: Consumable Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Identifie the consumable Name
   -  Attribute type: **Property**. 
   -  Optional
-  `amount`: Identifier the consumable amount
   -  Attribute type: **Property**. 
   -  Optional
-  `status`: Indicates the status of the order * '1' - waits for separation order * '2' - In separating fase * '3' - waits for someone from factory-flor to take the separeted order * '4' - Already on flor-factory. One of : `1`, `2`, `3`, `4`.
   -  Attribute type: **Property**. 
   -  Optional
-  `belongsTo`: Identification of the projet Name that this consumables will attached to
   -  Attribute type: **Relationship**. 
   -  Required



# Part

Identifies the part-name atributes that belongs to a specific project - Lista de Corte -
-  `id`: Unic Identifier of a Part of a Project
   -  Attribute type: **Property**. 
   -  Required
-  `partName`: REF PEÇA (A)
   -  Attribute type: **Property**. 
   -  Required
-  `sort`: TIPO (B)
   -  Attribute type: **Property**. 
   -  Required
-  `material`: MATERIAL (C)
   -  Attribute type: **Property**. 
   -  Required
-  `amount`: QUANTIDADE (D)
   -  Attribute type: **Property**. 
   -  Required
-  `length`: COMPRIMENTO (E)
   -  Attribute type: **Property**. 
   -  Optional
-  `width`: LARGURA (F)
   -  Attribute type: **Property**. 
   -  Required
-  `thickness`: ESPESSURA (G)
   -  Attribute type: **Property**. 
   -  Required
-  `tag`: ETIQUETA (H)
   -  Attribute type: **Property**. 
   -  Required
-  `nestingFlag`: NESTING (I)
   -  Attribute type: **Property**. 
   -  Optional
-  `cncFlag`: CNC (J)
   -  Attribute type: **Property**. 
   -  Optional
-  `f2`: FURO FACE 2 (K)
   -  Attribute type: **Property**. 
   -  Optional
-  `f3`: FURO FACE 3 (L)
   -  Attribute type: **Property**. 
   -  Optional
-  `f4`: FURO FACE 4 (M)
   -  Attribute type: **Property**. 
   -  Optional
-  `f5`: FURO FACE 5 (N)
   -  Attribute type: **Property**. 
   -  Optional
-  `veio`: VEIO (O)
   -  Attribute type: **Property**. 
   -  Optional
-  `orla2`: ORLA2 (P)
   -  Attribute type: **Property**. 
   -  Optional
-  `orla3`: ORLA3 (Q)
   -  Attribute type: **Property**. 
   -  Optional
-  `orla4`: ORLA4 (R)
   -  Attribute type: **Property**. 
   -  Optional
-  `orla5`: ORLA5 (S)
   -  Attribute type: **Property**. 
   -  Optional
-  `observation`: Observation (T)
   -  Attribute type: **Property**. 
   -  Optional
-  `weight`: PESO (U)
   -  Attribute type: **Property**. 
   -  Optional
-  `opcnc`: OPCNC (V)
   -  Attribute type: **Property**. 
   -  Optional
-  `belongsTo`: Identifies the project to wich the part belongs
   -  Attribute type: **Relationship**. 
   -  Optional



# Action

Machine cnc1, nesting1, manual cut1
-  `id`: Machine Type
   -  Attribute type: **Property**. 
   -  Required
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `endTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `machineStatus`: Indicates in wich stage are the parts of corresponding machine type * `waiting` - indicates Information already arrived the machine but waits for start-button * `active` - The parts to be made in this station is already start * `finished` - The parts belong to the station refered to a project are completed. One of : `waiting`, `active`, `finished`.
   -  Attribute type: **Property**. 
   -  Optional
-  `machineType`: Indicates in wich stage are the parts of corresponding machine type * `cnc1` - indicates cnc1 station is working * `nesting1` - indicates nesting1 station is working * `manualcut1` - indicates manualcut1 station is working * `receiving material` - indicates that raw material is entering the factory * `organizing the material` - indicates that raw material is being put away at the factory * `assembly` - indicates that assembly station is on use * `shipping` - indicates the order is shipping. One of : `cnc1`, `nesting1`, `manualcut1`, `receiving material`, `organizing te material`, `assembly`, `shipping`.
   -  Attribute type: **Property**. 
   -  Optional
-  `executedBy`: Identification worker that made the part
   -  Attribute type: **Relationship**. 
   -  Optional
-  `executedIn`: Identification the made part
   -  Attribute type: **Relationship**. 
   -  Optional



# Assembly

Indicates when a assembly process is completed
-  `id`: Assembly parts from a project
   -  Attribute type: **Property**. 
   -  Required
-  `startTime`: Date and hour on wich the assembly starts
   -  Attribute type: **Property**. 
   -  Optional
-  `endTime`: Date and hour on wich the assembly ends
   -  Attribute type: **Property**. 
   -  Optional
-  `status`: Indicates the status of the project's assembly * `1` - em espera para iniciar * `2` - em testes * `3` - testado e embalado. One of : `1`, `2`, `3`.
   -  Attribute type: **Property**. 
   -  Required
-  `belongsTo`: Identification of the projet to which this assembly corresponds
   -  Attribute type: **Relationship**. 
   -  Required



# Budget

Clients Budget
-  `id`: Budget Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Budget name
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Optional
-  `amount`: Value in euros
   -  Attribute type: **Property**. 
   -  Optional
-  `approvedDate`: Saves date and time information when the budget was approved
   -  Attribute type: **Property**. 
   -  Required
-  `madeFor`: Identification the project that this budget belongs to
   -  Attribute type: **Relationship**. 
   -  Required



# expedition

Indicates when an order has been shiped
-  `id`: Refers to the date of dispatch of the order
   -  Attribute type: **Property**. 
   -  Required
-  `expeditionTime`: Date and hour when the order left the factory in direction to the Owner
   -  Attribute type: **Property**. 
   -  Optional
-  `deliveryFlag`: Indicates if the order arrived to the destination
   -  Attribute type: **Property**. 
   -  Optional
-  `belongsTo`: Identification if the order is arrived the destination
   -  Attribute type: **Relationship**. 
   -  Required



## Examples

### OK


