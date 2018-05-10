Where can I find the version of ThoughtSpot I am using?

### I'm not seeing certain columns/values in the drop-down, why?
It could be a few things
Index has not built with the latest data, or something is causing it to be dropped. Look at the varz page to see if the column is there and if its index_type not DONT_INDEX.
It could be a ranking issue. Check index priority for the column on sage varz page.

### How do I track progress of current index build?
Other than tailing info logs, there is nothing much we can do rightnow. We will add add something to the varz page about number of columns processed vs total number of columns.

### How do I display the features used in my cluster configuration?

1. Log into the ThoughtSpot cluster as the `admin` user.
2. Use the `tscli feature` subcommand to display your current configuration.

    ```
    $ tscli feature get-all-config
    +---------------------------------+----------+---------------+
    |              NAME               |  STATUS  | CONFIGURATION |
    +---------------------------------+----------+---------------+
    | Firewall                        | Disabled |               |
    | Saml                            | Disabled |               |
    | Ldap                            | Disabled |               |
    | CustomBranding                  | Disabled |               |
    | CustomBrandingFontCustomization | Disabled |               |
    | DataConnect                     | Disabled |               |
    | RLS                             | Enabled  |               |
    | Callhome                        | Enabled  |               |
    | SSHTunnel                       | Enabled  |               |
    | Fileserver                      | Disabled |               |
    +---------------------------------+----------+---------------+
    ```