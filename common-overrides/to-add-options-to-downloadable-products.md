---
description: J2Commerce (formerly known as J2Store)
---

# To add options to downloadable products

By default, Downloadable Products don't have "Options" but occasonally there may be a need to enable Options and if this arises, follow these steps.

TAKE A FULL SITE BACKUP BEFORE THESE STEPS TO AVOID ISSUES!

#### Back End View

Copy&#x20;

```
/administrator/components/com_j2store/views/product/tmpl/formdownloadable.php
```

&#x20;To&#x20;

{% code overflow="wrap" %}
```
/administrator/templates/YOUR-DEFAULT-TEMPLATE/html/com_j2store/product/formdownloadable.php
```
{% endcode %}

**Example:** If you are using the Joomla 4 or 5 'Atum' administrator template, you would replace **YOUR-DEFAULT-TEMPLATE** with 'atum' to give you:

```
/administrator/templates/atum/html/com_j2store/product/formdownloadable.php
```

**Find the line shown below:**

{% code overflow="wrap" %}
```
<li><a href="#imagesTab" data-toggle="tab"><i class="fa fa-file-image-o"></i> <?php echo JText::_('J2STORE_PRODUCT_TAB_IMAGES'); ?></a></li>
```
{% endcode %}

**AFTER that line, insert a new line and with the following:**

{% code overflow="wrap" %}
```
<li><a href="#optionsTab" data-toggle="tab"><i class="fa fa-sitemap"></i> <?php echo JText::_('J2STORE_PRODUCT_TAB_OPTIONS'); ?></a></li>
```
{% endcode %}

**Find the line shown below:**

{% code overflow="wrap" %}
```
<div class="tab-pane" id="imagesTab"> <?php echo $this->loadTemplate('images');?> </div>
```
{% endcode %}

**AFTER that line, insert a new line and with the following:**

{% code overflow="wrap" %}
```
<div class="tab-pane" id="optionsTab"> <?php  echo $this->loadTemplate('options');?> </div>
```
{% endcode %}

**Find the line shown below:**

{% code overflow="wrap" %}
```
<?php echo \Joomla\CMS\HTML\HTMLHelper::_('uitab.addTab', 'j2storetab', 'filesTab', JText::_('J2STORE_PRODUCT_TAB_FILES')); ?>
<div class="row">
<div class="col-lg-12">
<?php  echo $this->loadTemplate('files');?>
</div>
</div>
<?php echo \Joomla\CMS\HTML\HTMLHelper::_('uitab.endTab'); ?>
```
{% endcode %}

**AFTER that line, insert a new line and with the following:**

{% code overflow="wrap" %}
```
<?php echo \Joomla\CMS\HTML\HTMLHelper::_('uitab.addTab', 'j2storetab', 'optionsTab', JText::_('J2STORE_PRODUCT_TAB_OPTIONS')); ?>
<div class="row">
<div class="col-lg-12">
<?php  echo $this->loadTemplate('options');?>
</div>
</div>
<?php echo \Joomla\CMS\HTML\HTMLHelper::_('uitab.endTab'); ?>
```
{% endcode %}

```
Save the file
/administrator/templates/atum/html/com_j2store/product/formdownloadable.php
```

If you now look at a Downloadable Product in the backend, you should see an **Options** tab in the layout

#### Front End View

To ensure the options are seen in the front end, you need to know the layout of the app you are using for layouts in J2Commerce.

**Example:** If you are using Bootstrap5, this is used in the file structure that you will copy

**Copy:**

```
/plugins/j2store/app_bootstrap5/app_bootstrap5/tmpl/bootstrap5/view_downloadable.php
```

\[note the repeated use of bootstrap5 in the above path!]

**To:**

{% code overflow="wrap" %}
```
/templates/YOUR-WEBSITE-TEMPLATE/html/com_j2store/templates/bootstrap5/view_downloadable.php
```
{% endcode %}

**Find the line below:**

```
<?php echo $this->loadTemplate('cart'); ?>
```

**BEFORE that line, insert a new line and with the following:**

```
<?php echo $this->loadTemplate('options'); ?>
```

**Save:**&#x20;

<pre data-overflow="wrap"><code><strong>/templates/YOUR-WEBSITE-TEMPLATE/html/com_j2store/templates/bootstrap5/view_downloadable.php 
</strong>[if using bootstrap5]
</code></pre>

Now the downloadable products should have an options tab on the backend, and the options should be visible on the frontend.&#x20;
