# Cleveland Metroparks Local Modifications

## jQuery Upgrade

Added:

app/static/app/js/vendor/jquery-3.7.1.min.js

Updated:

app/templates/app/base.html

Updated:

jest.config.js

Reason:
BitSight finding for jQuery 1.11.2.

Validation:
- Login successful
- Dashboard loads
- Project list loads
- jQuery.fn.jquery returns 3.7.1