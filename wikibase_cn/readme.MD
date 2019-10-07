### Requirements
* [docker](https://www.docker.com/)
* [docker-compose](https://docs.docker.com/compose/install/)

### Get the files
For Wikibase to start with Chinese settings the following files need to downloaded.
* Choose or create a directory to store the following two files:
* [LocalSettings.php.template](https://raw.githubusercontent.com/andrawaag/wikibase_languages/master/wikibase_cn/LocalSettings.php.template)
* [docker-compose.yml](https://raw.githubusercontent.com/andrawaag/wikibase_languages/master/wikibase_cn/docker-compose.yml)
[changes made](./changes.MD)

### Run docker-compose
```
docker-compose up
```
Depending on the OS you might need to use sudo
```
sudo docker-compose up
```