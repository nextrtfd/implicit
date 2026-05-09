.. meta::
    :description: Developer guide for integrating Ride-Hailing SDKs with Google Maps via deep-linking and location parameters.
    :keywords: Google Maps Ride-Hailing, Deep-linking Careem, Ride SDK Integration, Location Parameters, UAE Developer Guide
    :author: Muayed

===================================================
Ride-Hailing SDK Integration Guide for Google Maps
===================================================

Integrating ride-hailing services directly into map-based applications enhances user experience by providing seamless transitions from navigation to booking. This guide focuses on implementing deep-linking between transport directories and applications like Careem or Uber, specifically tailored for developers in the UAE.

Overview of Deep-Linking
========================

Deep-linking allows a mobile application to be opened to a specific page or state via a URL or intent. In the context of ride-hailing, this means passing location parameters (latitude and longitude) from a web-based transport directory (like Lignedebus) or a custom map interface directly to the Careem app.

How it Works
============

When a user selects a destination on a map, the application generates a deep-link URL. This URL is then intercepted by the ride-hailing application on the user's device, pre-filling the pickup and drop-off locations.

Key Parameters:
---------------

- **Destination Latitude/Longitude**: The exact coordinates of the user's destination.
- **Pickup Latitude/Longitude**: (Optional) The user's current location or a specific pickup point.
- **Provider ID**: Specifies which service to open (e.g., Careem, Uber).

Implementation for UAE Developers
=================================

Developers in the GCC region can leverage official SDKs or intent-based URLs to trigger these actions.

1. **Intent-based URLs**
   For Android and iOS, using custom schemes like `careem://` allows developers to pass parameters directly.

2. **Google Maps SDK for iOS/Android**
   Google Maps provides native support for ride-hailing providers. By registering your app, you can appear in the "Transport" tab of Google Maps. (For the end-user perspective, see :doc:`bpr`)

Automation and Order Flow
=========================

By sending precise `latitude` and `longitude` parameters, developers can automate the initial steps of the ordering process (further detailed in :doc:`careem-api-guide`), reducing friction and increasing conversion rates for transport-related services.

Benefits for Transport Directories
==================================

- **Enhanced Utility**: Connects static bus or transport data with on-demand mobility.
- **Seamless UX**: Users can find a route and book a ride in a few taps.
- **Ecosystem Integration**: Builds a bridge between public transport data and private ride-hailing services.

Conclusion
==========

Deep-link integration is a powerful tool for developers looking to unify the transport ecosystem in the UAE. By leveraging location parameters and mobile intents, you can provide a premium, automated experience for users transitioning from navigation to booking.

References
----------

- https://developer.uber.com/docs/riders/ride-requests/tutorials/deep-links/introduction
- https://developers.google.com/maps/documentation/urls/android-intents
