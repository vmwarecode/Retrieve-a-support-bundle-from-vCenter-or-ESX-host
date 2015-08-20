This sample code shows how to retrieve a support bundle from vCenter and ESX host

How To Run

In order to run this sample code you must provide four arguments:
[1] The server name or IP address
[2] The user name to log in as
[3] The password to use
[4] (optional) The esx host IP address (If provided, it will retrieve the ESX bundle instead of VC bundle)

You will need to get the vim25.jar library from the VMware vSphere JDK.  It is in the
VMware-vSphere-SDK-5.5.0\vsphere-ws\java\JAXWS\lib directory.

You can run this sample code by downloading the zip file below, unzipping it and running a command similar to the following:
1. To retrieve VC support bundle URL:
java -cp vim25.jar com.vmware.sample.GetSupportBundleUrlFromVcOrEsx <ip_or_name> <user> <password>
For example:
java -cp vim25.jar com.vmware.sample.GetSupportBundleUrlFromVcOrEsx 10.20.30.40 JoeUser JoePasswd

2. To Retrieve ESX support bundle URL:
java -cp vim25.jar com.vmware.scia.general.GetSupportBundleUrlFromVcOrEsx <ip_or_name> <user> <password> <esxHostIP>
For example:
java -cp vim25.jar com.vmware.scia.general.GetSupportBundleUrlFromVcOrEsx 10.20.30.40 JoeUser JoePasswd 10.20.30.41

Output

You will see the output similar to the following when you run the sample:
Generating the support bundle...  (depending on the bundle size, it may take several minutes)
Success in retrieving the support bundle
You can download the support bundle using the following URL: https://10.20.30.40:443/diagnostics/vcsupport-52fbfadc-de30-f1f3-08c6-f40007d6c60a.tgz

