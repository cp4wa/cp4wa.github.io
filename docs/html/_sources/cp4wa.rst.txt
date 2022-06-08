Cloud Pak for Watson AIOps
##########################

prerequisite
************

- OpenShift cluster, you can request a cluster, see instruction to request :doc:`openshift` .

Install CP4WA
*************

Do refer to instruction on setting up a non HA starter CP4WA version for testing `here <https://www.ibm.com/docs/en/cloud-paks/cloud-pak-watson-aiops/3.3.0?topic=manager-starter-installation-cli>`_.

IBMer and partner can request of an instance OpenShift cluster where you can install CP4WA for testing.

Do ensure you request the following 

- workers nodes x5 (16CPU x64GB)
- if you intent to have ODF then you will need additional 3 workers.

**Notes:**

When you provisioned a OCP with ODF, the `precheck for CP4WA 3.3 <https://github.com/IBM/cp4waiops-samples/tree/main/prereq-checker/3.3>`_ failed for OCP registry check.
To resolve this, you need to create a PVC and attach registry, see the `documentation <https://access.redhat.com/documentation/en-us/red_hat_openshift_data_foundation/4.9/html/deploying_and_managing_openshift_data_foundation_using_red_hat_openstack_platform/configure_storage_for_openshift_container_platform_services>`_ on how you can do this.

.. image:: ./images/precheck-failedreg.png
.. image:: ./images/precheck-pass.png

Sample Connection in CP4WA
**************************
.. image:: ./images/cp4wa-conn.png
   

Integrating to Splunk
*********************

To connect to Splunk you need to ensure Splunk REST API is enabled, the free trail version of Splunk Cloud REST API is disabled.

Splunk REST API is served by default at port 8089 over HTTPS.

Do refer to  :doc:`splunk` on how to install a Splunk Enterprise on OpenShift.

Add Connection: Splunk
======================

.. image:: ./images/splunk-connection.png
.. image:: ./images/splunk-connection-test.png
.. image:: ./images/splunk-connection-train.png

Integrating to Kubernetes (CP4WA)
*********************************

testing adding kubernetes connection, the following shows adding connection for a local OCP where CP4WA is hosted.

.. image:: ./images/cp4wa-k8sadd.png
.. image:: ./images/cp4wa-k8slocal.png
.. image:: ./images/cp4wa-k8sschedule.png
   

Integrating to ServiceNow
*************************

To test this integration, you can provisioned a developer instance at ServiceNow.

.. image:: ./images/cp4wa-snow.png
.. image:: ./images/cp4wa-snowconn.png
.. image:: ./images/cp4wa-snowtop.png
.. image:: ./images/cp4wa-snowtick.png
   

Resources
*********

- `CP4WAIOps samples <https://github.com/IBM/cp4waiops-samples>`_