# Customize a website with Joomla!

Steps to customize your own website, built with Joomla! templates, modules and extensions

1) Install a template and modules that suit your objectives, e.g.
- the [AS Joomla Hotel Booking Template|https://www.astemplates.com/free-joomla-template/944-et-hotel-booking]
- the [The J-HotelReservation Starter|https://www.cmsjunkie.com/joomla_hotel_reservation_starter]

2) Adapt the website, e.g.
- by including modules in articles and content you write in your Content Management System interface, by citing them with
{loadmodule mod_#yourmodulename#}, here: {loadmodule mod_jhotelreservation}
- by altering the content in the language files of your module BEFORE (re-)installing the module.
E.g., in the ZIP file of your module, go to '...\jhotelreservation_starter_v6.0.7_j3\admin\language\en-GB', make a safety copy of the config file 'en-GB.com_jhotelreservation' and then alter the original file with content according to your needs.

## Logo change
1) Upload your own logo via the menu "Extensions" --> "Templates" --> "Styles".
2) edit the "logo.php" and "preloader.php" in "/features/logo.php". Create an security backup copy of "logo.php" (optimally follow the convention that Joomla! uses for overrides. But indicate that it's not indeed a being-used override file, but an inactive backup, e.g. with "logo" and the current date, e.g. " logo-SAVED-20190325-163901.php"):
Change
```php
	$html .= '<img class="sp-default-logo'. $custom_logo_class .'" src="' . $this->helix3->getTemplateUri() . '/images/presets/' . $this->helix3->Preset() . '/logo.png" alt="'. $sitename .'">';
```
to
```php
	$html .= '<img class="sp-default-logo'. $custom_logo_class .'" src="' . $this->helix3->getTemplateUri() . '/images/presets/' . $this->helix3->Preset() . '/logo_swapski_466_73.png" alt="'. $sitename .'">';
```
