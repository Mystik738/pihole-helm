# pihole-helm


*BETA*

This defaults  the upstraem DNS for 8.8.8.8 and 10.0.0.1 (k8s)

## Values

```
image:
  pullPolicy: IfNotPresent
```
Storage options 
```
persistence:
  ## persistence.enabled Enables persistent volume - PV provisioner support necessary
  enabled: true
  ## persistence.keep Keep persistent volume after helm delete
  keep: false
  ## persistence.accessMode PVC Access Mode
  accessMode: ReadWriteMany
  ## persistence.size PVC Size
  size: 5Gi
```
Additional dns entries
```
configData: |-
  server=/local/192.168.1.1
  address=/.cminion.cf/192.168.1.132
```
Web Interface host for ingrss
```
ingress:
  host: dns.cminion.cf 

```
