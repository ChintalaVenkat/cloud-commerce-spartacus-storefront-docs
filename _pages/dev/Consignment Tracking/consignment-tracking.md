---
title: Consignment Tracking (DRAFT)
---

## Intro

Customers can view consignment tracking information to know the real-time status of their packages.

In the order details page, if the consignment is in **Shipped** status, a **Track Package** button will be viewable for each consignment. Click the button to get the tracking information of the selected consignment.

## Requirements

The consignment tracking feature requires the following extensions to work:
 - consignmenttrackingoccaddon AddOn
 - consignmenttrackingfacades  Extension
 - consignmenttrackingservices Extension
 - consignmenttrackingmock Extension
 - consignmenttrackingbackoffice Extension

 See https://help.sap.com/viewer/4c33bf189ab9409e84e589295c36d96e/1905/en-US/6eafde9f14e243d6a53e0bfbfd6996bc.html for more information. 

## Enabling Consignment Tracking

You can enable and disable consignment tracking with feature flags and feature levels. To enable the consignment tracking feature, set the feature flag as follows: 
```
features: {
   consignmentTracking: true
}
```
Or set feature level: 
```
features: {
   level: ‘1.2’(>=1.2)
}
```
This will enable all features configured <=1.2 in `app.module.ts`.

Or you can mix feature level and feature flags:
```
features: {
   level: ‘1.1’,
   consignmentTracking: true,
 }
```


## Configuring

No special configuration needed.

## Extending

No special extensibility available for this feature.