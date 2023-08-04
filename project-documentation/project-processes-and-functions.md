# KulturPass - Project Processes and Functions

The KulturPass project basically implements a cultural marketplace where the KulturPass app users consume the goods and services.
For the vendors the following processes and functions are relevant on the platform:

- Vendor Onboarding (including the steps: [vendor identification and registration](https://github.com/kulturpass-de/kulturpass-documentation/edit/feature/documentation-update/project-documentation/project-processes-and-functions.md#vendor-identification-and-registration), [initial shop settings](https://github.com/kulturpass-de/kulturpass-documentation/edit/feature/documentation-update/project-documentation/project-processes-and-functions.md#initial-shop-settings), [initial product maintenance](https://github.com/kulturpass-de/kulturpass-documentation/edit/feature/documentation-update/project-documentation/project-processes-and-functions.md#initial-product-maintenance), [initial offer creation]())
- Order Management including cancellation and returns
- Financial Processes

The young people, the users of the KulturPass app, are the consumers of the goods and services offered on the KulturPass marketplace. This mobile app implements a number of capabilities and functions for the youth:

- Registration
- Geospatial services
- Offer browsing and filtering
- Ordering, cancellation and returns of goods and services

This documentation focuses on the project side of the processes and functions. A more technical deep dive you find in the [Technical Processes and Functions](../technical-documentation/technical-processes-and-functions.md).

## Vendor identification and registration

To provide an attractive markteplace for the KulturPass users, it is crucial to have a colorful mix, a wide variety of sellers of cultural offers. Subsequently, the KulturPass comes with an open concept to identify and register as a seller. This process is as simple as possible, both legally and technically. In principle, there are no exclusion criteria for participation in the Kurlturpass, as long as a vendor is eligible under the EU cultural funding program. During the identification and registration process the seller has to pass basically three steps:
1. Agreements (terms & conditions, data safety and security)
2. EU questionnaire
3. ELSTER registration process with the digital certificate of the seller organization. To find more details about the technical registration, check the section [Seller Registration with ELSTER](https://github.com/kulturpass-de/kulturpass-documentation/blob/main/technical-documentation/seller-registration-with-elster.md) 

The registration procedure also asks for initial name of the marketplace shop and creates the vendor's shop in the background. A user-oriented description and FAQ for this procedure can be found in the [Help Center](https://service.kulturpass.de/help/de-de/6-registrierung-fur-anbietende) (German language only).

Once the registration process is completed successfully, the seller can access the shop and start with configuration of basic settings.

## Initial shop settings

From the shop owner's viewpoint, there are three important settings to be maintained:
- Physical address/location details of the shop; this is important for the distance calculation based on the geospacial services)
- Accessibility information for the shop location
- Bank account details; otherwise money transfer from BMK to the shop owner will fail.

If these tasks are perfomed successfully, the vendor can start entering the product and offer data into the system. There is also a user-focused article for first steps of the vendors in the [Help Center](https://service.kulturpass.de/help/de-de/6-registrierung-fur-anbietende/125-ubersicht-erste-schritte-nach-der-registrierung) (German language only).

## Initial product maintenance

Selling via KulturPass requires a shop owner at least to place offers at the marketplace. Those offers are always based on product master data.
The basic concept includes, that product master data - once published on Mirakl and synchronized with Commerce - can be shared across  all registered shops on the marketplace. (In principle, the same product could be entered multiple times, but there are technical measures in place to prioritize the one record (called master) that defines the attribute setting utilized for all offers based on this product.)
Minimum product settings must include the basic attributes
- Product category assignment
- SHOP_SKU (an unique private ID) and a descriptive name
- Photography or picture, that gives a visual impression of the product
- Verbal description. This description can be utilized to convey also supplementary details like venue location, URLs for external, or how the pick-up procedure is intended to be, which makes the description a substantial part of the offer visible in the KulturPass mobile app.

 Product creation can either be performed via file import or via manual product creationas first (optional) step during offer creation.

## Initial offer creation

Back to [Project documentation](README.md)
