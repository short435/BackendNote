# Logstash

Logstash is a sever side data collection tool. It was a part of the ELS which call Elastic Stack, including Elastic search, Kibana, Logstash.

## Objective

Logstash is a useful tool and with lots of the plungin tools. It's make the data collection become easier. Also there are amounts of the template mapping with the most used tools. Such as the Proxy service(Nginx, Apache)

## Example for configuration files

```json

input {
  file {
    path => "/your_file_path"
    start_position => "beginning"
  }
}

filter {
  if [path] =~ "access" {
    mutate { add_field => { "log_type" => "apache_access" } }
    grok {
      match => { "message" => "%{COMBINEDAPACHELOG}" }
    }
  }
  date {
    match => [ "timestamp" , "dd/MMM/yyyy:HH:mm:ss Z" ]
  }
}

output {
  elasticsearch {
    hosts => ["localhost:9200"]
    index => "apache_log"
  }
  stdout { codec => rubydebug }
}


```

## Operations

### start_position

**Options**
- beginning: Logstash reads the file from the start, useful for processing all existing logs on first-time setups.
- end: Logstash starts reading from the end of the file, ideal for ongoing monitoring where only new log entries are relevant.


==Configuration Example==
```
input {
  file {
    path => "/path/to/log/file"
    start_position => "beginning"
  }
}
```

**Key Points**
First Run: On its initial run, Logstash reads the file according to the start_position value.
Subsequent Runs: On restarts, Logstash continues from the last position recorded, regardless of the start_position setting, unless the sincedb file is reset or changed.
File Rotation Handling: Use wildcard patterns to manage log file rotations effectively, ensuring continuous log monitoring without data loss.

## General use cases


## Reference

- [Logstash Github](https://github.com/elastic/logstash)
- [Offical examples for config file](https://www.elastic.co/guide/en/logstash/current/config-examples.html)