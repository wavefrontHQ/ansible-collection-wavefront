# wavefront_proxy

Role to install and configure the VMware Wavefront Proxy

## Requirements

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

## Role Variables

| Variable                    | Default                                        | Description                            |
| --------------------------- | ---------------------------------------------- | -------------------------------------- |
| wavefront_api_endpoint      | https://vmwareprod.wavefront.com/api/          | Wavefront API Endpoint                 |
| wavefront_api_token         |                                                | Wavefront Authentication Token         |
| wavefront_proxy_port        | 2878                                           | Ports used to listen to Wavefront data |
| wavefront_proxy_repo_url    | https://packagecloud.io/wavefront/proxy        |                                        |
| wavefront_proxy_repo_gpgkey | https://packagecloud.io/wavefront/proxy/gpgkey |                                        |
| wavefront_proxy_package     | wavefront-proxy                                | Package name, can include version      |

### Advanced Vars

_Note:_ These vars are not required for installation or configuration of Wavefront Proxy

| Variable                                                         | Default | Description                                                                                       |
| ---------------------------------------------------------------- | ------- | ------------------------------------------------------------------------------------------------- |
| wavefront_proxy_push_listener_max_received_length                |         |                                                                                                   |
| wavefront_proxy_push_listener_http_buffer_size                   |         |                                                                                                   |
| wavefront_proxy_delta_counters_aggregation_listener_ports        |         |                                                                                                   |
| wavefront_proxy_delta_counters_aggregation_interval_seconds      |         |                                                                                                   |
| wavefront_proxy_graphite_ports                                   |         |                                                                                                   |
| wavefront_proxy_pickle_ports                                     |         |                                                                                                   |
| wavefront_proxy_graphite_format                                  |         |                                                                                                   |
| wavefront_proxy_graphite_delimiters                              |         |                                                                                                   |
| wavefront_proxy_graphite_fields_to_remove                        |         |                                                                                                   |
| wavefront_proxy_push_relay_listener_ports                        |         |                                                                                                   |
| wavefront_proxy_push_relay_histogram_aggregator                  |         |                                                                                                   |
| wavefront_proxy_opentsdb_ports                                   |         |                                                                                                   |
| wavefront_proxy_json_listener_ports                              |         |                                                                                                   |
| wavefront_proxy_write_http_json_listener_ports                   |         |                                                                                                   |
| wavefront_proxy_preprocessor_config_file                         |         |                                                                                                   |
| wavefront_proxy_custom_source_tags                               |         |                                                                                                   |
| wavefront_proxy_prefix                                           |         |                                                                                                   |
| wavefront_proxy_allow                                            |         |                                                                                                   |
| wavefront_proxy_block                                            |         |                                                                                                   |
| wavefront_proxy_data_backfill_cutoff_hours                       |         |                                                                                                   |
| wavefront_proxy_data_prefill_cutoff_hours                        |         |                                                                                                   |
| wavefront_proxy_flush_threads                                    |         | Number of threads that flush data to the server.                                                  |
| wavefront_proxy_push_flush_max_points                            |         | Max points per single flush. Default: 40000.                                                      |
| wavefront_proxy_push_flush_max_histograms                        |         | Max histograms per single flush. Default: 10000.                                                  |
| wavefront_proxy_push_flush_max_spans                             |         | Max spans per single flush. Default: 5000                                                         |
| wavefront_proxy_push_flush_max_span_logs                         |         | Max span logs per single flush. Default: 1000.                                                    |
| wavefront_proxy_push_flush_interval                              |         | Milliseconds between flushes to the Wavefront servers. Typically 1000.                            |
| wavefront_proxy_push_rate_limit                                  |         | Limit outbound points per second rate at the proxy. Default: do not throttle                      |
| wavefront_proxy_push_rate_limit_histograms                       |         | Limit outbound histograms per second rate at the proxy. Default: do not throttle                  |
| wavefront_proxy_push_rate_limit_spans                            |         |                                                                                                   |
| wavefront_proxy_push_rate_limit_span_logs                        |         |                                                                                                   |
| wavefront_proxy_push_rate_limit_max_burst_seconds                |         |                                                                                                   |
| wavefront_proxy_buffer                                           |         |                                                                                                   |
| wavefront_proxy_buffer_shard_size                                |         |                                                                                                   |
| wavefront_proxy_disable_buffer_sharding                          |         |                                                                                                   |
| wavefront_proxy_retry_backoff_base_seconds                       |         |                                                                                                   |
| wavefront_proxy_split_push_when_rate_limited                     |         |                                                                                                   |
| wavefront_proxy_proxy_host                                       |         |                                                                                                   |
| wavefront_proxy_proxy_port                                       |         |                                                                                                   |
| wavefront_proxy_proxy_user                                       |         |                                                                                                   |
| wavefront_proxy_proxy_password                                   |         |                                                                                                   |
| wavefront_proxy_http_user_agent                                  |         |                                                                                                   |
| wavefront_proxy_gzip_compression                                 |         |                                                                                                   |
| wavefront_proxy_gzip_compression_level                           |         |                                                                                                   |
| wavefront_proxy_http_connect_timeout                             |         |                                                                                                   |
| wavefront_proxy_http_request_timeout                             |         |                                                                                                   |
| wavefront_proxy_http_max_conn_total                              |         |                                                                                                   |
| wavefront_proxy_http_max_conn_per_route                          |         |                                                                                                   |
| wavefront_proxy_http_auto_retries                                |         |                                                                                                   |
| wavefront_proxy_listener_idle_connection_timeout                 |         |                                                                                                   |
| wavefront_proxy_disable_rdns_lookup                              |         |                                                                                                   |
| wavefront_proxy_so_linger_time                                   |         |                                                                                                   |
| wavefront_proxy_push_memory_buffer_limit                         |         |                                                                                                   |
| wavefront_proxy_push_blocked_samples                             |         |                                                                                                   |
| wavefront_proxy_blocked_points_logger_name                       |         |                                                                                                   |
| wavefront_proxy_blocked_histograms_logger_name                   |         |                                                                                                   |
| wavefront_proxy_blocked_spans_logger_name                        |         |                                                                                                   |
| wavefront_proxy_use_noop_sender                                  |         |                                                                                                   |
| wavefront_proxy_auth_method                                      |         |                                                                                                   |
| wavefront_proxy_auth_token_introspection_service_url             |         |                                                                                                   |
| wavefront_proxy_auth_token_introspection_authorization_header    |         |                                                                                                   |
| wavefront_proxy_auth_response_refresh_interval                   |         |                                                                                                   |
| wavefront_proxy_auth_response_max_ttl                            |         |                                                                                                   |
| wavefront_proxy_auth_static_token                                |         |                                                                                                   |
| wavefront_proxy_traffic_shaping                                  |         | Enables intelligent traffic shaping based on received rate over last 5 minutes. Default: disabled |
| wavefront_proxy_traffic_shaping_window_seconds                   |         | Sets the width (in seconds) for the sliding time window                                           |
| wavefront_proxy_traffic_shaping_headroom                         |         | Sets the headroom multiplier to use for traffic shaping when there's backlog. Default: 1.15       |
| wavefront_proxy_cors_enabled_ports                               |         | Enables CORS for specified comma-delimited list of listening ports. Default: none                 |
| wavefront_proxy_cors_origin                                      |         | Allowed origin for CORS requests, or '\*' to allow everything. Default: none                      |
| wavefront_proxy_cors_allow_null_origin                           |         | Allow 'null' origin for CORS requests. Default: false                                             |
| wavefront_proxy_tls_ports                                        |         | Enables TLS for specified listening ports (comma-separated list)                                  |
| wavefront_proxy_private_cert_path                                |         |                                                                                                   |
| wavefront_proxy_private_key_path                                 |         |                                                                                                   |
| wavefront_proxy_http_health_check_ports                          |         |                                                                                                   |
| wavefront_proxy_http_health_check_all_ports                      |         |                                                                                                   |
| wavefront_proxy_http_health_check_path                           |         |                                                                                                   |
| wavefront_proxy_http_health_check_response_content_type          |         |                                                                                                   |
| wavefront_proxy_http_health_check_pass_status_code               |         |                                                                                                   |
| wavefront_proxy_http_health_check_pass_response_body             |         |                                                                                                   |
| wavefront_proxy_http_health_check_fail_status_code               |         |                                                                                                   |
| wavefront_proxy_http_health_check_fail_response_body             |         |                                                                                                   |
| wavefront_proxy_admin_api_listener_port                          |         |                                                                                                   |
| wavefront_proxy_admin_api_remote_ip_allow_regex                  |         |                                                                                                   |
| wavefront_proxy_filebeat_port                                    |         |                                                                                                   |
| wavefront_proxy_raw_logs_port                                    |         |                                                                                                   |
| wavefront_proxy_raw_logs_max_received_length                     |         |                                                                                                   |
| wavefront_proxy_raw_logs_http_buffer_size                        |         |                                                                                                   |
| wavefront_proxy_logs_ingestion_config_file                       |         |                                                                                                   |
| wavefront_proxy_trace_listener_ports                             |         |                                                                                                   |
| wavefront_proxy_trace_listener_max_received_length               |         |                                                                                                   |
| wavefront_proxy_trace_listener_http_buffer_size                  |         |                                                                                                   |
| wavefront_proxy_custom_tracing_listener_ports                    |         |                                                                                                   |
| wavefront_proxy_custom_tracing_application_name                  |         |                                                                                                   |
| wavefront_proxy_custom_tracing_service_name                      |         |                                                                                                   |
| wavefront_proxy_trace_jaeger_listener_ports                      |         |                                                                                                   |
| wavefront_proxy_trace_jaeger_http_listener_ports                 |         |                                                                                                   |
| wavefront_proxy_trace_jaeger_grpc_listener_ports                 |         |                                                                                                   |
| wavefront_proxy_trace_jaeger_application_name                    |         |                                                                                                   |
| wavefront_proxy_trace_zipkin_listener_ports                      |         |                                                                                                   |
| wavefront_proxy_trace_zipkin_application_name                    |         |                                                                                                   |
| wavefront_proxy_trace_derived_custom_tag_keys                    |         |                                                                                                   |
| wavefront_proxy_trace_sampling_rate                              |         |                                                                                                   |
| wavefront_proxy_trace_sampling_duration                          |         |                                                                                                   |
| wavefront_proxy_histogram_state_directory                        |         |                                                                                                   |
| wavefront_proxy_histogram_accumulator_resolve_interval           |         |                                                                                                   |
| wavefront_proxy_histogram_accumulator_flush_interval             |         |                                                                                                   |
| wavefront_proxy_histogram_accumulator_flush_max_batch_size       |         |                                                                                                   |
| wavefront_proxy_histogram_max_received_length                    |         |                                                                                                   |
| wavefront_proxy_histogram_http_buffer_size                       |         |                                                                                                   |
| wavefront_proxy_histogram_minute_listener_ports                  |         |                                                                                                   |
| wavefront_proxy_histogram_minute_flush_secs                      |         |                                                                                                   |
| wavefront_proxy_histogram_minute_compression                     |         |                                                                                                   |
| wavefront_proxy_histogram_minute_accumulator_size                |         |                                                                                                   |
| wavefront_proxy_histogram_minute_memory_cache                    |         |                                                                                                   |
| wavefront_proxy_histogram_minute_accumulator_persisted           |         |                                                                                                   |
| wavefront_proxy_histogram_hour_listener_ports                    |         |                                                                                                   |
| wavefront_proxy_histogram_hour_flush_secs                        |         |                                                                                                   |
| wavefront_proxy_histogram_hour_compression                       |         |                                                                                                   |
| wavefront_proxy_histogram_hour_accumulator_size                  |         |                                                                                                   |
| wavefront_proxy_histogram_hour_memory_cache                      |         |                                                                                                   |
| wavefront_proxy_histogram_hour_accumulator_persisted             |         |                                                                                                   |
| wavefront_proxy_histogram_day_listener_ports                     |         |                                                                                                   |
| wavefront_proxy_histogram_day_flush_secs                         |         |                                                                                                   |
| wavefront_proxy_histogram_day_compression                        |         |                                                                                                   |
| wavefront_proxy_histogram_day_accumulator_size                   |         |                                                                                                   |
| wavefront_proxy_histogram_day_memory_cache                       |         |                                                                                                   |
| wavefront_proxy_histogram_day_accumulator_persisted              |         |                                                                                                   |
| wavefront_proxy_histogram_dist_listener_ports                    |         |                                                                                                   |
| wavefront_proxy_histogram_dist_flush_secs                        |         |                                                                                                   |
| wavefront_proxy_histogram_dist_compression                       |         |                                                                                                   |
| wavefront_proxy_histogram_dist_accumulator_size                  |         |                                                                                                   |
| wavefront_proxy_histogram_dist_memory_cache                      |         |                                                                                                   |
| wavefront_proxy_histogram_dist_accumulator_persisted             |         |                                                                                                   |
| wavefront_proxy_push_relay_histogram_aggregator_flush_secs       |         |                                                                                                   |
| wavefront_proxy_push_relay_histogram_aggregator_compression      |         |                                                                                                   |
| wavefront_proxy_push_relay_histogram_aggregator_accumulator_size |         |                                                                                                   |

## Dependencies

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

## License

BSD

## Author Information

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
