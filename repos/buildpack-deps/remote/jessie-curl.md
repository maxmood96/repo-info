## `buildpack-deps:jessie-curl`

```console
$ docker pull buildpack-deps@sha256:1d130c9957290aa7fe5b30ae99cf5b23e6a8d1807dc42a75528b828de38d355d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9c03cc1d3e1d8b740a1a21b596031bcb8c34b7f5288c08b3cba309c34282592a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71936674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ffe66d54be973f7c35124f35888d421014eebf8b3f9493b5690bfc8bb95b9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:20:54 GMT
ADD file:63fdbdcc45a46a993700d252a6f9652db8ab25688daa8bbceaed90b73b2654cf in / 
# Wed, 13 May 2020 21:20:55 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:31:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0bc53e9ecf017dd9c8c8ba0c497d08e2d7c04f4a57dfce491d755cb37613f58a`  
		Last Modified: Wed, 13 May 2020 21:26:59 GMT  
		Size: 54.4 MB (54390659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf82ca715cf8b41a88bfb26ad7225ae77537b5999a2f9a3ed1c430b19bc98d`  
		Last Modified: Wed, 13 May 2020 22:46:29 GMT  
		Size: 17.5 MB (17546015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b6f3012cd03ef014e3fb2a49e92f488a66b520384e32061e6d3b6cca9709d18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69619315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0801eda1228a5e6d493c654d385deb0a4694eb777d419e60e2ad8a69b771517d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 14 May 2020 22:38:25 GMT
ADD file:63b1bfb335518fc40ecfe92c179a8d32d00b3dee86ccf70751c74ed2ca14cd28 in / 
# Thu, 14 May 2020 22:38:30 GMT
CMD ["bash"]
# Fri, 15 May 2020 03:47:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 03:47:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ef4eb1ad38349445de10c8a3682121a581770f589f1a35b7cb327b49bb1797d`  
		Last Modified: Thu, 14 May 2020 22:47:16 GMT  
		Size: 52.6 MB (52582082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303f3d44466578cfe6461e4b482b19224356c7b6537b39780b2e75a727ff8ed7`  
		Last Modified: Fri, 15 May 2020 04:03:29 GMT  
		Size: 17.0 MB (17037233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9c140de246f523d9b93ef731736ccff2e34f2b6c641a3b07db2305e3233f86c3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67028362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a406ba0e5b52ef46103d8123ecbb58ab3a1897b5fb3a47459e4adabcd4f8533e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 01:00:40 GMT
ADD file:a56bb3e7bad583ad3aa641fc5aa4f91db9848e13388179a63b14ab0aa7fe06dc in / 
# Fri, 15 May 2020 01:00:50 GMT
CMD ["bash"]
# Fri, 15 May 2020 10:38:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 10:38:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2cbbcc58403b5ede472aaa750e8ded783a6a7d6c87b217ae8713700515dfd33`  
		Last Modified: Fri, 15 May 2020 01:11:43 GMT  
		Size: 50.3 MB (50304981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f880f61061969936f29c8cc4a0b12ac569f2e4d7946b61d7f077d65f13e5c4`  
		Last Modified: Fri, 15 May 2020 10:58:53 GMT  
		Size: 16.7 MB (16723381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a00b89c28e14a579a1378577e40bde0b4f30db27a4942012e1176fa7e2993847
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74464558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6823e6411ecfe9c33f8f855c9a1f29513637f3dea29041299121f18965d2de97`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 15 May 2020 07:08:25 GMT
ADD file:4f7aa7ecb1a9f0f641f4c7dfe0e5360a0705c5e0eb159391b79bec0e4442bc34 in / 
# Fri, 15 May 2020 07:08:26 GMT
CMD ["bash"]
# Fri, 15 May 2020 17:11:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 17:11:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6277e17fa0a21fe6d4617d7259f00c2649972514e9940fbd56cb6d7b75e60de5`  
		Last Modified: Fri, 15 May 2020 07:18:45 GMT  
		Size: 54.6 MB (54608707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5e945f79d261702a2e4dcb64d114abca64e1b6503a3b336cc15a1c68960260`  
		Last Modified: Fri, 15 May 2020 17:27:52 GMT  
		Size: 19.9 MB (19855851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
