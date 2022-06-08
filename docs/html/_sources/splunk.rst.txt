Splunk
######

The following provides guidance in setting splunk on OpenShift using the community splunk-operator.

Prerequisite 

- OpenShift cluster

Deploy Splunk Operator
**********************

login to OpenShift
==================

get OpenShift login credential

from a terminal, login to openshift

create project
==============

You can create the project in advance and choose the created project when you install the splunk-operator. Alternatively, you can also create project aka namesapce during installatin of splunk-operator.

.. code-block:: bash
    
    oc new-project splunk-operator

create splunk-operator namespace aka project

install the operator
====================

install the operator using openshift UI

.. image:: ./images/deploy-splunk-operator.png
.. image:: ./images/install-splunk-operator.png
.. image:: ./images/fill-operator-form.png
.. image:: ./images/create-namespace.png
.. image:: ./images/operator-namespace.png
.. image:: ./images/operator-install-progress.png
.. image:: ./images/installed-operator.png
.. image:: ./images/operator-pod-ready.png

Deploy Splunk Enterprise Standalone 
************************************

install the standalone splunk server

Deploy Splunk standalone
========================

.. image:: ./images/operator-view.png
.. image:: ./images/standalone-create.png
.. image:: ./images/standalone-label.png
.. image:: ./images/standalone-form-create.png
.. image:: ./images/standalone-progress.png
.. image:: ./images/standalone-pod.png
.. image:: ./images/standalone-podready.png
.. image:: ./images/splunk-servicename.png
     

get password for splunk web
---------------------------

to get the password to login Splunk as admin

.. code-block:: bash

   oc get secret splunk-example-standalone-secrets -o custom-columns=PASSWORD:.data.password --no-headers | base64 -D

quick local test splunk web
---------------------------

to test Splunk Web with your machine locally, you need to forward the port, run the following command in terminal.

.. code-block:: bash

   kubectl port-forward splunk-example-standalone-0 8000

After you have forward the port locally, by default, the Splunk web is accessbile using using http @ http://localhost:8000

You can login to Splunk and configure to use SSL later.

Test drive splunk
*****************

clink on the route to Splunk web, login to see the following.

.. image:: ./images/splunk-webui.png

Configure Splunk
================

Splunk preferences (Optional)
-----------------------------

Global preferences

.. image:: ./images/splunk-globalpref.png

SPL Editor

.. image:: ./images/splunk-splpref.png

Server settings
---------------

.. image:: ./images/server-setting.png

General settings

.. image:: ./images/splunk-generalsettings.png

Server controls
---------------

to restart the server after your changes in configuration.

.. image:: ./images/splunk-restart.png

Users (Optional)
----------------

You can add users and roles accordingly.

Add user

.. image:: ./images/splunk-users.png

Add data
========

you can access Add data from the Splunk Web home page or from the Settings menu.

.. image:: ./images/splunk-adddata.png

You can download Splunk tutorial zip to test out the add data.

Search data
===========

after you add the tutorial data, you can test the search, see the link to the tutorials at Resources below.

create route
============

After setting the Splunk to be served using https, you can expose your Splunk Web and API to be accessbile outside of OCP cluster.

To do that, you will need to create routes using port 8000 and 8089 for Splunk Web and Splunk REST API respectively.

Create route for Splunk web
---------------------------

Provide a name for the route and set the following as shown and choose port 8000.

.. image:: ./images/splunkweb-routeweb.png


Create route for Splunk REST API
--------------------------------

Provide a name for the route and set the following as shown and choose port 8089.

.. image:: ./images/splunk-routeapi.png

Splunk public 
--------------

You should have two routes where Splunk is accessible publicly, clink on the **Location** link.

.. image:: ./images/splunk-routes.png

Resources
*********

- `Splunk search tutorial <https://docs.splunk.com/Documentation/Splunk/8.2.6/SearchTutorial/WelcometotheSearchTutorial>`_
