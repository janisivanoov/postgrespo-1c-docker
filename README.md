# Postgrespro-1c-Docker
[Postgres Pro with 1C support] (https://postgrespro.ru/products/1c) in the container [doCker] (https://www.docker.com/)

Collected for testing.

*** A serious revision is required to use the Production environment. ***

For launch, you can use Docker-Compose:
Example `doCker-compose.yml`
`` `
Version: '3.1'

Services:

  Postgres:
    Build:
      CONTEXT: https://github.com/atropichev/postgrespro-1c-docker.git
    Image: Atropichev/Postgrespro-1c-Docker: 13
    Container_name: Postgres
    Hostname: Postgres
    ENVIRONMENT:
      Postgres_password: Supersecretpassword

  Adminer:
    Image: Adminer
    Container_name: adminer
    Hostname: Adminer
    depends_on:
      - Postgres
`` `
Additional information on the topic:

[Server installation 1s 8.3.16.1063 + postgres pro 12 on Linux Debian 9.5] (http://linux-bash.ru/menusistem/120-120-120-120-120-120-120-120-120-120-120-120)