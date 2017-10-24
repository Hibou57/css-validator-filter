# css-validator-filter

## IDE / text‑editor filter for the W3C CSS validator

Output filter for `org.w3c.css.css.CssValidator` from `css-validator.jar`.

Primarly to be used for IDE/text editor integration.

A sample output from the filter may be:

    Found 2 error(s)
    index.css:6: Parse error (invalid or unsupported).
    index.css:13: Property -text-decoration doesn't exist.
    Found 1 warning(s)
    index.css:465: Properties for other media might not work for usermedium.

Note if the option `--warning=-1` is passed to the validator, a count of
warnings may be printed, but no warning message. This is not an error, since
the validator still output the count of warnings when this option is given
this value.

Additionally, the exit status is set to 1 if errors were found by the
validator, since some IDE/text editor are aware of exit codes. The validator
does not set this exit code otherwise.

The filter supposes the validator output mode is text. If the output format
from the validator differs in any future version of the validator, this filter
will need to be updated.
