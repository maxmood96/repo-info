## `debian:stable-backports`

```console
$ docker pull debian@sha256:bee9d00144ddf6b7daa73d9199b9b7fd90c7da0a4e981ecd79dbd6a729cfc1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2187d19932824b6c236814e797fb9d64a843fb78fda30d5437c7d83072903015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd871f6204fe0e75b5e8a4455f3e297b45f8dbd31e039698a6c527d10f24596`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:46 GMT
ADD file:fd936c4956e463da4f9cd14877854a452fa42fb901d98abbc6b1f8fb0803e164 in / 
# Wed, 16 Aug 2023 01:01:47 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:01:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b88a3f767a5e4df3297b4c81f2cd8254c9542cade686d57f351014f0e35d4ad8`  
		Last Modified: Wed, 16 Aug 2023 01:07:48 GMT  
		Size: 49.6 MB (49557364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca52435b2b47b81b7133aa778bc2d9360d110d70ceb745176ec5a61e439607a4`  
		Last Modified: Wed, 16 Aug 2023 01:07:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1bc092bcf58e6b52fc12c54b28339a01e51d7568046a93b6a4f2acfa5e6a9da3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47415211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a71e20ab4f69b1566cba1c2b2c784d6cb11807f4d819aba4cc3e911f40d0c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:25 GMT
ADD file:8dc6eaf906602786cbd9987cf43dcee5a498e22fc886e23a09942a544185206d in / 
# Tue, 15 Aug 2023 23:49:25 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:49:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bc3aecc99440091f319da44ca13cf8fcc17ea6d16aa081e4dc943a04de7dffad`  
		Last Modified: Tue, 15 Aug 2023 23:53:35 GMT  
		Size: 47.4 MB (47414986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c931aae837293a555f69f1d1ab39ae154a6b2071b0116a9057fb3b22e9ff91ba`  
		Last Modified: Tue, 15 Aug 2023 23:53:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bf80e81bf90539ccaaf4ef65ee11c8d7a16cf2674169c76ac999641adf79944b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45233171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469eb3c4173a3cd7131f20667fa883e8d05beb111814e01d77291fa0917b86ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:18:58 GMT
ADD file:d3fecb22c0369c4005be0bf4b91cff371b5cf8566f179707b8d53c95290e1893 in / 
# Wed, 16 Aug 2023 00:18:59 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:19:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:61bc0ba094fab9a2cbb0e720b72a23be8b72357b58cff391db823e3dd65011df`  
		Last Modified: Wed, 16 Aug 2023 00:24:37 GMT  
		Size: 45.2 MB (45232949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b0e66a5baddb9adecc3791d7d7a65f4ee95a52c8a2043ffa146af52f5b8561`  
		Last Modified: Wed, 16 Aug 2023 00:24:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1197b08341458739995e52580c7380e5b05a0e3d036b3048265cd2748cb68ded
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16c7ec8bf942d9fb77982d91eb6e35dc9d2c047f3d56fc87c7517b69ab05797`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:13 GMT
ADD file:a09ec75380775bbf01dde2c0e1c1b8cde93bc2a0df9f1f0991ec4ef6eb2d74cb in / 
# Tue, 15 Aug 2023 23:41:14 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:41:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3e7f93afe9888e6966033933fb176e84297a1aa924b48df5246a9be951cff26d`  
		Last Modified: Tue, 15 Aug 2023 23:46:20 GMT  
		Size: 49.6 MB (49591309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b59c18b1e0d64a55be6fd785707641a93205cf4afbd5a6af10d317cbd40ffd`  
		Last Modified: Tue, 15 Aug 2023 23:46:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:fbc187555324b75fb7c552f65107100ce17bdea422a290ab76d4c4ca5cb40f69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50568230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39998b53d00f4dd01d138076ba0a689703f849d4b212887c7ccdb6a20f15af8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:52 GMT
ADD file:b881220bd52b0e29ab527bbb127826af28137394707aa96ef81fc5e8a092b131 in / 
# Tue, 15 Aug 2023 23:40:53 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:40:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6682406395788a3f43e3ef89b4b2d8f23bd65e00473ca4a3fe73eb68ac15c85a`  
		Last Modified: Tue, 15 Aug 2023 23:47:05 GMT  
		Size: 50.6 MB (50568006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20b75553f6be14320de84d99fa19a105353ef56360a264681a45ca20b29c8c1`  
		Last Modified: Tue, 15 Aug 2023 23:47:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:2ef466c9633271567a7f47a8b33c4c7a368a8ee82ce6cf1e1d46f863d38aecea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49542213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc78a521ca313373506fa3228ee70d6c21f6ed23920895cb916f34466cc9de10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:12:55 GMT
ADD file:06637dd3312db7f58e3e86bc596a2ef81713c7af49a8095bfe0fc610388a1b48 in / 
# Wed, 16 Aug 2023 00:13:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:13:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e578ce5d601a1f13d04dcbebcaf82135112659cb16028c646388af0ebc772072`  
		Last Modified: Wed, 16 Aug 2023 00:24:05 GMT  
		Size: 49.5 MB (49541989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34520328d7a1ce57ee1bc4d6647aa0dd468807a0bf22762898ac0432c24586f3`  
		Last Modified: Wed, 16 Aug 2023 00:24:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4a4b39e793180186f31b380073c1fc93229f4ea7b90b68828317f7ddda297484
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53543956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6c882b35d446355301b8444b9b6358be2f401c49282406c374524322459eb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:11:40 GMT
ADD file:db4e242663b2df91e9d6c7a94bb0e4ef5cd1cbcd74d4471e2da36f5ddaaebf53 in / 
# Wed, 16 Aug 2023 01:11:43 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:11:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9a3975b2ee9f80473278d001800747fa4b9a7e882bb8a40e8e59c882d0a71fb3`  
		Last Modified: Wed, 16 Aug 2023 01:19:14 GMT  
		Size: 53.5 MB (53543731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e049e3aca7f448a6c3330f284f5d6c86462a2982b49b57156c36893600794663`  
		Last Modified: Wed, 16 Aug 2023 01:19:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:65b5381a6e86588380ebc8ec323489dddccd6e7873a5265f1b414b3054779ba2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47922257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdc7bf77b2e0df60628652df3882fdba36347de59c675e34e4c4e0ab2ffbdef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:44:19 GMT
ADD file:17756dcd18bc59a255a8c6b01ed9549c2e3abfdfa944090abd110bd44831e414 in / 
# Tue, 15 Aug 2023 23:44:26 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:44:32 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2b0ffa164418dcf7104b29fee7c17204350bdc187cf3fe5d71eb1fce50d92471`  
		Last Modified: Tue, 15 Aug 2023 23:49:23 GMT  
		Size: 47.9 MB (47922032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70502d5fff11c2cbd06be7ac42c78e0f767284afe2e701b715492755cb6f9bb6`  
		Last Modified: Tue, 15 Aug 2023 23:49:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
