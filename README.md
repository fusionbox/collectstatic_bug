# Demonstration of a bug in Django manage.py collectstatic

## Steps to reproduce:
* Run `python manage.py collectstatic` with `app_one` and `app_two` installed.
* See that `static/example.txt` is the one from `app_one`.
* Remove `app_one` from installed apps.
* Re-run `python manage.py collectstatic`.

## Expected Behavior:
`static/example.txt` should be the version from `app_two`.

## Observed Behavior:
`static/example.txt` is still the version from `app_one`, which is no longer installed.
