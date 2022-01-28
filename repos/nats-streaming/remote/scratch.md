## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:17fd1f851dc22d096470791f6d209fbe05e0aca349ae85f6863cf6c1fa6f5067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8208976899bae2b07c52ed71ba15d3006a8ea342e751fe2071d134c7d97702c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feacf64f84db353574b80d0552104f93839360bb95e872e22139e42053e95742`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 27 Jan 2022 23:29:13 GMT
COPY file:7cb6d7b391f88ad91a3d8b81c68623a0f3c92c9e73939aa4823b990ac9676822 in /nats-streaming-server 
# Thu, 27 Jan 2022 23:29:14 GMT
EXPOSE 4222 8222
# Thu, 27 Jan 2022 23:29:14 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 27 Jan 2022 23:29:14 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4edc1ec2dc80f100e623e2dd8e3424851cca1d9950d197169f07aa9d5148a308`  
		Last Modified: Thu, 27 Jan 2022 23:30:03 GMT  
		Size: 7.0 MB (7039723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:70edae45d21ebba44c24fb1c18f3192158d7e00ed2c4af215d45477a72463994
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6558012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694806db44c422954ff476d7eb07a53b5b7ebd04177699afaa53a4f525842e07`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 27 Jan 2022 00:55:51 GMT
COPY file:b1726d9c592d47fd10b019c5be7309fe30f8c1b8fee7cad066ae205324061c96 in /nats-streaming-server 
# Thu, 27 Jan 2022 00:55:51 GMT
EXPOSE 4222 8222
# Thu, 27 Jan 2022 00:55:52 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 27 Jan 2022 00:55:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4d610c82a45aa47531bfb809dc3656603559a8bfa3d5b53480c8d2659b7c977b`  
		Last Modified: Thu, 27 Jan 2022 00:58:09 GMT  
		Size: 6.6 MB (6558012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:cf7abf017ca4b10bcc16492ee29f54f9901fc6c40ae0e5eeba35423ce4346312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f2b939f92968d68a30b61db2b05fae78f9b7545fb1060ebb0c535069d2a6e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 20 Nov 2021 02:34:09 GMT
COPY file:f737534371c307ebba33d860a23821186a07bfe6bac93b4f8db1052afabca519 in /nats-streaming-server 
# Sat, 20 Nov 2021 02:34:09 GMT
EXPOSE 4222 8222
# Sat, 20 Nov 2021 02:34:10 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 20 Nov 2021 02:34:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f09d0d006743cce0f69db665ba3e97775e3e7ec87b782222a87b0e299de7abdd`  
		Last Modified: Sat, 20 Nov 2021 02:36:04 GMT  
		Size: 6.8 MB (6763075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:914869f94268b390a923b18f68d361a52db8122753a2557936baf1ee26e7b164
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6470229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a309e28d4efdde4dee3074f6a51aff746b87b4c06a4bbed71988185c85e59ab`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 27 Jan 2022 05:48:55 GMT
COPY file:8720a79121901c2f53c331a49132991f11ec3f28fb10f5b6a41d7097cecd1939 in /nats-streaming-server 
# Thu, 27 Jan 2022 05:48:55 GMT
EXPOSE 4222 8222
# Thu, 27 Jan 2022 05:48:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 27 Jan 2022 05:48:57 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:10d48e610369adb731205f3e174258c831f690cbe438b07fdb77887e7fcb36c9`  
		Last Modified: Thu, 27 Jan 2022 05:49:57 GMT  
		Size: 6.5 MB (6470229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
