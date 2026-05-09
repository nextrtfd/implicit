.. meta::
    :description: Overview of Careem Super App architecture, fleet management APIs, and POS integration for merchants.
    :keywords: Careem API Documentation, Fleet Management API, POS Integration, Super App Architecture, Careem Merchant API
    :author: Muayed

======================================================================
Careem API Documentation: Fleet Management and Order Automation
======================================================================

Careem's transition into a Super App has opened up a variety of API surfaces for partners, merchants, and fleet operators. This guide provides an overview of the Careem API architecture and how developers can leverage it for order automation and fleet management.

Careem Super App Architecture
=============================

The Careem ecosystem is built on a microservices architecture that handles millions of requests across transport, food, grocery, and payments. For developers, the most relevant entry points are:

- **Merchant API**: For payment processing and order status.
- **Fleet API**: For managing captain availability and dispatch (typically for partners).
- **Identity API**: For secure OAuth2-based user authentication.

Getting Started: API Keys and Authentication
============================================

Access to Careem APIs is generally restricted to registered partners.

1. **Merchant Portal**: Register your business on the Careem Merchant Portal.
2. **Credential Generation**: Once approved, you can generate your `Client ID` and `Client Secret` (ensure you secure these properly, as described in :doc:`nodejs-payment-security`).
3. **OAuth2 Flow**: Use these credentials to obtain a Bearer token for authorized requests.

.. code-block:: bash

   curl -X POST https://api.careem.com/token \
     -d "grant_type=client_credentials" \
     -u "CLIENT_ID:CLIENT_SECRET"

Order Automation for Merchants
==============================

Automating orders allows businesses to integrate their existing Point of Sale (POS) systems directly with Careem.

- **Menu Sync**: Keep your restaurant or shop menu updated in real-time.
- **Order Webhooks**: Receive instant notifications when a new order is placed or a captain is assigned (for implementation details, see :doc:`webhook-integration`).
- **Status Updates**: Programmatically update order status (e.g., "Preparing", "Ready for Pickup").

Fleet Management and Captain Dispatch
=====================================

For logistics partners, the Fleet API allows for:

- **GPS Tracking**: Real-time monitoring of captain locations.
- **Dispatch Logic**: Assigning orders to the nearest available captain based on complex routing algorithms.
- **Performance Analytics**: Tracking delivery times and captain efficiency.

POS Integration Strategies
==========================

To ensure a smooth operational flow, it is recommended to use a middleware that bridges your POS and Careem's API. This minimizes the risk of order delays and ensures consistent inventory management across all sales channels.

Conclusion
==========

The Careem API suite offers powerful tools for businesses looking to scale within the MENA region. Whether you are a small restaurant owner or a large logistics provider, understanding and integrating these APIs can significantly improve your operational efficiency and customer reach.

References
----------

- https://www.careem.com/en-ae/merchants/
- https://api.careem.com/docs (Partner Access Required)
