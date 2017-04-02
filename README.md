# Concourse Pipeline for Calico

## Worker Nodes

Use the Vagrantfile to create local worker node at `192.168.100.4:8080`.

## Install `fly`

Download the fly binary by vising your instance web page: http://192.168.100.4:8080/

## Login

```
fly -t calico login -c http://192.168.100.4:8080
```

## Run the Traaaack

```
fly -t calico set-pipeline -p calico -c calico-pipeline.yml
```

## Unpause the Pipeline

```
fly -t calico unpause-pipeline -p calico
```

## Delete the Traaaack

```
fly -t calico destroy-pipeline -p calico
```
