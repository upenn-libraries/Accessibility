# SSL Census: How are we doing?

This stub is to document how far we've come to enabling HTTPS across all our sites and services.
Please update this page with any corrections or additional information you might have.

## Penn Libraries Web: http://www.library.upenn.edu/
* In the current site, HTTPS is available, but not enforced by default. Most resources (images, scripts, CSS, etc) are all fetched over HTTP, so much of the site breaks when it is accessed over HTTPS. Locating and fixing all these resource calls is impossibly onerous, and since we're replacing the site with something in Drupal, we're choosing to let it be.
* In the new Drupal site (https://sites.library.upenn.edu/), HTTPS is enforced by default. If you visit through HTTPS, you're redirected through HTTPS. Yay!
This goes for all Drupal sites we've hosted on Pantheon (such as the [Publisher Policy DB](https://pubpolicy.library.upenn.edu/) and [Biomed 3D Print](https://3dprint.library.upenn.edu/)).

## Springshare Suite ("LibApps")
* **LibGuides**: http://guides.library.upenn.edu/
	* HTTPS is available, but not enforced by default.

* **LibAnswers**: http://faq.library.upenn.edu/
	* HTTPS is unavailable, but since Springshare recently made HTTPS a possibility, we're working on acuiring the necessary certs to enable it.

* **LibCal**: http://libcal.library.upenn.edu/
	* HTTPS is unavailable.

## Franklin: http://franklin.library.upenn.edu/index.html
* HTTPS is unavailable. (?)

## Account Services: https://dla.library.upenn.edu/ils/
* HTTPS is enforced by default.

## Articles+ (Summon): http://upenn.summon.serialssolutions.com/
* HTTPS is available, but not enforced by default.

## PennText (360 Link): http://elinks.library.upenn.edu/?SS_Page=refiner
* HTTPS is unavailable.

## Classic Franklin: https://classicfranklin.library.upenn.edu/
* HTTPS is unavailable.

## Aeon: https://aeon.library.upenn.edu/
* HTTPS is enforced by default.