command docker inspect we can see the internal configuration of container , volume , network

```
e.g docker inspect of spring boot application running on container
$ docker inspect e3c
[
    {
        "Id": "e3c65fd391c52b493791d0fdcd8e57c33671bd43524de9c973a204ce2427147d",
        "Created": "2022-07-22T07:57:10.072632974Z",
        "Path": "java",
        "Args": [
            "-jar",
            "/coffee-customer-0.0.1-SNAPSHOT.jar"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 12177,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2022-07-22T07:57:11.248830087Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:e54e475ad3602df411352fffc35b3516199299ad7bd72c81b67939df15069593",
        "ResolvConfPath": "/var/lib/docker/containers/e3c65fd391c52b493791d0fdcd8e57c33671bd43524de9c973a204ce2427147d/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/e3c65fd391c52b493791d0fdcd8e57c33671bd43524de9c973a204ce2427147d/hostname",
        "HostsPath": "/var/lib/docker/containers/e3c65fd391c52b493791d0fdcd8e57c33671bd43524de9c973a204ce2427147d/hosts",
        "LogPath": "/var/lib/docker/containers/e3c65fd391c52b493791d0fdcd8e57c33671bd43524de9c973a204ce2427147d/e3c65fd391c52b493791d0fdcd8e57c33671bd43524de9c973a204ce2427147d-json.log",
        "Name": "/apps",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": [],
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "customer_mysql",
            "PortBindings": {
                "8081/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "8082"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "on-failure",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": [],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "host",
            "Dns": null,
            "DnsOptions": null,
            "DnsSearch": null,
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": null,
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": null,
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "KernelMemory": 0,
            "KernelMemoryTCP": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/b4386e8da8df75f6162da013ee756d05480273d797ff89e13c12d0e485cc7193-init/diff:/var/lib/docker/overlay2/d1gxb1i7heehyn1uqqvgeetpb/diff:/var/lib/docker/overlay2/a166dfd6f19740be28011a6fc2fbe5b3a5729ad2801780130dec4e5607dd7ab9/diff:/var/lib/docker/overlay2/ed872fea85814cdec1aeef4b6bba2b3e5b571b6c01042f67ae250db6584a1a5d/diff:/var/lib/docker/overlay2/236c990003704eb4d8a59860488bf7f09dcb7f9b1aa1d01866e92318c998d513/diff:/var/lib/docker/overlay2/ac740d6cdabf2c6ef8fc5c5b06a360e583b718f396c38b5b84615683bfa9c7fe/diff:/var/lib/docker/overlay2/083c5d95dd8a6967635f4554b037ed0c254f111e8eeb155e38be6cbd2f5c640b/diff:/var/lib/docker/overlay2/60eb3e02bca69613ed1482cd36fcbf824693d841bdde5a85acc4f0dd5f33fba8/diff:/var/lib/docker/overlay2/7d7b4694ebb66a2551579d3c3a60baa94e8a2ae62d71655cc106992599af95fe/diff",
                "MergedDir": "/var/lib/docker/overlay2/b4386e8da8df75f6162da013ee756d05480273d797ff89e13c12d0e485cc7193/merged",
                "UpperDir": "/var/lib/docker/overlay2/b4386e8da8df75f6162da013ee756d05480273d797ff89e13c12d0e485cc7193/diff",
                "WorkDir": "/var/lib/docker/overlay2/b4386e8da8df75f6162da013ee756d05480273d797ff89e13c12d0e485cc7193/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "e3c65fd391c5",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "8081/tcp": {},
                "8082/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "JAVA_HOME=/usr/local/openjdk-11",
                "LANG=C.UTF-8",
                "JAVA_VERSION=11.0.15"
            ],
            "Cmd": null,
            "Image": "coffee-customer_app",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "java",
                "-jar",
                "/coffee-customer-0.0.1-SNAPSHOT.jar"
            ],
            "OnBuild": null,
            "Labels": {
                "com.docker.compose.config-hash": "16f62469c5ca7a0d6525891bdeeed3d090d5a5b8ee25c679dc122d7f1aa50dcd",
                "com.docker.compose.container-number": "1",
                "com.docker.compose.oneoff": "False",
                "com.docker.compose.project": "coffee-customer",
                "com.docker.compose.project.config_files": "docker-compose.yml",
                "com.docker.compose.project.working_dir": "C:\\Users\\NILESHkUMAR\\git-w3\\coffee-customer",
                "com.docker.compose.service": "app",
                "com.docker.compose.version": "1.28.5"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "2a668d8ac46926b995ccaca57999b88788e7bea9816a176992f3ab952772abcc",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "8081/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "8082"
                    }
                ],
                "8082/tcp": null
            },
            "SandboxKey": "/var/run/docker/netns/2a668d8ac469",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",
            "Networks": {
                "customer_mysql": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": [
                        "e3c65fd391c5",
                        "app"
                    ],
                    "NetworkID": "bde5c27bc28aeb7937b50d9f5816a46473b0b9f744f41e0c86b3592727472f22",
                    "EndpointID": "11915ea44fe88f142ff9275f52e52e8d7d8eb530d34cbd8f7dc9571b0791e211",
                    "Gateway": "172.22.0.1",
                    "IPAddress": "172.22.0.3",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:16:00:03",
                    "DriverOpts": null
                }
            }
        }
    }
]

```
