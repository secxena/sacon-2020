

## Vulnerability Test cases

- [x] Kubernetes version disclosure.
- [x] Access to Kubernetes API
- [x] Insecure (HTTP) access to Kubernetes API 
- [x] Specific Access to Kubernetes API 
- [x] Possible Arp Spoof 
- [x] Certificate Includes Email Address
- [x] Critical Privilege Escalation CVE
- [x] Denial of Service to Kubernetes API Server
- [x] Possible Ping Flood Attack
- [x] Possible Reset Flood Attack
- [x] Arbitrary Access To Cluster Scoped Resources
- [x] Kubectl Vulnerable To CVE-2019-11246
- [x] Kubectl Vulnerable To CVE-2019-1002101
- [x] Dashboard Exposed
- [x] Possible DNS Spoof
- [x] Etcd Remote Write Access Event
- [x] Etcd Remote Read Access Event
- [x] Etcd Remote version disclosure
- [x] Etcd is accessible using insecure connection (HTTP)
- [x] Anonymous Authentication
- [x] Exposed Container Logs
- [x] Exposed Running Pods
- [x] Exposed Exec On Container
- [x] Exposed Run Inside Container
- [x] Exposed Port Forward
- [x] Exposed Attaching To Container
- [x] Cluster Health Disclosure
- [x] Privileged Container
- [x] Exposed System Logs
- [x] Exposed Kubelet Cmdline
- [x] Pod With Mount To /var/log
- [x] Read access to Pod service account token
    

## vulnerability privilege escalation


1.  **readOnlyRootFilesystem**,  check if not set or explicitly set to false
2.  **RunAsNonRoot**, check if not set in ContainerSecurityContext, which results in root user being allowed!
3.  **AllowPrivilegeEscalation**, it allows privilege escalation if not set, set it to false
4.  **Capability not dropped**, if thats the case then following capabilities are there with every docker.

    1. SETPCAP,
    2. SYS_MODULE, 
    3. SYS_RAWIO,
    4. SYS_PACCT ,
    5. SYS_ADMIN, 
    6. SYS_NICE, 
    7. SYS_RESOURCE, 
    8. SYS_TIME, 
    9. SYS_TTY_CONFIG, 
    10. MKNOD, 
    11. AUDIT_WRITE, 
    12. AUDIT_CONTROL, 
    13. MAC_OVERRIDE, 
    14. MAC_ADMIN, 
    15. NET_ADMIN, 
    16. SYSLOG, 
    17. CHOWN, 
    18. NET_RAW, 
    19. DAC_OVERRIDE, 
    20. FOWNERDAC_READ_SEARCH, 
    21. FSETID, 
    22. KILL, 
    23. SETGID, 
    24. SETUID, 
    25. LINUX_IMMUTABLE, 
    26. NET_BIND_SERVICE, 
    27. NET_BROADCAST, 
    28. IPC_LOCK, 
    29. IPC_OWNER, 
    30. SYS_CHROOT, 
    31. SYS_PTRACE, 
    32. SYS_BOOT, 
    33.  LEASE, 
    34. SETFCAP, 
    35. WAKE_ALARM, 
    

## Good Practices

-   Keep Kubernetes updated
-   Use a minimal OS
-   Use minimal IAM roles
-   Use private IPs on your nodes
-   Monitor access with audit logging
-   Verify binaries that are deployed
-   Set a Pod Security Policy
-   Protect secrets
-   Consider sandboxing
-   Limit the identity used by pods
-   Use a service mesh for authentication & encryption


# Hardening (Coming Soon) -

    



