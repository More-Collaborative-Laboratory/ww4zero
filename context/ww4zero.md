# Organization

Describes the organization entity
-  `id`: Organization Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `legalName`: Organization's legal name
   -  Attribute type: **Property**. [legalName](https://schema.org/legalName)
   -  Required
-  `vat`: Client/Institution Tax ID
   -  Attribute type: **Property**. [vatID](https://schema.org/vatID)
   -  Required
-  `email`: Contact email address
   -  Attribute type: **Property**. [email](https://schema.org/email)
   -  Required
-  `active`: if the work is an active user or not
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Required



# Project

Contains the information of a project
-  `assemblyBy`: Identification assembled parts belong to some project made for some worker
   -  Attribute type: **Relationship**. 
   -  Optional
-  `belongsTo`: Identification the budget that this project belongs to
   -  Attribute type: **Relationship**. 
   -  Required
-  `category`: Movel type
   -  Attribute type: **Property**. 
   -  Optional
-  `expedition`: Identification the addres that will recieve the oreder name
   -  Attribute type: **Relationship**. 
   -  Optional
-  `id`: Projects id Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `image`: url da imagem
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
   -  Optional
-  `name`: Project name
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Required
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Required
-  `producedBy`: Identification of the operators giveName that are working in specific project Name
   -  Attribute type: **Relationship**. 
   -  Optional
-  `status`: Indicates the actual workers station * `waiting` - Projects budget approved * `working` - Projects parts are already in the factorys floor * `finished` - Projects parts are all done * `assembly` - Projects parts are being assembled in the test zone * `expedition` - The request from a client is already out from the factory. One of : `Waiting`, `working`, `finished`, `assembly`, `expedition`.
   -  Attribute type: **Property**. 
   -  Optional



# Owner

Identifies a client (Owner of a project)
-  `id`: Client Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `legalName`: Institution legal name
   -  Attribute type: **Property**. [legalName](https://schema.org/legalName)
   -  Optional
-  `givenName`: Client first name
   -  Attribute type: **Property**. [givenName](https://schema.org/givenName)
   -  Optional
-  `familyName`: Client last name
   -  Attribute type: **Property**. [familyName](https://schema.org/familyName)
   -  Optional
-  `vat`: Client/Institution Tax ID
   -  Attribute type: **Property**. [vatID](https://schema.org/vatID)
   -  Required
-  `isCompany`: This property aims to indicate if the owner is a Institution or not
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Required
-  `address`: The client's address
   -  Attribute type: **Property**. [address](https://schema.org/address)
   -  Required
-  `addressDelivery`: The delivery address
   -  Attribute type: **Property**. [address](https://schema.org/address)
   -  Optional
-  `email`: Contact email address
   -  Attribute type: **Property**. [email](https://schema.org/email)
   -  Required
-  `active`: status of an acount (0-inactive) (2-active)
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Required
-  `telephone`: Mobile or telephone contact
   -  Attribute type: **Property**. [telephone](https://schema.org/telephone)
   -  Optional
-  `image`: url da imagem
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
   -  Optional
-  `tos`: date of acceptance of the system operation terms
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Required



# Worker

Identifies a worker within an organization
-  `id`: Worker Identifier
   -  Attribute type: **Property**. 
   -  Optional
-  `givenName`: Worker first name
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `familyName`: Worker last name
   -  Attribute type: **Property**. [Person](https://schema.org/Person)
   -  Optional
-  `email`: Contact email address
   -  Attribute type: **Property**. [email](https://schema.org/email)
   -  Optional
-  `active`: if the work is an active user or not
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `performanceRole`: Indicates the actual worker's station * `CNC` - CNC Operator * `Nesting` - Nesting Operator * `Manual-Cut` - Manual Cut Operator * `Assembly` - Assembly Operator * `Manager` - Factory manager * `Office` - Office Department * `Warehouse` - Warehouse Department (consumables and wood's stock) * `Other` - Other Operation, like merchandise distributor. One of : `CNC`, `Nesting`, `Manual Cut`, `Assembly`, `Manager`, `Office`, `Warehouse`, `Other`.
   -  Attribute type: **Property**. [PerformanceRole](https://schema.org/PerformanceRole)
   -  Optional
-  `image`: url da image
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
   -  Optional
-  `hasOrganization`: Identification of the Organization where the Worker is currently employed.
   -  Attribute type: **Relationship**. [Organization](https://schema.org/Organization)
   -  Optional



# Consumable

Describes a consumable list associated with a project
-  `id`: Consumable Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Identify the consumable Name
   -  Attribute type: **Property**. 
   -  Optional
-  `tag`: ETIQUETA (H)
   -  Attribute type: **Property**. 
   -  Optional
-  `material`: MATERIAL (C)
   -  Attribute type: **Property**. [material](https://schema.org/material)
   -  Optional
-  `amount`: Identifier the consumable amount
   -  Attribute type: **Property**. 
   -  Optional
-  `status`: Indicates the status of the order * '1' - waits for separation order * '2' - In separating fase * '3' - waits for someone from factory-flor to take the separeted order * '4' - Already on flor-factory. One of : `1`, `2`, `3`, `4`.
   -  Attribute type: **Property**. 
   -  Optional
-  `image`: url da imagem
   -  Attribute type: **Property**. 
   -  Optional
-  `belongsTo`: Identification of the projet Name that this consumables will attached to
   -  Attribute type: **Relationship**. 
   -  Required
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Optional



# Part

Identifies the part-name atributes that belongs to a specific project - Lista de Corte -
-  `amount`: QUANTIDADE (D)
   -  Attribute type: **Property**. [amount](https://schema.org/amount)
   -  Required
-  `belongsTo`: Identifies the project to which the part belongs
   -  Attribute type: **Relationship**. 
   -  Required
-  `belongsToModule`: Identifies the project to which the part belongs
   -  Attribute type: **Relationship**. 
   -  Optional
-  `cncFlag`: CNC (J)
   -  Attribute type: **Property**. 
   -  Optional
-  `dimensions`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon
   -  Attribute type: **Geoproperty**. 
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
-  `groove`: Veio (O)
   -  Attribute type: **Property**. 
   -  Optional
-  `id`: Unic Identifier of a Part of a Project
   -  Attribute type: **Property**. 
   -  Required
-  `image`: url da imagem
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
   -  Optional
-  `location`: PART LOCATION IN STOCK
   -  Attribute type: **Property**. [location](https://schema.org/location)
   -  Optional
-  `material`: MATERIAL (C)
   -  Attribute type: **Property**. [material](https://schema.org/material)
   -  Required
-  `nestingFlag`: NESTING (I)
   -  Attribute type: **Property**. 
   -  Optional
-  `observation`: Observation (T)
   -  Attribute type: **Property**. [Observation](https://schema.org/Observation)
   -  Optional
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Required
-  `orla2`: ORLA2 (P)
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `orla3`: ORLA3 (Q)
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `orla4`: ORLA4 (R)
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `orla5`: ORLA5 (S)
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `partName`: REF PEÇA (A)
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Required
-  `sort`: TIPO (B)
   -  Attribute type: **Property**. 
   -  Required
-  `tag`: ETIQUETA (H)
   -  Attribute type: **Property**. 
   -  Optional
-  `thickness`: ESPESSURA (G)
   -  Attribute type: **Property**. [size](https://schema.org/size)
   -  Optional
-  `tupia`: TUPIA
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `weight`: PESO (U)
   -  Attribute type: **Property**. [weight](https://schema.org/weight)
   -  Optional



# Machine

Machine cnc1, nesting1, manual cut1
-  `id`: Machine Type
   -  Attribute type: **Property**. 
   -  Required
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `finishTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `machineStatus`: Indicates in which stage are the parts of corresponding machine type * `waiting` - indicates Information already arrived the machine but waits for start-button * `active` - The parts to be made in this station is already start * `finished` - The parts belong to the station referred to a project are completed. One of : `waiting`, `active`, `finished`.
   -  Attribute type: **Property**. 
   -  Optional
-  `machineType`: Indicates in wich stage are the parts of corresponding machine type * `cnc1` - indicates cnc1 station is working * `nesting1` - indicates nesting1 station is working * `manualcut1` - indicates manualcut1 station is working * `receiving_material` - indicates that raw material is entering the factory * `organizing_material` - indicates that raw material is being put away at the factory * `assembly` - indicates that assembly station is on use * `shipping` - indicates the order is shipping. One of : `cnc1`, `nesting1`, `manualcut1`, `receiving_material`, `organizing_material`, `assembly`, `shipping`.
   -  Attribute type: **Property**. 
   -  Optional
-  `executedBy`: Identification worker that made the part
   -  Attribute type: **Relationship**. 
   -  Optional
-  `executedIn`: Identification the made part
   -  Attribute type: **Relationship**. 
   -  Optional
-  `belongsTo`: Identification of the project to which this assembly corresponds
   -  Attribute type: **Relationship**. 
   -  Optional



# Assembly

Indicates when a assembly process is completed
-  `id`: Assembly parts from a project
   -  Attribute type: **Property**. 
   -  Required
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `finishTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `statusAssembly`: Indicates the actual workers station * 0 - Waiting * 1 - Assembling * 2 - Testing * 3 - Packed. One of : ``, ``, ``, ``.
   -  Attribute type: **Property**. 
   -  Optional
-  `belongsTo`: Identification of the project to which this assembly corresponds
   -  Attribute type: **Relationship**. 
   -  Required
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Optional



# Budget

Clients Budget
-  `id`: Budget Identifier
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Budget name
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Optional
-  `category`: Movel type
   -  Attribute type: **Property**. 
   -  Optional
-  `amount`: Value in euros
   -  Attribute type: **Property**. 
   -  Optional
-  `approvedDate`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. [Date](https://schema.org/Date)
   -  Required
-  `image`: url da imagem
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
   -  Optional
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Optional



# Expedition

Indicates when an order has been shiped
-  `id`: Refers to the date of dispatch of the order
   -  Attribute type: **Property**. 
   -  Required
-  `expeditionTime`: Date and hour when the order left the factory in direction to the Owner
   -  Attribute type: **Property**. [Time](https://schema.org/Time)
   -  Required
-  `deliveryFlag`: Indicates if the order arrived to the destination
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Required



# Module

Indicates a corresponding module of a project under assembly
-  `belongsToAssembly`: Identification of the assembly to which this module belongs
   -  Attribute type: **Property**. 
   -  Required
-  `finishTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `id`: Module of a project under assembly
   -  Attribute type: **Property**. 
   -  Required
-  `name`: name-project_module-name
   -  Attribute type: **Property**. 
   -  Optional
-  `parts`: parts that make up the module
   -  Attribute type: **Property**. 
   -  Optional
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Optional



## Examples

### OK


