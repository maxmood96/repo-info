## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:5689159a8226e5752536b3f33048c5d1d4002df39f34f542cb67046eb4cc79cb
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9c75b7563b930bff763dec4ea7b9f97261b6d7aa446202240ba8ef534e5ca738
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76075117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdddb18cc17a290f069ecafd4676bfe129e5f2aaf4a9b7a28cf96ae52cc8ce1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:37:59 GMT
ADD file:8ad3e26aeda90bbd087b64f3a0110c8f2e520a774d62a26d5aeb7c5006e472ca in / 
# Wed, 31 Jan 2024 22:38:00 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a946c083680d9a81b8eb8383bbc21cd34444b1c5f3212c5d3fc463e0220d7b73`  
		Last Modified: Wed, 31 Jan 2024 22:44:39 GMT  
		Size: 52.3 MB (52283197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aaa07716edd95aa6e78fbf886a2b62004144888c2eb3728580637af2de7642`  
		Last Modified: Wed, 31 Jan 2024 23:36:36 GMT  
		Size: 23.8 MB (23791920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:df7c9595206514a99d2f1bd89d012f4e3721ac1bca68b8fa08ae914590399d81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72133500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a97c53229b5026c5850603dac3341aa7c22673919291795678b49880673df0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:08 GMT
ADD file:7144257253ce293f694d917fb06ea4d03cb3cffd94c432e47fa5a77e03a5a2f7 in / 
# Wed, 31 Jan 2024 22:46:09 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9be7d01dbe3e5ca74f21aad18f318e9da338902efa0bdf09221df8cf061d6b3a`  
		Last Modified: Wed, 31 Jan 2024 22:51:27 GMT  
		Size: 49.4 MB (49400791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a34997ca134aedbce87b0387fb6c33340c58bb878c2ee87be402220de4c0f68`  
		Last Modified: Wed, 31 Jan 2024 23:26:16 GMT  
		Size: 22.7 MB (22732709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:93b651595e2f60da0d3719b391dbfbcc48e323e5d3ab05a9ee82584bbf879b3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69166681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e161c2fd80f021232959d9b8eca8f6d8326eed584e9a39d452e3d983cbc3e3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:45:43 GMT
ADD file:2578bbd6242f569b630ed2a8dbbe60a6317a1fd910aebe4814313b4c0eb7a482 in / 
# Thu, 11 Jan 2024 02:45:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d77eb11f48fd53e8f4a4cad655e31f2fb5f91177fb35abe347a055a3352eff1b`  
		Last Modified: Thu, 11 Jan 2024 02:53:33 GMT  
		Size: 45.1 MB (45063448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37916331c99d3b698aae6553fb6c2a2c76d2cdb8dea2d3cc6e825c690f03420`  
		Last Modified: Thu, 11 Jan 2024 03:34:33 GMT  
		Size: 24.1 MB (24103233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f94442107673ba98dce40ae18bb0c5157589f8a0a31969039f0f47ab8966952a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75698646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f425a02055ba9a29659238a7d2d0ecec6c60512085fda16ab27c4c4010774c04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:46:18 GMT
ADD file:22615a550fb316cdf09ee3c185139fbdb9bf6b776c7f96bba26ba5cc5b14fbb4 in / 
# Wed, 31 Jan 2024 22:46:19 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b24f8e2b921fe314282df3bbfa20988c1046ee499441de80fd5229551987d1eb`  
		Last Modified: Wed, 31 Jan 2024 22:52:31 GMT  
		Size: 52.2 MB (52161387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3734a145b10aaff86d0b31ab8c862448f17bd19fd0bf41ea74f065b5217e8d0`  
		Last Modified: Wed, 31 Jan 2024 23:55:53 GMT  
		Size: 23.5 MB (23537259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a5f681bfc51b9fbb37b5825f5edd3c78d648e5e6b96c961f114d9bdba6db757
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78011698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c048c496b2873336578aa7b7c5d880581b7d6776b96ef8b295414496db2ccc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:41:43 GMT
ADD file:443c10cf2bd14299f3b496a80df4429c5642d898fb2f3e8c184e8c4d58fb8cd2 in / 
# Wed, 31 Jan 2024 22:41:44 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c71e0026d29ede0429851d35323a9a769fb82ad7760740b559b172f3789ae3b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:09 GMT  
		Size: 53.1 MB (53140039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e20811788aefb929a0e339e49aea232089bba4dfdd96c9f7d13061e0608071c`  
		Last Modified: Wed, 31 Jan 2024 23:50:35 GMT  
		Size: 24.9 MB (24871659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8d8f8572554c24a4a5140ef38ba287518427e5385eb62996695b85aed096bad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75538201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca7f9fefa124774b1983005ef3a10453f3f34b181db0d117219bad2773bf343`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:18:24 GMT
ADD file:f8968c17bd3825e4f058fd68c683a3c699e06368b69577a14d575a0c3ac70e6c in / 
# Thu, 11 Jan 2024 02:18:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc5cc64b8a2f7c7d0c78917ac707955e566c39f9c62003870eb7cd32f7b23a5f`  
		Last Modified: Thu, 11 Jan 2024 02:30:01 GMT  
		Size: 49.3 MB (49333270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136a6eeb1b81bae44e0e846833442693a689a375fce576961be0a2c167f5f861`  
		Last Modified: Thu, 11 Jan 2024 03:34:44 GMT  
		Size: 26.2 MB (26204931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:118430b1869f01f710d0c4107bcf6c221a7afd930c73ce730bf12e95fbd8e2ca
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82391924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f43854fa4a7022ab1f801e519f2be0edc86e84bf3ae9dae0a8328ce2f94c4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ba056f52a3a3f9fb8ddeab8c15f4923d3aee8ca28982082fee3b8e7078539e`  
		Last Modified: Wed, 31 Jan 2024 23:51:34 GMT  
		Size: 26.2 MB (26193139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3398a38e8165291e04adf7d360035cf102c95a23b69e951e1268c9ae228e0500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76291680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514e2d2dca99e46bc3c8b4c1792e00a3006331ee6944d40330830ca21526cf78`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:25 GMT
ADD file:3ce2a6c625c267468f6ecc7899fd855c1705b7efb767d466e8b5e859b1047897 in / 
# Thu, 11 Jan 2024 01:48:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:15:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14c1c69c5e90f50e1791d192ea58f134dbc8ecc231a5b815d4c7ee99ef3a1ff7`  
		Last Modified: Thu, 11 Jan 2024 01:53:03 GMT  
		Size: 49.1 MB (49091863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3694e83d440b396cbb77938e6510f4437f21e56dc3bfaed630e6caab9214d`  
		Last Modified: Thu, 11 Jan 2024 02:23:52 GMT  
		Size: 27.2 MB (27199817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
