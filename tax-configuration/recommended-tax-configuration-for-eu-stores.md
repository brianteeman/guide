# Recommended Tax Configuration for EU stores

This guide will walk you through the configuration of tax in J2Commerce for EU stores. This is an example configuration for stores in Europe. For detailed information on tax, please consult an expert.

> Important: No guarantee is offered with respect to any of the information given here. Please contact an expert before you take any decisions about tax matters.

NOTE: The example assumes you have a store in Germany and you charge 19% tax on the goods. All customers coming originating from Germany are charged with 19 % of tax.

## Step 1 : Create a geozone for base rates (home country tax) <a href="#step-1--create-a-geozone-for-base-rates-home-country-tax" id="step-1--create-a-geozone-for-base-rates-home-country-tax"></a>

Go to Components > J2Commerce > Localization -> Geozones -> New

<figure><img src="../.gitbook/assets/geo-zone.webp" alt=""><figcaption><p>Geo Zone Germany</p></figcaption></figure>

<figure><img src="../.gitbook/assets/geo-zone-germany.webp" alt=""><figcaption><p>Geo Zone Germany</p></figcaption></figure>

Geozone Name: Base rates

Country : Germany

Zones : All

## Step 2: Create a tax rate <a href="#step-2-create-a-tax-rate" id="step-2-create-a-tax-rate"></a>

Go to Localization -> Tax Rates -> New

<figure><img src="../.gitbook/assets/tax-rate.webp" alt=""><figcaption><p>Tax Rate Germany</p></figcaption></figure>

<figure><img src="../.gitbook/assets/tax-rate-germany.webp" alt=""><figcaption><p>Tax Rate Germany</p></figcaption></figure>

Name : VAT

Tax Percent : 19

Geozone : Base rates

Status : Published

## Step 3: Create a tax profile and rules <a href="#step-3-create-a-tax-profile-and-rules" id="step-3-create-a-tax-profile-and-rules"></a>

Go to Localization -> Tax Profiles -> New

<figure><img src="../.gitbook/assets/tax-profile.webp" alt=""><figcaption><p>Tax Profile Germany</p></figcaption></figure>

<figure><img src="../.gitbook/assets/tax-profile-germany.webp" alt=""><figcaption></figcaption></figure>

Name: Base Tax Profile

Enabled: Yes

Tax rules

Click Add

Rate: VAT

Associated Address: Shipping

## Step 4: Configure tax settings <a href="#step-4-configure-tax-settings" id="step-4-configure-tax-settings"></a>

Go to Setup -> Configuration -> Tax

<figure><img src="../.gitbook/assets/tax-config-germany.webp" alt=""><figcaption></figcaption></figure>

Prices Entered with Tax: Yes, I will enter prices with tax

Calculate tax based on: Shipping address

Default Customer address: Store address

Display prices in product pages: Including tax

Display prices in cart / checkout : Including tax

Apply discounts : After tax

Save.

## Step 5: Create a product and choose the tax profile <a href="#step-5-create-a-product-and-choose-the-tax-profile" id="step-5-create-a-product-and-choose-the-tax-profile"></a>

J2Commerce uses Joomla articles as products. So go to Article Manager and create a New Article / Product (If you sue any other catalog source like Zoo or Sebold, you should head there).

Product creation steps are explained under the topic Products.

Here let us just see how to choose the tax profile:

Go to J2Store Cart tab -> General tab

Tax Profile : Base tax profile

<figure><img src="../.gitbook/assets/j2store-tax-germany.webp" alt=""><figcaption><p>Base Tax Profile</p></figcaption></figure>

IMPORTANT: If you do not choose the tax profile, then tax will not apply in the store front.

## Step 6: Selling in multiple countries with multiple tax rates <a href="#step-6-selling-in-multiple-countries-with-multiple-tax-rates" id="step-6-selling-in-multiple-countries-with-multiple-tax-rates"></a>

If you are selling your products to other countries in Europe, then there are three scenarios

* Charge the same VAT rate for customers from certain countries. In this case, you will just have to open the Base Geozone and add the countries / zones to which you want to charge 19%. Then all customers from all those countries will be charged with the 19% tax rate.
* Charge different VAT rate for customers from certain countries.  Let us say, you want to charge 12% tax for customers from Switzerland and France. Create a new Geozone and include Switzerland and France. Create a new tax rate and set the tax percent to 12%. Go to Components > J2Commerce > Localization > Tax Profiles > Open Base tax profiles. Under Tax rules, Click add, Choose your New tax rate and associate it to the Shipping address. Save. Now customer from Switzerland and France will be charged with 12 % of tax instead of your base rate of 19%.

Video Tutorial:

{% embed url="https://youtu.be/ejYMqa5-5Q4" %}
