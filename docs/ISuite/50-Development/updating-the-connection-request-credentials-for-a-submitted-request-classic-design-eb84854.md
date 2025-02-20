<!-- loioeb84854e31d943b490af77cfb218ddbb -->

# Updating the Connection Request Credentials for a Submitted Request \[Classic Design\]

Update the credentials you've used to establish a connection between the API portal and the API business hub enterprise.



<a name="loioeb84854e31d943b490af77cfb218ddbb__prereq_unb_5nc_tpb"/>

## Prerequisites

-   Only the users who submitted the connection request and has the *AuthGroup.APIPortalRegistration* role assigned to themselves can edit the credentials.

-   To update the API portal access credentials, you must first generate it. To generate the credentials from the API Portal, you must have the *APIPortal. Administrator* role assigned to you.

    1.  Log in to the Integration Suite.

    2.  Choose the navigation icon on the left and choose *Settings* \> *APIs*.

    3.  Choose the *Connection* tab.

    4.  Choose *Generate Credentials* under *Connect the API Portal to the centralized API Business Hub Enterprise* and *Copy* the API portal access credentials.


    > ### Note:  
    > The client credentials get generated for the *APIPortal .Service.CatalogIntegration* role.


You must also have the *AuthGroup.APIPortalRegistration* role assigned to you.



## Context

To establish the connection between the API portal and the API business hub enterprise, the API Portal client Id and the client secret is shared during the connection request process.

If you encounter one of the following situations when your connection request is in the submitted state, you have to update the credentials:

-   You have submitted incorrect credentials while raising a connection request, and your request is in pending approval or submitted state.

-   You've deleted the service instance, or the service key, after the connection request was submitted. In this case, the credentials you used before deleting the service instance or the service key becomes invalid.


> ### Note:  
> This document describes the classic design of the API business hub enterprise. To view the documentation for the new design, see [Updating the Connection Request Credentials for a Pending Request \[New Design\]](updating-the-connection-request-credentials-for-a-pending-request-new-design-dd37a7b.md).



## Procedure

1.  Log on to the *API Business Hub Enterprise*.

2.  Navigate to the *Manage* tab and choose *Establish API Portal Connectivity with API Business Hub Enterprise* tile.

3.  Go to the *Actions* column of the connection request that you want to edit and choose *Edit Credentials*.

4.  On the *Edit Credentials for <API Portal Alias Name \>* popup, enter the mandatory *API Portal Access Credentials* that you copied earlier from the API portal.

    Sample credentials:

    ```
    {
      "url": "https://<application name>.cfapps.sap.hana.ondemand.com",
      "tokenurl": "https://<name>.authentication.sap.hana.ondemand.com/oauth/token",
      "certurl": "https://xxxxxx.authentication.cert.sap.hana.ondemand.com",
      "certificate": "xxxxxxxxxxxxxxxxxxx",
      "key": "xxxxxxxxxxxxxx"
    }
    ```

    > ### Note:  
    > These credentials will remain valid for a period of 65 days. Please make sure to regenerate them and reestablish the connection within this timeframe.

5.  Choose *Save*.




<a name="loioeb84854e31d943b490af77cfb218ddbb__result_yk3_ng1_x4b"/>

## Results

You’ve updated the API Portal access credentials successfully.

