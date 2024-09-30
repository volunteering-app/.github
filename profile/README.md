# Volunteering management system/database

## Design document

### Context and shape
**Volunteering app** - is a Windows applicaiton for managing projects for helping people, environment and etc. In one word, application for voluntiring management. It is not a web service where users can crate and manage their own projects. It is a software, for organisations, where they can manage their projects.

### Goals and Non-goals
#### Goals
* Managing projects and tasks
* Managing employers, activity overwiev, reward
* Managing Enents

#### Non-goals
* Multiplatform
* Employer functionality not needed, because it is an organisation database software.

#### Possible features
* Generating report

### Subsystems
**Client** - windows desktop application, written on .NET WPF framework using C# language.

**Backend** - server written on TypeScript using Nest.js framework.

**Database** - postgresql database where will be stored all data across the system. Main models:
  * **Project** - general database entity. Project can have different events, and volunteers.
  * **Event** - like a project task. Events where volunteers do something.
  * **Volunteer** - just a volunteer on a project or event.

### Bussiness logic
**Project**:

* Create project
* Updated project info
* Close project
* Add volunteer to the project
* Delete volunteer from the project
* Add event

**Event**:

* Create event
* Update event info
* Close/Delete event
* Rate volunteers and event after closing for generating future reports
* Add volunteer to the event
* Delete volunteer from the project

**Volunteers**:

* Create volunteer
* Update volunteer info
* Fire volunteer
* Assign to the event
* Assign to the project
* Calculate average volunteer rating based on the events

## Authors

- [@REFLAXua](https://github.com/REFLAXua)
- [@stbestichhh](https://www.github.com/stbestichhh)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE)
