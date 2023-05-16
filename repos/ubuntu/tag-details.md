<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:22.10`](#ubuntu2210)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20230412`](#ubuntubionic-20230412)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20230412`](#ubuntufocal-20230412)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20230425`](#ubuntujammy-20230425)
-	[`ubuntu:kinetic`](#ubuntukinetic)
-	[`ubuntu:kinetic-20230412`](#ubuntukinetic-20230412)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230420`](#ubuntulunar-20230420)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20230511.1`](#ubuntumantic-202305111)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:18.04`

```console
$ docker pull ubuntu@sha256:8aa9c2798215f99544d1ce7439ea9c3a6dfd82de607da1cec3a8a2fae005931b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:18.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:0779371f96205678dbcaa3ef499be2e5f262c8b09aadc11754bf3daf9f35e03e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3941d3b032a8168d53508410a67baad120a563df67a7959565a30a1cb2114731`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c5227665c11379f79e9da3d3e4f1724f9316b87d259ac0131628ca1b923a392`  
		Last Modified: Wed, 08 Mar 2023 03:59:25 GMT  
		Size: 25.7 MB (25688211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:715ddeafc950876ef9451c460d43ac1ba3e90655f582d845c7f656ee557bd2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21394593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0feaeaa2e651a8712ecfc0727458ba88952949b4b9136d20f0e7adb6a743c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:55e299352d1e9c6f1d6e7aee23f9204c8e147eec9fb877be5649ad7f1af58bca`  
		Last Modified: Wed, 08 Mar 2023 03:59:37 GMT  
		Size: 21.4 MB (21394593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e77e90f3a41b2c9480c68088c746065623ba9ca77f4e311070ebf404ac6ef2dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1adc1968c7b7646687f8585de8e3473681323cb9052956ed8f509529a52e61d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:13f679bb266a0be5756ce3bb145f89ccd6395d778b1a4bed5a0b0b26105bde2b`  
		Last Modified: Wed, 08 Mar 2023 03:59:31 GMT  
		Size: 22.7 MB (22710750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:7cbc4fafddce3cf793a94c3b5dc6295a3f569b9222c5e4e74b38aa00a65442fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713953b7d565f057a079026363b57bd30e4e9fef8aeaf217f6c4c8b20d968f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:472741f7e602c0ee1b34eaf14bb55e0a9377b9f28b0b00fd7ddb5b9d07046a7d`  
		Last Modified: Wed, 08 Mar 2023 03:59:42 GMT  
		Size: 26.1 MB (26095131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c955620556f7490d6c4cbd7c1d73faeaad2f635cc3207ee8278832c897d1a7e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342b45b2835cf4d380d116f2d5e52053a8335089236b194c117adf34efac0409`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:293f1b6b3486ffa5f90fdcf0f22fc2091718a3e012fadf073bf57b6a8604df20`  
		Last Modified: Wed, 08 Mar 2023 03:59:48 GMT  
		Size: 29.4 MB (29350183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:1e8deff80e7d247c13e32a88efe3ca7314c2e8eb6ab5224e1a7671d7d8076428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24743830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed683baf1b6cc5ec9754e58ee88c3414d4781d2b27d33dc89e16d191249bd0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff61d052565af59dfea677d587c19bf7759efb08fa5db9c11019e2b30b183d9b`  
		Last Modified: Wed, 08 Mar 2023 03:59:54 GMT  
		Size: 24.7 MB (24743830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:db8bf6f4fb351aa7a26e27ba2686cf35a6a409f65603e59d4c203e58387dc6b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:6de8d817428e3d064da83ce59b4dccf7c6749aa60b36a17ad6cc3b1f7d10123c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23609760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b1180d68d3d67c103b16d57b364242467c2eacbbe69a9ddc04dcf1cf801d75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:39f91c5e27647c786293528ceed473da81ca1f8e8a07bd92474a6d695bad1e22`  
		Last Modified: Thu, 13 Apr 2023 13:46:09 GMT  
		Size: 23.6 MB (23609760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:144e6a778925a0c11c4cd9fe5fce1172e620f215b0410bb43e7fa41bbcfe4522
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758cd4ebb2178eb0cd2ce78dea8ffad569f5bba415c4b33b694e891e7697e854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8659cf1709ef03be2c0b2dc339b19432bff8a0753d2d7d53f47272f098f56ef4`  
		Last Modified: Thu, 13 Apr 2023 13:46:03 GMT  
		Size: 26.0 MB (25972971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:91c315263bf6ce2500fa1b15cdb916c2c7e77a2e436dafde1788b40bc3105250
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42c37c658114d3d2893b096a54d2deab61f556eb08c89764d35cdf13faf7ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4c3f72acab731ed4e440147b25e7d155c3d98eb8738b731250868ad184e54d9`  
		Last Modified: Thu, 13 Apr 2023 13:46:21 GMT  
		Size: 26.4 MB (26364733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:dfd64a3b4296d8c9b62aa3309984f8620b98d87e47492599ee20739e8eb54fbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:ca5534a51dd04bbcebe9b23ba05f389466cf0c190f1f8f182d7eea92a9671d00
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b418d7b466ac6275a6bfcb0c86fbe4422ff6ea0af444a294f82d3bf5173ce74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf6a9befcdeecbb8813406afbd62ce81394e3869d84599f19f941aa5c74f3d1`  
		Last Modified: Tue, 25 Apr 2023 18:16:55 GMT  
		Size: 29.5 MB (29534634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2faed463fb00a57a51cc1fe0e0884d46eacac8e7784ca7a93c3e861661d3e752
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb792700b74824c2d05fca92a19eabc234d542f7dc4699bdb95b35d6fb5f795a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c082b7c88a9dba576d2339a3074cb358c028fb37a204afe47144788c8a242b32`  
		Last Modified: Tue, 25 Apr 2023 18:17:07 GMT  
		Size: 26.1 MB (26141443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6f8fe7bff0bee25c481cdc26e28bba984ebf72e6152005c18e1036983c01a28b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27349920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ef9003cefb5e93a3fb4d9f175527a6751dd2f18d5179cb530c29298550b92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79d0ea7dc1a848165a31e288cada1fa51dcd9bf302a305fe83a353c5c407110b`  
		Last Modified: Tue, 25 Apr 2023 18:17:01 GMT  
		Size: 27.3 MB (27349920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:93fbac516e3f64e076e953306215d0a05e691e8350bf7c2e6b600ed2678990e5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34594820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048699846e4395b96648953c996e16964162e51473be900161346bb6ee97a45b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:17 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:21 GMT
ADD file:e75f08a67f0576b5441bb2fe454cad4b5b31a9d4efea23be791af62e1e0c712f in / 
# Tue, 25 Apr 2023 17:30:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:680addf267238cca0a5d13b4eb4be2f06465f4b0f7865751e1109069a1971f46`  
		Last Modified: Tue, 25 Apr 2023 18:17:14 GMT  
		Size: 34.6 MB (34594820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:6f86459a9bb50cb27768ad53ba78d6f02612bbf7f1efeb513569bd2160c76834
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28017013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa44e363572ab7e275bd5517e384c3e0e9e0f0d69e926aa68e85eaafc35e1373`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:27be50396e3447f2e65a022e1d493eb54352cd28760269836b6a06f99639e4cf`  
		Last Modified: Tue, 25 Apr 2023 18:17:20 GMT  
		Size: 28.0 MB (28017013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.10`

```console
$ docker pull ubuntu@sha256:a9a425d086dbb34c1b5b99765596e2a3cc79b33826866c51cd4508d8eb327d2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9afa28d1eb80d78129debbef52b3f2a59b19479b2c15f01d16c2beeccd72dc10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781448a65e540dff394a6ae765d032b6c5fee3e0bc008f323330bd44a5aa797`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:049083b382db595e625c4760cee04d50fb6110bda597a3dd936406027ce01994`  
		Last Modified: Fri, 14 Apr 2023 11:09:28 GMT  
		Size: 25.1 MB (25067534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9ff03c2930fce7e915f3b321c6c601380ffb845140bd36715c44ec31d7ae551e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25759013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490b20d4c90f834abcf386620a8906d21821aaa4db91c4665016883f043a10e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4bb7992c0b6c454d95752fadeb8ec30f02376e386e2dbcde466ab9e74283ed78`  
		Last Modified: Fri, 14 Apr 2023 11:09:21 GMT  
		Size: 25.8 MB (25759013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:3761fb8cb1cfa0facc994bb50e559e50144c999ff6ac5a43712396f98dd92045
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d1b46d5d955e3fbe7be0da291db9a566b03ebbac3335bca37d70d66078e9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:91664c4b18004c964fd7a8e4cc1d53adb98ce8158f5d0dde54befa1c1f754635`  
		Last Modified: Fri, 14 Apr 2023 11:09:40 GMT  
		Size: 25.5 MB (25488667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:db2764b64a490a9ce44a7ce0c7ba7cc6d0472c8c44684960dbca7a06525eb597
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:ce7f6664be1081be78dfcf319cb11d7bceeef17b32df373282a66fe940e47f6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0120ea4307c597784895e9f539a67d88239d2c71ebfa830195fa2a650e4f3b5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cc1fe050fbd8eee8b0e2ef684c783d2c269fb7f61a0df0dee4639340bf612925`  
		Last Modified: Thu, 20 Apr 2023 18:59:08 GMT  
		Size: 26.8 MB (26825231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2d379e00f7bf822cf2133d5f353ef6a5e4621a2c34334f99d800bb6440b0e97a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24632909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdc4400067184574d122f092a66f0f8d2ed3d785bb9cbd8be35a0093b594151`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:604aa9b61f196d7ae0abd17a6d697aeab5a916fb6500d6887e59a05d362a1a06`  
		Last Modified: Thu, 20 Apr 2023 18:59:21 GMT  
		Size: 24.6 MB (24632909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e73844b55fb1ba94e595d64538acfcc1c4840b750f967ce368d91a51fa5007ee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513df0534cf35764514504f883f2163eb1bda7be89a511cad89c8c7d38b2626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0da974cf49e20cf8a8d93e9fda8598c48fbe9736275600c0efafa363ab592eb2`  
		Last Modified: Thu, 20 Apr 2023 18:59:15 GMT  
		Size: 26.1 MB (26079115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2089e70e7b8920b03336e193bc9033456b915b5b8c4121560c7a3da7d30099d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad251fd919f54dab755c74649e0840aaa3f64b540f00b79db2980bf4cff7fc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:26 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:29 GMT
ADD file:8d28b8fff20cf3ef8af5805d942e8aa5d19026e5ee01beb77e5863eb33637893 in / 
# Thu, 20 Apr 2023 18:20:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:441a86ac5a883ce4ca690a47f648f87bc8b93a71f7142dabb2c24c577ca5927b`  
		Last Modified: Thu, 20 Apr 2023 18:59:27 GMT  
		Size: 31.0 MB (31018578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:d4cede9f231a2ccae7481724b428d8ba496cfea01e5f4e4229fe92283851d15c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25706020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec03e420e560be9d01dfa32aaaade4fbf8062261fdde810eca6c4ec0e13dd411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:21:08 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:21:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:21:10 GMT
ADD file:96d7710293ddafe0813d47d0fbeae45dc31a20c6115c489702cab4d2352d48bd in / 
# Thu, 20 Apr 2023 18:21:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:99b4daa0c7842dc58f7f322faa32fd0ecc93065e8815d65f3c296b7e9ea970cb`  
		Last Modified: Thu, 20 Apr 2023 18:59:34 GMT  
		Size: 25.7 MB (25706020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

**does not exist** (yet?)

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:8aa9c2798215f99544d1ce7439ea9c3a6dfd82de607da1cec3a8a2fae005931b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic` - linux; amd64

```console
$ docker pull ubuntu@sha256:0779371f96205678dbcaa3ef499be2e5f262c8b09aadc11754bf3daf9f35e03e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3941d3b032a8168d53508410a67baad120a563df67a7959565a30a1cb2114731`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c5227665c11379f79e9da3d3e4f1724f9316b87d259ac0131628ca1b923a392`  
		Last Modified: Wed, 08 Mar 2023 03:59:25 GMT  
		Size: 25.7 MB (25688211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:715ddeafc950876ef9451c460d43ac1ba3e90655f582d845c7f656ee557bd2b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21394593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0feaeaa2e651a8712ecfc0727458ba88952949b4b9136d20f0e7adb6a743c1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:27:01 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:27:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:27:08 GMT
ADD file:21d7947367fe1aa8cc668c943d11c4841b0ead14b9103ef46fb8db8084603a75 in / 
# Wed, 08 Mar 2023 03:27:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:55e299352d1e9c6f1d6e7aee23f9204c8e147eec9fb877be5649ad7f1af58bca`  
		Last Modified: Wed, 08 Mar 2023 03:59:37 GMT  
		Size: 21.4 MB (21394593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e77e90f3a41b2c9480c68088c746065623ba9ca77f4e311070ebf404ac6ef2dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22710750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1adc1968c7b7646687f8585de8e3473681323cb9052956ed8f509529a52e61d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:25:33 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:25:34 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:25:35 GMT
ADD file:5f229d85bac2e85aa7ce97b2168fc61bd401d0151e8940a12d244356f984e65f in / 
# Wed, 08 Mar 2023 03:25:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:13f679bb266a0be5756ce3bb145f89ccd6395d778b1a4bed5a0b0b26105bde2b`  
		Last Modified: Wed, 08 Mar 2023 03:59:31 GMT  
		Size: 22.7 MB (22710750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:7cbc4fafddce3cf793a94c3b5dc6295a3f569b9222c5e4e74b38aa00a65442fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713953b7d565f057a079026363b57bd30e4e9fef8aeaf217f6c4c8b20d968f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:19 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:19 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:21 GMT
ADD file:6cf3e34995c6c44762ed692b86a0442d981e9a69fa4288960047e505d75c0223 in / 
# Wed, 08 Mar 2023 03:13:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:472741f7e602c0ee1b34eaf14bb55e0a9377b9f28b0b00fd7ddb5b9d07046a7d`  
		Last Modified: Wed, 08 Mar 2023 03:59:42 GMT  
		Size: 26.1 MB (26095131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:c955620556f7490d6c4cbd7c1d73faeaad2f635cc3207ee8278832c897d1a7e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342b45b2835cf4d380d116f2d5e52053a8335089236b194c117adf34efac0409`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:13:23 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:13:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:13:23 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:13:26 GMT
ADD file:5ea8615c09f693252cb9d45458421679f82f84d315200a7611165869195b3a69 in / 
# Wed, 08 Mar 2023 03:13:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:293f1b6b3486ffa5f90fdcf0f22fc2091718a3e012fadf073bf57b6a8604df20`  
		Last Modified: Wed, 08 Mar 2023 03:59:48 GMT  
		Size: 29.4 MB (29350183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:1e8deff80e7d247c13e32a88efe3ca7314c2e8eb6ab5224e1a7671d7d8076428
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24743830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed683baf1b6cc5ec9754e58ee88c3414d4781d2b27d33dc89e16d191249bd0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 03:23:29 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:23:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:23:29 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:23:31 GMT
ADD file:a6309e462d28398152cb726a11615118d79858da963b8c614772b87d87465967 in / 
# Wed, 08 Mar 2023 03:23:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff61d052565af59dfea677d587c19bf7759efb08fa5db9c11019e2b30b183d9b`  
		Last Modified: Wed, 08 Mar 2023 03:59:54 GMT  
		Size: 24.7 MB (24743830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic-20230412`

**does not exist** (yet?)

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:cb3a8c6cf45e9b18a430760ad7a7e4b80184acb9dac098e4f5cef4640ad91e58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:2f18a21d414ad3c0a8eea08fec8f98d730c5c02ddb0d5fef9c60ca72ac53329c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c92df8590c370b0dcf10c9273b5c18a74e08fb6089ae37d4ad9590fbdecc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cdca6f9f82cb2f31168afd36307721605cb5f89b51b97fa630583843ddb624a4`  
		Last Modified: Sat, 15 Apr 2023 05:20:43 GMT  
		Size: 26.8 MB (26825187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0749c2600c12e4e4fc06b75e036ecb673d3904de5b794f7f445d89fe3f9f4d56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24632844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2c91c5607776d99bf4abba5ce062e72eb05395777c764efd07a17f88017ee7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5ae278f595c8aaf2841d3b4e3561e918526de91fa4262e7ab9d259c210250be1`  
		Last Modified: Sat, 15 Apr 2023 05:20:55 GMT  
		Size: 24.6 MB (24632844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:381fbfde06af523912a2b9d52e0d6949c645218eb390ef442d633896fc5a4e81
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26080266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cffe7679257a2c07ddfffb306d7c3e5aa934bfd73151581ee868d5a38a5a08`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:39ad74439531de770151e38be6c76c635a3a0c97a4d8dac144680eea451e4b43`  
		Last Modified: Sat, 15 Apr 2023 05:20:49 GMT  
		Size: 26.1 MB (26080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f871f7609ee2d4dcf0ab6d2597e9c3e425482e189c7abff04de33ff54511759b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb6dcc0aed4be2d1b12ad54505515a29a6eef8502a249ea14dfb671f3ad9d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea416d41ef40856710483d8bb41ae5d7cc41d5da1075df7ef64e9694b18b3e0f`  
		Last Modified: Sat, 15 Apr 2023 05:21:01 GMT  
		Size: 31.0 MB (31018597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:3af6f4dd8a997017ff74949f2f4e88d672dfa28b5ea06e4093a3e15193bb9391
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25705932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa77ff3a8aeaf751ae3c673bb074b5f67528671ede73189cecded4d61348f7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6dd1be43160c095f202288009f4efedacf98863e9604b1af368e386488389a6`  
		Last Modified: Sat, 15 Apr 2023 05:21:07 GMT  
		Size: 25.7 MB (25705932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:db8bf6f4fb351aa7a26e27ba2686cf35a6a409f65603e59d4c203e58387dc6b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:6de8d817428e3d064da83ce59b4dccf7c6749aa60b36a17ad6cc3b1f7d10123c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23609760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b1180d68d3d67c103b16d57b364242467c2eacbbe69a9ddc04dcf1cf801d75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:39f91c5e27647c786293528ceed473da81ca1f8e8a07bd92474a6d695bad1e22`  
		Last Modified: Thu, 13 Apr 2023 13:46:09 GMT  
		Size: 23.6 MB (23609760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:144e6a778925a0c11c4cd9fe5fce1172e620f215b0410bb43e7fa41bbcfe4522
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758cd4ebb2178eb0cd2ce78dea8ffad569f5bba415c4b33b694e891e7697e854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8659cf1709ef03be2c0b2dc339b19432bff8a0753d2d7d53f47272f098f56ef4`  
		Last Modified: Thu, 13 Apr 2023 13:46:03 GMT  
		Size: 26.0 MB (25972971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:91c315263bf6ce2500fa1b15cdb916c2c7e77a2e436dafde1788b40bc3105250
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42c37c658114d3d2893b096a54d2deab61f556eb08c89764d35cdf13faf7ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4c3f72acab731ed4e440147b25e7d155c3d98eb8738b731250868ad184e54d9`  
		Last Modified: Thu, 13 Apr 2023 13:46:21 GMT  
		Size: 26.4 MB (26364733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20230412`

```console
$ docker pull ubuntu@sha256:db8bf6f4fb351aa7a26e27ba2686cf35a6a409f65603e59d4c203e58387dc6b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20230412` - linux; amd64

```console
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:6de8d817428e3d064da83ce59b4dccf7c6749aa60b36a17ad6cc3b1f7d10123c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23609760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b1180d68d3d67c103b16d57b364242467c2eacbbe69a9ddc04dcf1cf801d75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:39f91c5e27647c786293528ceed473da81ca1f8e8a07bd92474a6d695bad1e22`  
		Last Modified: Thu, 13 Apr 2023 13:46:09 GMT  
		Size: 23.6 MB (23609760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:144e6a778925a0c11c4cd9fe5fce1172e620f215b0410bb43e7fa41bbcfe4522
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758cd4ebb2178eb0cd2ce78dea8ffad569f5bba415c4b33b694e891e7697e854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8659cf1709ef03be2c0b2dc339b19432bff8a0753d2d7d53f47272f098f56ef4`  
		Last Modified: Thu, 13 Apr 2023 13:46:03 GMT  
		Size: 26.0 MB (25972971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; s390x

```console
$ docker pull ubuntu@sha256:91c315263bf6ce2500fa1b15cdb916c2c7e77a2e436dafde1788b40bc3105250
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42c37c658114d3d2893b096a54d2deab61f556eb08c89764d35cdf13faf7ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4c3f72acab731ed4e440147b25e7d155c3d98eb8738b731250868ad184e54d9`  
		Last Modified: Thu, 13 Apr 2023 13:46:21 GMT  
		Size: 26.4 MB (26364733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:dfd64a3b4296d8c9b62aa3309984f8620b98d87e47492599ee20739e8eb54fbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:ca5534a51dd04bbcebe9b23ba05f389466cf0c190f1f8f182d7eea92a9671d00
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b418d7b466ac6275a6bfcb0c86fbe4422ff6ea0af444a294f82d3bf5173ce74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf6a9befcdeecbb8813406afbd62ce81394e3869d84599f19f941aa5c74f3d1`  
		Last Modified: Tue, 25 Apr 2023 18:16:55 GMT  
		Size: 29.5 MB (29534634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2faed463fb00a57a51cc1fe0e0884d46eacac8e7784ca7a93c3e861661d3e752
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb792700b74824c2d05fca92a19eabc234d542f7dc4699bdb95b35d6fb5f795a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c082b7c88a9dba576d2339a3074cb358c028fb37a204afe47144788c8a242b32`  
		Last Modified: Tue, 25 Apr 2023 18:17:07 GMT  
		Size: 26.1 MB (26141443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6f8fe7bff0bee25c481cdc26e28bba984ebf72e6152005c18e1036983c01a28b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27349920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ef9003cefb5e93a3fb4d9f175527a6751dd2f18d5179cb530c29298550b92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79d0ea7dc1a848165a31e288cada1fa51dcd9bf302a305fe83a353c5c407110b`  
		Last Modified: Tue, 25 Apr 2023 18:17:01 GMT  
		Size: 27.3 MB (27349920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:93fbac516e3f64e076e953306215d0a05e691e8350bf7c2e6b600ed2678990e5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34594820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048699846e4395b96648953c996e16964162e51473be900161346bb6ee97a45b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:17 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:21 GMT
ADD file:e75f08a67f0576b5441bb2fe454cad4b5b31a9d4efea23be791af62e1e0c712f in / 
# Tue, 25 Apr 2023 17:30:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:680addf267238cca0a5d13b4eb4be2f06465f4b0f7865751e1109069a1971f46`  
		Last Modified: Tue, 25 Apr 2023 18:17:14 GMT  
		Size: 34.6 MB (34594820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:6f86459a9bb50cb27768ad53ba78d6f02612bbf7f1efeb513569bd2160c76834
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28017013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa44e363572ab7e275bd5517e384c3e0e9e0f0d69e926aa68e85eaafc35e1373`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:27be50396e3447f2e65a022e1d493eb54352cd28760269836b6a06f99639e4cf`  
		Last Modified: Tue, 25 Apr 2023 18:17:20 GMT  
		Size: 28.0 MB (28017013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20230425`

```console
$ docker pull ubuntu@sha256:dfd64a3b4296d8c9b62aa3309984f8620b98d87e47492599ee20739e8eb54fbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20230425` - linux; amd64

```console
$ docker pull ubuntu@sha256:ca5534a51dd04bbcebe9b23ba05f389466cf0c190f1f8f182d7eea92a9671d00
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b418d7b466ac6275a6bfcb0c86fbe4422ff6ea0af444a294f82d3bf5173ce74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf6a9befcdeecbb8813406afbd62ce81394e3869d84599f19f941aa5c74f3d1`  
		Last Modified: Tue, 25 Apr 2023 18:16:55 GMT  
		Size: 29.5 MB (29534634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230425` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2faed463fb00a57a51cc1fe0e0884d46eacac8e7784ca7a93c3e861661d3e752
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb792700b74824c2d05fca92a19eabc234d542f7dc4699bdb95b35d6fb5f795a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c082b7c88a9dba576d2339a3074cb358c028fb37a204afe47144788c8a242b32`  
		Last Modified: Tue, 25 Apr 2023 18:17:07 GMT  
		Size: 26.1 MB (26141443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230425` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6f8fe7bff0bee25c481cdc26e28bba984ebf72e6152005c18e1036983c01a28b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27349920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ef9003cefb5e93a3fb4d9f175527a6751dd2f18d5179cb530c29298550b92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79d0ea7dc1a848165a31e288cada1fa51dcd9bf302a305fe83a353c5c407110b`  
		Last Modified: Tue, 25 Apr 2023 18:17:01 GMT  
		Size: 27.3 MB (27349920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230425` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:93fbac516e3f64e076e953306215d0a05e691e8350bf7c2e6b600ed2678990e5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34594820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048699846e4395b96648953c996e16964162e51473be900161346bb6ee97a45b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:17 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:21 GMT
ADD file:e75f08a67f0576b5441bb2fe454cad4b5b31a9d4efea23be791af62e1e0c712f in / 
# Tue, 25 Apr 2023 17:30:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:680addf267238cca0a5d13b4eb4be2f06465f4b0f7865751e1109069a1971f46`  
		Last Modified: Tue, 25 Apr 2023 18:17:14 GMT  
		Size: 34.6 MB (34594820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230425` - linux; s390x

```console
$ docker pull ubuntu@sha256:6f86459a9bb50cb27768ad53ba78d6f02612bbf7f1efeb513569bd2160c76834
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28017013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa44e363572ab7e275bd5517e384c3e0e9e0f0d69e926aa68e85eaafc35e1373`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:27be50396e3447f2e65a022e1d493eb54352cd28760269836b6a06f99639e4cf`  
		Last Modified: Tue, 25 Apr 2023 18:17:20 GMT  
		Size: 28.0 MB (28017013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic`

```console
$ docker pull ubuntu@sha256:a9a425d086dbb34c1b5b99765596e2a3cc79b33826866c51cd4508d8eb327d2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic` - linux; amd64

```console
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9afa28d1eb80d78129debbef52b3f2a59b19479b2c15f01d16c2beeccd72dc10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781448a65e540dff394a6ae765d032b6c5fee3e0bc008f323330bd44a5aa797`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:049083b382db595e625c4760cee04d50fb6110bda597a3dd936406027ce01994`  
		Last Modified: Fri, 14 Apr 2023 11:09:28 GMT  
		Size: 25.1 MB (25067534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9ff03c2930fce7e915f3b321c6c601380ffb845140bd36715c44ec31d7ae551e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25759013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490b20d4c90f834abcf386620a8906d21821aaa4db91c4665016883f043a10e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4bb7992c0b6c454d95752fadeb8ec30f02376e386e2dbcde466ab9e74283ed78`  
		Last Modified: Fri, 14 Apr 2023 11:09:21 GMT  
		Size: 25.8 MB (25759013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; s390x

```console
$ docker pull ubuntu@sha256:3761fb8cb1cfa0facc994bb50e559e50144c999ff6ac5a43712396f98dd92045
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d1b46d5d955e3fbe7be0da291db9a566b03ebbac3335bca37d70d66078e9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:91664c4b18004c964fd7a8e4cc1d53adb98ce8158f5d0dde54befa1c1f754635`  
		Last Modified: Fri, 14 Apr 2023 11:09:40 GMT  
		Size: 25.5 MB (25488667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic-20230412`

```console
$ docker pull ubuntu@sha256:a9a425d086dbb34c1b5b99765596e2a3cc79b33826866c51cd4508d8eb327d2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic-20230412` - linux; amd64

```console
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9afa28d1eb80d78129debbef52b3f2a59b19479b2c15f01d16c2beeccd72dc10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781448a65e540dff394a6ae765d032b6c5fee3e0bc008f323330bd44a5aa797`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:049083b382db595e625c4760cee04d50fb6110bda597a3dd936406027ce01994`  
		Last Modified: Fri, 14 Apr 2023 11:09:28 GMT  
		Size: 25.1 MB (25067534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9ff03c2930fce7e915f3b321c6c601380ffb845140bd36715c44ec31d7ae551e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25759013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490b20d4c90f834abcf386620a8906d21821aaa4db91c4665016883f043a10e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4bb7992c0b6c454d95752fadeb8ec30f02376e386e2dbcde466ab9e74283ed78`  
		Last Modified: Fri, 14 Apr 2023 11:09:21 GMT  
		Size: 25.8 MB (25759013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; s390x

```console
$ docker pull ubuntu@sha256:3761fb8cb1cfa0facc994bb50e559e50144c999ff6ac5a43712396f98dd92045
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d1b46d5d955e3fbe7be0da291db9a566b03ebbac3335bca37d70d66078e9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:91664c4b18004c964fd7a8e4cc1d53adb98ce8158f5d0dde54befa1c1f754635`  
		Last Modified: Fri, 14 Apr 2023 11:09:40 GMT  
		Size: 25.5 MB (25488667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:dfd64a3b4296d8c9b62aa3309984f8620b98d87e47492599ee20739e8eb54fbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:ca5534a51dd04bbcebe9b23ba05f389466cf0c190f1f8f182d7eea92a9671d00
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b418d7b466ac6275a6bfcb0c86fbe4422ff6ea0af444a294f82d3bf5173ce74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf6a9befcdeecbb8813406afbd62ce81394e3869d84599f19f941aa5c74f3d1`  
		Last Modified: Tue, 25 Apr 2023 18:16:55 GMT  
		Size: 29.5 MB (29534634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2faed463fb00a57a51cc1fe0e0884d46eacac8e7784ca7a93c3e861661d3e752
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb792700b74824c2d05fca92a19eabc234d542f7dc4699bdb95b35d6fb5f795a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c082b7c88a9dba576d2339a3074cb358c028fb37a204afe47144788c8a242b32`  
		Last Modified: Tue, 25 Apr 2023 18:17:07 GMT  
		Size: 26.1 MB (26141443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6f8fe7bff0bee25c481cdc26e28bba984ebf72e6152005c18e1036983c01a28b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27349920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ef9003cefb5e93a3fb4d9f175527a6751dd2f18d5179cb530c29298550b92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:79d0ea7dc1a848165a31e288cada1fa51dcd9bf302a305fe83a353c5c407110b`  
		Last Modified: Tue, 25 Apr 2023 18:17:01 GMT  
		Size: 27.3 MB (27349920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:93fbac516e3f64e076e953306215d0a05e691e8350bf7c2e6b600ed2678990e5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34594820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048699846e4395b96648953c996e16964162e51473be900161346bb6ee97a45b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:17 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:18 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:21 GMT
ADD file:e75f08a67f0576b5441bb2fe454cad4b5b31a9d4efea23be791af62e1e0c712f in / 
# Tue, 25 Apr 2023 17:30:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:680addf267238cca0a5d13b4eb4be2f06465f4b0f7865751e1109069a1971f46`  
		Last Modified: Tue, 25 Apr 2023 18:17:14 GMT  
		Size: 34.6 MB (34594820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:6f86459a9bb50cb27768ad53ba78d6f02612bbf7f1efeb513569bd2160c76834
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28017013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa44e363572ab7e275bd5517e384c3e0e9e0f0d69e926aa68e85eaafc35e1373`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:44:52 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:44:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:44:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:44:54 GMT
ADD file:bbc65a9f059dc165e33f9a25ffaa40aab1a1f65164198a44394ec3065c82ae21 in / 
# Tue, 25 Apr 2023 17:44:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:27be50396e3447f2e65a022e1d493eb54352cd28760269836b6a06f99639e4cf`  
		Last Modified: Tue, 25 Apr 2023 18:17:20 GMT  
		Size: 28.0 MB (28017013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:db2764b64a490a9ce44a7ce0c7ba7cc6d0472c8c44684960dbca7a06525eb597
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar` - linux; amd64

```console
$ docker pull ubuntu@sha256:ce7f6664be1081be78dfcf319cb11d7bceeef17b32df373282a66fe940e47f6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0120ea4307c597784895e9f539a67d88239d2c71ebfa830195fa2a650e4f3b5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cc1fe050fbd8eee8b0e2ef684c783d2c269fb7f61a0df0dee4639340bf612925`  
		Last Modified: Thu, 20 Apr 2023 18:59:08 GMT  
		Size: 26.8 MB (26825231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2d379e00f7bf822cf2133d5f353ef6a5e4621a2c34334f99d800bb6440b0e97a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24632909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdc4400067184574d122f092a66f0f8d2ed3d785bb9cbd8be35a0093b594151`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:604aa9b61f196d7ae0abd17a6d697aeab5a916fb6500d6887e59a05d362a1a06`  
		Last Modified: Thu, 20 Apr 2023 18:59:21 GMT  
		Size: 24.6 MB (24632909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e73844b55fb1ba94e595d64538acfcc1c4840b750f967ce368d91a51fa5007ee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513df0534cf35764514504f883f2163eb1bda7be89a511cad89c8c7d38b2626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0da974cf49e20cf8a8d93e9fda8598c48fbe9736275600c0efafa363ab592eb2`  
		Last Modified: Thu, 20 Apr 2023 18:59:15 GMT  
		Size: 26.1 MB (26079115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2089e70e7b8920b03336e193bc9033456b915b5b8c4121560c7a3da7d30099d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad251fd919f54dab755c74649e0840aaa3f64b540f00b79db2980bf4cff7fc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:26 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:29 GMT
ADD file:8d28b8fff20cf3ef8af5805d942e8aa5d19026e5ee01beb77e5863eb33637893 in / 
# Thu, 20 Apr 2023 18:20:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:441a86ac5a883ce4ca690a47f648f87bc8b93a71f7142dabb2c24c577ca5927b`  
		Last Modified: Thu, 20 Apr 2023 18:59:27 GMT  
		Size: 31.0 MB (31018578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:d4cede9f231a2ccae7481724b428d8ba496cfea01e5f4e4229fe92283851d15c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25706020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec03e420e560be9d01dfa32aaaade4fbf8062261fdde810eca6c4ec0e13dd411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:21:08 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:21:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:21:10 GMT
ADD file:96d7710293ddafe0813d47d0fbeae45dc31a20c6115c489702cab4d2352d48bd in / 
# Thu, 20 Apr 2023 18:21:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:99b4daa0c7842dc58f7f322faa32fd0ecc93065e8815d65f3c296b7e9ea970cb`  
		Last Modified: Thu, 20 Apr 2023 18:59:34 GMT  
		Size: 25.7 MB (25706020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20230420`

```console
$ docker pull ubuntu@sha256:db2764b64a490a9ce44a7ce0c7ba7cc6d0472c8c44684960dbca7a06525eb597
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar-20230420` - linux; amd64

```console
$ docker pull ubuntu@sha256:ce7f6664be1081be78dfcf319cb11d7bceeef17b32df373282a66fe940e47f6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0120ea4307c597784895e9f539a67d88239d2c71ebfa830195fa2a650e4f3b5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cc1fe050fbd8eee8b0e2ef684c783d2c269fb7f61a0df0dee4639340bf612925`  
		Last Modified: Thu, 20 Apr 2023 18:59:08 GMT  
		Size: 26.8 MB (26825231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230420` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2d379e00f7bf822cf2133d5f353ef6a5e4621a2c34334f99d800bb6440b0e97a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24632909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdc4400067184574d122f092a66f0f8d2ed3d785bb9cbd8be35a0093b594151`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:604aa9b61f196d7ae0abd17a6d697aeab5a916fb6500d6887e59a05d362a1a06`  
		Last Modified: Thu, 20 Apr 2023 18:59:21 GMT  
		Size: 24.6 MB (24632909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230420` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e73844b55fb1ba94e595d64538acfcc1c4840b750f967ce368d91a51fa5007ee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513df0534cf35764514504f883f2163eb1bda7be89a511cad89c8c7d38b2626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0da974cf49e20cf8a8d93e9fda8598c48fbe9736275600c0efafa363ab592eb2`  
		Last Modified: Thu, 20 Apr 2023 18:59:15 GMT  
		Size: 26.1 MB (26079115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230420` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2089e70e7b8920b03336e193bc9033456b915b5b8c4121560c7a3da7d30099d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad251fd919f54dab755c74649e0840aaa3f64b540f00b79db2980bf4cff7fc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:26 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:29 GMT
ADD file:8d28b8fff20cf3ef8af5805d942e8aa5d19026e5ee01beb77e5863eb33637893 in / 
# Thu, 20 Apr 2023 18:20:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:441a86ac5a883ce4ca690a47f648f87bc8b93a71f7142dabb2c24c577ca5927b`  
		Last Modified: Thu, 20 Apr 2023 18:59:27 GMT  
		Size: 31.0 MB (31018578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230420` - linux; s390x

```console
$ docker pull ubuntu@sha256:d4cede9f231a2ccae7481724b428d8ba496cfea01e5f4e4229fe92283851d15c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25706020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec03e420e560be9d01dfa32aaaade4fbf8062261fdde810eca6c4ec0e13dd411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:21:08 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:21:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:21:10 GMT
ADD file:96d7710293ddafe0813d47d0fbeae45dc31a20c6115c489702cab4d2352d48bd in / 
# Thu, 20 Apr 2023 18:21:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:99b4daa0c7842dc58f7f322faa32fd0ecc93065e8815d65f3c296b7e9ea970cb`  
		Last Modified: Thu, 20 Apr 2023 18:59:34 GMT  
		Size: 25.7 MB (25706020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

**does not exist** (yet?)

## `ubuntu:mantic-20230511.1`

**does not exist** (yet?)

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:db2764b64a490a9ce44a7ce0c7ba7cc6d0472c8c44684960dbca7a06525eb597
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:ce7f6664be1081be78dfcf319cb11d7bceeef17b32df373282a66fe940e47f6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0120ea4307c597784895e9f539a67d88239d2c71ebfa830195fa2a650e4f3b5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cc1fe050fbd8eee8b0e2ef684c783d2c269fb7f61a0df0dee4639340bf612925`  
		Last Modified: Thu, 20 Apr 2023 18:59:08 GMT  
		Size: 26.8 MB (26825231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2d379e00f7bf822cf2133d5f353ef6a5e4621a2c34334f99d800bb6440b0e97a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24632909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdc4400067184574d122f092a66f0f8d2ed3d785bb9cbd8be35a0093b594151`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:604aa9b61f196d7ae0abd17a6d697aeab5a916fb6500d6887e59a05d362a1a06`  
		Last Modified: Thu, 20 Apr 2023 18:59:21 GMT  
		Size: 24.6 MB (24632909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:e73844b55fb1ba94e595d64538acfcc1c4840b750f967ce368d91a51fa5007ee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513df0534cf35764514504f883f2163eb1bda7be89a511cad89c8c7d38b2626`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0da974cf49e20cf8a8d93e9fda8598c48fbe9736275600c0efafa363ab592eb2`  
		Last Modified: Thu, 20 Apr 2023 18:59:15 GMT  
		Size: 26.1 MB (26079115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2089e70e7b8920b03336e193bc9033456b915b5b8c4121560c7a3da7d30099d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad251fd919f54dab755c74649e0840aaa3f64b540f00b79db2980bf4cff7fc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:26 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:29 GMT
ADD file:8d28b8fff20cf3ef8af5805d942e8aa5d19026e5ee01beb77e5863eb33637893 in / 
# Thu, 20 Apr 2023 18:20:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:441a86ac5a883ce4ca690a47f648f87bc8b93a71f7142dabb2c24c577ca5927b`  
		Last Modified: Thu, 20 Apr 2023 18:59:27 GMT  
		Size: 31.0 MB (31018578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:d4cede9f231a2ccae7481724b428d8ba496cfea01e5f4e4229fe92283851d15c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25706020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec03e420e560be9d01dfa32aaaade4fbf8062261fdde810eca6c4ec0e13dd411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:21:08 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:21:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:21:10 GMT
ADD file:96d7710293ddafe0813d47d0fbeae45dc31a20c6115c489702cab4d2352d48bd in / 
# Thu, 20 Apr 2023 18:21:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:99b4daa0c7842dc58f7f322faa32fd0ecc93065e8815d65f3c296b7e9ea970cb`  
		Last Modified: Thu, 20 Apr 2023 18:59:34 GMT  
		Size: 25.7 MB (25706020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
