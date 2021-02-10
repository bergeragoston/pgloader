# What is this

This is a fork of [pgloader](https://github.com/Bonn93/pgloader) which is itself based on the original 3.6.1 of [pgloader](https://github.com/dimitri/pgloader)


## Why a fork?
I needed to migrate an SQL Server DB to Postgres but had issues with the original tool. I found that a combination of Bonn93's solution, a CCL build and [this fix](https://github.com/dimitri/pgloader/pull/1091) worked in my situation. I put it up here for myself to find later and for anyone else who might use it.


## Quick Start:
- Clone the repo and build the image using one of the dockerfiles.
`docker run -e MSSQL_USER=sa -e MSSQL_PASS=averysecurepassword -e "MSSQL_SERVER_ADDR=192.168.10.3" -e SOURCE_DB=yourdb -e PSQL_USER=pguser -e PSQL_PASS=pgpass -e "PSQL_SERVER_ADDR=192.168.10.3" -e DEST_DB=confluence pgloader-custom`
