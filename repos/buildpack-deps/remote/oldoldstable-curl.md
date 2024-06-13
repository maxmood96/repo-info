## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:7d05c913226d1bd2e8d019d03ed34310c3742f30b818f54fda97ee8d2a9fbb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c8aa318418d49b4d9865955785ed695ac8713243513a61590382ecb24536dbfa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68243796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2bd1dc75b4020f60a3d38ac2925a2f5ffae2211bbd00ec5d3c934633b35332`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:28 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 13 Jun 2024 01:21:29 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ab8bed435ee0e35413bb45d14dae2283dc0841644d881be35089debdc88cc3`  
		Last Modified: Thu, 13 Jun 2024 03:51:25 GMT  
		Size: 17.6 MB (17586423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2b2b08e5f7d65e57a63584b81a2f05fc6772eb7a7f1fa2d4c1ddfdd33d82e8e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62346851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13269db2769cd336ff6d9cc88c9faf8953c1c9907361cef468f271064f526437`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:09 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 13 Jun 2024 00:58:09 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde0a02dfec0ceee2c7c23d86d1a306cffd3a1c9b4907db8b4fa768c14abd3ad`  
		Last Modified: Thu, 13 Jun 2024 01:35:26 GMT  
		Size: 16.2 MB (16216998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0a12206ccc16be1f39097d53710a573d58d225fb96770065f783ac17adf5dada
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66910301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28be86697782ffdff28be275c56e51b574c799aceea87e8c6e2e5de642b36331`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:13 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 13 Jun 2024 00:40:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0606e294c7cef3e3fc7bdc4e83c5d17bd0ef8ae487db37628efb49fb6a03ed2`  
		Last Modified: Thu, 13 Jun 2024 01:32:04 GMT  
		Size: 17.5 MB (17457043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aeb938e48735722eb9cff265ba97fbd08b28ec796222f5c1aa450f6eb0a0d3d1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69518207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e623017bf02e26de81c186a51fa3c6c450384b948113c06ef36885c744a4d9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b199b6fd9cf013c26330a6ba185ef8be1adf3ec49220a3d9f496e533501402b`  
		Last Modified: Thu, 13 Jun 2024 01:21:27 GMT  
		Size: 18.1 MB (18098294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
