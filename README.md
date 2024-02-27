# splunk

 :arrow_right:Splunk Indexer

 :arrow_right:Splunk Forwarder

Configuration Files and Paths in Splunk Forwarder:

- Inputs: /opt/splunkforwarder/etc/system/local/inputs.conf
  - Explanation: This file contains configurations for data inputs such as files, directories, and network ports that the forwarder monitors for data forwarding to the Splunk indexers.

- Outputs: /opt/splunkforwarder/etc/system/local/outputs.conf
  - Explanation: Here, you define where the forwarder sends data. Typically, this includes the IP address or hostname of the Splunk indexer along with the receiving port.

- Forwarder Deployment: /opt/splunkforwarder/etc/system/local/deploymentclient.conf
  - Explanation: This file is used to configure deployment client settings, such as the deployment server's address and authentication details, for forwarder management.

- Forwarder Deployment: /opt/splunkforwarder/etc/apps/
  - Explanation: This directory contains any apps deployed by the deployment server to the forwarder. Apps may include custom configurations, scripts, or add-ons.

- Forwarder Inputs/Outputs App: /opt/splunkforwarder/etc/apps/<app_name>/local/inputs.conf or /opt/splunkforwarder/etc/apps/<app_name>/local/outputs.conf
  - Explanation: If you have app-specific configurations for inputs or outputs, they can be defined in these files within the respective app's directory.

- Forwarder Monitoring: /opt/splunkforwarder/etc/system/local/inputs.conf (or specific app inputs)
  - Explanation: You can configure the forwarder to monitor its own performance metrics or system logs for monitoring purposes.

- Forwarder Logging: /opt/splunkforwarder/etc/system/local/inputs.conf (or specific app inputs)
  - Explanation: Configuration related to logging behavior can be defined here, including log file paths, log levels, and log file rotation settings.

- Authentication: /opt/splunkforwarder/etc/system/local/authentication.conf
  - Explanation: This file contains authentication-related settings, such as user authentication mechanisms and settings for LDAP or Active Directory integration.

- Forwarder Props and Transforms: /opt/splunkforwarder/etc/system/local/props.conf and /opt/splunkforwarder/etc/system/local/transforms.conf
  - Explanation: These files are used for custom data processing configurations, such as field extractions, event line-breaking, and data transformations before indexing.

- Forwarder Deployment Apps Logs: /opt/splunkforwarder/var/log/splunk/
  - Explanation: This directory contains logs specific to the forwarder's operation, including deployment client activity, startup/shutdown events, and data forwarding status.

-add splunk account and set a password

-install Splunk Forwarder and configure forwarder

-test forwarder

-Troubleshooting : forwarder configuration, port and services
