# Setting Up MongoDB

## Process to Follow installation on K8s

In Master Node :


    sudo mkdir /mnt/data
    kubectl label nodes controlplane size=large
    kubectl apply -k .
    kubectl get pod
    kubectl exec -it mongodb-test-0 -- sh
    mongo
    use test
    db.auth('test','password#@12')


### Checkov Logs 

checkov -d . --framework kubernetes
[ kubernetes framework ]: 100%|████████████████████|[8/8], Current File Scanned=Secret.yaml               

       _               _              
   ___| |__   ___  ___| | _______   __
  / __| '_ \ / _ \/ __| |/ / _ \ \ / /
 | (__| | | |  __/ (__|   < (_) \ V / 
  \___|_| |_|\___|\___|_|\_\___/ \_/  
                                      
By Prisma Cloud | version: 3.2.106 

kubernetes scan results:

Passed checks: 68, Failed checks: 23, Skipped checks: 0

Check: CKV_K8S_68: "Ensure that the --anonymous-auth argument is set to false"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-anonymous-auth-argument-is-set-to-false-1
Check: CKV_K8S_148: "Ensure that the --tls-cert-file and --tls-private-key-file arguments are set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-tls-cert-file-and-tls-private-key-file-arguments-are-set-as-appropriate-for-kubelet
Check: CKV_K8S_96: "Ensure that the --service-account-lookup argument is set to true"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-service-account-lookup-argument-is-set-to-true
Check: CKV_K8S_138: "Ensure that the --anonymous-auth argument is set to false"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-anonymous-auth-argument-is-set-to-false
Check: CKV_K8S_105: "Ensure that the API Server only makes use of Strong Cryptographic Ciphers"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-api-server-only-makes-use-of-strong-cryptographic-ciphers
Check: CKV_K8S_151: "Ensure that the Kubelet only makes use of Strong Cryptographic Ciphers"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-kubelet-only-makes-use-of-strong-cryptographic-ciphers
Check: CKV_K8S_145: "Ensure that the --make-iptables-util-chains argument is set to true"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-make-iptables-util-chains-argument-is-set-to-true
Check: CKV_K8S_114: "Ensure that the --profiling argument is set to false"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-profiling-argument-is-set-to-false-1
Check: CKV_K8S_111: "Ensure that the --root-ca-file argument is set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-root-ca-file-argument-is-set-as-appropriate
Check: CKV_K8S_71: "Ensure that the --kubelet-https argument is set to true"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-kubelet-https-argument-is-set-to-true
Check: CKV_K8S_115: "Ensure that the --bind-address argument is set to 127.0.0.1"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-bind-address-argument-is-set-to-127001-1
Check: CKV_K8S_94: "Ensure that the --audit-log-maxsize argument is set to 100 or as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-audit-log-maxsize-argument-is-set-to-100-or-as-appropriate
Check: CKV_K8S_73: "Ensure that the --kubelet-certificate-authority argument is set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-kubelet-certificate-authority-argument-is-set-as-appropriate
Check: CKV_K8S_74: "Ensure that the --authorization-mode argument is not set to AlwaysAllow"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-authorization-mode-argument-is-not-set-to-alwaysallow-1
Check: CKV_K8S_16: "Container should not be privileged"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-15
Check: CKV_K8S_72: "Ensure that the --kubelet-client-certificate and --kubelet-client-key arguments are set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-kubelet-client-certificate-and-kubelet-client-key-arguments-are-set-as-appropriate
Check: CKV_K8S_80: "Ensure that the admission control plugin AlwaysPullImages is set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-admission-control-plugin-alwayspullimages-is-set
Check: CKV_K8S_110: "Ensure that the --service-account-private-key-file argument is set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-service-account-private-key-file-argument-is-set-as-appropriate
Check: CKV_K8S_100: "Ensure that the --tls-cert-file and --tls-private-key-file arguments are set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-tls-cert-file-and-tls-private-key-file-arguments-are-set-as-appropriate
Check: CKV_K8S_141: "Ensure that the --read-only-port argument is set to 0"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-read-only-port-argument-is-set-to-0
Check: CKV_K8S_146: "Ensure that the --hostname-override argument is not set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-hostname-override-argument-is-not-set
Check: CKV_K8S_93: "Ensure that the --audit-log-maxbackup argument is set to 10 or as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-audit-log-maxbackup-argument-is-set-to-10-or-as-appropriate
Check: CKV_K8S_90: "Ensure that the --profiling argument is set to false"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-profiling-argument-is-set-to-false-2
Check: CKV_K8S_88: "Ensure that the --insecure-port argument is set to 0"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-insecure-port-argument-is-set-to-0
Check: CKV_K8S_27: "Do not expose the docker daemon socket to containers"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-26
Check: CKV_K8S_139: "Ensure that the --authorization-mode argument is not set to AlwaysAllow"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-authorization-mode-argument-is-not-set-to-alwaysallow
Check: CKV_K8S_18: "Containers should not share the host IPC namespace"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-17
Check: CKV_K8S_34: "Ensure that Tiller (Helm v2) is not deployed"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-32
Check: CKV_K8S_86: "Ensure that the --insecure-bind-address argument is not set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-insecure-bind-address-argument-is-not-set
Check: CKV_K8S_118: "Ensure that the --auto-tls argument is not set to true"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-auto-tls-argument-is-not-set-to-true
Check: CKV_K8S_85: "Ensure that the admission control plugin NodeRestriction is set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-admission-control-plugin-noderestriction-is-set
Check: CKV_K8S_108: "Ensure that the --use-service-account-credentials argument is set to true"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-use-service-account-credentials-argument-is-set-to-true
Check: CKV_K8S_97: "Ensure that the --service-account-key-file argument is set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-service-account-key-file-argument-is-set-as-appropriate
Check: CKV_K8S_25: "Minimize the admission of containers with added capability"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-24
Check: CKV_K8S_104: "Ensure that encryption providers are appropriately configured"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-etcd-cafile-argument-is-set-as-appropriate
Check: CKV_K8S_19: "Containers should not share the host network namespace"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-18
Check: CKV_K8S_83: "Ensure that the admission control plugin NamespaceLifecycle is set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-admission-control-plugin-namespacelifecycle-is-set
Check: CKV_K8S_144: "Ensure that the --protect-kernel-defaults argument is set to true"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-protect-kernel-defaults-argument-is-set-to-true
Check: CKV_K8S_75: "Ensure that the --authorization-mode argument includes Node"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-authorization-mode-argument-includes-node
Check: CKV_K8S_102: "Ensure that the --etcd-cafile argument is set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-etcd-cafile-argument-is-set-as-appropriate-1
Check: CKV_K8S_116: "Ensure that the --cert-file and --key-file arguments are set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-cert-file-and-key-file-arguments-are-set-as-appropriate
Check: CKV_K8S_107: "Ensure that the --profiling argument is set to false"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-profiling-argument-is-set-to-false
Check: CKV_K8S_149: "Ensure that the --rotate-certificates argument is not set to false"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-rotate-certificates-argument-is-not-set-to-false
Check: CKV_K8S_14: "Image Tag should be fixed - not latest or blank"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-13
Check: CKV_K8S_33: "Ensure the Kubernetes dashboard is not deployed"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-31
Check: CKV_K8S_119: "Ensure that the --peer-cert-file and --peer-key-file arguments are set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-peer-cert-file-and-peer-key-file-arguments-are-set-as-appropriate
Check: CKV_K8S_77: "Ensure that the --authorization-mode argument includes RBAC"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-authorization-mode-argument-includes-rbac
Check: CKV_K8S_84: "Ensure that the admission control plugin PodSecurityPolicy is set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-admission-control-plugin-podsecuritypolicy-is-set
Check: CKV_K8S_99: "Ensure that the --etcd-certfile and --etcd-keyfile arguments are set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-etcd-certfile-and-etcd-keyfile-arguments-are-set-as-appropriate
Check: CKV_K8S_69: "Ensure that the --basic-auth-file argument is not set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-basic-auth-file-argument-is-not-set
Check: CKV_K8S_112: "Ensure that the RotateKubeletServerCertificate argument is set to true"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-rotatekubeletservercertificate-argument-is-set-to-true-for-controller-manager
Check: CKV_K8S_17: "Containers should not share the host process ID namespace"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-16
Check: CKV_K8S_113: "Ensure that the --bind-address argument is set to 127.0.0.1"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-bind-address-argument-is-set-to-127001
Check: CKV_K8S_81: "Ensure that the admission control plugin SecurityContextDeny is set if PodSecurityPolicy is not used"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-admission-control-plugin-securitycontextdeny-is-set-if-podsecuritypolicy-is-not-used
Check: CKV_K8S_92: "Ensure that the --audit-log-maxage argument is set to 30 or as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-audit-log-maxage-argument-is-set-to-30-or-as-appropriate
Check: CKV_K8S_82: "Ensure that the admission control plugin ServiceAccount is set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-admission-control-plugin-serviceaccount-is-set
Check: CKV_K8S_91: "Ensure that the --audit-log-path argument is set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-audit-log-path-argument-is-set
Check: CKV_K8S_95: "Ensure that the --request-timeout argument is set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-request-timeout-argument-is-set-as-appropriate
Check: CKV_K8S_39: "Do not use the CAP_SYS_ADMIN linux capability"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-36
Check: CKV_K8S_89: "Ensure that the --secure-port argument is not set to 0"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-secure-port-argument-is-not-set-to-0
Check: CKV_K8S_79: "Ensure that the admission control plugin AlwaysAdmit is not set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-admission-control-plugin-alwaysadmit-is-not-set
Check: CKV_K8S_70: "Ensure that the --token-auth-file argument is not set"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-token-auth-file-parameter-is-not-set
Check: CKV_K8S_143: "Ensure that the --streaming-connection-idle-timeout argument is not set to 0"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-streaming-connection-idle-timeout-argument-is-not-set-to-0
Check: CKV_K8S_147: "Ensure that the --event-qps argument is set to 0 or a level which ensures appropriate event capture"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-event-qps-argument-is-set-to-0-or-a-level-which-ensures-appropriate-event-capture
Check: CKV_K8S_117: "Ensure that the --client-cert-auth argument is set to true"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-client-cert-auth-argument-is-set-to-true
Check: CKV_K8S_26: "Do not specify hostPort unless absolutely necessary"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-25
Check: CKV_K8S_35: "Prefer using secrets as files over secrets as environment variables"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-33
Check: CKV_K8S_106: "Ensure that the --terminated-pod-gc-threshold argument is set as appropriate"
        PASSED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-that-the-terminated-pod-gc-threshold-argument-is-set-as-appropriate
Check: CKV_K8S_21: "The default namespace should not be used"
        FAILED for resource: Service.default.mongodb-test
        File: /Service.yaml:1-10
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-20

                1  | apiVersion: v1
                2  | kind: Service
                3  | metadata:
                4  |   name: mongodb-test
                5  |   labels:
                6  |     app: database
                7  | spec:
                8  |   clusterIP: None
                9  |   selector:
                10 |     app: database

Check: CKV_K8S_30: "Apply security context to your containers"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-28

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_28: "Minimize the admission of containers with the NET_RAW capability"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-27

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_38: "Ensure that Service Account Tokens are only mounted where necessary"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-35

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_15: "Image Pull Policy should be Always"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-14

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_37: "Minimize the admission of containers with capabilities assigned"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-34

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_31: "Ensure that the seccomp profile is set to docker/default or runtime/default"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-29

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_11: "CPU limits should be set"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-10

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_12: "Memory requests should be set"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-11

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_23: "Minimize the admission of root containers"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-22

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_13: "Memory limits should be set"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-12

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_8: "Liveness Probe Should be Configured"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-7

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_40: "Containers should run as a high UID to avoid host conflict"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-37

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_22: "Use read-only filesystem for containers where possible"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-21

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_43: "Image should use digest"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-39

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_10: "CPU requests should be set"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-9

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_29: "Apply security context to your pods and containers"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/ensure-securitycontext-is-applied-to-pods-and-containers

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_20: "Containers should not run with allowPrivilegeEscalation"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-19

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_21: "The default namespace should not be used"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-20

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_9: "Readiness Probe Should be Configured"
        FAILED for resource: StatefulSet.default.mongodb-test
        File: /StatefulSet.yaml:1-73
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-8

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_21: "The default namespace should not be used"
        FAILED for resource: ConfigMap.default.mongodb-configmap
        File: /ConfigMap.yaml:1-51
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-20

                Code lines for this resource are too many. Please use IDE of your choice to review the file.
Check: CKV_K8S_21: "The default namespace should not be used"
        FAILED for resource: Secret.default.mongodb-secret
        File: /Secret.yaml:1-11
        Guide: https://docs.prismacloud.io/en/enterprise-edition/policy-reference/kubernetes-policies/kubernetes-policy-index/bc-k8s-20

                1  | apiVersion: v1
                2  | kind: Secret
                3  | metadata:
                4  |   name: mongodb-secret
                5  | type: Opaque
                6  | data:
                7  |   MONGO_ROOT_USERNAME: YWRtaW4K
                8  |   MONGO_ROOT_PASSWORD: cGFzc3dvcmQK
                9  |   MONGO_USERNAME: dGVzdAo=
                10 |   MONGO_PASSWORD: cGFzc3dvcmQK
                11 |   MONGO_USERS_LIST: dGVzdDpkYkFkbWluLHJlYWRXcml0ZTpwYXNzd29yZAo=

Check: CKV2_K8S_6: "Minimize the admission of pods which lack an associated NetworkPolicy"
        FAILED for resource: Pod.default.mongodb-test.app-database.selector-mongodb-test
        File: /StatefulSet.yaml:1-73

                Code lines for this resource are too many. Please use IDE of your choice to review the file.

