## v2022-09-29
          Tested OpenShift with Current Daffy Release
              GCP       4.8.49 / 4.10.32
              AWS       4.8.49 / 4.10.32
              Azure     4.8.49 / 4.10.32
              ROKS      4.8.49 / 4.10.32
              VSphere   4.8.49 / 4.10.32
              KVM       4.8.49 / 4.10.32
              IBM IPI   4.10.32
          Cloud Pak for Business Automation
              Added Support for 22.0.1 IF002
              Added Support for Decision Production Service(Step 3 - Build DB and LDAP assets and Deploy Services)
              Added new starter services all (removed old samples)
          OpenShift
              Added support for all IPI installs to enable Masters true (OCP_MASTER_NODES_SCHEDULABLE=true)
              Added support to auto login to IBM Account for ROKS install (IBMCLOUD_ACCOUNT_ID="")
              Added ability to increase wait time for VSPhere UPI reboot for  (VSPHERE_IGNITION_FILES_DEPLOYMENT_WAIT_TIME="500")
              Added Support to override VSphere UPI network device (VSPHERE_NETWORK_ADAPTER="")
              Added Red Hat pull secret validation precheck
              Upgraded RHACM to 2.6
              Upgraded Mirror Registry to 1.2.6
              Added support for 4.11
              Added precheck to IBM ipi for CIS instance and domain name
              Added support for 4.11(OCP only)
              Added support for Manual credentials mode on GCP & AWS
              Added prechecks for bring your own VPC for GCP, AWS, & Azure
          Cloud Pak for Data
              Added support for 4.5.2
              Removed support for 4.0.2-4.0.5
          Cloud Pak for Integration
              Removed support for 2021.3.1 & 2021.2.1
          Cloud Pak for WAIOps
              Added support for 3.4.1 & 3.4.2
              Added deployment of Infrastructure Automation component (CP4WAIOPS_DEPLOY_IA=true)
              Reconfigured scripts to align with Daffy deployment pattern.
                  Infrastructure Automation and Event Manager will be installed with the service.sh script. AI Manager gets deployed with the base of the cloud pak.
          IBM IPI
              Added precheck CIS and DNS domain
              Added VPC quota precheck that builds VPC, subnet, and instances to test for quota limits (Can be toggled off IBM_ALLOW_VPC_PRECHECK=false)
          AppStore
              New AppStore feature
                New App - IBM Sterling B2B Install tool
          Misc
              Remove support for OCP 4.6 and 4.7 -  https://access.redhat.com/support/policy/updates/openshift
              Updated IDS LDAP install and --console info to include search filters on output
              During cleanup for ROKS, logout from ibmcloud
              Added ROKS and ibm-ipi to security-cleanup tool
              Added OpenShift Ceph Tools into any installation of OCS/ODF.
              Added install of dos2unix util for prepare host
              Removed install of nmon for prepare host
              Added ROKS and IBM IPI to security-cleanup.sh
              Added OpenShift Ceph Tools into any installation of OCS/ODF
              Updated CloudCTL and added support to install stand alone via tools.sh

## v2022-08-17b
          Cloud Pak for Integration
              Fixed Daffy code issue with Platform Navigator not finishing operator install

## v2022-08-17a
          Cloud Pak for Data
              Fixed issue with operators for services stuck in Upgrade Pending
              (Known CP4D issue with release of 4.5.2, breaking previous releases of 4.5.0 and 4.5.1. Would occur with Daffy, CP4D-cli, or running manually)

## v2022-08-17
          Tested OpenShift with Current Daffy Release
              GCP       4.8.46 / 4.10.22
              AWS       4.8.46 / 4.10.22
              Azure     4.8.46 / 4.10.22
              ROKS      4.8.46 / 4.10.22
              VSphere   4.8.46 / 4.10.22
              KVM       4.8.46 / 4.10.22
              IBM IPI   4.10.22
          Cloud Pak for Business Automation
              Added Support for 22.0.1 IF001
              Added Support for Decision Production Service(Step 2 - Namespace and base Operators)
              Added Support for Content Production Service(Step 2 - Namespace and base Operators)
              Added Support for Workflow Production Service(Step 2 - Namespace and base Operators)
              Addd New RPA Server
                  MSSQL Server project and Database configured
                  OpenLDAP for RPA configured
                  Added 21.0.3
                  Added 21.0.2 IF005
          Cloud Pak for Integration
              Add support for each service to be in its own namespace
          Cloud Pak for Data
              Added Support for 4.5.0 and 4.5.1
              Added Support to specify different storage class for each service
              Added new service Match 360
              Added new service Open OpenPages
              Added new service Analytics Engine powered by Apache Spark
              Added new service Db2 Warehouse
              Added new service Data Privacy
              Added new service Cognos Analytics
              Added new service Db2 OLTP              
		  Turbonomics
              Added Platform Operator Install
              Added Kubeturbo Operator Metrics Collector
          Watsion WAIOps
              Added support for 3.4.0
          IBM IPI
              Added support for new platform type of IBM Cloud (ibm-ipi) OCP 4.10+
          Misc
              Added ability to install older version of daffy with refresh.sh (--list)
              Fixed bug for KVM precheck on Host that has Memory > 1 TB
              Added precheck to validate the number of cluster nodes matches the number of nodes in environment file
