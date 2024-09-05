https://www.youtube.com/watch?v=un6ZyFkqFKo&list=WL&index=127

29/07/2024 - 2h
02/08/2024 - 2h30m
03/08/2024 - 3h22m
11/08/2024 - 3h47m
13/08/2024 - 3h47m
20/08/2024 - 4h06m
23/08/2024 - 4h49m
26/08/2024 - 5h30m
30/08/2024 - 5h30m
31/08/2024 - 6h03m
01/09/2024 - 7h12m
04/09/2024 - 7h31m

linux command for build and running the built binary
go build && ./<project_name>

go mod vendor

go mod tidy - to tidy up imports

Start postgres by running:
sudo service postgresql start

The db name is rss_agg
The postgres password is password

Run the command in the sql/schema directory:
goose postgres postgres://postgres:password@localhost:5432/rss_agg up
it will run the migration

running migration multiple times is ok as it will not run the same migration multiple times

after you have defined the sql/schema and sql/queries
you can run sqlc generate at the root folder of the project where the sqlc.yaml is stored
this will generate all the go codes based on the schema provided
