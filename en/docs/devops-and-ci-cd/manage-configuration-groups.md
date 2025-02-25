
# Manage Configuration Groups

**Configuration groups** are collections of key-value pairs that can be linked to any component within the organization, enabling centralized configuration management.

Configuration values can be maintained for a set of environments. During deployment, a configuration group can be linked to inject its keys as environment variables or file mounts. Choreo manages the secrets and configurations, ensuring they are applied correctly during deployment and promotion.

!!!important
    All the values provided for configuration groups are encrypted and stored in the environment specific key vaults.

## Create a new configuration group

#### Prerequisites

- To create and manage configuration groups, you must have the `CONFIGURATION-GROUP-MANAGEMENT` permission. By default, `CONFIGURATION-GROUP-MANAGEMENT` permission is granted to Admin and Choreo DevOps roles.


To create a new configuration group, follow the steps given below:

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to the organization where you want to create a new configuration group. 
2. In the left navigation menu, click **DevOps** and then click **Configuration Groups**.
3. On the **Configuration Groups** page, click **Create** and specify the following details to create a new configuration group:
   
    - **Name**: A name for the configuration group (Unique within the organization).
    - **Description**: A description for the configuration group (Optional).
    - **Define Keys**: Define the keys for the configuration group.

        !!!note
            Configuration keys are used to uniquely identify the values of the configuration group. You can map the keys defined here to environment variables or file names at deployment time as required. Keys are unique within a configuration group.

    - **Assign Values**: Define values by environment for the keys defined.
  
        !!!note
            By default, critical and non-critical environments are grouped together allowing you to manage configuration smoothly. You can remove and manage configuration values for environments separately based on your requirements.

    - **Create**: Click **Create** to create the configuration group. Now you can link this configuration group to any component within the organization.

## Link and use configuration groups

The configuration groups created at organization level can be linked to any component within the organization. A configuration group can be linked as **Environment Variables** or **File Mounts** at deployment time.

Linking a configuration group will inject the values defined in the configuration group using the keys defined as the environment variable name or the file name at deployment time. You can use a custom environment variable name or file name instead of the default by mapping to the configuration group key.

To link a configuration group to a component, follow the steps given below:

1. Navigate to the component you want to link the configuration group to.
2. On the **Deploy** page, click **Configure & Deploy**, this will open the configuration and deployment wizard.
3. Link configuration groups as **Environment Variables** or **File Mounts** as required.

    === "Environment Variables"

        - Select the configuration group you want to link to the component.
        - Click **Link** to link the configuration group to the component.

    === "File Mounts"

        - Select the configuration group you want to link to the component.
        - Specify the **Mount Path** to mount the configuration files.
            
            !!!note
                All the configuration within the configuration group will be mounted to the specified path / directory as files.

        - Click **Link** to link the configuration group to the component.

4. Complete the deployment wizard by providing the required details and click **Deploy** to deploy the component with the updated configurations.

## View & edit a configuration group

To view & edit a configuration group, follow the steps given below:

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to your organization.
2. In the left navigation menu, click **DevOps** and then click **Configuration Groups**. 
3. In the **Configuration Groups** list, click on the corresponding record to view the configuration group.

    !!!note
        - Only non-sensitive configuration values are displayed in the view mode.
        - Updating the configuration group will not impact the current deployment but the changes will be reflected when the component is redeployed.

### Edit the configuration group

Configuration keys defined in the configuration group can be altered and the changes will impact the components using the particular configuration group when redeployed.

To edit the configuration group, click **Edit the Configuration Group** and update the required details.

- Configuration keys can be added, removed.
- Configuration group name and description can be updated.

### Edit the configuration values

Configuration values can be edited in each set of environments separately and the component using the configuration group needs to be redeployed for the changes to reflect.

To edit the configuration values, click the edit icon in the corresponding set of environments and update the required details.

- Configuration values can be updated.
- Configuration environment can be added or removed from an existing set of environments.

!!! warning
    - **Adding a new environment:** All the non-sensitive configuration values will be copied to the new environment but the sensitive values will not be copied. Hence the sensitive values will be cleared from all the environments in the particular set. **A new value needs to be provided for the sensitive values**.
    - **Removing an environment:** All the configuration values for the environment will be deleted.

## Delete a configuration group

To delete a configuration group, follow the steps given below:

!!! warning
    Configuration group deletion is a permanent, non-reversible operation. Ensure that the configuration group is not linked to any component before deleting it.

1. Sign in to the [Choreo Console](https://console.choreo.dev/) and switch to your organization.
2. In the left navigation menu, click **DevOps** and then click **Configuration Groups**. 
3. In the **Configuration Groups** list, click the delete icon corresponding to the configuration group you want to delete. This displays a confirmation dialog with details on the impact of deletion.
4. Review the details, then type the configuration group name to confirm the deletion.
5. Click **Delete**.