## v2022-07-14
          Tested OpenShift with Current Daffy Release
              GCP       4.8.42 / 4.10.17
              AWS       4.8.42 / 4.10.17
              Azure     4.8.42 / 4.10.17
              ROKS      4.8.42 / 4.10.17
              VSphere   4.8.42 / 4.10.17
              KVM       4.8.42 / 4.10.17
          Cloud Pak for Business Automation
              Added 21.0.3 IF008 and IF009
              Added 22.0.1
              New Samples ocp-starter-ocs-all-22.0.1 and roks-starter-ibm-all-22.0.1
          Cloud Pak for Integration
              Updated to install via single operator per product
              Added support for 2022.2.1
          Cloud Pak for Data
               Added 4.0.8 and 4.09
          WebSphere Automation
              Added support for v1.4
          Cloud Pak for Security
              Added support for v1.10
          OpenShift
              Added ability to enable masters as worker nodes (UPI Only) - OCP_MASTER_NODES_SCHEDULABLE=true(Default is false)
              Added support for mirror-registry to support airgap and building of own registry(Quay mirror-registry)
              Added support Red Hat Advanced Cluster Management (RHACM)
              Added support for ODF overview page in OpenShift Console
          Misc
              Added new icons to output messages to help users with types of messages being displayed
              Added new logging to capture all info displayed to console for each process and list log location
              Added support to create new disk for NFS
              Added precheck to validate cluster version matches environment file OCP version
              Added precheck for OCS/ODF to make sure that your cluster has at least 6 workers
              Added precheck for Cluster Name to make sure that it matches environment file value
              Fixed bug to catch errors and exit when creating ROKS cluster
              Fixed bug with OS check, will exit now if not running on support platform              
              Fixed bug with OCP 4.10 and Local registry mirrors (dkikuchi@us.ibm.com)
              Fixed bug with CP4BA using wrong variable CP_DEPLOYMENT_PLATFORM should be CP4BA_AUTO_PLATFORM (Toby.Liu@ibm.com)
              Fixed order of OCP installs as it relates to Airgap and Local Registry Auth Info (gmarcy@us.ibm.com)

## v2022-05-23
          Tested OpenShift with Current Daffy Release
              GCP       4.8.40
              AWS       4.8.40
              Azure     4.8.40
              ROKS      4.8.36
              VSphere   4.8.40
              KVM       4.8.40
          OpenShift
              Added support for AWS Zone overrides(1,2 or 3)
              Added support for AWS KMS keys for disk encryption (via AWS_ENABLE_KMS_KEY=true)
              Added support for AWS to skip the AdministratorAccess precheck
              Added AWS sample security policies to use if not allowing AdministratorAccess policy
          VSphere
              Added support for VSphere Data Center with more then one VSphere Cluster
              Added ability to pause VSphere Install prior deploying ignition files (OCP_DEPLOY_ALL_IGNTIION_FILES_PAUSE=true)
          Cloud Pak for Security
              Added new cloud pak and Version 1.9
          Cloud Pak for Business Automation
              Starter Services
                  workflow - workflow-workstreams,bai,baml,baw_authoring,case,content_integration,pfs,workstreams
              Added IF008 support
              Added support for basic sample CP4BA CR's.  List, Status, Console support at basic non dynamic way
              Added support for Open Prediction Service HUB(OPS)
              Added support for OpenShift 4.9 and 4.10
          Cloud Pak for Data
              Renamed Service Cognos to Cognos Dashboards
          Cloud Pak for WAIOps
              Added support for version 3.3
              Added AI Manager 3.3
              Added Event Manager 3.3
          IBM
              TechZone flag to help with using ROKS Cluster provisioned by TechZone (ROKS_PROVIDER=techzone)
          Misc
              Added precheck for DNS PTR reverse lookup for UPI install with (DNSMASQ_BUILD=false)
              **Tech Preview - Added support for Macbook bastion (Except vsphere-*, kvm-upi, db2 and ldap)
              Added new tools process to install supporting tools outside of the daffy process. (oc,aws,gcloud,cloudctl,mustgather etc)
              Added new mustgather process
              Add new Variables to help track usage of daffy tool
          Bug
              Added logic to check for errors during prepareHost step
              Fixed logic to test exact name for storage class, not partial name check
              Fixed order logic to approveVCenterCert during precheck
              Fixed channel name for CP4D Scheduling Operator based on release

