---
description: J2Commerce (formerly known as J2Store)
---

# How to write language override for plugin in multilingual site

Sometimes you need to translate some text (which is rendered from any apps or plugins) for your multilingual site. This guide will help you to translate them. Please keep following the instructions given below.

## Find the language constant <a href="#find-the-language-constant" id="find-the-language-constant"></a>

First thing, you have to find the language string for the text that you want to translate.

For example, if you are using the Sagepay payment plugin on your site and want to translate the error message, please open the downloaded plugin file.

![lang override](https://raw.githubusercontent.com/j2store/doc-images/master/translation/how-to-write-language-override-for-plugin-multilingual-site/plugin_lang_override_01.png)

Open the language folder and edit the INI file.

Find the language constant for the text that you want to translate.

![plugin langoverride 2](https://raw.githubusercontent.com/j2store/doc-images/master/translation/how-to-write-language-override-for-plugin-multilingual-site/plugin_lang_override_02.png)

Once find the language constant, go to Extensions > Language > Overrides

Before creating the override, set the Filter to ADMINISTRATOR (of the language that you wanted to create the override. Say, your language is French. Then you should select the German (fr-FR) Administrator in the filter)

![plugin langoverride 5](https://raw.githubusercontent.com/j2store/doc-images/master/translation/how-to-write-language-override-for-plugin-multilingual-site/plugin_lang_override_05.png)

Click NEW button.

![plugin langoverride](https://raw.githubusercontent.com/j2store/doc-images/master/translation/how-to-write-language-override-for-plugin-multilingual-site/plugin_lang_override_04.png)&#x20;

Enter your language constant in the language constant text box and enter the value in the Text box.

Check both locations and save.

![plugin langoverride3](https://raw.githubusercontent.com/j2store/doc-images/master/translation/how-to-write-language-override-for-plugin-multilingual-site/plugin_lang_override_03.png)

NOTE: For translating the plugin’s text in a multilingual site, please don’t put the language strings directly into your site’s language file. Please create a language override for the specific language.
