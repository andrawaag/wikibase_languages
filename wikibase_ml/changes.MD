## Changing docker-compose.yml
The ```docker-compose.yml``` is an adaptation of the orginal docker file from the [Wikibase docker github repo](https://github.com/wmde/wikibase-docker). The following adaptions have been made

### The ports were changed to 7171. 

```
- "7171:80"
```
This is an arbitrary choice, and be left untouched or another number can be given. I changed it to 7171 to prevent conflicts with other wikibases running on the same machine


### A volume pointing to LocalSettting.php.template was created

```
    volumes:
      - mediawiki-images-data:/var/www/html/images
      - ./LocalSettings.php.template:/LocalSettings.php.template
      - quickstatements-data:/quickstatements/data
```

## Edit LocalSettting.php.template
### Change the language code to "ml"
```
${DOLLAR}wgShellLocale = "ml_ML.utf8";
${DOLLAR}wgLanguageCode = "ml";
```

### Add the location of the Malayalam Wikibase logo (To be designed)
```
${DOLLAR}wgLogo = '';
```