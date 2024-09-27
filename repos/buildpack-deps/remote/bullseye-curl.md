## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:14645e4afe63e502131efe1cfd7e843778395528722ed4782c9ad8e48156ded9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:493c3a47ac40dfb1b98b81aa90975efaf13260da7541c93f07942965bdc90e80
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70845705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa31de3a8326a44ac072e5b372515ac96493ac4f6d6f00204179bacdcf7b0400`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8ebfacf3feed4218f9e12eb5cee975a5057d03049a1b15398e9fb5a28fc1d300
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67958471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a482f2c7d653185b09ffd82af2b1df92db3b06ba2b6b043cd2a6ac064bc809`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 00:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af64ccde22e77ee4dbfcddc6165730a7acf92e30572bc7ca38ce8823aab8bea`  
		Last Modified: Thu, 05 Sep 2024 00:25:07 GMT  
		Size: 15.4 MB (15375718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0f8ea823454d8e07af80adfe6fc4d2ece17f96c194bbd11f22b5d22e0073a656
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffd1af5abfc86f8ab9ad2686f3ebc030fe4608cdf6e6facd16ddfa2d99ea583`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:842922b68678f1fac48d835049726c5398604b702ee421f40636d9e459d56491
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69483562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e86dfc5995a61ab1d4efcd1df3d5327b56e7039fb319cc94e5e6684cba5247`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3d8cb4112d4b04633bb393b5a807b261208d72c1a3b573b4a4bcdd6eccb2cd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72344582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5514e433d3d2c001a6ebd4510c3dc44fb6f0134f3609a97d5eb8d818ca95237`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:11 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 27 Sep 2024 07:23:12 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:00:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d8f32e100154b6cafdcf65ece0dbebfe80d8db1ef99ba3702f31f7e7492e8`  
		Last Modified: Fri, 27 Sep 2024 08:08:06 GMT  
		Size: 16.3 MB (16268079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b0c44eec3cf0efabb2a856de91bc08e41348c65692be30a61a648130acb1a606
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75716340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531a5affad292f28c15e65049ce4833d4028619916ba23511818f7f815703a5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:03:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e76b45808a7b15592738cc59f261bb4109d1d280c5fa410f157dd270ddbf8c9`  
		Last Modified: Wed, 04 Sep 2024 23:14:50 GMT  
		Size: 16.8 MB (16766250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c4f581b3e295ad448ff126d8e1c343741cd89f99a5da30ec6876f5ccbb34616
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68959590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902b95c547ebd20c6b67b00d60bb7f0519e8220ae8bebb7034450158166ba3a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:05 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 21:43:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3deb07fb0f47d9daa6d0bf809dee66d9c90207821b4a8f6c849f8287efdda0fd`  
		Last Modified: Thu, 05 Sep 2024 00:00:53 GMT  
		Size: 15.6 MB (15642390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
