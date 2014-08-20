# Drupal <img src="/images/d8-logo.png" alt="Drupal 8 logo" width="100" style="background:none; border:none; margin: 0; box-shadow: none">

## For Site Builders

Kim Pepper

<kim@previousnext.com.au>

[@kimb0oo](https://twitter.com/kimb0oo)

---

## So What's Wrong With Drupal 7?

Note:

- Often, don't notice there was an issue until something better comes along
- D7 was a big improvement over D6: fields, entities (only half baked)
- Still rely heavily on contrib: wysiwyg, menu block, and ctools for basic building blocks

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
- Entities: lots of things are now fieldable
- Plugins: easier/consistent way to extend core features.

---

## Redundant Modules

- Views
- Views Bulk Opertations
- Admin Views
- Bean
- WYSIWYG
- Link
- Date
- Email
- Phone

--

## Redundant Modules

- UUID
- Entity API
- Entity Cache
- Entity Reference
- Entity View Modes
- Menu Block*
- Webform*

- ...and many more.

---

## Blocks

- Fieldable <!-- .element: class="fragment" -->
- Multiple instances  <!-- .element: class="fragment" -->
- Config exportable  <!-- .element: class="fragment" -->
- Conditions Plugins API  <!-- .element: class="fragment" -->

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

---

# Fields

New field types:

- Link <!-- .element: class="fragment"  -->
- Date <!-- .element: class="fragment"  -->
- Email <!-- .element: class="fragment" -->
- Phone <!-- .element: class="fragment" -->
- Entity Reference <!-- .element: class="fragment" -->

--

## Mobile Friendly

![Mobile Screenshots](/images/fields/mobile.png)

---

## Comments

- Attached to **any** entity (via fields) <!-- .element: class="fragment"  -->
- Private / public threads? <!-- .element: class="fragment"  -->
- Comments on user profiles? <!-- .element: class="fragment"  -->

--

### Comment Types

![Comment Types](/images/comments/comment-types.png)

--

### Article Fields

![Comment Types](/images/comments/article-fields.png)

--

### Article Comment Settings

![Comment Types](/images/comments/article-settings.png)

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

## Contact Forms

- Fieldable Entity
- Webform Replacement?

Note:

- Requires storage and reporting

--

### Contact Form Fields

![Contact Form](/images/contact/contact-form.png)

---

## Responsive

- Responsive toolbar
- Responvive Images

--

## Responsive Images

![Responsive](/images/responsive/responsive-image.png)

Note:

- No UI for breakpoints
- Moving to theme.info.yml

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

## Drupal 8 Multilingual

- Entities <!-- .element: class="fragment" -->
- Fields (including base fields) <!-- .element: class="fragment" -->
- Configuration <!-- .element: class="fragment" -->
- <!-- .element: class="fragment" --> _Installer_ <!-- .element: class="fragment" -->

<br/>

More than all of the D7 contrib modules combined. <!-- .element: class="fragment" -->

--

## Multilingual Modules

![Multilingual Modules](/images/multilingual/modules.png)

--

## Drupal Installer

![Install Drupal](/images/multilingual/install-drupal.png)

--

## Drupal Installer

![Install Drupal](/images/multilingual/install-2.png)

---

# The Future


- Menu Block?
- Display Suite?
- Page Manager / Panels?
- Metatags?
- Pathauto?


- When will Drupal 8 be released?

---

# Questions?

---

## Thanks!

<kim@previousnext.com.au>

[@kimb0oo](https://twitter.com/kimb0oo)
