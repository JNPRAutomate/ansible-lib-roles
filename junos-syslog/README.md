
# 'junos-syslog' role  

Create configuration for Junos devices to create new syslog file or remote host

### Supported Sensors

- phy-interface: /junos/system/linecard/interface/


## Variables needed by the template

```yaml


junos_syslog:
    172.29.106.53:
        port: 6000
        match: COMMIT
        any: any
```

### Example

**For Device 'xxxx'**
```yaml
# host_vars/xxxx/ssdfdf

```
