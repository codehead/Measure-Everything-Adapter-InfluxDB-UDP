# NAME

Measure::Everything::Adapter::InfluxDB::UDP - A Measure::Everything adapter to feed InfluxDB through UDP.

# VERSION

version 0.01

# SYNOPSIS

    Measure::Everything::Adapter->set( 'InfluxDB::UDP', 
      host => '127.0.0.1', 
      port => 8089
    );

# DESCRIPTION

Reporting metrics over UDP is ideal in real-time environments where
performance is preferred over reliability. This adapter allows you to write
stats to an
[InfluxDB UDP listener](https://docs.influxdata.com/influxdb/v0.10/write_protocols/udp/).

By definition, delivery of UDP packets is not guaranteed, and the presence of
the InfluxDB listener is not verified at all. It is your responsability to
configure the listener properly and to provide a persistent, reliable and
secure "line of sight" to an UDP listener. Your stats will be discarded
silently otherwise.

# SEE ALSO

- [Measure::Everything](https://metacpan.org/pod/Measure::Everything), of course
- [https://docs.influxdata.com/influxdb/v0.10/write\_protocols/udp/](https://docs.influxdata.com/influxdb/v0.10/write_protocols/udp/) Configure InfluxDB to support writes over UDP.

# AUTHOR

Javier Arturo Rodriguez <javier@rodriguez.org.mx>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2016 by Javier Arturo Rodriguez.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
