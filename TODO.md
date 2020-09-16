# UBC Config Modules - changes for Sept/2020

## Disable
- Workflows (complicates and confuses editing experience, especially with node Revisions on)

## Remove
- image_widget_crop (too situation-specific and requires too much config)
- Slideshow Paragraph (js library in use is problematic in practice, needs a rethink)

## Add
### Asset Library / Media settings
- Media Bulk Upload (adds bulk upload options)
- Media Entity File Replace (adds ability to replace file instead of renaming as _0)
- Linkit Media Library (adds Media Library button to Link wysiwyg button popup, for inserting links to docs)

### Editing tweaks / enhancements
- Focal Point (instead of Manual Crops - allows for simpler editing experience and more latitude than image_widget_crop)
- Formtips (tooltips on hover / click)
- Maxlength (set field input length with realtime status)
- Optional End Date (allows dates to be handled easier in a single field - extends daterange)
- Scheduler (provides scheduled node publication)
- Text Summary Options (exposes settings to require / always show the summary field)
- Editor Advanced Link (adds some additional options to Link wysiwyg button popup - used to add Target)
- Editor Button Link (integrate button classes in Link wysiwyg button)
- Chosen (Admin and public facing, allows selects to be searchable, themeable - does make jQuery a requirement though)

### Other
- Google Tag Manager (add by default, but leave it disabled)
- Redirect (missed this one)

## Needed
### Events
- recurring date function (eg, every wednesday during may at 6pm)
- ongoing flag (instead of a start-end date)
- Views to accomodate these with upcoming events
- Add to Calendar module (eg Allard) with config / options

### Custom blocks
- Twitter Stream embed
- Instagram embed

### Image gallery library and styles
- Vue, Tinyslider (Sauder)?

### WYSIWYG
- iFrame (ckeditor_iframe module is essentially abandoned. Do we roll our own?, Use Media type, other?)

### Sitewide alerts
- could start with Security implementation?

## Drupal 9 compatibility
### UBC Content Items
- Custom module not currently D9 compatible - 19 errors, 3 warnings
- Errors
  - Call to deprecated method entityManager()
  - Call to deprecated function format_date()
  - Call to deprecated method link()
  - Call to deprecated function drupal_set_message()
  - Call to deprecated constant REQUEST_TIME
- Warnings
  - .info version requirement
  - Class PHPUnit\Framework\TestCase not found
