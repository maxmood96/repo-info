## `buildpack-deps:jessie-scm`

```console
$ docker pull buildpack-deps@sha256:6434d30659483952c16fd6aa5a3ff03b5f275d470da9452149511e8806443c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4a07904be46981c591c331f43db673d9a8123fbbac19f1cae264b558283a7b5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115268936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0c799d23ebba72e147d6c638f3b7f8e671df4842ce095f2055f770282d94bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:15 GMT
ADD file:00e3c0ca649cf82da02cd7fec7b3121205c2c54c4569209a2212c4924c73d5a9 in / 
# Tue, 31 Mar 2020 01:21:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:00:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:00:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 02:02:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f27d6ed8cebc4be4a992767cb74cd433e5e145ae55c57e9e913e47d315b1dbdf`  
		Last Modified: Tue, 31 Mar 2020 01:26:56 GMT  
		Size: 54.4 MB (54389951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2886394fe026f40712d4f22ecfe40e26911d758627d04e684d9d5ff5637296`  
		Last Modified: Tue, 31 Mar 2020 02:10:58 GMT  
		Size: 17.5 MB (17545721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c79486f9007497ffa7c18e154e42d395db78950bb662ad3788d208c2b7b9599`  
		Last Modified: Tue, 31 Mar 2020 02:11:11 GMT  
		Size: 43.3 MB (43333264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f166b1eabf8b766932c6c284dbbab2e03aeb4e3493c90eecb963eba0e1e4b771
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110775747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0677629aff0689f7b8de6956046980ce220b43c6ee685c6c42292be7c6943649`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:48:18 GMT
ADD file:dfeb6a347568f49dda331c0a3507c2f67adbd728b7d05bb73981892d7e1a602c in / 
# Wed, 26 Feb 2020 00:48:20 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:42:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:42:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 03:44:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ecda12258fd08534cd1becb346cca0f577a29d87b9a0e10f9506312ca70a556`  
		Last Modified: Wed, 26 Feb 2020 00:59:47 GMT  
		Size: 52.6 MB (52579149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347038a62fb32cd535e9daedd7ec90325fb85dfe551edeffed203385b1fc4a58`  
		Last Modified: Wed, 26 Feb 2020 04:02:38 GMT  
		Size: 17.0 MB (17036652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a36680cec80c39312e70464848dba16bd184e4d413a2439d6c54bb9f4c355`  
		Last Modified: Wed, 26 Feb 2020 04:03:06 GMT  
		Size: 41.2 MB (41159946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:53c1e278975c57852a1c16b8cd1e437cfd7935b10053c943e4fc2bae8b57bec1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106801497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862ee7d6e6a6f0ced10fe2254acacb55741fdddc612f9e1efef3f28d5284f2ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:52:39 GMT
ADD file:a467dd7304add7a1979638d51c2e28f9355aedccfd4727532a90b0db7fb1d9d6 in / 
# Wed, 26 Feb 2020 00:52:45 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:16:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:16:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 02:18:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:10fa2b45efadcc8561689d641256044af7890a575a625a567d96dfbbac1c5d05`  
		Last Modified: Wed, 26 Feb 2020 01:07:57 GMT  
		Size: 50.3 MB (50302762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc01a96123ffaa0c4c0e711f6d51ee89062e113913ee9965abdd34e60170cc3`  
		Last Modified: Wed, 26 Feb 2020 02:35:03 GMT  
		Size: 16.7 MB (16722914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c627136ee3d7a33f5e4b63afd27dbb92239f6a01ab462de1efd491552191ee2`  
		Last Modified: Wed, 26 Feb 2020 02:35:22 GMT  
		Size: 39.8 MB (39775821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3f3669c2138682b851cff1f15a701ec259dd8d2dd062c9d9e6c3a2abc176915e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118439288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28958bfd6a4a0fe1d7fa3b1f840c9d487eea0e68440c7ac40a905640fe4e2e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:59 GMT
ADD file:ee61b11b0132f3aa493c1fe2d59c8c7225e31b99c52f87f49a49512a80a203ae in / 
# Tue, 31 Mar 2020 00:39:59 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:15:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:15:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:18:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f263b30518dd64881c8ace989042a8efd1273a1175e0dc751ca62444e9f2ff81`  
		Last Modified: Tue, 31 Mar 2020 00:45:52 GMT  
		Size: 54.6 MB (54607453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f5a9dd559c3a0035cf2826e46fcddd2f78535e67543e52c97156d68f2b89b6`  
		Last Modified: Tue, 31 Mar 2020 01:30:29 GMT  
		Size: 19.9 MB (19855790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54e4a737961a715ee92034bb56cf77c442fa2e42a168bbdea4cdf47ae036de6`  
		Last Modified: Tue, 31 Mar 2020 01:30:46 GMT  
		Size: 44.0 MB (43976045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
