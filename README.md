# XeroCurrencyConverter
This is a script you can inject into xero and it converts line items prices into a specified currency. It will conver the prices when you click Approve or Edit on and Invoice. All you need to do is append the base currency and target currency to the description in this format: USD->AUD
It should work with New Invoices and Editing Invoices.

##How to use
1. In Xero create a new invoice.
2. Create line item and set the price to the Base Currency Price
3. Append [Base Currency]->[Target Currency] to the description. eg. USD->AUD
4. Click Approve and the script should take over, convert the prices one by one and submit the form.

##Google Chrome Setup Instructions
1. Sign up for a free [openexchangerates.org](https://openexchangerates.org/signup/free) account. (If you want to use a base currency different to USD you will need to choose a paid plan)
2. Install the [Custom Javascript for Websites Extension](https://chrome.google.com/webstore/detail/custom-javascript-for-web/poakhlngfciodnhlhhgnaaelnpjljija?hl=en)
3. Copy the code from script.js. Login to Xero and click the CJS button. Paste the entire script into the textfield.
4. Update the OPEN_EXCHANGE_RATES_APP_ID value to match your Open Exchange Rates APP ID.

##Firefox Setup Instructions
1. Sign up for a free [openexchangerates.org](https://openexchangerates.org/signup/free) account. (If you want to use a base currency different to USD you will need to choose a paid plan)
2. Install the [Javascript Injector for Firefox Extension](https://addons.mozilla.org/en-gb/firefox/addon/jsinjector)
3. Copy the code from script.js.
4. Create a new script. Set the path to "https://go.xero.com/*"
5. Paste the entire script into the textfield.
6. Update the OPEN_EXCHANGE_RATES_APP_ID value to match your Open Exchange Rates APP ID.
7. Click Add

###Notes
This script will break when Xero update their code. I will endevour to keep it updated when this happens.
Also, Xero is written with Prototype which I'm not familiar with. This script injects jQuery to speed up development. Future versions might be converted into Prototype.

##Credit
I wrote this script out of pure frustration with Xero. It wasn't overly easy. If you would like to make a donation to support my efforts please do via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=marc%40launchinteractive%2ecom%2eau&lc=AU&item_name=Launch%20Interactive&no_note=0&currency_code=AUD&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHostedGuest)