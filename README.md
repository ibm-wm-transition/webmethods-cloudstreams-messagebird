# webMethods CloudStreams Provider for Messagebird
This project provides a sample webMethods CloudStreams Provider Project for Messagebird. The following APIs are available:

## Requirements

The project was developed and tested on the following installation:
1. Integration Server 9.12
2. CloudStreams Server 9.12
3. Software AG Designer 9.12 with Service Development and CloudStreams Development

## Quick start

To install the project on your local development environment follow these steps.

### Prepare CloudStreams connection

1. In Software AG Designer open ```Window > Preferences```.
2. Navigate to ```Software AG > CloudStreams Servers```.
3. Add your local Integration Server. If there is already an entry make sure username and password are correct by clicking the Test button.

### Import CloudStreams Provider Project

1. In Software AG Designer switch to the ```CloudStreams Development``` perspective.
2. Select File > Import and choose ```Software AG > CloudStreams Provider Project```. Click Next.
3. Select the root of this repository as the Root Directory.
4. Select the ```Messagebird``` project.
5. Check ```Copy project into workspace```.
6. Click Finish.
7. Expand the newly imported project.
8. Right-click ```com.softwareag.messagebird``` and select Deploy.

### Import Integration Server packages
The CloudStreams Provider Project does not contain neccessary doctypes.

1. Copy Messagebird.zip and MessagebirdTests.zip to ```<install_dir>/IntegrationServer/instances/<instance>/replicate/inbound```.
2. Open Integration Server Administration in your browser.
3. Install both packages with ```Install Inbound Releases``` in Package Management.

### Add Messagebird Accesskey and activate connection

To access Messagebird an Accesskey is neccessary. Generate your Messagebird Trial account here: https://www.messagebird.com.

1. Open Integration Server Administration in your browser.
2. Navigate to ```Solutions > CloudStreams > Providers > Messagebird```.
3. Select ```com.softwareag.messagebird``` from the Connector List.

You will find one (disabled) connection: wmmessagebirdTests:connection. You need to modify this connections:
1. Click the Edit button of the connection.
2. Enter your Accesskey and save the changes. Note: The Accesskey field needs the following content: "AccessKey [live|test]_[apikey]"
3. Enable the connection.

### Run tests

1. In Software AG Designer switch to the ```Service Development``` perspective.
2. Expand the ```MessagebirdTests``` package.
3. Run the ```*Test``` flow services you find in the subsequent directories.
______________________
These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.
_____________
Contact us at [TECHcommunity](mailto:technologycommunity@softwareag.com?subject=Github/SoftwareAG) if you have any questions.
