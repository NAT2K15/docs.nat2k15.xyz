---
description: >-
  To ensure successful integration of your product with the NPWD framework,
  please follow these detailed steps carefully:
---

# Installing npwd-framework

1. **Configure the NPWD-Framework:**
   * Navigate to the `npwd-framework` configuration settings.
   * Verify that the framework's name matches the exact folder name of your resource. By default, this is set to `framework`.
2. **Database Integration:**
   * Import the `patch.sql` file into your SQL server. This step is crucial to ensure that the integration functions correctly.
3. **Server Configuration:**
   * When editing the `server.cfg` file, it is imperative to adhere to the specific starting order detailed below. This order ensures that the framework operates efficiently, with `npwd` being initiated after its prerequisites:
     * `ensure screenshot-basic`
     * `ensure pma-voice`
     * `ensure npwd`
     * `ensure framework`
     * `ensure npwd-framework`

By following these steps, you'll facilitate a smooth integration process, allowing our product to work seamlessly with the NPWD technology.
