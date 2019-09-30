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
### Change the language code to "ja"
```
${DOLLAR}wgShellLocale = "ja_JA.utf8";
${DOLLAR}wgLanguageCode = "ja";
```

### Add the location of the Japanese Wikibase logo
```
${DOLLAR}wgLogo = 'https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Wikibase_logo_Japanese.png/200px-Wikibase_logo_Japanese.png';
```