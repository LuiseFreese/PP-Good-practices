# Setup ALM

## Setup your Azure DevOps organization

* Open [dev.azure.com](https://dev.azure.com)
* Create a new organization
* Create a new project
* Create a repository to hold your code
* Optional, but a good idea: clone this repo so you can work locally
* Optional, but also a good idea: invite co-worker to the project
* Open **Project Settings** (lower left corner) --> **Repositories** --> **Security** and select **Contribute** permissions for **Project Collection Service Accounts** and <ProjectName> Build Service <OrgName>

## Create an app registration

* Open [portal.azure.com](https://portal.azure.com)
* Select **Azure Active Directory**
* Select **App registrations** --> **New app registration**
* Give it a name, select **Register**
* Select **Certificates and secrets**, create a secret, take note of it.
* Also copy the values of the **app id** and **tenant id** - we need them later.

## Create environments

AS a first step, we need to ensure that we have all environments in place:

* Open [aka.ms/ppac](https://aka.ms/ppac)
* Create environments for DEV, BUILD, TEST, PROD - make sure all of them have a Dataverse database

## Create an Application user

Now we need to make sure that we create an Application user in all of our 4 environments.

* Open [aka.ms/ppac](https://aka.ms/ppac)
* Select your environment
* Select **Settings**
* Select **Application users** under **Users & permissions**
* Select **new app users**
* Select **add an app**
* Select the default business unit
* Select the pen icon next to **Security roles** and add the **System Administrator** role
* Select **Save**
  

