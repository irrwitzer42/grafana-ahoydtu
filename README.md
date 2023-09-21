# grafana-ahoydtu

- Grafana dashboard to use with
	- ahoyDTU (https://ahoydtu.de)
	- prometheus-enabled build (can be found here: https://github.com/lumapu/ahoy/releases in latest zip file, e.g. xxxxxx_ahoy_0.7.zz_yyyyyy_esp32_prometheus.bin)
	- running prometheus as data source

- example prometheus job:
```
  - job_name: 'ahoydtu'
    scrape_interval: 30s
    static_configs:
      - targets:
        - 192.168.23.42			# asuming that's the IP of ahoyDTU
        labels:
          site: garage			# to identify different locations
```

- Screenshots:
  - ![Screenshot of overview](images/screenshot01.png?raw=true "Overview")
  - ![Screenshot of DC, AC and Radio statistics](images/screenshot02.png?raw=true "DC & AC & Radio stats")