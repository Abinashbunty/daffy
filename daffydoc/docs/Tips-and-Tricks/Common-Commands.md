<script>
  document.title = "Common Commands";
</script>

This page lists some of the most commonly used Daffy commands for installation, troubleshooting, and cleanup.

## **Delete Environment**
Run the following command to delete all resources created by Daffy, including but not limited to the OpenShift cluster, Cloud Paks, services, VM systems, and tools.

```console
/data/daffy/cleanup.sh
```

## **Daffy Versioning**

### Upgrade/Refresh
Run the following command to upgrade Daffy to the newest release.

```console
/data/daffy/refresh.sh

```

### Downgrade Version
Run the following command to install older version of Daffy. This will output a list of previous releases to select and install.

```console
/data/daffy/refresh.sh --list
```

??? Screenshot "Example Output"
      <img src='../../images/tips/daffyUpgrade2.jpg'   align="top"  style = "float">

!!! Warning
    If you already downgraded to an older version and want to install another older version, you must first upgrade to the latest release and then downgrade to the other version you want.

### Get Version
Run the following command to view the current Daffy version.

```console
/data/daffy/version.sh
```

## **Daffy Tools**
Run the following command to install other tools you might need.

```console
/data/daffy/tools.sh
```

??? note "Tools Flags"
      ```console
      Daffy Tools
      --prepareHost                          This will run the prepareHost for daffy
      --mustGather                           This will run the mustGather for daffy
      --installOC                            This will install the oc command line tool
      --installAWS                           This will install the aws commandline tool
      --installAzure                         This will install the azure commandline tool
      --installGCloud                        This will install the gcloud commandline tool
      --installGOVC                          This will install the govc commandline tool(VMware)
      --installCloudCTL                      This will install the cloudctl for CP4D
      --installCP4DCloudCLI                  This will install the CP4D Cloud CLI utility
      ```

## **Gather Logs**
Run the following command to package all Daffy logs into a tar file. When troubleshooting, please send the gathered logs at `#!pypylog /tmp/daffy/daffy_mustgather.tar.gz` to the Daffy team.

```console
/data/daffy/tools.sh --mustGather
```

## **Security Cleanup**
Run the following command to clear all security (or individual) credentials.

```console
/data/daffy/security-cleanup.sh
```

??? note "Additional Cleanup Flags"
      ```console
      --all                            This will cleanup all security including RH Pull Secret, SSH key, and IBM Entitlement keys
      --aws                            This will cleanup the aws security information
      --azure                          This will cleanup the azure security information
      --gcp                            This will cleanup the gcp credential information
      --ibm                            This will cleanup the IBM Entitlement Key and ibmcloud sesssion info
      --vsphere                        This will cleanup vsphere information
      --pullSecret                     This will cleanup your RedHat Pull Secret
      --ssh                            This will cleanup your local ssh key
      --turbo                          This will cleanup your local ssh key
      --help|--?|?|-?|help|-help       This help menu
      ```
