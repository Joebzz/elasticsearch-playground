# Installing the Earthquake Example Data

Steps are copied from -> https://github.com/elastic/examples/tree/master/Exploring%20Public%20Datasets/earthquakes

Replacing the <password> with the password generated when runnin docker-compose setup.

`
curl --user elastic:<password> -XPUT -H "Content-Type: application/json" -k "https://localhost:9200/_ingest/pipeline/ncedc-earthquakes" -d @ncedc-earthquakes-pipeline.json
`

`
curl --user elastic:<password> -XPUT -H "Content-Type: application/json" -k "https://localhost:9200/_ingest/pipeline/ncedc-earthquakes" -d @ncedc-earthquakes-pipeline.json
`

`
docker-compose exec filebeat filebeat -e -c ./example_data/earthquake/ncedc-earthquakes-filebeat.yml
`
