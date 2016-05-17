
# 'junos-rpm' role  

Create configuration for Junos devices to enable RPM

## Variables needed by the template

```yaml
rpm_probes:
  <owner-name>:                         # << Name of the owner     
    <test-name>:                        # << Name of the test
      type: <probe type>
      interval: <interval in sec>       # Optional / default = 30
      count: <<probe type>              # Optional / default = 3
      target_url: <probe url>
      target_address: <probe address>
```

### Example

**For Device 'xxxx'**
```yaml
# host_vars/xxxx/ssdfdf


```
