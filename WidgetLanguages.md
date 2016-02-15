# Introduction #

When deploying the NPS question in foreign languages, it is very important to get a consistent translation. This sections outlines how to configure the widget to appear in languages other than English.


# Widget Language Parameter #

To use a language, the corresponding language code must be specified as part of the nps\_language parameter in the script tag, eg:

```
<script type="text/javascript">
   nps_project_id = 24;
   nps_project_name = "Share Online 4.3b";
   nps_language="en";
</script>
```

The language specified must first exist on the server as a language configuration file.


# Widget Language Server Configuration #

Location of the language file on the server is : /var/www/html/nps\_widget/l10n/lang

A new language file must be created before it can be called in the script tag, e.g. lang_.ini (file name shoud be same like lang\_en.ini)._

A sample language file will be added to the downloads.