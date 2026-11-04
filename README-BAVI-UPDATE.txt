BAVI website update

Files
- index.html: updated storefront, product color cards, color-specific gallery, green completed tracking stages, notification bell/panel.
- assets/: product photos extracted from the supplied IMG_2331.pdf reference.
- config.js: existing API configuration remains blank.

Important backend items still required
1) config.js currently has window.BAVI_API = ''. The supplied ZIP contains no Google Apps Script/backend source.
2) The website therefore does not create customer accounts or centrally store orders at present; without the API it keeps the draft order in the customer's browser and uses WhatsApp flow.
3) Coupon validation is now intentionally disabled while the API is blank. Browser-only coupon checks/localStorage are not secure and can be bypassed or reset. To enforce one redemption per verified phone, the server must validate the phone and atomically record redemption against the order.
4) The notification bell is a visible UI entry point, but real order/offer notifications are not active until a backend supports authenticated customer identity (OTP), notifications feed, and optionally Web Push subscriptions/service worker. Do not expose order details by phone-number-only lookup.

To finish security + notifications, provide the Google Apps Script source project (or its current deployed API code and access to edit it).
