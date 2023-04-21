# Application Lifecycle Management for Power Platform

Almost non-technical description for how we Power Platform with healthy ALM process

## Why would we care?

Power Platform solutions are being developed and used in so-called environments.

There are several issues with

* A one-environment strategy
* Not logging all code to source control and
* Not automating the build process for solutions in environments:

It leads to solutions being subjects to change for end-users all the time - so that they can't rely on a feature to be tested and working as planned.

It also means that developers can't revert/undo changes and leads to lots of manual and chaotic ad-hoc work, which puts unneccesary stress on admins and developers:

* We operate at open heart when developing solutions while users keep using them
* We can't roll back to previous versions
* Code only exists as opaque zip files in an environment

To mitigate risks that come along with these issues, its a good idea to

* Log all code into source control
* Move solutions across separated environments
* Have an automated process for that

## How do we care?

### Basics

* All Power Platform components are packaged and distributed across environments using solutions
* There are 2 types of solutions
  * Unmanaged:
    * Collection of references to components
    * No restrictions on what can be added, removed, or modified
    * recommended only during development of the soluition
  * Managed:
    * Components can't be added or removed or modified
    * Cannot be exported
    * Recommended when a solution is not actively being customized
* Source control should be your source of truth for storing and collaborating on your components

### Azure DevOps Build Tools for Power Platform

* Azure DevOps Pipelines automatically builds code projects and ship it to any target
* Support both GitHub and Azure repos
* Azure DevOps Build Tools for Power Platform are a collection of build and release tasks related to Power Platform

![Build Pipelines](images/alm_pp.png)

### Overview of environments

* **DEV** - only for development purposes, only developers and maintainers have access to it
* **BUILD** - only used to store the exported unmanaged solution and export it as managed solution (this separates the solution from the solution that is currently and ongoing developed in **DEV**)
* **TEST** - only for User Acceptance Testing - A subset of enduser can test functionality of this release.
* **PROD** - production use of apps in the organization

### Process of building and releasing versions

Every new feature, all bug fixes are implemented in **DEV**. Once the release passed the technical tests in **DEV**, it is build in **BUILD** and then finally released to **TEST**, where endusers can try out and test the release. If they approve it, the release gets published to **PROD**. If they don't approve it, development starts again in **DEV** and bug fixes/features get implemented in the next sprint.

### Setup instructions

(pretty technical) - can be found here: [setup ALM](setup-ALM.md)
