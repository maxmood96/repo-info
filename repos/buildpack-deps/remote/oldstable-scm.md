## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:23c13d7e999d140f54ba36b6f53390d1bb269221e17a14e49cf97f9cc469d84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1b1d6fa6bbb9ba956b9ed0c04d65b499f564bb63a96a2d3b6bf7fc84a8216a7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119907902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce71ba17b3e4c960c8bc425b73184e8e53c5f20bb7ac37102b7a1dc05e3aa94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3f93f5ae83b7041e7c477830bc9d94f39a89c4d7b46e3f124b26f9156be09173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109519984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c0cb64af656f18074794932c5384458f7144482507eb4721ad6c4556f7a174`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:48:07 GMT
ADD file:74b52d80515b2979b2bff8c2728f69628ac807640a577b25413dc0b78f4beb4a in / 
# Tue, 02 May 2023 23:48:07 GMT
CMD ["bash"]
# Wed, 03 May 2023 21:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 21:54:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a27c159ac2b737e1d483c37cee9c17e75a5d0ef0c98efbb30d12bd873bf30b2`  
		Last Modified: Tue, 02 May 2023 23:51:48 GMT  
		Size: 45.9 MB (45916301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ec1909c2922a5c6c5bf75a16c5cbf25bf1ad255d06d49cd303cea68327f3e4`  
		Last Modified: Wed, 03 May 2023 22:10:02 GMT  
		Size: 16.2 MB (16211235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e9e4ad2f04fa9eb620f478838a3ccc831823134f31b64b3536a7f760577d92`  
		Last Modified: Wed, 03 May 2023 22:10:18 GMT  
		Size: 47.4 MB (47392448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d433e55f981a544cf40af3c4b35e2ee8f7b62fbfc742f62a1414ed1dd8810bc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118879486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fce201239029033025eb59825dad8f5153000dda8ef5f717918c26861f0835b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:21 GMT
ADD file:a5100e7ed3c2665c1b4dfbb32eb2b47b85783f2a6800e0ae9004db0ce021dfa5 in / 
# Tue, 23 May 2023 00:43:22 GMT
CMD ["bash"]
# Tue, 23 May 2023 05:56:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 05:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5ea482247e9a0d1ae4ed218fb0828063b9cce53822e64fd4621f587ab85a7e6d`  
		Last Modified: Tue, 23 May 2023 00:46:24 GMT  
		Size: 49.2 MB (49238292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b9a832fb21afaa962a9cab69bf1b4044aa29ef4bd4684505838c4c7cabb76f`  
		Last Modified: Tue, 23 May 2023 06:03:52 GMT  
		Size: 17.5 MB (17450452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49fbb768597d28581cacecb6d008fd42c9ce8fe13fb045d488db3f8ac1b8ac9`  
		Last Modified: Tue, 23 May 2023 06:04:06 GMT  
		Size: 52.2 MB (52190742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:acf49c8ddf2fc4cee690ee333ba0be3fc3d205336b712c6c2b388c2131f50101
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122775652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa27fb1e57239b698f7835169bbf1bfaeae0e96e2951552d5e6586a2cd183e41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:39:45 GMT
ADD file:d82a514985e1c8796d6c5572290d84fdff0dc1c748d7d2e469d3066ac0344c5f in / 
# Tue, 23 May 2023 00:39:45 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:59:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:59:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a48e9012f51ff679af95460521da76c7184da775e3adaa39fed65c912ce0a57`  
		Last Modified: Tue, 23 May 2023 00:44:49 GMT  
		Size: 51.2 MB (51205678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc7a25298904d5eca066c7a365d1c5c9fb1b9d6b1e716ae9a27e37b32a4ad3`  
		Last Modified: Tue, 23 May 2023 02:06:24 GMT  
		Size: 18.1 MB (18097872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de809a24a7c935e1db2594ae9d95cd2a19313955c833a1bd9bbef6dcdf11b43d`  
		Last Modified: Tue, 23 May 2023 02:06:43 GMT  
		Size: 53.5 MB (53472102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
