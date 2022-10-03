## Installation

### Environment

- The command line utility needs **Java version 11** to function
  - An embedded JavaRuntimeEnvironment 11 is included along with the delivery zip / tar files. Once the archive extracted, "/java" directory contains the JRE binaries.

### Windows Instructions
Download AzureStorage_Windows.zip file from the desired [release available here](https://github.com/SMATechnologies/azure-storage-java/releases).

After download, extract the zip file to the location you'd like to install the connector to. Once unzipped, everything needed should be located under the root folder of that directory.

After extract, copy the Enterprise Manager Job-Subtype from the /emplugins directory to dropins directory of each Enterprise Manager that will create job
definitions (if the directory does not exist, create it).

Restart Enterprise Manager and a new Windows Job Sub-Type Azure Storage should be visible (if not restart Enterprise Manager using 'Run as Administrator'). 

Create a global property **AzureStoragePath** that contains the full path of the installation directory.

Create an encrypted global property that contains the storage account key, which will used by the job subtype.
 
## Configuration
The Azure Storage connector uses a configuration file **Connector.config** that contains the connector information.

**Connector.config** file example:
```
[CONNECTOR]
NAME=Azure Storage Connector
DEBUG=OFF

```
