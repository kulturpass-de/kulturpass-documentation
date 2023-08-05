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

**Note:** The product itself does not carry attributes for the price and for the available stock quantity. Those attributes need to be set as part of the [offer creation procedure](project-processes-and-functions.md#initial-offer-creation). 

Product creation can either be performed via file import or via manual product creationas first (optional) step during offer creation. As soon as a product was validated by the Mirakl marketplace system, it get's an internal unique ID assigned (called the _product ID_) which becaomes an important link for the later offer creation. For better understanding the internal representation of products and offers in the Mirakl marketplace system there is a more deeper look into technical requirements and restrictions in the article [Technical product and offer maintenance](../technical-documentation/technical-product-and-offer-maintenance.md).

## Initial offer creation

The basic KulturPass concept is that only those articles can be reserved/purchased, that have fulfill three conditions:
1. There is an valid product record published on the marketplace for the respective article.
2. Also, there ar valid offers (at least one offer) for this product set.
3. The available quantity for the offer is greater or equal 1.

Subsequently, for a vendor it is crucial to create offers, once the products are globally available on the marketplace. When creating an offer, a product must be referred first. The Mirakl marketplace place system provides a number of of attributes that can be set for the offer. However, the KulturPass only requires the price and the available quantity of the offer. For better store and stock management, a private SKU can be assigned to the offer and a quantity warning can be configured as threshold. 

**Note:** The offer description will _not yet_ displayed at any time. Also the KulturPass implementation and term & condition expect the user to collect the article onsite; subsequently, shipping costs cannot be charged. This also applies to any kind of fees, markups, taxes, and other surcharges - they all have to be zero, which means: The given price shown in the KulturPass mobile app is a total price. 

For better understanding the internal representation of products and offers in the Mirakl marketplace system there is a more deeper look into technical requirements and restrictions in the article [Technical product and offer maintenance](../technical-documentation/technical-product-and-offer-maintenance.md).

##

Back to [Project documentation](README.md)

Follow up the [Technical documentation](../technical-documentation/README.md)

Back to [start of KulturPass documentation](../../README.md)