## v2022-04-20c
          OpenShift
              Added support for AWS to skip the AdministratorAccess precheck
              Added AWS sample security policies to use if not allowing AdministratorAccess policy
              Skip DNS check for AWS Publish Internal
              Support AWS OCP Internal Publish

## v2022-04-20b
          OpenShift
              Support Azure OCP Internal Publish
          Cloud Pak for Data
              Support for 4.0.8 (cloudctl and Single Catalog)

## v2022-04-20a
          OpenShift
              Support ability to Skip HAProxy Build
              Support ability to Skip DNSMasq Build
          Misc
              Support Proxy for bastion host

## v2022-04-20
          Tested OpenShift with Current Daffy Release
              GCP       4.8.36
              AWS       4.8.36
              Azure     4.8.36
              ROKS      4.8.35
              VSphere   4.8.36
              KVM       4.8.36
          Cloud Pak for Business Automation
              Added IF007 support
              Added support to install DB2 on Ubuntu/Redhat Linux Server
              Added support to install IDS(LDAP) on RedHat Linux Server
          Cloud Pak for Data
              Precheck and only support OCP 4.8 for CPD 4.0.X
              Fixed DV bug on ROKS  - New Db2 Tuning added(With Warning)
              Support for 4.0.7 (cloudctl not working only Single Catalog)
              Added new service Cognos Dashboard
              Added new service DB2 Data Management Console
          WebSphere Automation
              Added support for version 1.3
              Added an environment file for wsa
          VSphere
              Updated ISO images to latest version for each base version
              Added better error message for UPI install and Missing ISO Image
          OpenShift
              Updated TShirt Size output to allow copy/paste to simplify overrides
              Added support to install custom openshift-install program (TechZone request)
              Added VSphere IPI support to specify resource pool from custom openshift-install program (TechZone request)
              Added support for 4.10 (Note: Currently only CP4I supports 4.10)
              Added support for OpenShift Data Foundation(ODF) for OCP 4.10 only
          Misc
              Added support for RHEL 8.X bastion (Except UPI)
              Added new Security Cleanup script
              Added new version script in the root of daffy
              Added support for the all-in-one command to skip Cloud Pak install
              Enhanced Secure MQ demo and documentation
          Bug
              Fixed master cleaup.sh if user passed wrong env file, it would then do rebuild not cleanup.
              VSphere UPI install was broken with worker7-9 logic and haproxy and dnsmasq template files.
              Fixed daffy-init.sh to check for root user and exit if not root

## v2022-03-31
          Tested OpenShift with Current Daffy Release
                GCP       4.8.31
                AWS       4.8.31
                Azure     4.8.31
                ROKS      4.8.31
                VSphere   4.8.31
                KVM       4.8.31
          Cloud Pak for Business Automation
                Added IF005 support
          Cloud Pak for Data
                Added support for Cloud Pak for Data 4.0.6
                Added install for python3 and pip3 for >= 4.0.6
                Added build/remove of portworx storage classes
                Added support for WKC, WML and WS on ROKS
                Added new service Decision Optimization(DODS)
                Added new service DataStage
                Updated cloudctl install only supports latest version of CP4D
          Cloud Pak for Integration
                Added new single MQ instance
                Added new App Connect Designer instance
                Added new API Connect instance
                Added new App Connect Dashboard instance
                Added new Operations Dashboard tracing instance
                Added new Event Streams instance
                Added new HA MQ instance
                Added new Asset Repository instance
          WebSphere Automation (WSA)
                Added new component that supports install of WebSphere Automation
          OpenShift
                Added support for Proxy Install
                Added new root level cleanup.sh, that calls the ocp cleanup.sh
                Added confirmation during cleanup.sh of OCP
                Added logic to not restart ROKS nodes multiple times if doing more than one service at different times
                Added support for KVM UPI to support up to 9 worker nodes
          Misc
                Added logic to support user overrides for cloud Pak components versions(All Supported Cloud Paks)
                Added support for AWS custom Subnets and AMI ID overrides in OCP install
                Added new confirmation of warranty during Daffy install

## v2022-02-15b
          Cloud Pak for Business Automation
                Switched from Patterns to Services terminology
                Added logic to support user overrides for cloud Pak components versions

## v2022-02-15a
          Automated ROKS oc login step
          validated cluster name to be lower case and alphanumeric

