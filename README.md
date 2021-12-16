# azure-devops-splunk-detector-gate
Add Azure DevOps Release Gates based on the status of detectors in Splunk Observability Cloud.

## Setup your Service Connection
After installing the Splunk Alert Gates extension you will need to setup 
your Splunk API Service Endpoint 
1. Click Project Settings from the bottom left side of your screen in the main Azure DevOps Project area
2. Click Service Connections from the Pipelines area of Project Settings
3. Click New Service Connection in the top right
4. Choose the `Splunk Observability Alerts API` as your new service connection
5. Enter your Splunk Observability API URL *including trailing `/`* (E.G. `https://api.us1.signalfx.com/v2/`)
6. Enter your Splunk Observability Cloud User API token which you obtained from Splunk Observability Cloud > Account Settings. ![Example](./images/api-token.png)

## Setup your Release Pipeline to check a Detector
1. Edit your Release Pipeline by clicking Releases under the Pipeline heading in the left sidebar
2. Select your Release Pipeline and click the Edit button in the upper right
3. Click either Pre-Deployment or Post-Deployment conditions 
    ![deployment-conditions](./images/deployment-conditions.png)
4. Enable Gates and click Add to add your Splunk Detector Gate configuration
    - Add a Display name for your gate and choose the Splunk Observability Alerts API Service Connection you created earlier
    - Include the Detector Id of the detector you'd like to use as your gate.
    ![release-gate-settings](./images/release-gate-settings.png)
    

## License

Copyright 2021 Splunk Inc.
 
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
 
http://www.apache.org/licenses/LICENSE-2.0
 
Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.    