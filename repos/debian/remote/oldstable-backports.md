## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:163666c012cfa25a13cbe007ae5d239359bb8a29de87a03935ba516858605a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:41277eec93e0986eda3d3ec7c092bcd09250c772529e5dd6ee57a58d31f3789b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c31bacedd467bdd19145d0b770e14ec71378b303280be1fc1a2e3bbca98878`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:35 GMT
ADD file:1346760040aad25f5016d1e18017c03365c1868d0117faf968e1540cc36dee0a in / 
# Wed, 12 May 2021 01:21:35 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:21:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:112ad5ea04834916ec18c651cae89223b7bc1791166c26c362cf2df9039473a0`  
		Last Modified: Wed, 12 May 2021 01:27:49 GMT  
		Size: 45.4 MB (45380104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52198b8ff9fe9411748150c726278ff5da8e753fa4a1f8dc457e6d0094dfe6ef`  
		Last Modified: Wed, 12 May 2021 01:28:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e396c3207fced013f938a705a72b697ce04926886bd7afeed0879dda0c4fe9e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72afc9ee9def68573afe690998b70b225e74b68a55d0edf8e0f3310ef2cde632`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:56:19 GMT
ADD file:9de218aca97a215df0993e557a3c1ac0364a08743b1083864d30c1ea586ec75f in / 
# Wed, 12 May 2021 00:56:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:56:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef3a483c68def455cc14d66ef31eec707cee2d23c3f5f358f79e131edb292ed5`  
		Last Modified: Wed, 12 May 2021 01:10:49 GMT  
		Size: 44.1 MB (44092109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19334d9da7b53a1f6b10dc087c0321a94f39a7cda770746d6c501a79a10a75a7`  
		Last Modified: Wed, 12 May 2021 01:10:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fc6122c07ebb472dd5cb059577cc16b7f75d73e3215a6ab6fcc09717aebd424a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb84c7c21445eefc7c71e6b93b78c003bb5d595d91a3107b9006782e1e6e3ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:04:42 GMT
ADD file:0aa4e949cfead9864e288775f0a9c8ab982c4017626c66cedc428b96dae4de46 in / 
# Wed, 12 May 2021 01:04:51 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:05:47 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:124e493df453ae98368fc827d00d1b8eeb7644e3aaf9ebdd58aece4c2dd399b8`  
		Last Modified: Wed, 12 May 2021 01:19:33 GMT  
		Size: 42.1 MB (42120283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af460b5f7ff72b58803e6aa00a93572c4f47e128a0e80ef49e72715d20d0e3e7`  
		Last Modified: Wed, 12 May 2021 01:19:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:159c47a28d9a50e6b7c20d2312895d7a34e2fb8c60d8fd011873c7d24657d758
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43178078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545ee5dbf4887a84de4c1e5c89c5aa879ac83f4b95234ff177a12bb4111e2d9e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:53:10 GMT
ADD file:9e8b5cbce6bf725dfaf76e21afe9eee77c81e9b544fd6d878e1e68190cba7de4 in / 
# Wed, 12 May 2021 00:53:18 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:53:31 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a629f056faf44282bab78e941dcde71181353bc1e12ab6d6bb4ae39c85a82c1e`  
		Last Modified: Wed, 12 May 2021 01:02:25 GMT  
		Size: 43.2 MB (43177852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7000e9d9aab5ef12e4511057747e94dd758ca3134bc043d75242e71bf6a4f9ab`  
		Last Modified: Wed, 12 May 2021 01:02:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:7f52f39cf5372682e6f1ad8122e7e690654ad22215240aa54a90a699bfccaf76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f69d7733f2b831b911619264ce1b2d82562d9abda1d37a1e9e2ff54b2b14aaa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:40:07 GMT
ADD file:de95eb40860641f63f850d606281b22129ed5dd41055c9936edfd6f0c1bbe3e7 in / 
# Wed, 12 May 2021 00:40:08 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:40:14 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bc111c045f0c7b2d5dbf00c70b31ce157c92cb1a4520938bde38cae2a324838d`  
		Last Modified: Wed, 12 May 2021 00:47:04 GMT  
		Size: 46.1 MB (46098751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f7325b0f61e1187ef3822c7cd467160d3787af17aab01169fbc91938687837`  
		Last Modified: Wed, 12 May 2021 00:47:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
