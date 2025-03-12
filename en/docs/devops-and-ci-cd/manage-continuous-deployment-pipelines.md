# Manage Continuous Deployment Pipelines

By default, all the organizations in Choreo are provisioned with a default continuous deployment pipeline(i.e., Default).

Environments within an organization are applied to projects in the order specified by the continuous deployment pipeline. By default, the organization's default continuous deployment pipeline is applied to all the projects. You can create additional pipelines and customize the sequence in which environments are applied in projects.

## Create a new continuous deployment pipeline

### Prerequisites

- To create a new continuous deployment pipeline in an organization, you must have the `ENVIRONMENT-MANAGEMENT` permission. By default, `ENVIRONMENT-MANAGEMENT` permission is granted to Admin and Choreo DevOps roles.

To create a new pipeline, follow the steps given below:

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to the organization where you want to create a new pipeline. 
2. In the left navigation menu, click **DevOps** and then click **CD Pipelines** (note that this is the **CD Pipelines** page under your organization, not your projects).
3. On the **CD Pipelines** page, click **Create Pipeline** and specify the following details required to create a new pipeline:
   
    - **Name**: A display name for the new pipeline.
    - **Mark as Default**: Select if you want to assign this new pipeline as the default pipeline for all new projects.
4. Click **Add Environment** and add required environments for the pipeline according to the preferred environment sequence.
5. Click **Create**.

## Edit a continuous deployment pipeline

### Prerequisites

- To edit a continuous deployment pipeline in an organization, you must have the `ENVIRONMENT-MANAGEMENT` permission. By default, `ENVIRONMENT-MANAGEMENT` permission is granted to Admin and Choreo DevOps roles.

To edit a pipeline, follow the steps given below:

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to the organization where you want to edit a pipeline.
2. In the left navigation menu, click **DevOps** and then click **CD Pipelines**.
3. Click the edit icon corresponding to the pipeline you want to edit.
4. Update the pipeline name, mark the pipeline as default, and change the sequence of environments.
5. Click **Update**.


## Delete a continuous deployment pipeline

To delete a pipeline, follow the steps given below:

!!! warning
    Continuous deployment pipeline deletion is a permanent, non-reversible operation.

!!! info "Note"
        The **default** continuous deployment pipeline of the organization cannot be deleted.

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to your organization.
2. In the left navigation menu, click **DevOps** and then click **CD Pipelines**. 
3. Click the delete icon corresponding to the pipeline you want to delete. This displays a confirmation dialog with details on the impact of deletion.

    !!! info "Note"
        If the pipeline is used by one or more projects, you will not be able to delete the pipeline. To delete such pipeline, first you need to remove the pipeline from each project using it.

4. Review the details, then type the pipeline name to confirm the deletion.
5. Click **Delete**.


## Add a continuous deployment pipeline to a project

### Prerequisites

- To add a continuous deployment pipeline to a project, you must have the `ENVIRONMENT-MANAGEMENT` or `PROJECT-MANAGEMENT` permission. By default, `ENVIRONMENT-MANAGEMENT` permission is granted to Admin and Choreo DevOps roles and `PROJECT-MANAGEMENT` permission is granted to Admin, Choreo DevOps, and Project Admin roles.

To add a pipeline to a project, follow the steps given below:

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to the organization where the project is created.
2. Click the project you want to add the pipeline.
3. In the left navigation menu, click **DevOps** and then click **CD Pipelines**.
4. Click **Add** and select the pipelines you want to add to the project.
5. Click **Add**.


## Remove a continuous deployment pipeline from a project

### Prerequisites

- To remove a continuous deployment pipeline from a project, you must have the `ENVIRONMENT-MANAGEMENT` or `PROJECT-MANAGEMENT` permission. By default, `ENVIRONMENT-MANAGEMENT` permission is granted to Admin and Choreo DevOps roles and `PROJECT-MANAGEMENT` permission is granted to Admin, Choreo DevOps, and Project Admin roles.

To remove a pipeline from a project, follow the steps given below:

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to the organization where the project is created.
2. Click the project you want to remove the pipeline.
3. In the left navigation menu, click **DevOps** and then click **CD Pipelines**.
4. Click **Remove** corresponding to the pipeline you want to remove from the project. This displays a confirmation dialog with details on the impact of deletion.
5. Review the details, then type the pipeline name to confirm the deletion.
6. Click **Remove**.

## Change default continuous deployment pipeline of a project

### Prerequisites

- To change the default continuous deployment pipeline of a project, you must have the `ENVIRONMENT-MANAGEMENT` or `PROJECT-MANAGEMENT` permission. By default, `ENVIRONMENT-MANAGEMENT` permission is granted to Admin and Choreo DevOps roles and `PROJECT-MANAGEMENT` permission is granted to Admin, Choreo DevOps, and Project Admin roles.

To change the default pipeline of a project, follow the steps given below:

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to the organization where the project is created.
2. Click the project you want to change the default pipeline.
3. In the left navigation menu, click **DevOps** and then click **CD Pipelines**.
4. Click **Set as Default** corresponding to the pipeline you want to set as the default pipeline for the project.
