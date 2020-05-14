## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:882ca8b2cf5e9dca8aac5d6512d5b1b03c890e76088b863d806f47e55d6f305c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

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

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:481a6d1891e69096653072f759eb1b08b64732dbd94e03af0dc4795a3e61001a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69618261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd358e1c8706584378ef579e2d25d69a799f2c7887acccba8416d7d0ee133c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:50:39 GMT
ADD file:621441e8cf0bd677ecfb646d7c54417894fedb89b8b03295c25a4ea0ebefbaf3 in / 
# Wed, 13 May 2020 21:50:42 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:37:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:37:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:535d6dc5159c1d8f20f2d1a86a8433d89941a1933de7a6930246eef7811be611`  
		Last Modified: Wed, 13 May 2020 21:59:45 GMT  
		Size: 52.6 MB (52581076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73189ba1a9ac8eb7f3c4a34630c9eacf6ef34fde77675eed4b21857d50d7a3e`  
		Last Modified: Wed, 13 May 2020 22:56:53 GMT  
		Size: 17.0 MB (17037185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:af29b0d9556b3ad4a3cfae5636c32133518ffa36470a6231befabae75f40c1ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67027553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073b6fecd01fe67cdf75d809db0e261de48fb330bda260fb064671543de14250`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:47 GMT
ADD file:348008ec05929291b5465cf2ea0b89cbd08f4eb55d53f50f37727783e36e439d in / 
# Thu, 23 Apr 2020 01:03:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:14:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:14:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a08cb6362fece7101fb94628a874d1a40b2ffc270a3fcb4fc3f4ed97228fd505`  
		Last Modified: Thu, 23 Apr 2020 01:11:30 GMT  
		Size: 50.3 MB (50304341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4f5614a4faaa521ea475ca54cf68fd7fe337514cb7551af1c9c7d465f0a424`  
		Last Modified: Thu, 23 Apr 2020 04:31:26 GMT  
		Size: 16.7 MB (16723212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:23d6474aa06fbe8fc38ea9c4349fd4184e8cde5a2355023a520848948363d326
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74463694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6ce21730f6557207d3c258ab45ab1ae3f3d9323d72971589f13392980d2e5a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:50 GMT
ADD file:5a51343ededbfe4c380e189c99b1136cd1143a41ea66cee7cbdc3b9b523ac86a in / 
# Thu, 23 Apr 2020 00:39:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:46:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:46:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:46bce17837ebb6f15aa73ef7b5c4ce1f32c9108c2dc291e4af9944c5bb7130e9`  
		Last Modified: Thu, 23 Apr 2020 00:44:51 GMT  
		Size: 54.6 MB (54607867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a64d5974b96b34da72142a0155b10ccf50819700a2fd7d3faf98329ad3808cf`  
		Last Modified: Thu, 23 Apr 2020 02:01:40 GMT  
		Size: 19.9 MB (19855827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
