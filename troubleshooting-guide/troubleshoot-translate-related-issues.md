---
description: J2Commerce (formerly known as J2Store)
---

# Troubleshooting Translate related Issues

## 1. Did you download and installed the translations for your language from our website ? <a href="#id-1-did-you-download-and-installed-the-translations-for-your-language-from-our-website" id="id-1-did-you-download-and-installed-the-translations-for-your-language-from-our-website"></a>

Do you see your language listed?

If your language is 100% complete, go head and download the language pack and install it using the Joomla installer. Yes you read it correct. Via the JOOMLA installer.

If your language is not complete, please translate the strings by following the guide at [click here](https://www.j2store.org/support/user-guide/translate-j2store-in-your-language.html)

## 2. Did you set your site Default language to your language in Language manager? <a href="#id-2-did-you-set-your-site-default-language-to-your-language-in-language-manager" id="id-2-did-you-set-your-site-default-language-to-your-language-in-language-manager"></a>

* Go to Joomla administrator->Extensions->Language Manager

Set your language as the default one (NOTE: You should have installed your Joomla language pack (NOT J2Store language pack) before doing this)

* Assuming that Spanish is your language. Set Spanish as your Default Language.

Note down the language code of yours. For example, the language code for English (UK) is en-GB, Spanish = es-ES. (Google to know your language code)

* Now go to Joomla admin->Components->J2store. Does all text in your language?
* If yes, you are fine and carry on with your work.
* If not all strings are translated, go to step 3

## 3. Translate the missing/untranslated strings <a href="#id-3-translate-the-missinguntranslated-strings" id="id-3-translate-the-missinguntranslated-strings"></a>

Open the /language/yourLanguage-Code/yourLanguage-Code.com\_j2store.ini

if you are using french, then your language code is fr-FR and you will be opening the /language/fr-FR/fr-FR.com\_j2store.ini

you will find untranslated strings like

;J2STORE\_CHECKOUT\_OPTIONS=“Checkout Options”

What you have to do is: Remove the semicolon and add your translation. So the translated string should look like **J2STORE\_CHECKOUT\_OPTIONS=“your translation”**

NOTE: the semicolon is removed.

Now do the same for administrator language files located in

/administrator/language/yourLanguage-Code folder

/administrator/language/yourLanguage-Code/yourLanguage-Code.com\_j2store.ini handles the language for the J2store administration area.

> IMPORTANT: All J2store language strings will start with J2STORE\_ or COM\_J2STORE if you see something like ;checkout or ;orders DO NOT translate them. They are comments.
