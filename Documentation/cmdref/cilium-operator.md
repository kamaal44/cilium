<!-- This file was autogenerated via cilium-operator --cmdref, do not edit manually-->

## cilium-operator

Run the cilium-operator

### Synopsis

Run the cilium-operator

```
cilium-operator [flags]
```

### Options

```
      --api-server-port uint16                 Port on which the operator should serve API requests (default 9234)
      --aws-client-burst int                   Burst value allowed for the AWS client used by the AWS ENI IPAM (default 4)
      --aws-client-qps float                   Queries per second limit for the AWS client used by the AWS ENI IPAM (default 20)
      --cilium-endpoint-gc                     Enable CiliumEndpoint garbage collector (default true)
      --cilium-endpoint-gc-interval duration   GC interval for cilium endpoints (default 30m0s)
      --cluster-id int                         Unique identifier of the cluster
      --cluster-name string                    Name of the cluster (default "default")
      --cnp-node-status-gc                     Enable CiliumNetworkPolicy Status garbage collection for nodes which have been removed from the cluster (default true)
      --cnp-node-status-gc-interval duration   GC interval for nodes which have been removed from the cluster in CiliumNetworkPolicy Status (default 2m0s)
  -D, --debug                                  Enable debugging mode
      --enable-metrics                         Enable Prometheus metrics
      --eni-parallel-workers int               Maximum number of parallel workers used by ENI allocator (default 50)
  -h, --help                                   help for cilium-operator
      --identity-allocation-mode string        Method to use for identity allocation (default "kvstore")
      --identity-gc-interval duration          GC interval for security identities (default 15m0s)
      --identity-heartbeat-timeout duration    Timeout after which identity expires on lack of heartbeat (default 15m0s)
      --ipam string                            Backend to use for IPAM
      --k8s-api-server string                  Kubernetes api address server (for https use --k8s-kubeconfig-path instead)
      --k8s-client-burst int                   Burst value allowed for the K8s client
      --k8s-client-qps float32                 Queries per second limit for the K8s client
      --k8s-kubeconfig-path string             Absolute path of the kubernetes kubeconfig file
      --kvstore string                         Key-value store type
      --kvstore-opt map                        Key-value store options (default map[])
      --metrics-address string                 Address to serve Prometheus metrics (default ":6942")
      --nodes-gc-interval duration             GC interval for nodes store in the kvstore (default 2m0s)
      --synchronize-k8s-nodes                  Synchronize Kubernetes nodes to kvstore and perform CNP GC (default true)
      --synchronize-k8s-services               Synchronize Kubernetes services to kvstore (default true)
      --unmanaged-pod-watcher-interval int     Interval to check for unmanaged kube-dns pods (0 to disable) (default 15)
      --version                                Print version information
```
