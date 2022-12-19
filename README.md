# Use Grafana Plugins without internet

- [Source](https://grafana.com/docs/grafana/latest/setup-grafana/installation/docker/#build-with-pre-installed-plugins)

- build image

        docker build --build-arg "GRAFANA_VERSION=latest" --build-arg "GF_INSTALL_PLUGINS=grafana-clock-panel,grafana-simple-json-datasource" -t grafana-custom -f Dockerfile .

- run on a machine without internet conncetion

        docker run -d -p 3000:3000 --name=grafana grafana-custom

- see that plugins are installed
