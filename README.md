- Step 1: Install Docker from your favorite package manager
- Step 2: verify that the `UpSansaardb.sql` file in `./script/` folder is correct.
- Step 3: issue the command `docker-compose up` to setup, start and bootstrap the PostgreSQL DB with the data from `scripts/UpSansaardb.sql`.
- Step 4: Install [PGCli](https://www.pgcli.com/install) and access it using the command:
`pgcli postgres://app_user:password@localhost:5432/app_db`

To clean and restart the DB, use the following command:

`docker-compose down && docker-compose rm && rm -rf pgdata/ && docker-compose up --remove-orphans`
