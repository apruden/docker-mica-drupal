Docker Mica Drupal
==================

Mica Drupal client docker. Depends on the dockers:

* mysql
* mongodb
* opal
* mica

To launch the whole Mica stack:

```
# Run and link MongoDB, MySQL, Opal, Mica and Mica Drupal
make run-all
```

To seed some data in Opal and Mica:

```
# Prior to seeding, if not already done, install the opal and mical python clients
./seed/setup.sh

# Then import some data
make seed-all
```

Then connect to:

* Opal [https://localhost:8843](https://localhost:8843)
* Mica Admin [https://localhost:8845](https://localhost:8845)
* Mica Drupal [http://localhost:8888](http://localhost:8888) and [http://localhost:8888/?q=user/login](http://localhost:8888/?q=user/login) for login

All username passwords are `administrator/password`.

To shutdown the whole Mica stack:

```
# Stop and remove all docker containers
make clean-all
```

How to get the latest builds from docker repositories:

```
# Pull Opal, Mica, Mica Drupal dockers
make pull-all
```

