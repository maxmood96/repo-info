## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:8c53a7e0190d12012da2b972d5e6d6f9899f507d976381246f4418eb7d8a1d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d6033b7f2d2dc5f9bf1860f5e59ebf4d4901774a9a6ac1d918ffc7213db46df1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120137666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6549d95b040b11fe6a80c17ce9911246b5c40ea472af8a5f819e387c70128c94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:28:36 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 14 May 2024 01:28:37 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e7d6cb6a5235443faadc8d241ebb270739fd828ca9f0b78c63a1e7f36f8405`  
		Last Modified: Tue, 14 May 2024 03:06:29 GMT  
		Size: 51.9 MB (51894320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:89e831c74e06f0da076ba1cd9b94ea39b4cc812f83a01b73cdb45f8117719ef7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109758069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629a02dec12f34ac8b0e7d5296927fcaa21462913bb2277cf7d4de351d86b326`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:09 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 13 Jun 2024 00:58:09 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:26:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:26:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:38716c4e5c9c098df6d6fe31c91df92948117751c7c1013c686dbf50412911c7`  
		Last Modified: Thu, 13 Jun 2024 01:35:42 GMT  
		Size: 47.4 MB (47411218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:70b5b500a26771201bf14d42d178c1aa5947c2180ace836d958968d87e98c8bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119141852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a854abbbcc018be755cf89aa2c6799fb1ebbb42dec58ef32d1755febcf79969b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:13 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 13 Jun 2024 00:40:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2afdcf6433347dce5e44f4ff0bc3de90b44a9fa538fa39a22d9b21f9ee5365d4`  
		Last Modified: Thu, 13 Jun 2024 01:32:18 GMT  
		Size: 52.2 MB (52231551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aaf4ab111ccd4cc110ef841c71d265dbf97042efa29841b0e1ed4b55d2e7f083
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123009911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bb6af7cbe4b117b6cba60a1c63815a41dc0add378ef6c1fdecc5cc66648686`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:29 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 13 Jun 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:12:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7aa8cbd7f32e12d211b1f55f9163945f9210759618d50cbf096e4b934b9cfb2b`  
		Last Modified: Thu, 13 Jun 2024 01:21:46 GMT  
		Size: 53.5 MB (53491704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