## v2022-02-15
          Tested OpenShift with Current Daffy Release
                  GCP       4.8.26
                  AWS       4.8.26
                  Azure     4.8.26
                  ROKS      4.8.26
                  VSphere   4.8.26
                  KVM       4.8.26
          Added Cloud Pak
                Cloud Pak for Business Automation 21.0.3
                    Starter Services
                        content - filenet,cmis,ier,tm,bai
                        decisions - odm,bai
                        content-decisions  - filenet,cmis,ier,tm,odm,bai
          Added new OCP_INSTALL_TYPE
                  msp = Managed Service Provider(roks-msp)
          Added ROKS Support
                Build and Cleanup of ROKS Cluster
                Install Cloud Paks on existing Cluster(Daffy did not build ROKS Cluster)
                Supports Classic only
          Added support for Cloud Pak for Data 4.0.5
          Added new consoleFooter Function
          Added logic to support local cert folder outside of Daffy and not to remove on refresh command
          Updated refresh logic to display current version and new version during execution

          Updated command line options to support multiple case options(--precheck|--Precheck, etc)
          Updated default Storage Class and Vendor logic to support roks via env.sh files
          Updated all Cloud Paks and Service install precheck to use prepare host function
          Updated cp4waiops logic, renamed and removed old preinstall logic
          Updated sample env files to new testing versions of Openshift 4.8.26
          Updated imageContentSources.yaml for AirGap install to list more standard mirrors

          Bug Fixes
              VSphere OCP install-config.yaml - added quotes around cluster and network values
              Before OCP Install cluster, remove ocp-install dir to remove old trans files
              Fixed Typos and Spelling errors
              Hide errors when sourcing .profile if it does not exist

## v2022-01-18

          Added Cloud Pak
                Cloud Pak for WAIOps
                Multi-Cloud Pak in single Cluster
          Added Support for Case Install
                Cloud Pak for Data
                Cloud Pak for Data Services
          Added support for Cloud Pak for Data 4.0.3 and 4.0.4
          Added support for Cloud Pak for Data services operations tools
          Added support for Cloud Pak for Integration 2021.4.1
          Added Cloud Pak for Data services
                Statistical Package for the Social Sciences(SPSS)
                Watson Machine Learning(WML)
          Added Support for Bastion on Windows WLS2(Ubuntu 20.04)
          Added Daffy version to all status commands
          Added support for VSphere restricted folder install
          Added support for Image Registry for UPI install of OCP
          Added support to allow full install of OpenShift and Cloud Pak from single command(all-in-one)

          Updated CP4D
                New Namespace was added and all CP4D services/operands will be deployed in separate/new namespace

          Updated CP4D Services
                Added more info to service status output
                Added new single status command for all Daffy Supported Services
                Added ability to install more then once service at a time
                Added ability to remove service via cleanup function for each service

          Cleaned Up logging
                  Moved more logs from tmp to log folder
                  Displayed more log names and location in output

          Bug Fixes
                VSphere install now allows for special character passwords(dalmeter@us.ibm.com)
                Nodes were mislabeled for OpenShift Container Storage
                Taint added to OpenShift Nodes for OpenShift Container Storage
                Local Volumes for UPI install now have tolerance for OpenShift Container Storage nodes
                Added Overwrite Flag for 99-worker-cp4d-crio-conf to allow for node expansions with IPI install(dkikuchi@us.ibm.com)
                GCP removed unused roles required for precheck
                Corrected CP4D version(dkikuchi@us.ibm.com)
                Data Virtualization was looking for hard coded version and would not install post 4.0.2
                KVM IP precheck only checked that IP given was part of local not not full IP

          Removed Features
                Removed support for OpenShift 4.7

## v2021-12-01

          Added Cloud Pak
              (CP4I) Cloud Pak for Integration 2021.3.1 and 2021.2.1
          Added Platform Support
              AWS(aws) - IPI
          Added OpenShift Support for 4.9
          Added pre check logic to validate base domain and cluster name to verify valid DNS Syntax (FQDN)
          Added support - Subdomain for base domain on KVM and VSphere Installs
          Added support for KVM Web Dashboard - vmdashboard

          Updated OpenShift Container Storage for IPI to use provider Storage Class
              IPI Installs now have easy disk expansion from Console for OCS
          Updated OCS to label all Storage nodes as Infrastructure(Infra) nodes
          Update Daffy Stats URL and new arguments

## v2021-11-12 - Initial Release

          OpenShift Supported 4.6,4.7 and 4.8
          Cloud Pak for Data Supported 4.01
          OpenShift Container Storage Supported
          Platforms Supported
                   Google Cloud Provider(gcp) - IPI
                   Azure(az) - IPI
                   VSphere(vsphere) - IPI and UPI
                   KVM(kvm) - UPI
