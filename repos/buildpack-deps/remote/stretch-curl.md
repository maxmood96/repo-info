## `buildpack-deps:stretch-curl`

```console
$ docker pull buildpack-deps@sha256:196b3d01bc361f683625120b3811a31dcf8823600cb2a0ffc0cb36c62bec7dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:stretch-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:163d5a64fa7c0c51860eb64d0cca9189c0b4c55220889ee65ce7cd857f0b1635
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61073462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae58812f064e987538314d076b3bccfd243eb7f9f8142ee47fced60ae3085f5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:37 GMT
ADD file:0d1703dd365e8d6f8625b40addc388cab8f0423af2bca03b0baea5d27f585a9c in / 
# Thu, 17 Mar 2022 04:06:37 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:35:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:35:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d172ccdc78ea7d453ae5fa3feafee94e3837e6f8e282d8501e668329c49551ed`  
		Last Modified: Thu, 17 Mar 2022 04:13:38 GMT  
		Size: 45.4 MB (45427778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f105b7903980816bf5941ec222e4372a54ab3a577c78837ab69c91736c6a110`  
		Last Modified: Fri, 18 Mar 2022 07:07:26 GMT  
		Size: 11.3 MB (11302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ae525c10a70b17275982d1dc19125faa52b3dcf3c595e3f7fb2c22e2a11c6d`  
		Last Modified: Fri, 18 Mar 2022 07:07:25 GMT  
		Size: 4.3 MB (4343017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ceba6b54adb4e06f4759e9218df280b28f7b132277cc39a58a174ed3b2a0090a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58638095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da02dafe4b2a84e14f6c9d9a787c372140c55fc603b0d667764c5be15d2cc5d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:24:45 GMT
ADD file:502df3a2fb53e6d518d3768d7f30f7acc923f449d178dd694170b32a593580b1 in / 
# Thu, 17 Mar 2022 05:24:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:29:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:29:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b98d59bd3c31e00cb09cc21caa721461182c00c580ab28fd0b2403c246b7b169`  
		Last Modified: Thu, 17 Mar 2022 05:42:06 GMT  
		Size: 44.1 MB (44123565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c0ec4a93e05d1c89659316755af8b668a2ffd2770fd1ee5cf48f175621ac96`  
		Last Modified: Thu, 17 Mar 2022 19:46:37 GMT  
		Size: 10.4 MB (10352438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0435fd593ca094788922fe884de2c1d5ca3c31a7fb47190a1d8721b08f1232ba`  
		Last Modified: Thu, 17 Mar 2022 19:46:35 GMT  
		Size: 4.2 MB (4162092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:84ef15c11de920399af76ffbf297e0e35023de04b8b1949005484c94cd2878c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (55994691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641e1ca87ee95a4efcd4b50ea6cafeb8449d63551a778e89c0ecd3a8e47f84c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:52 GMT
ADD file:32b09ecc1f1473cc68b2fe74354febc64a9530d26aa83549020fed06caa8ba8b in / 
# Tue, 01 Mar 2022 02:08:53 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:37:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:37:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:57f32f9fdf459a27691c3a29131c270edd06bf53c003de1f42bb0a6ff8824e31`  
		Last Modified: Tue, 01 Mar 2022 02:25:39 GMT  
		Size: 42.1 MB (42116971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e724a8423f66e29c28d1f7eb411c0fc8b5e925a2dba9d9984b26ba548383e5`  
		Last Modified: Tue, 01 Mar 2022 09:59:33 GMT  
		Size: 10.0 MB (9956523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdac683edae6f35034917112b5fe629e9a55d8911f2afdd7746b8dfba6c1638`  
		Last Modified: Tue, 01 Mar 2022 09:59:30 GMT  
		Size: 3.9 MB (3921197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5cc0481a1d70bdedc0c10e80f7dd37b558d8efb3e88ddce3539b14af4e7246db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57305214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26769edb2bf581cf2034eda01009578d213071340c2b4c2332f983f9789c162a`
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

### `buildpack-deps:stretch-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8f34696f728ea91d90a3585889663f76bb909ac1df985a1514f237a6ea626330
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62022401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f166d375e08bb5bf8f7d46b3fd49d531587ebbf562297de638dc848ab1dd4f9e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:10:13 GMT
ADD file:bc15f0e456e3757963e61c9b01f81ce157b35fb751d837cf7b6ddd9277872821 in / 
# Tue, 01 Mar 2022 02:10:13 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:46:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:46:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4d460050f4b628f05281226d933aa11a10afffc452771e0d9dd815bb6858e254`  
		Last Modified: Tue, 01 Mar 2022 02:20:11 GMT  
		Size: 46.1 MB (46097796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f57a4965e785e81bf52d7df87a7b3b5abeeb384075fef0b195b12bdf3864206`  
		Last Modified: Tue, 01 Mar 2022 05:56:48 GMT  
		Size: 11.4 MB (11359682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc782b42f9af37d9d74bb076c8d6bb03945730f16d04982ff3a85814c557f12e`  
		Last Modified: Tue, 01 Mar 2022 05:56:47 GMT  
		Size: 4.6 MB (4564923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
