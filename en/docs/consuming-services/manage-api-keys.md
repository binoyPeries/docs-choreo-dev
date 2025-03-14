# Manage API Keys

To access a published API secured with an API Key, you need to generate a dedicated API Key for that specific API. This key acts as a unique identifier, enabling authorized usage while maintaining security and control over how the API is consumed.  

Once created, API Keys can be managed through two locations within the Choreo Developer Portal:

- **Credentials section of the API**: This section provides an overview of all API Keys associated with the specific API, enabling API owners to monitor and manage access.
- **Credentials section of the Application**: This section allows application owners to view and manage all API Keys linked to their application, ensuring they have control over API subscriptions and access.

From these sections, you can perform various API Key management actions, such as regenerating and deleting.

## Creating an API key

To consume an API secured with an API Key, an API Key is required. To obtain an API Key, an application must first be created in the Choreo Developer Portal. This application represents a physical entity (such as a mobile app, web app, or device) and serves as the means to subscribe to APIs under a defined usage policy. The API Key is associated with a specific application, and an application can be created during the API Key generation process if needed.

### Steps to create an API key

1. Navigate to the [Choreo Developer Portal](https://devportal.choreo.dev) and sign in.
2. Click on **APIs** in the Developer Portal header.
3. Select the desired API that requires an API Key for access.
4. This will take you to the API overview page, where you can manage credentials.

#### Generating API keys.

Choreo allows you to generate API keys for production and sandbox environments.

!!! note
    Access to production endpoints may be restricted based on your user role. Ensure you have the required permissions before generating production keys.

Follow these steps to generate an API Key:

1. In the left navigation menu, select the desired environment under **Credentials**. The **API Keys** pane for the chosen environment will open.
2. If any API keys already exist, they will be listed here.
3. Click **Generate API Key** and configure the following options:
    - **Key Name**: Provide a suitable name for the API key.
    - **Application**: Select an existing application or create a new one.
    - **Subscription Policy**: Choose an appropriate subscription policy.
4. Click **Generate**. The newly created API Key will be displayed.


!!! note
    If the selected application is already subscribed to the chosen API, the subscription selection step will be skipped.
    If multiple environments have been enabled for the API, a specific environment needs to be selected during the API Key generation.


## API Key Regeneration

API Key regeneration allows you to obtain a new secret key for an existing API Key while ensuring minimal disruption to service. When an API Key is regenerated, a new secret key is generated, and the existing key remains valid for a grace period of one hour before being revoked. This ensures that applications have sufficient time to update their credentials without experiencing service interruptions.

!!! warning
    Ensure that all applications using the existing API Key are updated with the newly generated key within the grace period to prevent any disruptions in API invocations.

## API Key Deletion

API Keys can be deleted when they are no longer needed. Deleting an API Key immediately revokes its access, preventing further use of the key for API invocations. This action is irreversible and should be performed with caution, as any application relying on the deleted API Key will lose access to the API immediately.