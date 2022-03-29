## `buildpack-deps:stretch-scm`

```console
$ docker pull buildpack-deps@sha256:19e609a8a7669a834749aa85cf96f99b4bde31d79b7fb9e8f02d50e325f6919c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:stretch-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ff09cd2bb2c6993aac10c07aa1844b010552cc23f3e879c09752fc89afa38d36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110838159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791a1a9069177ddbaa128346d5af8b5f72e6d98b022b6c284b7654fe469ce3d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:34:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628acdaf85032c817e9eb7f4749b887f3733c8c590d2e3c2f396f2051406557f`  
		Last Modified: Tue, 29 Mar 2022 17:41:47 GMT  
		Size: 49.8 MB (49765499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:71ffbe15c3b081c0f4ee9ce90707685c3f66a7b3a5bab14d1e6f7824af4edae3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106626237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19832e0ce3b29a5810a63e5841bbb0844498386c7f422132eb495146394ac425`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:55:32 GMT
ADD file:4e79cc43996ddc8062073aea4d6352c3ca3c736e9b09f1eb440f913d5a52469d in / 
# Tue, 29 Mar 2022 00:55:33 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:56:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 07:56:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 07:57:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a58c023b263eaa1973763831b149ed127bbe67ee8cae67d60e261db1e9d54b63`  
		Last Modified: Tue, 29 Mar 2022 01:12:11 GMT  
		Size: 44.1 MB (44123307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c0117421f3f6b9a01b30e38d3562bc7a42dc789c5af5f80877e67cd59edcb5`  
		Last Modified: Tue, 29 Mar 2022 08:14:25 GMT  
		Size: 10.4 MB (10352487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c612024a40834a1cb0833f65b0e86ed44bcd14476cd83a108eca13607211c477`  
		Last Modified: Tue, 29 Mar 2022 08:14:21 GMT  
		Size: 4.2 MB (4162114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85145e2987592dd2778a62d3efaf2f38a56d30e11db945369406880db586d665`  
		Last Modified: Tue, 29 Mar 2022 08:15:12 GMT  
		Size: 48.0 MB (47988329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ca2ad409efd851ac41520dd152886a24a4d191e22cc9ee027ab8c98f87aab283
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102157904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ef572c435fec362bd5afc34c0d5b6129d4f0930006521c974c1fffaa38e84f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:25 GMT
ADD file:e869f7223f16639eccabff7b2c6a85a7e6b075d0933c31f2fecae79c1c26d5be in / 
# Thu, 17 Mar 2022 09:36:26 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 03:04:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9f775cd9058b832779f6c0dd1ca0fbb1417961dd87ca3ba6200f41aa283371b`  
		Last Modified: Thu, 17 Mar 2022 09:53:00 GMT  
		Size: 42.2 MB (42151366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5c76f62b4a80636807fcffcd72fa68808c0faab499371e9e49ea3805cb8de8`  
		Last Modified: Sat, 19 Mar 2022 03:37:42 GMT  
		Size: 10.0 MB (9956816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe67020a39019149bd81805e6b89528643f4464d33964fe8bd1c39ed3c68dfd`  
		Last Modified: Sat, 19 Mar 2022 03:37:39 GMT  
		Size: 3.9 MB (3921814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e702730ae6d526889d4f3bf7fc8325d0e4dc614242f04fc606d1134abb2bbb4`  
		Last Modified: Sat, 19 Mar 2022 03:38:26 GMT  
		Size: 46.1 MB (46127908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:746b5a66020956ca525230183ae9b5ae6d5552ce9466d23d8ecd6a2d08626911
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105040790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428e653e4dda6809715abc7b5986f10afd11234d89a67efce273512ff2fddae0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:02 GMT
ADD file:eb07f8b0889bb0b4499fbba08599cdf04f3efaafdec453e96fa4175723f4fec1 in / 
# Thu, 17 Mar 2022 03:24:03 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:15:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:15:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:15:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0d6ecff05d590b97ebc357d19bd439c17d4142359ceceb25dda468284e978583`  
		Last Modified: Thu, 17 Mar 2022 03:32:27 GMT  
		Size: 43.2 MB (43213043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf8187d7f23f7722584cf9a7359b8e6859ca891c112d0398819cecdac7fa008`  
		Last Modified: Thu, 17 Mar 2022 22:24:30 GMT  
		Size: 10.2 MB (10217652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9ad8247187d77aea7d1a40486c48551a68a63e2b6be93a43c47cc27d726beb`  
		Last Modified: Thu, 17 Mar 2022 22:24:29 GMT  
		Size: 3.9 MB (3874519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b13fc30419a0a45924b8386c468bbaf3f0ba8ebcfe179f82d46e2317ff28066`  
		Last Modified: Thu, 17 Mar 2022 22:24:48 GMT  
		Size: 47.7 MB (47735576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a0a0fd2c430e6c5d96b9744ff159e9d1802ea876df0616cc312682fe1ec3c7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113342530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69df42b1ddf20b3c76d35eaa34afa6ce6b776c2568f16df4ff5dab452d5f81db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:18:34 GMT
ADD file:60679f2ddce5e36577f1a8d320d5221029cdbdf145c7043ae099312d74451d17 in / 
# Thu, 17 Mar 2022 08:18:34 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:32:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 14:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e21a7d1d60294e341bf8cde8b67cd64035b84fd968946be519fd79ec45925ece`  
		Last Modified: Thu, 17 Mar 2022 08:28:24 GMT  
		Size: 46.1 MB (46147889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b8c8176f5881909d36b8bc4d5ddfa2a2b80e8161e45e01b75b1d367bf2bb8d`  
		Last Modified: Fri, 18 Mar 2022 14:48:17 GMT  
		Size: 11.4 MB (11360144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeaf0a804dd2d29797cd2ba58b689e56b24ae765d0e8a4369f839bd12b7dbde5`  
		Last Modified: Fri, 18 Mar 2022 14:48:16 GMT  
		Size: 4.6 MB (4565572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820a1f9ce0df9b3396ab2aa573cea32bd54f0e24d6efe3761805c1eaa8bb625d`  
		Last Modified: Fri, 18 Mar 2022 14:48:41 GMT  
		Size: 51.3 MB (51268925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
