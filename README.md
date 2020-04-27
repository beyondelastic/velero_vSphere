# velero_vSphere
Test yaml files for backup and restore with the Velero vSphere Plugin. 

Storage Class yaml (cis-sc.yaml):
- Make sure to enter your own storage class name and fatastoreurl into the file before applying it. 

Ghost Persistent Volume Claim yaml (ghost-claim.yaml):
- Edit the file and change the storage class name if you have used a different name. 

Ghost Application yaml (ghost.yaml):
- The yaml file is configured for the default ghost repo and uses service type LoadBalancer to expose the application.
