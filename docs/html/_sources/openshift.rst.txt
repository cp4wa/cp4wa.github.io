Red Hat OpenShift
#################

IBMers and partners can request for Red Hat OpenShift Kubernetes Service (ROKS) from IBM Techzone.

Reserve an instance
*******************

You can reserve an instance of OpenShift for self enablement or POC, `access <https://techzone.ibm.com/collection/custom-roks-vmware-requests>`_ to reserve your instance.

You can request custom Managed OpenShift clusters through the new self-service reservation form. Choose cluster size, flavor, and size by clicking reserve now.

    - Managed OpenShift cluster (ROKS) in IBM Cloud (“classic”) with NFS support.
    - Managed OpenShift cluster (ROKS) in IBM Cloud (VPC/"Gen2") with OCS support.

To access the link above you need to have IBMid, to create an `IBMid <https://www.ibm.com/account/reg/signup?formid=urx-19776&target=https%3A%2F%2Flogin.ibm.com%2Foidc%2Fendpoint%2Fdefault%2Fauthorize%3FqsId%3D8bdd0123-f231-42b5-9f2a-2cad9ebed217%26client_id%3DODllMDk4YzItMjgxOC00>`_.

To reserve OpenShift Instance on IBM Cloud click on **Reserve** for ROKS on classics infrastructure or VPC.

.. image:: ./images/ocp-reserve.png
   
You can view your `reservation <https://techzone.ibm.com/my/reservations>`_ as shown below.

.. image:: ./images/ocp-reservation.png

When you reservation is ready, an email will be sent to you with your OCP information on how you can access the cluster and also to add yourself as user to access the cluster in IBM Cloud.

You can delate your reservation as shown.

.. image:: ./images/ocp-delete.png

Pre-requisite
*************

You need to install and ensure you have the following

- `IBM Cloud CLI getting started <https://cloud.ibm.com/docs/cli?topic=cli-getting-started>`_
- `OpenShift CLI getting started <https://docs.openshift.com/container-platform/4.8/cli_reference/openshift_cli/getting-started-cli.html>`_


Get OpenShift login token for use with oc 
******************************************

.. image:: ./images/ocp-logincmd.png
.. image:: ./images/ocp-token.png

Once you run the above ``oc login`` you will be able to use oc to managed the ocp cluster.

List projects in ocp
====================

.. code-block:: bash

   oc projects

List current project
====================

.. code-block:: bash

   oc project

List routes in current project
==============================

.. code-block:: bash

   oc get routes

List storage class
==================

.. code-block:: bash

   oc get sc

Resources
*********

- get started with `OpenShift on IBM Cloud <https://cloud.ibm.com/docs/openshift?topic=openshift-getting-started>`_