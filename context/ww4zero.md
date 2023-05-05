# Organization

Describes the organization entity
-  `id`: Unique identifier of the organization
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Organization`.
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
-  `id`: Unique identifier of the project
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Project`.
   -  Attribute type: **Property**. 
   -  Required
-  `hasBudget`: Relationship property: Identifies the budget related
   -  Attribute type: **Relationship**. 
   -  Required
-  `category`: Type of furniture
   -  Attribute type: **Property**. 
   -  Optional
-  `name`: Project name
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Required
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Required
-  `projectStatus`: Indicates the actual project status * drawing - Initial state of a project, in which CAD drawings are being developed... * production - While in the production phase on the factory floor... * testing - While in the assembly and testing phase... * transport - While in the transportation phase, which begins after the completion of assembly... * finished - When installed at the site.. One of : `drawing`, `production`, `testing`, `transport`, `finished`.
   -  Attribute type: **Property**. 
   -  Optional



# Owner

Identifies a client (owner of a project)
-  `id`: Unique identifier of the client
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Owner`.
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
-  `active`: Status of an acount
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Required
-  `telephone`: Mobile or telephone contact
   -  Attribute type: **Property**. [telephone](https://schema.org/telephone)
   -  Optional
-  `image`: Image URL
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
   -  Optional
-  `tos`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Optional



# Worker

Identifies a worker within an organization
-  `id`: Unique identifier of the worker
   -  Attribute type: **Property**. 
   -  Optional
-  `type`: NGSI Entity type. One of : `Worker`.
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
-  `active`: If the work is an active user or not
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `performanceRole`: Indicates the actual worker's station * `CNC` - CNC Operator * `Nesting` - Nesting Operator * `Manual-Cut` - Manual Cut Operator * `Assembly` - Assembly Operator * `Manager` - Factory manager * `Office` - Office Department * `Warehouse` - Warehouse Department (consumables and wood's stock) * `Other` - Other Operation, like merchandise distributor. One of : `CNC`, `Nesting`, `Manual Cut`, `Assembly`, `Manager`, `Office`, `Warehouse`, `Other`.
   -  Attribute type: **Property**. [PerformanceRole](https://schema.org/PerformanceRole)
   -  Optional
-  `image`: Image URL
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
   -  Optional
-  `hasOrganization`: Identification of the Organization where the Worker is currently employed.
   -  Attribute type: **Relationship**. [Organization](https://schema.org/Organization)
   -  Optional



# Consumable

Describes a consumable list associated with a project
-  `id`: Unique identifier of the consumable
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Consumable`.
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Identify the consumable name
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
-  `status`: Indicates the status of the order * '1' - waits for separation order * '2' - In separating fase * '3' - waits for someone from factory-flor to take the separeted order * '4' - Already on flor-factory. One of : ``, ``, ``, ``.
   -  Attribute type: **Property**. 
   -  Optional
-  `image`: Image URL
   -  Attribute type: **Property**. 
   -  Optional
-  `belongsTo`: Identification of the projet name that this consumables will attached to
   -  Attribute type: **Relationship**. 
   -  Required
-  `orderBy`: Identification of the owner name associated to the project with status in execution
   -  Attribute type: **Relationship**. 
   -  Optional



# Part

Identifies the part-name atributes that belongs to a specific project - Lista de Corte
-  `id`: Unique identifier of the part of a project.
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Part`.
   -  Attribute type: **Property**. 
   -  Required
-  `amount`: QUANTIDADE (D)
   -  Attribute type: **Property**. [amount](https://schema.org/amount)
   -  Required
-  `belongsTo`: Identifies the project to which the part belongs
   -  Attribute type: **Relationship**. 
   -  Required
-  `belongsToGroup`: Identifies the group to which the part belongs
   -  Attribute type: **Relationship**. 
   -  Optional
-  `belongsToFurniture`: Identifies the piece of furniture to which the part belongs.
   -  Attribute type: **Relationship**. 
   -  Optional
-  `belongsToModule`: Identifies which assembler module the part belongs to (optional)
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
-  `image`: URL of the part image
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
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
-  `width`: Width in mm
   -  Attribute type: **Property**. [width](https://schema.org/width)
   -  Optional
-  `length`: Length in mm
   -  Attribute type: **Property**. [size](https://schema.org/size)
   -  Optional



# Machine

Identifies the attributes of a machine in the organization
-  `id`: Unique identifier of the machine
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Machine`.
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Machine name
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Optional
-  `machineType`: Indicates in wich stage are the parts of corresponding machine type * `cnc1` - indicates cnc1 station is working * `nesting1` - indicates nesting1 station is working * `manualcut1` - indicates manualcut1 station is working * `receiving_material` - indicates that raw material is entering the factory * `organizing_material` - indicates that raw material is being put away at the factory * `assembly` - indicates that assembly station is on use * `shipping` - indicates the order is shipping. One of : `cnc1`, `nesting1`, `manualcut1`, `receiving_material`, `organizing_material`, `assembly`, `shipping`.
   -  Attribute type: **Property**. 
   -  Optional
