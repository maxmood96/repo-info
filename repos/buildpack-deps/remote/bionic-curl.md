## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:9068113f02d80986baa20d142bf213d714e8f8ec78fa84f0f4e52422882b3323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e1d8c4faf8376dd4483913b372086027b131dc7be7d4675692597fc0a5966678
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36372771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129fbf08223c38de16bf8bc67c4b46cf546cee23a07897342a6b06bb8c10ebf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:38:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:38:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222ef3f2ac944896d21cb971be4b7ec028ac826242cd0451df060b0b4412b92f`  
		Last Modified: Fri, 18 Mar 2022 07:08:55 GMT  
		Size: 6.6 MB (6641832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3f005ad8fda9d934f3bab809914d7cf447e57835543823c59da423475b8f58`  
		Last Modified: Fri, 18 Mar 2022 07:08:54 GMT  
		Size: 3.0 MB (3022305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e5e40504ed9e3e97b0e04d1bed1ee70dfa2af244bc6aad7a27f38a3237967227
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30605227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc3cf87206bd5f8f6e9e0681f70332e4a25cacb811366f004052e60b733bbcb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:10 GMT
ADD file:c60e89df1905b44d4771a78ca9fa8113b55681f00e5bb55e798028b77ce6c120 in / 
# Thu, 03 Mar 2022 21:21:11 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 03:14:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:15:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f04b2e36c59d7fb6bb1129d2ffaff71df9aa51f235875df61b423ebbdfcc1ae3`  
		Last Modified: Thu, 03 Mar 2022 21:24:40 GMT  
		Size: 22.3 MB (22308282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e431ad97ffcaf1c68228dcb4bf9624755667fdf428dac81d5cbd251b22c35`  
		Last Modified: Fri, 04 Mar 2022 03:35:17 GMT  
		Size: 5.7 MB (5712255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c19bea23eeb8e7d57acd3ab7f212f26d69090b55badcd6895f6f6389931551`  
		Last Modified: Fri, 04 Mar 2022 03:35:14 GMT  
		Size: 2.6 MB (2584690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a58612831945616a0bca6b4b6858c38c8bdfcec7eadea2fe0577d91285bd342
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32382303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734b8511b29340aced3d2bfca203681e7237f9c172642a586bc0337315bd7cb2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:06:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:06:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b00c8ed3e482790555b6ba75dc2fe88a431898579874f982bd42af6e94adaca`  
		Last Modified: Thu, 03 Mar 2022 20:16:15 GMT  
		Size: 6.1 MB (6082527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355a1859624fa4241536a77dd88b7f379d0cfcecb8c9d1647065d1fce7976682`  
		Last Modified: Thu, 03 Mar 2022 20:16:14 GMT  
		Size: 2.6 MB (2570125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:11312aba05e1a970bdc16ec6e63fb2876e77b9d4cdc35fe0c419407567eb40ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37344053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddf060cd05caf64e6c1ae34cff0a29e69a1d618cff630d4f99a9c80b95e177b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:18:47 GMT
ADD file:2ae34e7bffe3a59f3167a286025a093609188772be7b14601867a334bb3c0166 in / 
# Thu, 03 Mar 2022 20:18:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:37:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:250799bdfa37968bdaf47cc4d86f759e4e574d5e795f888e42c66ec0b7e92034`  
		Last Modified: Thu, 03 Mar 2022 20:19:35 GMT  
		Size: 27.2 MB (27161874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac28247ef04d1b842fabfcf6c1d41142412aa75bc7a718d9ee2f0a5294e7fb5`  
		Last Modified: Thu, 03 Mar 2022 20:43:48 GMT  
		Size: 6.9 MB (6930049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4db160b7628ac1a70c90af6b530d3f743602f72afb95d72926eb8e64f2348b`  
		Last Modified: Thu, 03 Mar 2022 20:43:47 GMT  
		Size: 3.3 MB (3252130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3d14c47fe1b4474337844054c06799cee1109c5c444e3f4cc312e3a24778af26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41213803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5288e0dc2c0fc46f160ce1c5397f77c602d2c82e8b58181df003ede205ffa5cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:27:52 GMT
ADD file:1070cef5a9454e0fdf7349b67652cf1ee9f02fb2679b05c10cfd1d7e2c378145 in / 
# Thu, 03 Mar 2022 20:27:59 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:11:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b055ba315c818484fa9979213cb00d276e7ec194a6928dd1270f73cf2aaa73b2`  
		Last Modified: Thu, 03 Mar 2022 20:31:51 GMT  
		Size: 30.4 MB (30437967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0253aa808a4a4801d83aa1d00c4ad4634c1f77aad211d65ef2ae9e34abdf1194`  
		Last Modified: Thu, 03 Mar 2022 21:56:52 GMT  
		Size: 7.1 MB (7056561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d945feb70f5ae95204f28dcb65ae6b9b5784e8fd4ad76bcbddaa6807a2347f9b`  
		Last Modified: Thu, 03 Mar 2022 21:56:45 GMT  
		Size: 3.7 MB (3719275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c646e20a1b9680f7a68ec964cd65827dbe8e38c19ff7ee0fdfa5460782dd2a1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34672721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ecf0baa7d5161064bc53c263bbde7c9d1ad16118a65fe81d5c2b217181bf63`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:41 GMT
ADD file:84b8165a5044433cc2f9fdf9670d391f085aad3799d5e6dae035f8338dbe6081 in / 
# Thu, 03 Mar 2022 19:41:44 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:33:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:33:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:084e045c78b3a9e38ef6caaf47c3ef1c3d672d3cc2e60543ae9629511a5e1c8b`  
		Last Modified: Thu, 03 Mar 2022 19:43:09 GMT  
		Size: 25.4 MB (25365258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f451b0973e7815327265ae400866c266a9df0155f7711ddc54f80cda51301f0`  
		Last Modified: Thu, 03 Mar 2022 20:42:23 GMT  
		Size: 6.3 MB (6332491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae3cd2e93934ab0fa445573a52ddb393438bacf99a6402e72555da0ec0b4a31`  
		Last Modified: Thu, 03 Mar 2022 20:42:22 GMT  
		Size: 3.0 MB (2974972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
