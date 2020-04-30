# velero_vSphere
Test yaml and configuration files I have used for my backup and restore test with the Velero vSphere Plugin. 

Storage Class yaml (cis-sc.yaml):
- Storage Class used for the test application on source cluster (backup cluster). Make sure to enter your own storage class name and datastoreurl into the file before applying it.

Ghost Persistent Volume Claim yaml (ghost-claim.yaml):
- Edit the file and change the storage class name if you have used a different name. 

Ghost Application yaml (ghost.yaml):
- The yaml file is configured for the default ghost repo and uses service type LoadBalancer to expose the application.

Credentials file for MinIO S3 object storage (credentials):
- The credentials file is used during the velero installation/configuration to specify credentials to the required S3 bucket. Make sure to enter your own ID and access keys. 

Export file for velero installation (exports):
- This file exports the envrionment variables REGION and BUCKET for the velero installation on source and target cluster.

CSI vSphere config file to create the necessary secret on the TKG cluster (csi-vsphere.conf)
- This file is used to create the required CSI vSphere secret "vsphere-congig-secret" on TKG clusters. Make sure to enter your own values.
