# Introduce

This project is used to show the way which build a ethnode for stat site
by docker.

[docker](https://docs.docker.com/engine/installation/) and [compose](https://docs.docker.com/compose/install/) must have been installed.

# usage

* start up

```bash
# cp docker-compose-sample.yml docker-compose.yml
# <Customize on docker-compose.yml: >
# <    set values of `instance` and `contact_details` environments>
# <    change volume for your REAL folder>
# docker-compose up -d
```

* upgrade/downgrade

```bash
# < edit image version on docker-compose.yml >
# docker-compose down
# docker-compose up -d
```

