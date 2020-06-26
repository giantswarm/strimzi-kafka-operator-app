# Cruise Control example

1. Create a tenant cluster

```bash
gsctl create cluster -f testcluster.yaml
```
1. Deploy strimzi-kafka-operator-app from the playground catalog (see `strimzi-kafka-operator-app.yaml`)

1. Request a Kafka cluster

```bash
kubectl apply -f my-cluster/
```

1. Request Cruise Control to rebalance the cluster

```bash
kubectl apply -f kafka-rebalance.yaml
```

1. Observe rebalance request status transition until ProposalReady

```bash
kubeclt describe kafkarebalances -n kafka my-rebalance
```

1. If request is stale, one can request refresh with

```bash
kubectl annotate kafkarebalance my-rebalance strimzi.io/rebalance=refresh -n kafka
```

1. Once happy with the rebalance proposal, one can approve it with

```bash
kubectl annotate kafkarebalance my-rebalance strimzi.io/rebalance=approve -n kafka
```
