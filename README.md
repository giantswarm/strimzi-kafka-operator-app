[![CircleCI](https://circleci.com/gh/giantswarm/strimzi-kafka-operator-app.svg?style=shield)](https://circleci.com/gh/giantswarm/strimzi-kafka-operator-app)

# strimzi-kafka-operator-app chart

Giant Swarm offers a strimzi-kafka-operator-app as a Playground App which can be installed, tested, and played with in tenant clusters.
Here we define the strimzi-kafka-operator-app chart with its templates and default configuration.

## Warning

Deploying this application in a Giant Swarm cluster will not work if you dont pass along the RBAC and PodSecurityPolicies (PSP) needed to ensure kafka operator is able to create and manage the desired kafka cluster. Find an example [here](https://github.com/giantswarm/strimzi-kafka-operator-app/tree/master/example/cruise-control).

## Credit

* https://github.com/strimzi/strimzi-kafka-operator
