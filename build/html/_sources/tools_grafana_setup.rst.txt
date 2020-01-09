Setting up Grafana
==========================================

**Grafana** is an open-source data visualization tool that accepts different data sources.

Grafana on Fedora
-------------------

The steps described in this section apply to `Fedora 29 Workstation <https://getfedora.org>`_.

To set up Grafana on Fedora, perform the following steps:

1. Add the Grafana repository.

   ::

    $ touch /etc/yum.repos.d/grafana.repo

     $ nano /etc/yum.repos.d/grafana.repo

   ::

    [grafana]
     name=grafana
     baseurl=https://packages.grafana.com/oss/rpm
     repo_gpgcheck=1
     enabled=1
     gpgcheck=1
     gpgkey=https://packages.grafana.com/gpg.key
     sslverify=1
     sslcacert=/etc/pki/tls/certs/ca-bundle.crt

2.  Update the repository and install Grafana, as well as additional fonts for rendering text.

    ::

      $ dnf update
      $ dnf install grafana fontconfig freetype* urw-fonts

3. Start the Grafana service, check the status, and set server to start on boot.

    ::

      $ /sbin/chkconfig --add grafana-server
      $ systemctl daemon-reload
      $ systemctl start grafana-server
      $ systemctl status grafana-server
      $ systemctl enable grafana-server.service

4. Access http://localhost:3000/ and log in using the default username and password.

    Username: admin

    Password: admin

5. Update the user password.

The following table lists the default paths for **Red Hat** and **Fedora** based installs of **Grafana**.

.. list-table:: Grafana paths
   :widths: 50 50
   :header-rows: 1

   * - Description
     - Path
   * - Logs
     - ``/var/log/grafana``
   * - SQLite database
     - ``/var/lib/grafana/grafana.db``
   * - Configuration file
     - ``/etc/grafana/grafana.ini``
   * - Systemd environment file
     - ``/etc/sysconfig/grafana-server``

Grafana on Azure
-------------------

**Grafana** is available on **Microsoft Azure** as a dedicated service, a container, or a **Bitnami** service.

To set up **Grafana** on **Azure**, users would require an existing or new **Virtual Machine** or **Resource Group**.
