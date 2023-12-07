# NIM-System-REST-Skyward-OneRoster-v1.2
Skyward OneRoster v1.2

<p align="center"> 
  <img src="https://www.tools4ever.nl/connector-logos/skywardqmlativ-logo.png">
</p>

## Table of Contents
- [Setting up the API Access](#setting-up-the-api-access)
  - [General Notes](#general-notes)
  - [API User](#api-user)
  - [API User Access](#api-user-access)
  - [Integration Access Secrets](#integration-access-secrets)
- [Configure NIM](#configure-nim)
- [NIM docs](#nim-docs)


## Setting up the API Access
### General Notes
Each API Vendor should have an Integration record available in Qmlativ.

 ![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/64e32e13-72a4-466e-a453-cb0ac99aa9ad)

The APIs used by an Integration can also be viewed from the Integration List screen by looking at the lower browse.  The APIs may also be viewed from the Integration APIs tab on the Integration Details screen.

 ![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/e629fce7-210e-4eac-8cf8-7c1e84ec4d37)

If the vendor has indicated that they are using the Custom API, select it to see which Objects and Fields are being used, and what types of access they have to them.

 ![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/2a5f2eff-4c45-4ba1-a5c8-b6dfb29cc781)

An Integration Access record is required to grant Qmlativ API access, similar to the API User record.
If the vendor has requested to set up new Integration Access credentials and their Integration is not visible in the Integration List, please reach out to Skyward to ensure that the Integration Sync process is working properly.

### API User
A new Integration Access record should exist for each active API User record.
API User records may be found under the API area by selecting the User feature:

 ![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/13404ad4-8452-4efa-92a1-505245b443a8)

You may find/create Integration Access records by going to the API area and select the Integration Access feature:

 ![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/2441eb2e-3bb1-40f2-a823-f6a65cfffe88)

Integration Access records can also be found/created from the Integration Details screen.

 ![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/19180006-f55e-40c3-864d-16a5bdc821b4)

It is recommended to copy most of the API User’s settings into the Integration Access.

![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/5764c1ec-85ad-4138-b6b5-273af858544e)

![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/153329dc-a7d7-4f4f-87bc-b543391212ab)

The areas highlighted in red (1-4) can be taken from the API User record. The area highlighted in blue (5) can be taken from the API User Access records associated with the API User record. These values can also be changed to something new but keeping them the same reduces the possibility of errors during the initial conversion.

**NOTE**: _OAuth1 as an Authentication Type has been removed for the Integration Access system. Each vendor that used OAuth1 should migrate to OAuth2 for the new Integration Access system._

### API User Access

One of the main benefits of the Integration Access system is that each Integration is already pre-packaged with which APIs it uses, and therefore with which configuration records it is associated. When configuring an Integration Access, selecting the vendor’s Integration will automatically display the expected API Configuration sections.
Here is an example of the Integration Access screen when the selected Integration uses all APIs. As you can see, the Configuration section displays all configuration options for the APIs:

 ![image](https://github.com/Tools4ever-NIM/NIM-System-REST-Skyward-Qmlativ/assets/24281600/1318e043-58d0-48c3-89d5-4dab27c9ff71)

**NOTE:** _OneRoster, Time Tracking, Identification, Attendance, and Enrollment Configuration records can be shared between the API User Access and Integration Access records._

Custom API Entities is a new entity selector that controls which entities the vendor has access to.  For Integrations that use the Custom API, the modules, objects, and fields that are used by the Integration are now visible on the “Integration Objects” tab, so the old “Allow Security Module Write Operations” checkbox that was on the API User Access is now obsolete.

### Integration Access Secrets
Secrets work differently in the Integration Access system than they did in the API User system. In all situations, it is not possible for districts to generate their own complete set of API credentials. 

* For vendors who do not enable the district to create their own Secret, only a Key and Secret is required to authenticate themselves in the Qmlativ API. 
* For vendors who enable the district to create their own Secret, there is a hidden third value stored by the vendor that enables the Integration Access connection.

Secrets generated for Integration Access can only be viewed once; they cannot be retrieved after closing the confirmation dialog.


# Configure NIM
1.	Edit the System to configure the connection information

2.	Enter the necessary information for the system
    - Customer/tenant ID
        - This is the URL to the instance, typically in this format
            -<Customer>.skyward.com/<customer>API
    -	Client ID
        - Enter the Client Key from the Skyward integration Access Screen
    - Client Key
        -	Enter the Client Secret from the Skyward Integration Access Screen
    -	Integration Key
        - Please reach out to Tools4ever support (support@tools4ever.com) to obtain this key. This key is generated on a per customer basis for access to use the integration
          
# NIM Docs
The official NIM documentation can be found at: https://docs.nimsuite.com

