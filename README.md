[![CircleCI](https://circleci.com/gh/giantswarm/strimzi-kafka-operator-app.svg?style=shield)](https://circleci.com/gh/giantswarm/strimzi-kafka-operator-app)

# strimzi-kafka-operator-app chart

Giant Swarm offers a strimzi-kafka-operator-app as a Playground App which can be installed, tested, and played with in tenant clusters.
Here we define the strimzi-kafka-operator-app chart with its templates and default configuration.

## Warning

Once strizmi-kafka-operator-app has been deployed, to get desired Apache Kafka and ZooKeeper cluster up and running, in Giant Swarm tenant clusters besides Strimzi's Kafka custom resource (CR) one has to pass along necessary RBAC and PodSecurityPolicy (PSP) resources. You can find an example of Kafka CR and accompanying resources [here](https://github.com/giantswarm/strimzi-kafka-operator-app/tree/master/example/cruise-control/my-cluster).

## Credit

* https://github.com/strimzi/strimzi-kafka-operator
