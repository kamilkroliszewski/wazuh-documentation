.. Copyright (C) 2021 Wazuh, Inc.

.. _wazuh-modulesd:

wazuh-modulesd
==============

The wazuh-modulesd program manages the Wazuh modules described below.

.. topic:: Database wodle

  The Wazuh core uses list-based databases to store information related to agent keys, and FIM/Rootcheck event data. This information is highly optimized to be handled by the core.

  In order to provide well-structured data that can be accessed by the user or the Wazuh API, new **SQLite-based databases** have been introduced in the Wazuh manager. The Database Synchronization Module is a **user-transparent component** that collects the following information from the core:

    - Agent information: name, address, encryption key, last connection time, operating system, version and shared configuration hash.
    - FIM data: creation, modification and deletion of regular files and Windows registry entries.
    - Rootcheck detected defects: issue message, first detection date and last alert time.
    - Static core settings: maximum permitted agents or SSL being enabled for Authd.

.. topic:: CIS-CAT wodle

  The CIS-CAT wodle allows you to run CIS policy scans visualizing the results of assessments in the Wazuh App. See the :doc:`CIS-CAT integration <../../capabilities/policy-monitoring/ciscat/ciscat>` for more information on this functionality.

.. topic:: Command wodle

  The Command module allows running external commands asynchronously, one in each thread.

.. topic:: Syscollector wodle

  The Syscollector module performs periodic scans in the system to obtain information related to the installed hardware, operating system information, network information, installed packages, active ports, and running processes.

.. topic:: AWS S3 wodle

  The AWS S3 wodle allows you to gather and parse logs from multiple AWS services, such as Guard Duty, Macie, VPC Flow, etc. See the :ref:`AWS S3 <amazon>` section for more information on this functionality.

.. topic:: GitHub wodle

  The GitHub wodle allows you to gather audit logs from multiple GitHub organizations. See the :ref:`GitHub <github>` section for more information on this functionality.

.. topic:: Vulnerability detector wodle

  The Vulnerability Detector module detects applications that are known to be vulnerable (affected by a CVE).

.. topic:: Osquery wodle

  The Osquery wodle provides the user an operating system instrumentation tool that makes low-level operating system analytics and monitoring both efficient and intuitive using SQL-based queries. For more information, read through the documentation for :doc:`osquery integration <../../capabilities/osquery>`.

.. topic:: Key polling wodle

  The key polling wodle allows you to fetch a client key from an external source, for example, a database. This provides a mechanism to auto-register agents when they are not registered on a manager instance but reporting to it.

.. topic:: SCA module

  The :ref:`SCA module <manual_sec_config_assessment>` allows users to check the system configuration against policy files to determine vulnerabilities and misconfigurations.

.. topic:: Agent upgrade module

  The agent upgrade module manages, validates, executes and checks the result of all the agent upgrade requests. It uses the WPK files.

.. topic:: Task manager module

  The task manager module creates, updates and manages all the tasks performed on the agents.

wazuh-modulesd options
----------------------

+---------+---------------------------+
| **-d**  | Basic debug mode.         |
+---------+---------------------------+
| **-dd** | Verbose debug mode.       |
+---------+---------------------------+
| **-f**  | Run in the foreground.    |
+---------+---------------------------+
| **-h**  | Display the help message. |
+---------+---------------------------+
| **-t**  | Test configuration.       |
+---------+---------------------------+