-  `allocatedIn`: Identifier the organization the machine is allocated
   -  Attribute type: **Relationship**. 
   -  Required



# Assembly

Indicates when a assembly process is completed
-  `id`: Unique identifier for the assembly process of a project
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Assembly`.
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
   -  Required
-  `belongsTo`: Identification of the project to which this assembly corresponds
   -  Attribute type: **Relationship**. 
   -  Required



# Budget

Clients Budget
-  `id`: Unique identifier of a budget
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Budget`.
   -  Attribute type: **Property**. 
   -  Required
-  `number`: Budget number
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Optional
-  `name`: Budget name
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Optional
-  `price`: Price in euros
   -  Attribute type: **Property**. 
   -  Optional
-  `budgetStatus`: Budget possible states * must_be_analyzed -> initial budget value, which is pre-budget, where the necessary data for budget development is collected * waiting_budget - value before update * waiting_adjudication - value after budget was delivered to the customer for approval * adjudicated - value after budget adjudication * canceled - value after budget canceled. One of : `must_be_analyzed`, `waiting_budget`, `waiting_adjudication`, `adjudicated`, `canceled`.
   -  Attribute type: **Property**. 
   -  Optional
-  `observation`: Observation (T)
   -  Attribute type: **Property**. [Observation](https://schema.org/Observation)
   -  Optional
-  `approvedDate`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. [Date](https://schema.org/Date)
   -  Required
-  `requestDate`: Customer quote request date (1st contact) (DD/MM/YYYY hh:mm:ss )
   -  Attribute type: **Property**. [Date](https://schema.org/Date)
   -  Optional
-  `deliveryAgreementDate`: Agreed budget delivery date (DD/MM/YYYY hh:mm:ss )
   -  Attribute type: **Property**. [Date](https://schema.org/Date)
   -  Optional
-  `deliveryDate`: Actual quote delivery date (DD/MM/YYYY hh:mm:ss )
   -  Attribute type: **Property**. [Date](https://schema.org/Date)
   -  Optional
-  `lastUpdate`: Date of last amendment to the budget, until the budget is awarded (DD/MM/YYYY hh:mm:ss )
   -  Attribute type: **Property**. [Date](https://schema.org/Date)
   -  Optional
-  `orderBy`: Identification of the client for whom the budget was prepared
   -  Attribute type: **Relationship**. 
   -  Required
-  `approvedBy`: Identification of the worker who approved the budget
   -  Attribute type: **Relationship**. 
   -  Optional
-  `deliveryAddress`: The delivery address
   -  Attribute type: **Property**. 
   -  Optional



# Expedition

Indicates when an order has been shiped
-  `id`: Unique identifier of the shipping order
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Expedition`.
   -  Attribute type: **Property**. 
   -  Required
-  `expeditionTime`: Date and hour when the order left the factory in direction to the Owner
   -  Attribute type: **Property**. [Time](https://schema.org/Time)
   -  Required
-  `deliveryFlag`: Indicates if the order arrived to the destination
   -  Attribute type: **Property**. [Boolean](https://schema.org/Boolean)
   -  Optional
-  `belongsTo`: Identification of the project to which this expedition relates
   -  Attribute type: **Relationship**. 
   -  Required



# Module

Indicates a corresponding module of a project under assembly
-  `id`: Unique identifier of a module of a project under assembly.
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Module`.
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Module name (name-project_module-name)
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Optional
-  `belongsToFurniture`: Identification of the assembly to which this module belongs
   -  Attribute type: **Relationship**. 
   -  Required
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `finishTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional



# Furniture

Describes a piece of furniture from a project under assembly
-  `id`: Unique identifier of the piece of furniture
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Furniture`.
   -  Attribute type: **Property**. 
   -  Required
-  `lineNumber`: Line number
   -  Attribute type: **Property**. 
   -  Optional
-  `category`: Type of the piece of furniture
   -  Attribute type: **Property**. 
   -  Optional
-  `amount`: Quantity of elements
   -  Attribute type: **Property**. 
   -  Optional
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `finishTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `name`: Name of the piece of furniture
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Optional
-  `belongsToAssembly`: Identification of the assembly affected to the furniture.
   -  Attribute type: **Relationship**. 
   -  Optional
-  `hasBudget`: Identifies the budget related
   -  Attribute type: **Relationship**. 
   -  Required
-  `price`: Price in euros
   -  Attribute type: **Property**. 
   -  Optional
-  `furnitureType`: Type of line * furniture -> initial budget value, which is pre-budget, where the necessary data for budget development is collected * group * accessory - (Ex robinet, ...). One of : `furniture`, `group`, `accessory`.
   -  Attribute type: **Property**. 
   -  Required
-  `width`: Width in mm
   -  Attribute type: **Property**. [width](https://schema.org/width)
   -  Optional
-  `length`: Length in mm
   -  Attribute type: **Property**. [size](https://schema.org/size)
   -  Optional
-  `depth`: Depth in mm
   -  Attribute type: **Property**. [depth](https://schema.org/depth)
   -  Optional
-  `observation`: Observation (T)
   -  Attribute type: **Property**. [Observation](https://schema.org/Observation)
   -  Optional



# Group

Identifies a group associated with a module
-  `id`: Unique identifier of the group
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Group`.
   -  Attribute type: **Property**. 
   -  Required
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `finishTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional
-  `name`: Group name
   -  Attribute type: **Property**. [name](https://schema.org/name)
   -  Required
-  `belongsTo`: Identifies the module that is associated with this group
   -  Attribute type: **Relationship**. 
   -  Optional



# MachineTask

This entity creates a bridge table between the Machine and Part entities.
-  `id`: Unique identifier
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `MachineTask`.
   -  Attribute type: **Property**. 
   -  Required
-  `performedOn`: Identifies the part processed by the machine
   -  Attribute type: **Property**. 
   -  Required
-  `byMachine`: Identifies the machine that processed the part
   -  Attribute type: **Property**. 
   -  Required
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Required
-  `finishTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional



# WorkerTask

This entity creates a bridge table between the Worker and Part entities.
-  `id`: Unique identifier
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `WorkerTask`.
   -  Attribute type: **Property**. 
   -  Required
-  `executedBy`: Identifies the worker who processed the part
   -  Attribute type: **Relationship**. 
   -  Required
-  `executedIn`: Identifies the part processed by the worker
   -  Attribute type: **Relationship**. 
   -  Required
-  `machine`: Identifies the part processed by the worker
   -  Attribute type: **Relationship**. 
   -  Optional
-  `action`: Identifies the part processed by the worker
   -  Attribute type: **Property**. 
   -  Optional
-  `onProject`: Identifies the part processed by the worker
   -  Attribute type: **Relationship**. 
   -  Optional
-  `startTime`: Saves date and time information when the start button is pressed
   -  Attribute type: **Property**. 
   -  Required
-  `finishTime`: Saves date and time information when the finish button is pressed
   -  Attribute type: **Property**. 
   -  Optional



# LeftOver

Identifies the attributes of a leftover that belongs to an organization
-  `id`: Unique identifier of the leftover
   -  Attribute type: **Property**. 
   -  Required
-  `type`: NGSI Entity type. One of : `Leftover`.
   -  Attribute type: **Property**. 
   -  Required
-  `sort`: Type (B)
   -  Attribute type: **Property**. 
   -  Optional
-  `hasOrganization`: Relationship property: identifies the organization to which the leftover belongs
   -  Attribute type: **Relationship**. 
   -  Optional
-  `dimensions`: Dimensions of the leftover
   -  Attribute type: **Geoproperty**. 
   -  Optional
-  `image`: URL of the leftover image
   -  Attribute type: **Property**. [URL](https://schema.org/URL)
   -  Optional
-  `location`: Location of the leftover
   -  Attribute type: **Property**. [location](https://schema.org/location)
   -  Optional
-  `material`: MATERIAL (C)
   -  Attribute type: **Property**. [material](https://schema.org/material)
   -  Required
-  `thickness`: ESPESSURA (G)
   -  Attribute type: **Property**. [size](https://schema.org/size)
   -  Optional
-  `weight`: PESO (U)
   -  Attribute type: **Property**. [weight](https://schema.org/weight)
   -  Optional
-  `width`: Width in mm
   -  Attribute type: **Property**. [width](https://schema.org/width)
   -  Optional
-  `length`: Length in mm
   -  Attribute type: **Property**. [size](https://schema.org/size)
   -  Optional



## Examples

### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success



### Success


