# Drupal <img src="/images/d8-logo.png" alt="Drupal 8 logo" width="100" style="background:none; border:none; margin: 0; box-shadow: none">

## For Site Builders

Kim Pepper

<kim@previousnext.com.au>

[@kimb0oo](https://twitter.com/kimb0oo)

---

## Who Is This For?

- Drupal 7 Site Builders <!-- .element: class="fragment" data-fragment-index="1" -->
- Drupal 7 Developers <!-- .element: class="fragment" data-fragment-index="2" -->
- Drupal 7 Site Administrators <!-- .element: class="fragment" data-fragment-index="3" -->

Note:
- Drupal site builders, not developers, or themers
- Site admins might find it useful

---

## So What's New?

- Configuration management <!-- .element: class="fragment" data-fragment-index="1" -->
- Contrib modules now in core <!-- .element: class="fragment" data-fragment-index="2" -->
- Blocks improvements  <!-- .element: class="fragment" data-fragment-index="3" -->
- CKEditor  <!-- .element: class="fragment" data-fragment-index="4" -->
- New field types  <!-- .element: class="fragment" data-fragment-index="5" -->
- Display and form modes <!-- .element: class="fragment" data-fragment-index="6" -->
- Reponsive support  <!-- .element: class="fragment" data-fragment-index="7" -->
- Multingual  <!-- .element: class="fragment" data-fragment-index="8" -->
- much much more...  <!-- .element: class="fragment" data-fragment-index="9" -->

Note:
- Lots of architectural changes under the hood (symfony routing & services, plugins)
- A number of site-building improvements
- A lot of contrib modules are now core features

---

## Redundant Drupal 7 Contrib Modules

- Views <!-- .element: class="fragment" data-fragment-index="1" -->
- Views Bulk Opertations <!-- .element: class="fragment" data-fragment-index="2" -->
- Admin Views <!-- .element: class="fragment" data-fragment-index="3" -->
- Bean <!-- .element: class="fragment" data-fragment-index="4" -->
- WYSIWYG <!-- .element: class="fragment" data-fragment-index="5" -->
- Link <!-- .element: class="fragment" data-fragment-index="6" -->
- Date <!-- .element: class="fragment" data-fragment-index="7" -->
- Email <!-- .element: class="fragment" data-fragment-index="8" -->
- Phone <!-- .element: class="fragment" data-fragment-index="9" -->
- UUID <!-- .element: class="fragment" data-fragment-index="10" -->
- Entity API <!-- .element: class="fragment" data-fragment-index="11" -->
- Entity Cache <!-- .element: class="fragment" data-fragment-index="12" -->
- Entity Reference <!-- .element: class="fragment" data-fragment-index="13" -->
- Menu Block* <!-- .element: class="fragment" data-fragment-index="14" -->
- Webform* <!-- .element: class="fragment" data-fragment-index="14" -->
- ...and many more. <!-- .element: class="fragment" data-fragment-index="15" -->

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

## Configuration Management

### What problem does it solve?

- ~~Features~~ <!-- .element: class="fragment" data-fragment-index="1" -->
- ~~CTools Exportables~~ <!-- .element: class="fragment" data-fragment-index="2" -->
- ~~Variables~~ <!-- .element: class="fragment" data-fragment-index="3" -->
- ~~hook_update_N()~~ <!-- .element: class="fragment" data-fragment-index="4" -->

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

