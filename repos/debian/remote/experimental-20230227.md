## `debian:experimental-20230227`

```console
$ docker pull debian@sha256:2a20fd5ab188f0ec1d87835118013edfb036f6b83a7d92392b65835d1f250853
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

### `debian:experimental-20230227` - linux; amd64

```console
$ docker pull debian@sha256:301b6e0eb1383ba70a19e6366f278a51943df574b8121379158452b56fcda779
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49261502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc97ee223ae605e070a611b7dd86fbeefea71a25aa9fd82e0b73c9da453ff43`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:12:06 GMT
ADD file:dbf92bee170231a4a80e859bf48510468217880ed900ff23441d1324af2051b7 in / 
# Wed, 01 Mar 2023 04:12:06 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:12:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e5691ea88f53395815d6a2372cd7927234a45ab112cf06f5b9a0cb650d48e406`  
		Last Modified: Wed, 01 Mar 2023 04:17:32 GMT  
		Size: 49.3 MB (49261279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d237338c28e89e89f278d6c1f7895b269194a4175cb03a6d80426604e545e203`  
		Last Modified: Wed, 01 Mar 2023 04:17:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230227` - linux; arm variant v5

```console
$ docker pull debian@sha256:3179a8c3a858f622fe52a61f2b2fb26388e39e0a21a0e0b5aff85221f8b05c8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda7d7a9ae00da59e82175de7bff20e7c7b2a46f14126d654778fb9493aa9ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:52 GMT
ADD file:c3e085c3dff5f8a26c459819fec4fdc2ea28a857d84f1b06ea2536ab2c11f178 in / 
# Wed, 01 Mar 2023 01:49:52 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:50:02 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d9e0e6decf94a96d3649bc9614fd0ea25205676ea5004891847e53ead7e8b5f7`  
		Last Modified: Wed, 01 Mar 2023 01:55:14 GMT  
		Size: 48.1 MB (48107725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e529ac0697461ad7c874d3a0f17f7b81df8ad55567c76439918604add3a00d6`  
		Last Modified: Wed, 01 Mar 2023 01:55:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230227` - linux; arm variant v7

```console
$ docker pull debian@sha256:bfe53e149bebc51e24fc14a73abdc3316704c8a0d0d4112604b0714543e9eda6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45879161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047ad9cd600da9876ef2226f922a2868c16cd4499fa1ce3cc8bec3b053082a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:59:29 GMT
ADD file:a37e569a76cd9d80fe83d6cc15d442ea2ffc849415455cb6a8e017724ff6d05b in / 
# Wed, 01 Mar 2023 01:59:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:59:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:46b58fd36a9d0d3ccb7b3f47d82fbca683b31e8aaef9797a987b82692eb81560`  
		Last Modified: Wed, 01 Mar 2023 02:06:40 GMT  
		Size: 45.9 MB (45878940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f7667e455d107f9682da2ecb8d284066858f2c8059130be67f763d3fe31b88`  
		Last Modified: Wed, 01 Mar 2023 02:07:06 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230227` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f2291ba89ebbc647baf2aefe8a3bc1308ae1495a44af89937a65f5695e9d3cf0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49295549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5332ef1c147d93cf17c3313edac38d3406b6847d1cc3803fe63922c10d65356a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:22:07 GMT
ADD file:d3d245dd9b703a77c6718a640996a5acdc45ea159cf7a1294fb2d68846d0feac in / 
# Wed, 01 Mar 2023 02:22:08 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:22:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6bcfa56bba014c7c2207740bf9213f6434d84c206748886e3f2bcece14abd9a4`  
		Last Modified: Wed, 01 Mar 2023 02:27:16 GMT  
		Size: 49.3 MB (49295327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb77b93388b257c41b37002050f49d79595a627f408372dd601db49216183b73`  
		Last Modified: Wed, 01 Mar 2023 02:27:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230227` - linux; 386

```console
$ docker pull debian@sha256:0a400c8c523dfe59109a1fbffa7faa987d5b46d3230a0625b9d7fa953e3be72e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50314520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a7810f018017a0a406d7e73aeca3acf455e4ad41c197e4bd5b357f7752f40d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:41:04 GMT
ADD file:cd8e9789dd87e6ce334db0d011a57ad7006eb5fec80eb07858b7fbebcb442316 in / 
# Wed, 01 Mar 2023 01:41:04 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:41:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f7429bd849774125659d5323b68db4286e6b9c2b9d019a2ccfa72773e459ecf0`  
		Last Modified: Wed, 01 Mar 2023 01:48:44 GMT  
		Size: 50.3 MB (50314298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1a1be3a119681abbd62ad2e371f3ea705dbb4dadaccc476dc944ff1e8fbe8`  
		Last Modified: Wed, 01 Mar 2023 01:49:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230227` - linux; mips64le

```console
$ docker pull debian@sha256:fc93a8eeee50d7bf701c17102fe5cb17db6868127f799c58e304909d654f5624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49270843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05fa24d6011f6260fbb995ca100cf36b4c6f24bdc1eff3d36882d878e3776d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:14:57 GMT
ADD file:3c9761555a5ea142351615b9c67fa1d733eb4055b0a7ce13452185d0a0569a8a in / 
# Wed, 01 Mar 2023 02:15:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:15:40 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:488a223217255f1854f177e926f43908918ca067d20ac1205a5c8058bacba304`  
		Last Modified: Wed, 01 Mar 2023 02:23:05 GMT  
		Size: 49.3 MB (49270620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3335a1cbe608936e7e2ce0033bb81a3db2d76717e791d353e05fda95808900`  
		Last Modified: Wed, 01 Mar 2023 02:23:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230227` - linux; ppc64le

```console
$ docker pull debian@sha256:590122cb8cec4c19179b1038682311340c5a53b85640d1a5aed137503f6e573a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53273224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e6ca9ff1803b155501a5c81cb48a550256df7d91862b08ee47692c148a7794`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:50:06 GMT
ADD file:87be7e9eb6e59aed9d270ac466c0aaae2e1219c0962ea77878d0e1e2e379e7a7 in / 
# Wed, 01 Mar 2023 04:50:09 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:50:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a42971a48e8c57e8ab7b8b69dbe1b5e1fba784a37174b997fd813ec5c6279335`  
		Last Modified: Wed, 01 Mar 2023 04:56:55 GMT  
		Size: 53.3 MB (53273002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49beef18431296b3488de0b924aa7dcda58263a5ae78cbcfd1330eafa9103c4a`  
		Last Modified: Wed, 01 Mar 2023 04:57:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230227` - linux; s390x

```console
$ docker pull debian@sha256:36c41e6583a530aab7f2ac44d515c07e996f7cd1ddc302676456497bf7b2f989
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47629365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af87762e3efd2fcb176af8370563ad4653beb26e2ed1e0398b6a0dab3121697b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:52:09 GMT
ADD file:a6e58123df4c8bd45469178b62ccb1794d474c9ad69a1e3b7fac1aa9721e8c69 in / 
# Wed, 01 Mar 2023 02:52:12 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:52:29 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:89825b03aca05d3638ed276b9a89e412e369e6edb8d1d76bb1b754dbc90884b1`  
		Last Modified: Wed, 01 Mar 2023 02:56:19 GMT  
		Size: 47.6 MB (47629140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d39d7f48888cad9a4b88136b3ed2d02d0c1e9a7e0914064f19733eb13e758fe`  
		Last Modified: Wed, 01 Mar 2023 02:56:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
