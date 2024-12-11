<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.23`](#nats21023)
-	[`nats:2.10.23-alpine`](#nats21023-alpine)
-	[`nats:2.10.23-alpine3.21`](#nats21023-alpine321)
-	[`nats:2.10.23-linux`](#nats21023-linux)
-	[`nats:2.10.23-nanoserver`](#nats21023-nanoserver)
-	[`nats:2.10.23-nanoserver-1809`](#nats21023-nanoserver-1809)
-	[`nats:2.10.23-scratch`](#nats21023-scratch)
-	[`nats:2.10.23-windowsservercore`](#nats21023-windowsservercore)
-	[`nats:2.10.23-windowsservercore-1809`](#nats21023-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:ec58736bc9e1482c3b83df75c728af220a454f599d1f9756ae973fbefe605d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6532; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:1e5a70cbe4b8f4abb005798b8d6e1e65b826740ad1c4477c9833273400b15cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5496807d7c9654f0c5249d90ef8e6921bbe686d1e32f7c2ef204c62db7624f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c98ad5b05b548e9f478b509989b55e59bcf2e4a146185479bb60550b5ec676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54e18e4af8b01d10a888ef5b165b629e96e4d8eb7608bec0e99c5eee0c9159`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 5.9 MB (5886905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f4b8daef123fcda057eda55396c55ac8498119ece34a1cf67bcfc57ce3003`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec15026ac386efbe9f4900f958687e23f6a83cc6658b249ed6d0074c2bf0c25`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8b973b30c4ec652e1888226f0349110e99487bf399f6469eba04cefe74080923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d1290efd75581b0f72bee916079dfd7a5409ac55caec4568a82363e98e17e`

```dockerfile
```

-	Layers:
	-	`sha256:33a765323843ca2c36164b9fcd98bf4d1709a2e5a580674e4e3064c69fa752e7`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:1e5a70cbe4b8f4abb005798b8d6e1e65b826740ad1c4477c9833273400b15cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5496807d7c9654f0c5249d90ef8e6921bbe686d1e32f7c2ef204c62db7624f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c98ad5b05b548e9f478b509989b55e59bcf2e4a146185479bb60550b5ec676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54e18e4af8b01d10a888ef5b165b629e96e4d8eb7608bec0e99c5eee0c9159`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 5.9 MB (5886905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f4b8daef123fcda057eda55396c55ac8498119ece34a1cf67bcfc57ce3003`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec15026ac386efbe9f4900f958687e23f6a83cc6658b249ed6d0074c2bf0c25`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8b973b30c4ec652e1888226f0349110e99487bf399f6469eba04cefe74080923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d1290efd75581b0f72bee916079dfd7a5409ac55caec4568a82363e98e17e`

```dockerfile
```

-	Layers:
	-	`sha256:33a765323843ca2c36164b9fcd98bf4d1709a2e5a580674e4e3064c69fa752e7`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:e8394430b8b95464c6440deec610026c101e807cba0c7ec13bb1ed31a7b46e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:f5a294347d7bf963391de7dc25199d9050ebb6c081e6c811057892a3b15aaba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32c48f187027a1e176bf682f36cd8ca925c8b2f300c2623b84089183b475aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:34:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER=2.10.23
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Wed, 11 Dec 2024 20:34:29 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Wed, 11 Dec 2024 20:35:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2024 20:35:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Dec 2024 20:35:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 20:35:21 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 20:35:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 20:35:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d540cddf3428645e2fb13b50fd495690f1e45d67b52351579eac4694e76e0`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2908784fd11561cba324875871fe258d9079ee0d13e669ce09b9fba6fffb9`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac132287b3225bb7f91f3f5dbd1fb63e5b98cf04c8ee2f05f94af132fbe94d`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7c77aa73e3cba288995b5fc0f3b2672de762cc107cceefaeb2d2dff2e2053`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b803c4d46f308e998b9df759115294883b19178b18306bbea2420af8c9604`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e343a361900d03c36362f3a871c13d8d39f6ee75b1d665e51acb2fc3d6c6ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:29 GMT  
		Size: 469.5 KB (469548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d135136fec8fa104eb041a0092677d93e52f8f879a93a719f95ab5e84a0111`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 6.4 MB (6372268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c90b38196cb25099616e985446db783152ad6374b41843807ffdb6f6d28aaa`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b16184451fd779a0a8a367c53ab6fbfe9f091fbac698f2c8f741102c8e7f63`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca8cf13340ca74ec1deb970c737b68cb7dfbd7a33ed48025b076c64f7002bce`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeab0cb599ab0a578727497d94c6ddfc165b2f57720ed1ca0d11acf887d49dd`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:e8394430b8b95464c6440deec610026c101e807cba0c7ec13bb1ed31a7b46e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:f5a294347d7bf963391de7dc25199d9050ebb6c081e6c811057892a3b15aaba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32c48f187027a1e176bf682f36cd8ca925c8b2f300c2623b84089183b475aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:34:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER=2.10.23
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Wed, 11 Dec 2024 20:34:29 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Wed, 11 Dec 2024 20:35:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2024 20:35:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Dec 2024 20:35:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 20:35:21 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 20:35:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 20:35:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d540cddf3428645e2fb13b50fd495690f1e45d67b52351579eac4694e76e0`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2908784fd11561cba324875871fe258d9079ee0d13e669ce09b9fba6fffb9`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac132287b3225bb7f91f3f5dbd1fb63e5b98cf04c8ee2f05f94af132fbe94d`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7c77aa73e3cba288995b5fc0f3b2672de762cc107cceefaeb2d2dff2e2053`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b803c4d46f308e998b9df759115294883b19178b18306bbea2420af8c9604`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e343a361900d03c36362f3a871c13d8d39f6ee75b1d665e51acb2fc3d6c6ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:29 GMT  
		Size: 469.5 KB (469548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d135136fec8fa104eb041a0092677d93e52f8f879a93a719f95ab5e84a0111`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 6.4 MB (6372268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c90b38196cb25099616e985446db783152ad6374b41843807ffdb6f6d28aaa`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b16184451fd779a0a8a367c53ab6fbfe9f091fbac698f2c8f741102c8e7f63`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca8cf13340ca74ec1deb970c737b68cb7dfbd7a33ed48025b076c64f7002bce`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeab0cb599ab0a578727497d94c6ddfc165b2f57720ed1ca0d11acf887d49dd`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:ec58736bc9e1482c3b83df75c728af220a454f599d1f9756ae973fbefe605d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:1e5a70cbe4b8f4abb005798b8d6e1e65b826740ad1c4477c9833273400b15cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5496807d7c9654f0c5249d90ef8e6921bbe686d1e32f7c2ef204c62db7624f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c98ad5b05b548e9f478b509989b55e59bcf2e4a146185479bb60550b5ec676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54e18e4af8b01d10a888ef5b165b629e96e4d8eb7608bec0e99c5eee0c9159`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 5.9 MB (5886905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f4b8daef123fcda057eda55396c55ac8498119ece34a1cf67bcfc57ce3003`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec15026ac386efbe9f4900f958687e23f6a83cc6658b249ed6d0074c2bf0c25`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8b973b30c4ec652e1888226f0349110e99487bf399f6469eba04cefe74080923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d1290efd75581b0f72bee916079dfd7a5409ac55caec4568a82363e98e17e`

```dockerfile
```

-	Layers:
	-	`sha256:33a765323843ca2c36164b9fcd98bf4d1709a2e5a580674e4e3064c69fa752e7`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:1e5a70cbe4b8f4abb005798b8d6e1e65b826740ad1c4477c9833273400b15cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5496807d7c9654f0c5249d90ef8e6921bbe686d1e32f7c2ef204c62db7624f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c98ad5b05b548e9f478b509989b55e59bcf2e4a146185479bb60550b5ec676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54e18e4af8b01d10a888ef5b165b629e96e4d8eb7608bec0e99c5eee0c9159`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 5.9 MB (5886905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f4b8daef123fcda057eda55396c55ac8498119ece34a1cf67bcfc57ce3003`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec15026ac386efbe9f4900f958687e23f6a83cc6658b249ed6d0074c2bf0c25`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8b973b30c4ec652e1888226f0349110e99487bf399f6469eba04cefe74080923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d1290efd75581b0f72bee916079dfd7a5409ac55caec4568a82363e98e17e`

```dockerfile
```

-	Layers:
	-	`sha256:33a765323843ca2c36164b9fcd98bf4d1709a2e5a580674e4e3064c69fa752e7`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:e8394430b8b95464c6440deec610026c101e807cba0c7ec13bb1ed31a7b46e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:f5a294347d7bf963391de7dc25199d9050ebb6c081e6c811057892a3b15aaba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32c48f187027a1e176bf682f36cd8ca925c8b2f300c2623b84089183b475aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:34:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER=2.10.23
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Wed, 11 Dec 2024 20:34:29 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Wed, 11 Dec 2024 20:35:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2024 20:35:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Dec 2024 20:35:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 20:35:21 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 20:35:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 20:35:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d540cddf3428645e2fb13b50fd495690f1e45d67b52351579eac4694e76e0`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2908784fd11561cba324875871fe258d9079ee0d13e669ce09b9fba6fffb9`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac132287b3225bb7f91f3f5dbd1fb63e5b98cf04c8ee2f05f94af132fbe94d`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7c77aa73e3cba288995b5fc0f3b2672de762cc107cceefaeb2d2dff2e2053`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b803c4d46f308e998b9df759115294883b19178b18306bbea2420af8c9604`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e343a361900d03c36362f3a871c13d8d39f6ee75b1d665e51acb2fc3d6c6ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:29 GMT  
		Size: 469.5 KB (469548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d135136fec8fa104eb041a0092677d93e52f8f879a93a719f95ab5e84a0111`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 6.4 MB (6372268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c90b38196cb25099616e985446db783152ad6374b41843807ffdb6f6d28aaa`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b16184451fd779a0a8a367c53ab6fbfe9f091fbac698f2c8f741102c8e7f63`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca8cf13340ca74ec1deb970c737b68cb7dfbd7a33ed48025b076c64f7002bce`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeab0cb599ab0a578727497d94c6ddfc165b2f57720ed1ca0d11acf887d49dd`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:e8394430b8b95464c6440deec610026c101e807cba0c7ec13bb1ed31a7b46e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:f5a294347d7bf963391de7dc25199d9050ebb6c081e6c811057892a3b15aaba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32c48f187027a1e176bf682f36cd8ca925c8b2f300c2623b84089183b475aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:34:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER=2.10.23
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Wed, 11 Dec 2024 20:34:29 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Wed, 11 Dec 2024 20:35:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2024 20:35:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Dec 2024 20:35:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 20:35:21 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 20:35:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 20:35:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d540cddf3428645e2fb13b50fd495690f1e45d67b52351579eac4694e76e0`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2908784fd11561cba324875871fe258d9079ee0d13e669ce09b9fba6fffb9`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac132287b3225bb7f91f3f5dbd1fb63e5b98cf04c8ee2f05f94af132fbe94d`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7c77aa73e3cba288995b5fc0f3b2672de762cc107cceefaeb2d2dff2e2053`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b803c4d46f308e998b9df759115294883b19178b18306bbea2420af8c9604`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e343a361900d03c36362f3a871c13d8d39f6ee75b1d665e51acb2fc3d6c6ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:29 GMT  
		Size: 469.5 KB (469548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d135136fec8fa104eb041a0092677d93e52f8f879a93a719f95ab5e84a0111`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 6.4 MB (6372268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c90b38196cb25099616e985446db783152ad6374b41843807ffdb6f6d28aaa`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b16184451fd779a0a8a367c53ab6fbfe9f091fbac698f2c8f741102c8e7f63`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca8cf13340ca74ec1deb970c737b68cb7dfbd7a33ed48025b076c64f7002bce`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeab0cb599ab0a578727497d94c6ddfc165b2f57720ed1ca0d11acf887d49dd`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.23`

```console
$ docker pull nats@sha256:ec58736bc9e1482c3b83df75c728af220a454f599d1f9756ae973fbefe605d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10.23` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.23-alpine`

```console
$ docker pull nats@sha256:1e5a70cbe4b8f4abb005798b8d6e1e65b826740ad1c4477c9833273400b15cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.23-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5496807d7c9654f0c5249d90ef8e6921bbe686d1e32f7c2ef204c62db7624f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c98ad5b05b548e9f478b509989b55e59bcf2e4a146185479bb60550b5ec676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54e18e4af8b01d10a888ef5b165b629e96e4d8eb7608bec0e99c5eee0c9159`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 5.9 MB (5886905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f4b8daef123fcda057eda55396c55ac8498119ece34a1cf67bcfc57ce3003`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec15026ac386efbe9f4900f958687e23f6a83cc6658b249ed6d0074c2bf0c25`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8b973b30c4ec652e1888226f0349110e99487bf399f6469eba04cefe74080923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d1290efd75581b0f72bee916079dfd7a5409ac55caec4568a82363e98e17e`

```dockerfile
```

-	Layers:
	-	`sha256:33a765323843ca2c36164b9fcd98bf4d1709a2e5a580674e4e3064c69fa752e7`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.23-alpine3.21`

```console
$ docker pull nats@sha256:1e5a70cbe4b8f4abb005798b8d6e1e65b826740ad1c4477c9833273400b15cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.23-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5496807d7c9654f0c5249d90ef8e6921bbe686d1e32f7c2ef204c62db7624f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c98ad5b05b548e9f478b509989b55e59bcf2e4a146185479bb60550b5ec676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54e18e4af8b01d10a888ef5b165b629e96e4d8eb7608bec0e99c5eee0c9159`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 5.9 MB (5886905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f4b8daef123fcda057eda55396c55ac8498119ece34a1cf67bcfc57ce3003`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec15026ac386efbe9f4900f958687e23f6a83cc6658b249ed6d0074c2bf0c25`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8b973b30c4ec652e1888226f0349110e99487bf399f6469eba04cefe74080923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d1290efd75581b0f72bee916079dfd7a5409ac55caec4568a82363e98e17e`

```dockerfile
```

-	Layers:
	-	`sha256:33a765323843ca2c36164b9fcd98bf4d1709a2e5a580674e4e3064c69fa752e7`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.23-linux`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.23-linux` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-linux` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-linux` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.23-nanoserver`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10.23-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.23-nanoserver-1809`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:2.10.23-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.23-scratch`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.23-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.23-scratch` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.23-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.23-windowsservercore`

```console
$ docker pull nats@sha256:e8394430b8b95464c6440deec610026c101e807cba0c7ec13bb1ed31a7b46e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.23-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:f5a294347d7bf963391de7dc25199d9050ebb6c081e6c811057892a3b15aaba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32c48f187027a1e176bf682f36cd8ca925c8b2f300c2623b84089183b475aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:34:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER=2.10.23
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Wed, 11 Dec 2024 20:34:29 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Wed, 11 Dec 2024 20:35:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2024 20:35:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Dec 2024 20:35:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 20:35:21 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 20:35:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 20:35:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d540cddf3428645e2fb13b50fd495690f1e45d67b52351579eac4694e76e0`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2908784fd11561cba324875871fe258d9079ee0d13e669ce09b9fba6fffb9`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac132287b3225bb7f91f3f5dbd1fb63e5b98cf04c8ee2f05f94af132fbe94d`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7c77aa73e3cba288995b5fc0f3b2672de762cc107cceefaeb2d2dff2e2053`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b803c4d46f308e998b9df759115294883b19178b18306bbea2420af8c9604`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e343a361900d03c36362f3a871c13d8d39f6ee75b1d665e51acb2fc3d6c6ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:29 GMT  
		Size: 469.5 KB (469548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d135136fec8fa104eb041a0092677d93e52f8f879a93a719f95ab5e84a0111`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 6.4 MB (6372268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c90b38196cb25099616e985446db783152ad6374b41843807ffdb6f6d28aaa`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b16184451fd779a0a8a367c53ab6fbfe9f091fbac698f2c8f741102c8e7f63`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca8cf13340ca74ec1deb970c737b68cb7dfbd7a33ed48025b076c64f7002bce`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeab0cb599ab0a578727497d94c6ddfc165b2f57720ed1ca0d11acf887d49dd`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.23-windowsservercore-1809`

```console
$ docker pull nats@sha256:e8394430b8b95464c6440deec610026c101e807cba0c7ec13bb1ed31a7b46e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:2.10.23-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:f5a294347d7bf963391de7dc25199d9050ebb6c081e6c811057892a3b15aaba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32c48f187027a1e176bf682f36cd8ca925c8b2f300c2623b84089183b475aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:34:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER=2.10.23
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Wed, 11 Dec 2024 20:34:29 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Wed, 11 Dec 2024 20:35:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2024 20:35:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Dec 2024 20:35:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 20:35:21 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 20:35:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 20:35:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d540cddf3428645e2fb13b50fd495690f1e45d67b52351579eac4694e76e0`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2908784fd11561cba324875871fe258d9079ee0d13e669ce09b9fba6fffb9`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac132287b3225bb7f91f3f5dbd1fb63e5b98cf04c8ee2f05f94af132fbe94d`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7c77aa73e3cba288995b5fc0f3b2672de762cc107cceefaeb2d2dff2e2053`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b803c4d46f308e998b9df759115294883b19178b18306bbea2420af8c9604`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e343a361900d03c36362f3a871c13d8d39f6ee75b1d665e51acb2fc3d6c6ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:29 GMT  
		Size: 469.5 KB (469548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d135136fec8fa104eb041a0092677d93e52f8f879a93a719f95ab5e84a0111`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 6.4 MB (6372268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c90b38196cb25099616e985446db783152ad6374b41843807ffdb6f6d28aaa`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b16184451fd779a0a8a367c53ab6fbfe9f091fbac698f2c8f741102c8e7f63`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca8cf13340ca74ec1deb970c737b68cb7dfbd7a33ed48025b076c64f7002bce`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeab0cb599ab0a578727497d94c6ddfc165b2f57720ed1ca0d11acf887d49dd`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:1e5a70cbe4b8f4abb005798b8d6e1e65b826740ad1c4477c9833273400b15cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d5496807d7c9654f0c5249d90ef8e6921bbe686d1e32f7c2ef204c62db7624f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c98ad5b05b548e9f478b509989b55e59bcf2e4a146185479bb60550b5ec676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54e18e4af8b01d10a888ef5b165b629e96e4d8eb7608bec0e99c5eee0c9159`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 5.9 MB (5886905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f4b8daef123fcda057eda55396c55ac8498119ece34a1cf67bcfc57ce3003`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec15026ac386efbe9f4900f958687e23f6a83cc6658b249ed6d0074c2bf0c25`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8b973b30c4ec652e1888226f0349110e99487bf399f6469eba04cefe74080923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d1290efd75581b0f72bee916079dfd7a5409ac55caec4568a82363e98e17e`

```dockerfile
```

-	Layers:
	-	`sha256:33a765323843ca2c36164b9fcd98bf4d1709a2e5a580674e4e3064c69fa752e7`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:1e5a70cbe4b8f4abb005798b8d6e1e65b826740ad1c4477c9833273400b15cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:d5496807d7c9654f0c5249d90ef8e6921bbe686d1e32f7c2ef204c62db7624f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9464982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c98ad5b05b548e9f478b509989b55e59bcf2e4a146185479bb60550b5ec676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54e18e4af8b01d10a888ef5b165b629e96e4d8eb7608bec0e99c5eee0c9159`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 5.9 MB (5886905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f4b8daef123fcda057eda55396c55ac8498119ece34a1cf67bcfc57ce3003`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec15026ac386efbe9f4900f958687e23f6a83cc6658b249ed6d0074c2bf0c25`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8b973b30c4ec652e1888226f0349110e99487bf399f6469eba04cefe74080923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d1290efd75581b0f72bee916079dfd7a5409ac55caec4568a82363e98e17e`

```dockerfile
```

-	Layers:
	-	`sha256:33a765323843ca2c36164b9fcd98bf4d1709a2e5a580674e4e3064c69fa752e7`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:ec58736bc9e1482c3b83df75c728af220a454f599d1f9756ae973fbefe605d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.17763.6532; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:f0e492514748529a5d7d0ce2efc7f2dda4c0f353614f55fe6a866e1c09a2a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull nats@sha256:a3bb6c91e3449cbd30540fb2490a5c003eab807abff5723c05c3c9fc255140d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161246960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5750440207dbaa7aa1a2d07ababb79c735ac51e214e16c91d227f19f1aef88fb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Wed, 11 Dec 2024 00:27:52 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:30d04105f2ee103eeaefb4dfeda74eb010a83b5e5fa9197d530ae8b0c97bf56f in C:\nats-server.exe 
# Wed, 11 Dec 2024 00:27:55 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 00:27:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 00:27:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c7f2f005a3ad1d681ab2ca14dc1ea4c2733d5227836c6af61c7767a24e3e3`  
		Last Modified: Wed, 11 Dec 2024 00:28:03 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f803c64951e363e8bb6e13fc56e77d3bd1d9097615ffe352b24d544ddcd14e`  
		Last Modified: Wed, 11 Dec 2024 00:28:02 GMT  
		Size: 6.0 MB (6026775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19e8e4b929fa87b385d81646b8abc8268e33896c609eef70f7c1e00a1f6a72e`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e44ab9a12591fa447b36a9be3edbdff717f54bfd33730388a91cba21e9b7b`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74b942460a0488783b56ec5d5e6e791000eec5f5474d6f61223331815d524f5`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5034f809175db916849c3fb45d58ee4bac77cc8ec00e5fbc2886451da153972`  
		Last Modified: Wed, 11 Dec 2024 00:28:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:e8394430b8b95464c6440deec610026c101e807cba0c7ec13bb1ed31a7b46e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:f5a294347d7bf963391de7dc25199d9050ebb6c081e6c811057892a3b15aaba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32c48f187027a1e176bf682f36cd8ca925c8b2f300c2623b84089183b475aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:34:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER=2.10.23
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Wed, 11 Dec 2024 20:34:29 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Wed, 11 Dec 2024 20:35:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2024 20:35:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Dec 2024 20:35:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 20:35:21 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 20:35:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 20:35:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d540cddf3428645e2fb13b50fd495690f1e45d67b52351579eac4694e76e0`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2908784fd11561cba324875871fe258d9079ee0d13e669ce09b9fba6fffb9`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac132287b3225bb7f91f3f5dbd1fb63e5b98cf04c8ee2f05f94af132fbe94d`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7c77aa73e3cba288995b5fc0f3b2672de762cc107cceefaeb2d2dff2e2053`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b803c4d46f308e998b9df759115294883b19178b18306bbea2420af8c9604`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e343a361900d03c36362f3a871c13d8d39f6ee75b1d665e51acb2fc3d6c6ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:29 GMT  
		Size: 469.5 KB (469548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d135136fec8fa104eb041a0092677d93e52f8f879a93a719f95ab5e84a0111`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 6.4 MB (6372268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c90b38196cb25099616e985446db783152ad6374b41843807ffdb6f6d28aaa`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b16184451fd779a0a8a367c53ab6fbfe9f091fbac698f2c8f741102c8e7f63`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca8cf13340ca74ec1deb970c737b68cb7dfbd7a33ed48025b076c64f7002bce`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeab0cb599ab0a578727497d94c6ddfc165b2f57720ed1ca0d11acf887d49dd`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:e8394430b8b95464c6440deec610026c101e807cba0c7ec13bb1ed31a7b46e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull nats@sha256:f5a294347d7bf963391de7dc25199d9050ebb6c081e6c811057892a3b15aaba8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2021024348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32c48f187027a1e176bf682f36cd8ca925c8b2f300c2623b84089183b475aa`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:34:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:34:27 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER=2.10.23
# Wed, 11 Dec 2024 20:34:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.23/nats-server-v2.10.23-windows-amd64.zip
# Wed, 11 Dec 2024 20:34:29 GMT
ENV NATS_SERVER_SHASUM=4ec39c0df08823a062dcdaac23ccf7ee56e76ccc27b69134f3e9b1549bc0f305
# Wed, 11 Dec 2024 20:35:02 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Dec 2024 20:35:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 Dec 2024 20:35:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 11 Dec 2024 20:35:21 GMT
EXPOSE 4222 6222 8222
# Wed, 11 Dec 2024 20:35:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 Dec 2024 20:35:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1d540cddf3428645e2fb13b50fd495690f1e45d67b52351579eac4694e76e0`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2908784fd11561cba324875871fe258d9079ee0d13e669ce09b9fba6fffb9`  
		Last Modified: Wed, 11 Dec 2024 20:35:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ac132287b3225bb7f91f3f5dbd1fb63e5b98cf04c8ee2f05f94af132fbe94d`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7c77aa73e3cba288995b5fc0f3b2672de762cc107cceefaeb2d2dff2e2053`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b803c4d46f308e998b9df759115294883b19178b18306bbea2420af8c9604`  
		Last Modified: Wed, 11 Dec 2024 20:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e343a361900d03c36362f3a871c13d8d39f6ee75b1d665e51acb2fc3d6c6ca`  
		Last Modified: Wed, 11 Dec 2024 20:35:29 GMT  
		Size: 469.5 KB (469548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d135136fec8fa104eb041a0092677d93e52f8f879a93a719f95ab5e84a0111`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 6.4 MB (6372268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c90b38196cb25099616e985446db783152ad6374b41843807ffdb6f6d28aaa`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b16184451fd779a0a8a367c53ab6fbfe9f091fbac698f2c8f741102c8e7f63`  
		Last Modified: Wed, 11 Dec 2024 20:35:27 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca8cf13340ca74ec1deb970c737b68cb7dfbd7a33ed48025b076c64f7002bce`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeab0cb599ab0a578727497d94c6ddfc165b2f57720ed1ca0d11acf887d49dd`  
		Last Modified: Wed, 11 Dec 2024 20:35:26 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
