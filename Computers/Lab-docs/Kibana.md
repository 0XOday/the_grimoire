```
sudo /usr/share/elasticsearch/bin/elasticsearch-create-enrollment-token -s kibana
eyJ2ZXIiOiI4LjE0LjAiLCJhZHIiOlsiMTkyLjE2OC4xMjkuMjE0OjkyMDAiXSwiZmdyIjoiNzFkNDI0YjBhNWJmN2E0MDQyMDY0YjhlN2M4ZWE4YTBkOWJiNGJkMjdjYmQ3YzU0ZDFmZGQ4OTk5YTRkMjlhMSIsImtleSI6ImVnQ1JySllCMHQyRnlzbmE2M3BZOnl1eGd4bW94SEdCOXFsRnpFazNJWVEifQ==
```

931450

## [Directory layout of RPM](https://www.elastic.co/docs/deploy-manage/deploy/self-managed/install-kibana-with-rpm#rpm-layout)

The RPM places config files, logs, and the data directory in the appropriate locations for an RPM-based system:

|Type|Description|Default Location|Setting|
|---|---|---|---|
|home|Kibana home directory or `$KIBANA_HOME`|`/usr/share/kibana`||
|bin|Binary scripts including `kibana` to start the Kibana server and `kibana-plugin` to install plugins|`/usr/share/kibana/bin`||
|config|Configuration files including `kibana.yml`|`/etc/kibana`|`[KBN_PATH_CONF](configure-kibana.md)`|
|data|The location of the data files written to disk by Kibana and its plugins|`/var/lib/kibana`|`path.data`|
|logs|Logs files location|`/var/log/kibana`|`[Logging configuration](../../monitor/logging-configuration/kibana-logging.md)`|
|plugins|Plugin files location. Each plugin will be contained in a subdirectory.|`/usr/share/kibana/plugins`||