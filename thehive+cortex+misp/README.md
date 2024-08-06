This directory contains a docker-compose file which you can use to run TheHive, Cortex and Misp.

In order to run this file, It is recommended that you use a machine with a minimum of 16GB of RAM and 4vCPUs

To run it you'll first need to set the ip address field in the file to the your local machine's ip address

```yaml
      - "HOSTNAME=https://<server-ip-address>"
```

Then save it and type this command in your terminal

```bash
docker-compose up
```