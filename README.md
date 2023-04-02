# ww4.0 Project Data Model

openapi: 3.0.0

This project is developed under the ww4.0 initiative and aims to provide a data model for the MOFREITA component. The data model is defined using the OpenAPI 3.0.0 specification and includes various schemas for different entities, such as organizations, projects, owners, workers, consumables, parts, machines, assemblies, budgets, expeditions, modules, mobile devices, groups, machine tasks, and worker tasks.

## General Data Model Information

The `info` section of the OpenAPI specification provides the following information about the data model:

- `title`: ww4zero Project
- `description`: Data model for the MOFREITA component developed under the ww4.0 project
- `version`: 2.0.0
- `contact`: information about the Digitalization of Mofreita, including the name and a URL to the project's GitHub repository.
 ---

components:


- [`Organization`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/organization.yaml#/organization): defines the schema for an organization.
- [`Project`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/project.yaml#/project): defines the schema for a project.
- [`Owner`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/owner.yaml#/owner): defines the schema for an owner.
- [`Worker`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/worker.yaml#/worker): defines the schema for a worker.
- [`Consumable`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/consumable.yaml#/consumable): defines the schema for a consumable.
- [`Part`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/part.yaml#/part): defines the schema for a part.
- [`Machine`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/machine.yaml#/machine): defines the schema for a machine.
- [`Assembly`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/assembly.yaml#/assembly): defines the schema for an assembly.
- [`Budget`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/budget.yaml#/budget): defines the schema for a budget.
- [`Expedition`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/expedition.yaml#/expedition): defines the schema for an expedition.
- [`Module`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/module.yaml#/module): defines the schema for a module.
- [`Mobile`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/mobile.yaml#/mobile): defines the schema for a mobile device.
- [`Group`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/group.yaml#/group): defines the schema for a group.
- [`MachineTask`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/machineTask.yaml#/machineTask): defines the schema for a machine task.
- [`WorkerTask`](https://raw.githubusercontent.com/More-Collaborative-Laboratory/ww4zero/main/workerTask.yaml#/workerTask): defines the schema for a worker task.

---

## Representation

![alt text](./Documents/WoodWork4.0_v2.drawio.svg)