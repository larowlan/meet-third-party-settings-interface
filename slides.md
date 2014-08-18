# Drupal <img src="/images/d8-logo.png" alt="Drupal 8 logo" width="100" style="background:none; border:none; margin: 0; box-shadow: none">

## For Site Builders

Kim Pepper

<kim@previousnext.com.au>

[@kimb0oo](https://twitter.com/kimb0oo)

---

## So What's New?

- Configuration management <!-- .element: class="fragment" -->
- Contrib modules now in core <!-- .element: class="fragment" -->
- Blocks improvements  <!-- .element: class="fragment" -->
- CKEditor  <!-- .element: class="fragment" -->
- New field types  <!-- .element: class="fragment" -->
- Display and form modes <!-- .element: class="fragment"  -->
- Reponsive support  <!-- .element: class="fragment" -->
- Multingual  <!-- .element: class="fragment" -->
- much much more...  <!-- .element: class="fragment" -->

Note:
- Lots of architectural changes under the hood (symfony routing & services, plugins)
- A number of site-building improvements
- A lot of contrib modules are now core features

---

## Redundant Drupal 7 Contrib Modules

- Views <!-- .element: class="fragment" -->
- Views Bulk Opertations <!-- .element: class="fragment" -->
- Admin Views <!-- .element: class="fragment" -->
- Bean <!-- .element: class="fragment" -->
- WYSIWYG <!-- .element: class="fragment" -->
- Link <!-- .element: class="fragment" -->
- Date <!-- .element: class="fragment" -->
- Email <!-- .element: class="fragment" -->
- Phone <!-- .element: class="fragment" -->
- UUID <!-- .element: class="fragment" -->
- Entity API <!-- .element: class="fragment" -->
- Entity Cache <!-- .element: class="fragment" -->
- Entity Reference <!-- .element: class="fragment" -->
- Entity View Modes <!-- .element: class="fragment" -->
- Menu Block* <!-- .element: class="fragment" -->
- Webform* <!-- .element: class="fragment" -->
- ...and many more. <!-- .element: class="fragment" -->

---

## Blocks

- Fieldable
- Blocks support multiple instances
- Config exportable
- Conditions Plugins API

Note:

- Fieldable == BEAN

--

## Block Layout

![Block Layout Screen](/images/blocks/block-layout.png)

- Block _Types_ allow for multiple instances

--

## Configure Block

![Configure Block Screen](/images/blocks/configure-block.png)

Note:

- Conditions Plugins API

--

## Custom Block Types

![Custom Block Types](/images/blocks/custom-block-types.png)

Note:

- Fieldable
- Replaces BEAN & Fieldable Panel Panes

--

## Menu Block

- Core menus moving to blocks
- Basic `menu_block` functionality

--

## Page Manager

- Uses core Condition API
- (Coming soon)

---

# Fields

New field types:

- Link <!-- .element: class="fragment"  -->
- Date <!-- .element: class="fragment"  -->
- Email <!-- .element: class="fragment" -->
- Phone <!-- .element: class="fragment" -->
- Entity Reference <!-- .element: class="fragment" -->

Note:

- Mobile friendly fields


--

Link Field

![link Field](/images/fields/link-field.png)

--

Email Field

![Email Field](/images/fields/email-field.png)

--

Telephone Field

![Phone Field](/images/fields/phone-field.png)

--

<!-- .slide: data-transition="none" -->
Date Field

![Date Field 1](/images/fields/date-field-1.png)

--

<!-- .slide: data-transition="none" -->
Date Field

![Date Field 2](/images/fields/date-field-2.png)

---

## Comments

- Attached to **any** entity (via fields) <!-- .element: class="fragment"  -->
- Private / public threads? <!-- .element: class="fragment"  -->
- Comments on user profiles? <!-- .element: class="fragment"  -->

---

## Display Modes

- View Modes
- _Form_ Modes

--

## View Modes

![View Modes](/images/display-modes/view-modes.png)

Notes:

- Replaces Entity View Modes module

--

## Form Modes

![View Modes](/images/display-modes/manage-form.png)

--

## Configure Form Fields

![View Modes](/images/display-modes/form-modes.png)

---

## Configuration Management

Drupal 7 _workarounds_

- Features <!-- .element: class="fragment" --> **&#x2717;** <!-- .element: class="fragment cross" -->
- CTools Exportables <!-- .element: class="fragment" --> **&#x2717;** <!-- .element: class="fragment cross" -->
- Variables <!-- .element: class="fragment" --> **&#x2717;** <!-- .element: class="fragment cross" -->
- hook_update_N() <!-- .element: class="fragment" --> **&#x2717;** <!-- .element: class="fragment cross" -->

<br />

Drupal 8  <!-- .element: class="fragment" -->

- Drupal 8: Unified Configuration API <!-- .element: class="fragment" --> **&#x2713;** <!-- .element: class="fragment check" -->

Note:

- What features was trying to do
    - Lots of workarounds
    - ctools exportables
    - handling content types, variables, permissions
    - update hooks
- CMI is a unified API and approach

--

## Single Export / Import

![Single Export](/images/cmi-export.png)

--

## Config Deployment Workflow

1. Configure a config staging dir that is in git<!-- .element: class="fragment" data-fragment-index="1" -->
```php
$config_directories[CONFIG_STAGING_DIRECTORY]
    = 'config';
```
<!-- .element: class="fragment" data-fragment-index="1" -->
2. Export config <!-- .element: class="fragment" data-fragment-index="2" -->
```bash
drush config-export staging
```
<!-- .element: class="fragment" data-fragment-index="2" -->
3. Git commit and push <!-- .element: class="fragment" data-fragment-index="3" -->
4. Import config<!-- .element: class="fragment" data-fragment-index="4" -->
```bash
drush config-import staging
```
<!-- .element: class="fragment" data-fragment-index="4" -->
5. Profit! <!-- .element: class="fragment" data-fragment-index="5" -->

---

## Multilingual

Drupal 7 _workarounds_

- Core Locale & Content Translation <!-- .element: class="fragment" -->
- i18n module including <!-- .element: class="fragment" -->
    - i18n_block
    - i18n_contact
    - i18n_field
    - i18n_menu
    - i18n_path
    - i18n_redirect
    - i18n_string
    - i18n_taxonomy
    - i18n_user
    - i18n_variable
- Variable module <!-- .element: class="fragment" -->
- Title module <!-- .element: class="fragment" -->
- Entity Translation <!-- .element: class="fragment" -->
- ...more??? <!-- .element: class="fragment" -->


--

## Drupal 8

### Supports Translatable:

- Entities <!-- .element: class="fragment" -->
- Fields (including base fields) <!-- .element: class="fragment" -->
- Configuration <!-- .element: class="fragment" -->
- <!-- .element: class="fragment" --> _Installer_ <!-- .element: class="fragment" -->

<br/>

More than all of the D7 contrib modules combined. <!-- .element: class="fragment" -->
