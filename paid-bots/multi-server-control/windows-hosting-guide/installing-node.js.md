---
description: >-
  This is a very crucial part without installing node.js the bot simply wont
  run.
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 👨‍💻Installing Node.js

**Guide to Installing Node.js on a Windows VPS for Bot Hosting**

***

#### Step 1: Download Node.js Installer

1. **Open a Web Browser**
   * Launch a browser on your VPS, such as Microsoft Edge.
2. **Visit the Node.js Website**
   * Navigate to [https://nodejs.org/](https://nodejs.org/).
3. **Choose the Installer**
   * Select the **LTS (Long-Term Support)** version for stability.
   * Click on the Windows Installer (**.msi** file) to download it.

***

#### Step 2: Install Node.js

1. **Run the Installer**
   * Double-click the downloaded `.msi` file to start the installation process.
2. **Follow the Installation Wizard**
   * Click **Next** to proceed.
   * Accept the license agreement and click **Next**.
   * Choose the default installation path or specify a custom one.
3. **Select Components**
   * Ensure that the `npm package manager` option is selected.
   * Click **Next**.
4. **Complete the Installation**
   * Click **Install** and wait for the process to finish.
   * Click **Finish** once done.

***

#### Step 3: Verify Installation

1. **Open Command Prompt**
   * Press `Win + R`, type `cmd`, and hit Enter.
2. **Check Node.js Version**
   *   Run the following command:

       ```
       node -v
       ```
   * This will display the installed version of Node.js.
3. **Check npm Version**
   *   Run the following command:

       ```
       npm -v
       ```
   * This will display the installed version of npm (Node Package Manager).

***

#### Conclusion

You have successfully installed Node.js on your Windows VPS and set up the environment for hosting your bot. With Node.js and npm ready, you can now develop and deploy your bot seamlessly. For further customization and troubleshooting, refer to the Node.js documentation.
