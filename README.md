# MultiTech Conduit TTN Installer

For detailed instructions see the [documentation](https://www.thethingsnetwork.org/docs/current/multitech/).

## Installation

1.  Install LORA mCard as per [instructions](http://www.multitech.net/developer/products/accessory-cards/installing-an-accessory-card/) provided by MultiTech.

2.  Download [installer.sh](installer.sh).

3.  Connect to Conduit using the [instruction at item 2](http://www.multitech.net/developer/software/mlinux/getting-started-with-conduit-mlinux/).

4.  Copy [installer.sh](installer.sh) to the conduit using Putty SCP (`pscp.exe`) on Windows or `scp` on Mac/Linux:

    ```bash
    scp installer.sh root@192.168.2.1:
    ```

5.  Using the connection established in step 3, run the installer.

    ```bash
    sh installer.sh
    ```

6.  Provide answers to the prompts.

    * For the network you will need to choose a network with unrestricted access to the Internet. However, do not connect the Conduit directly (without firewall) to the Internet to prevent possible security issues!

    After the network settings have been provided the Conduit shuts down, once the leds on the front of the conduit stopped flashing, power the conduit down and connect it to the target network.

7. Log on to the Conduit using putty/ssh with the IP address information provided in step 6 or the IP address assigned to it by the DHCP server (when using DHCP)

8.  Restart the installer to continue installation.

    ```bash
    sh installer.sh
    ```

    Once the installer finished (without errors) the Conduit is connected to TheThingsNetwork.
