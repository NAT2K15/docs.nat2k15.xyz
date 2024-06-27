---
description: >-
  This document provides support information for integrating and using the FiveM
  resource with the our framework. Ensure the framework is installed and
  properly configured before proceeding
---

# ☎️ Framework 911 S (paid)

#### Step 1: Install the NAT2K15 Framework

If you haven't already, follow the instructions provided by the NAT2K15 framework documentation to install and configure it on your server.

#### Step 2: Disable the 911 Command

Edit the framework configuration file to disable the 911 command. This step is crucial to prevent conflicts with this resource. Locate the configuration file, typically found in the `config` folder of the framework, and set the `Command_911`parameter to `false`.

<figure><img src="https://i.imgur.com/Rwldx6U.png" alt=""><figcaption></figcaption></figure>

1. Download the resource files.
2. Place the resource folder in your server's `resources` directory.
3. Ensure the folder name remains unchanged for proper integration.

#### Step 3: Update Server Configuration

Open your server configuration file (`server.cfg`) and add the following line to ensure the resource is started after the Nat2k15 framework:

```lua
start framework #NAT2K15 Framework
start framework-911
```

Replace `framework-911` with the actual name of the resource folder. The resource must start with letters we recommend to call the resource `framework-911`

{% embed url="https://store.nat2k15.xyz/store/framework-911" %}
