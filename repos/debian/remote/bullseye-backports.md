## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:f258e62e69d8029b638dc731aaec2ea7bb0ca2b6de718856a8bd00deb3899b90
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:8090028eef518d02a09eef54903dddff5f203c5718f4edb782bd5385c26ac4e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55058128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44400edc0d34b235db215062482e41f01dcaf2d3f1deadcf7c5386f422ca5bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:21:50 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae56d1b7eb033a69056db7397e300d893acfa7134ec2898a27677c0f29d8c990`  
		Last Modified: Tue, 21 Nov 2023 05:26:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b2e56dc820ee87f96bb98b347ce80d4c51506ed95d4396857af52e8f09c6bb1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52563146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69dd34f99be067fd3159fa3e6e7c9514069fe4ae1ff6130bb38802f3f8fcfab9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:01:00 GMT
ADD file:a5c8bd4b0873bd9ad0402143df41b5fd89c50bd24bb071b7d010919e189d88f9 in / 
# Tue, 21 Nov 2023 05:01:00 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:01:04 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7378d71ea16926a061a2edbf0eb3dd13563fcb3ba9cf139c25e8334b36db1adf`  
		Last Modified: Tue, 21 Nov 2023 05:04:15 GMT  
		Size: 52.6 MB (52562921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac1b90bfe837e598126e3d6ae6d2e11ef7ab4c259929a7db280ed9e5fcc5b25`  
		Last Modified: Tue, 21 Nov 2023 05:04:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9404712c5bde071e817a2a62b66b371dcc8213c30d6723b0d46917c6a5121755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50215879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e1cff3fc7ce7787cbfa8c73a00046e5c81ee63d8d5498b30b9a4b8d5e19292`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:54 GMT
ADD file:ed8d88d0476fad37879d872d61d05a8cffff35609566f080f78bb882d1bae26b in / 
# Tue, 21 Nov 2023 03:57:54 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 03:57:57 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1dac19092a737e476f9b096fe28463512ae21c4f596dd2f8b84d62530416dffe`  
		Last Modified: Tue, 21 Nov 2023 04:02:11 GMT  
		Size: 50.2 MB (50215653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3542c93a14f8d85fec54ada9b31e1c77cf6b46e93c90c01929bd7c60c9156f9`  
		Last Modified: Tue, 21 Nov 2023 04:02:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d7803770587bd42ec2a630b071037359c843c0290b8ddeafdcd159e14f3fe717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53708098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10352a2c4841d4ebcae15b603909bd1019126ab5bbebd98ae09fbdad99efacf1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:27:16 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f9be83c54d8d4d4f70984c731dba6e9905486c4613cf048335172669255c11`  
		Last Modified: Tue, 21 Nov 2023 06:30:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:f79fed8982287b93bfa652b8f6189c84b1e844c0eb64876e44438f55205ea353
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56046526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300a097870e1707819547f6bd60ccb50364313e9a2a4815755d7942fd472135e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:40:03 GMT
ADD file:54170328827ccc52692c964f0c45a65ed6efdf39897f2c226672fdf526f3c412 in / 
# Tue, 21 Nov 2023 04:40:04 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:40:07 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e33c1468a29e45636d4d9529b663048f7e8aa83ff428eb0681253bd4200e23ec`  
		Last Modified: Tue, 21 Nov 2023 04:44:57 GMT  
		Size: 56.0 MB (56046301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6682ab21b4f7a30962402b064c63c096200ae1cac5f07d9a183f09404dd7a8`  
		Last Modified: Tue, 21 Nov 2023 04:45:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a10caf26cc34898556438957c79f9aacc618d52fd7c37f978196b53d83e57b4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce938debce1a8cde88c5db2fd19aaf2e4e9b7d54f5d3eb252da7ff6b37526bf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:10:25 GMT
ADD file:dbfc3d226166089c4db0c154fdcea8049b8758c6812f1c397dec1444985e8557 in / 
# Tue, 21 Nov 2023 04:10:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:10:41 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ca31218601e95f4aafae0dcadda7600aeb04db374e1e829d5c123f8033ba3472`  
		Last Modified: Tue, 21 Nov 2023 04:21:21 GMT  
		Size: 53.3 MB (53289162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a4fd5de915982c310c1e271a6e6c861a2daebc7ef32c92230e799b69babbb8`  
		Last Modified: Tue, 21 Nov 2023 04:21:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d3f4ec962dd44a4f434747dc94b43e8548e4d72789a80844b92bc1f27a0668f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1376e4b08d0aa73ca22ae51e1c270fc11372e7c2e0d3a8303d0548a1371dacdc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 04:24:35 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1de7384ea40de6440e18c443aeb36a7d0fa86cf9868a758b7706dd6316bb89`  
		Last Modified: Tue, 21 Nov 2023 04:29:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:325128c05582eed1f2c7559fb47eaa3e5187f04fae37d52824544834b016b9c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53296624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16bbbfeb0919637374153d2c03b32ca939423c0116ab0199bf5c1d2ba2d986f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:52 GMT
ADD file:b0a8fd50925b3555a0c10177e65551cae288917f9bad8fb4728ec83cc0765afe in / 
# Tue, 21 Nov 2023 05:05:01 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 05:05:09 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9488c1539560318cb45b39150f91e365b928c0a246788663f5c72d185864bd3e`  
		Last Modified: Tue, 21 Nov 2023 05:10:34 GMT  
		Size: 53.3 MB (53296396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7e5330deb05f184eca9b5e6cf81df03a133a79f3bf6286eeb6e05a46beb4e4`  
		Last Modified: Tue, 21 Nov 2023 05:10:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
