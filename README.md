# splunk
The Splunk Architecture comprises three main components:
- Splunk Forwarder
- Splunk Indexer
- Search Head

There are 2 types of Splunk Forwarders. These are:
- Splunk Universal Forwarder
- Splunk Heavy Forwarder

To Do

:arrow_right: Configure Indexer + Head

:arrow_right:Configure Forwarder

:arrow_right: Configure Log
  - Linux
    - Rsyslog | syslog-ng
    - Auditd
    - Ssh
    - SELinux
    - Application Log
 - Windows
   - Event Viewer

:arrow_right: SPL Search Processing Language

:arrow_right: Troubleshooting : forwarder configuration, port and services

 :arrow_right:Splunk Indexer

Configuration Files and Paths in Splunk Indexer

- Inputs: $SPLUNK_HOME/etc/system/local/inputs.conf
  - Explanation: This file contains configurations for data inputs such as receiving data from forwarders, scripted inputs, and network ports for data ingestion.

- Indexes: $SPLUNK_HOME/etc/system/local/indexes.conf
  - Explanation: Here, you define configurations for Splunk indexes, including storage paths, retention policies, and other index-specific settings.

- Outputs: $SPLUNK_HOME/etc/system/local/outputs.conf
  - Explanation: This file is used to configure where the indexer sends replicated or aggregated data, such as to other indexers or search heads.

- Authentication: $SPLUNK_HOME/etc/system/local/authentication.conf
  - Explanation: Contains settings for user authentication mechanisms, such as local authentication, LDAP, or Active Directory integration.

- Indexes (Clustered Environment): $SPLUNK_HOME/etc/master-apps/_cluster/local/indexes.conf
  - Explanation: In a clustered environment, index configurations are managed at the cluster master level. This file contains cluster-wide index configurations.

- Inputs/Outputs App: $SPLUNK_HOME/etc/apps/<app_name>/local/inputs.conf or $SPLUNK_HOME/etc/apps/<app_name>/local/outputs.conf
  - Explanation: If you have app-specific configurations for inputs or outputs, they can be defined in these files within the respective app's directory.

- License: $SPLUNK_HOME/etc/system/local/server.conf
  - Explanation: Contains settings related to licensing, including license master configuration and license slave settings.

- Search Head Pooling: $SPLUNK_HOME/etc/system/local/server.conf
  - Explanation: This file includes configurations related to search head pooling, which allows load balancing and high availability for search heads.

- Cluster: $SPLUNK_HOME/etc/system/local/server.conf
  - Explanation: Contains settings for indexer clustering, including cluster master and peer configurations.

- Props and Transforms: $SPLUNK_HOME/etc/system/local/props.conf and $SPLUNK_HOME/etc/system/local/transforms.conf
  - Explanation: These files are used for custom data processing configurations, such as field extractions, event line-breaking, and data transformations before indexing.

- Forwarder Management: $SPLUNK_HOME/etc/system/local/server.conf
  - Explanation: Configurations related to forwarder management, such as deployment server settings and forwarder monitoring.


 :arrow_right:Splunk Forwarder

Configuration Files and Paths in Splunk Forwarder

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

-test forwarder

