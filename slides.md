# Drupal <img src="images/d8-logo.png" alt="Drupal 8 logo" width="100" style="background:none; border:none; margin: 0; box-shadow: none">

## Third Party Settings Interface

Lee Rowlands

<larowlan@previousnext.com.au>

[@larowlan](https://twitter.com/larowlan)

---

## What?

![window to weight gain](http://i.imgur.com/yUje9.jpg)

- ThirdPartySettingsInterface is your window to <del>weight gain success</del> other module's config entities

---

## Drupal 7

![content types](https://www.dropbox.com/s/a8rnhq76oh8bk9t/Screenshot%202014-11-27%2010.09.42.png?dl=1)

---

## Drupal 7

![dumping ground](https://www.dropbox.com/s/e6dduanxeqeoba3/Screenshot%202014-11-27%2010.11.00.png?dl=1)

---

## Drupal 7

- Array PIs

---

## Drupal 8

![default config](https://www.dropbox.com/s/te37plz78vpua5e/Screenshot%202014-11-27%2010.13.21.png?dl=1)

- Config entities

---

## Drupal 8

- Defined interfaces ```$contact_form->getRecipients();```
- 1:N of something

---

## Drupal 8

- Config schema
- validates
- translations
- governs what is written

---

# Drupal 8

- Extension point - third party settings interface
- ```\Drupal\Core\Config\Entity\ThirdPartySettingsInterface```

---

# Drupal 8

![use the trait](https://www.dropbox.com/s/dljwm5wy0pymnu8/Screenshot%202014-11-27%2010.18.13.png?dl=1)

- As an owner - ```Drupal\Core\Config\Entity\ThirdPartySettingsTrait```

---

# Drupal 8

![schema](https://www.dropbox.com/s/y7t8dfl76klqdb9/Screenshot%202014-11-27%2010.17.18.png?dl=1)

- Config schema entry

---

# Drupal 8

![consumer schema](https://www.dropbox.com/s/9hvwl2fodmp3rm3/Screenshot%202014-11-27%2010.19.17.png?dl=1)

- As a consumer - define config for your stuff

---

# Drupal 8

![tinker forms](https://www.dropbox.com/s/3sxv2t2z4l5t1rf/Screenshot%202014-11-27%2010.20.23.png?dl=1)

- form alter your fields into the form

---

# Drupal 8

- Sample code - see contact module and contact_storage_test module in core.

---

# Questions?

---

## Thank you!

<larowlan@previousnext.com.au>

[@larowlan](https://twitter.com/larowlan)
