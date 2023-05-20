# CLOUD CONSULTING PROJECT 

## Content



> Team Members
>
> Goals
>
> Model Object and Relations
>
> Funcionality

## Team Members

- Arturo Petrich.
- Belen Banegas.
- Bernardo Mingoia.
- Johan Revilla.
- Julian Aquino.

## Abstract
This project is the final work presented to conclude a Salesforce bootcamp. Cloud Consulting is a consulting company that provides Salesforce services to other companies. Its employees serve as resources in roles such as developers, architects, consultants, or project managers.

The application aims to facilitate project management for Cloud Consulting, starting from the opportunity that arises in the sales department. Once the opportunity's status changes to closed/won, it automatically transforms into a project through a flow. After the project is created, the Project Manager has access to their own application, where they can view graphical reports and a list of the assigned projects. They can also access the details of each project, such as start and end dates, budget, project status, client, Squad Lead, profit-loss, and reports that provide information on cost-benefit, assigned resources, requested roles, hours logged, and pending hours (per role). The Project Manager performs resource allocation through their application, using an LWC component, where they can select users based on roles.

Within the assigned resources for the project, the Project Manager assigns a Squad Lead, who can assign tasks to the selected resources in the project, indicating estimated hours, start dates, and corresponding end dates.

The resources, who are also users, have their own application where they can see the projects they have been assigned to. Through an LWC component, they can manage the tasks assigned by their Project Manager, start tasks, and record the hours dedicated as they complete them.

## Resumen
Este proyecto es el trabajo final presentado para concluir un bootcamp de Salesforce. En el que Cloud Consulting es una empresa consultora que se dedica a brindar servicios de Salesforce a otras empresas. Sus empleados son recursos en roles de desarrolladores, arquitectos, consultores o Project Managers.

La aplicación tiene como objetivo facilitar la gestión de proyectos para Cloud Consulting, comenzando desde la oportunidad que surge en el área de ventas, la cual, una vez cambiado su estado a cerrada/ganada se transforma automáticamente en un proyecto mediante un flow. Una vez creado el proyecto, el Project Manager tiene acceso a su propia aplicación, desde donde puede ver reportes en graficos y una lista de los proyectos asignados. Además, puede acceder a los detalles de cada proyecto, como la fecha de inicio y finalización, el presupuesto, el estado del proyecto, el cliente, el Squad Lead, la ganancia-pérdida, y los informes que brindan información sobre el costo-beneficio, los recursos asignados, los roles solicitados, las horas cargadas y las horas pendientes (por rol). El Project Manager realiza la asignación de recursos desde su aplicación, utilizando un componente LWC, donde puede seleccionar usuarios por rol.

Dentro de los recursos asignados al proyecto, el Project Manager asigna un Squad Lead, quien puede asignar tareas a los recursos seleccionados en el proyecto, indicando las horas estimadas, fechas de inicio y finalización correspondientes.

Los usuarios que son recursos también tienen su propia aplicación, donde pueden ver los proyectos a los que han sido asignados. A través de un componente LWC, pueden gestionar las tareas asignadas por su Project Manager, iniciar las tareas y registrar las horas dedicadas a medida que las completan.


## Goals

Build an application with a system that allows Cloud Consulting to manage software projects and get out of the manual processes that they have today through excels, documents and repositories that are not integrated or automated.

## Model Object and Relations

Data model from Schema Builder: [click here](https://losrompebytes-dev-ed.develop.lightning.force.com/lightning/setup/SchemaBuilder/home)

Data model (Diagram): [click here](https://app.diagrams.net/#G15Cen1jPO0dfw5jFGSE4BUlqYc6EBiAWt)

## Funcionality
### Flow Create Project
![Create Project](https://github.com/Arturo750/Cloud_consulting/assets/115192739/dfc9f22f-f6a0-444f-8767-fb11a5f15127)

### App Project Management
#### Home
![Home- Project Management](https://github.com/Arturo750/Cloud_consulting/assets/115192739/817d7652-1e95-4de5-a8c6-d7f466b280fd)

#### Project
![Home- Project Management](https://github.com/Arturo750/Cloud_consulting/assets/115192739/d15d390d-834c-409d-97c2-a0491482c4df)

#### Resource Allocation (LWC)
![Resource allocation](https://github.com/Arturo750/Cloud_consulting/assets/115192739/a7fc3cb9-5a2e-4ba6-9754-f150723c2dba)

### Flow project start
![Flow Schedule Inicio del proyecto](https://github.com/Arturo750/Cloud_consulting/assets/115192739/3bbf09b8-f46d-4022-9638-5cdbe2f3c785)

On the project start date, the system automatically updates the project status to "In Progress."
This occurs only if the allocated resources cover the required number of hours. If this condition is not met, a notification email is sent to the Project Manager.
Validation is performed to ensure that the project has a Squad Lead assigned before transitioning to the "In Progress" state. Only one resource can be assigned as the Squad Lead, and an error message is displayed if no Squad Lead is assigned.
If the project is in a "Loss" situation (where the estimated cost exceeds the amount sold) prior to starting, it prevents the transition to the "In Progress" state and sends an email notification to the Project Manager regarding the issue.

### App Resource
![App Resource](https://github.com/Arturo750/Cloud_consulting/assets/115192739/ecc4e60b-a83a-49cc-bfbc-70abed206da1)

#### Assign hours (LWC)
![Assign hours](https://github.com/Arturo750/Cloud_consulting/assets/115192739/d0c3edc2-d356-406d-aca0-b23fb0a1a267)

### Flow Holiday and Days off request

![Tux, the Linux mascot](/img/flow_reques_holiday_and_day_off.jpeg)

**Flow Send Email When I'ts approved:** send a email for approval to the whole team members. 


