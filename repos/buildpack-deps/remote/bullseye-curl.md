## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:b7fc4babe862fbc69a6f6808000cdb0643f9240764d40c442c5850d97bbada7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:760dfa0949d136dd3d8ce38b851d7dbe1224e42a01bb9404d16b010ec2da4dab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70789709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22c72e270695960712b46c1bc16fbab3a8f9bd37a21743fed17b236451b2cd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:09 GMT
ADD file:edfe2fd644e397f293f4634d48f0fbdadcbf9e5d3f226da6daa213811d4bfb90 in / 
# Tue, 31 Mar 2020 01:20:09 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:54:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:54:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ac0531d9afaea848836097ce37941ab7f0d2533a1b6c1cec0eefed4bb8d4d9cc`  
		Last Modified: Tue, 31 Mar 2020 01:25:55 GMT  
		Size: 51.9 MB (51922687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d3ba615f9226bd102b19db9df18370bdec917f3ea1a9f936592e6f52c8e445`  
		Last Modified: Tue, 31 Mar 2020 02:08:55 GMT  
		Size: 7.9 MB (7924126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565bca0dadc92e2cf00fe101b4193e199d780837062441b521c17415ea8f86df`  
		Last Modified: Tue, 31 Mar 2020 02:08:55 GMT  
		Size: 10.9 MB (10942896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:30f46fa0b5f70583785fcc069f9cbee6c753f49751ee7d93fb02a320bbb04f5d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68070736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeccff5ef475aceff75d9e7ec178977bd661a1976423ff1ef31ec13e159b4b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:41 GMT
ADD file:4315cf04b632155858b9a0c6d22c433dba5c9b23c240abe83ceeca80e94a841a in / 
# Tue, 31 Mar 2020 01:23:44 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:18:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:19:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c0806b4d4e10fd104cbda1f65b5dcee9a5b4202716f5e8367e2bff3143216eda`  
		Last Modified: Tue, 31 Mar 2020 01:32:04 GMT  
		Size: 49.9 MB (49920582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0382c643bf4a04c23f9e10efeb789cdadcdcbfd9c890261da945bbfb379473`  
		Last Modified: Tue, 31 Mar 2020 03:45:41 GMT  
		Size: 7.5 MB (7504856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d3b4a29b142be89febad4954c371a81253e3970f04a9664005d4733ece339f`  
		Last Modified: Tue, 31 Mar 2020 03:45:41 GMT  
		Size: 10.6 MB (10645298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2ec92e2b6177ffb4660841fba71f1df0925d81d113a6b278d777e99157f354d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65173157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e6eae57f36bb11af13b27d704cf5cc1f618b6cbdacf856706ec9e9bc5d4bb5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:46:41 GMT
ADD file:4c71aa071e0d9e5b1dd3c77008be8bdca4a1b4b8da0d154f063b5291ee1d952a in / 
# Tue, 31 Mar 2020 01:46:44 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:33:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:33:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:976828a7d5a0b588a99d1c171efd6a1ee4b2f20c93bec91c9fe807cb0c749c6c`  
		Last Modified: Tue, 31 Mar 2020 01:55:26 GMT  
		Size: 47.6 MB (47645691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c119afb8e454887043c7265522a611d2778a2c7f6aece88dcc7548a5a78a84`  
		Last Modified: Tue, 31 Mar 2020 03:58:33 GMT  
		Size: 7.2 MB (7247259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b0723408046fc4e2ede8f289dfb0a05596a340affbeb852b0be812092e017`  
		Last Modified: Tue, 31 Mar 2020 03:58:33 GMT  
		Size: 10.3 MB (10280207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8d0e11bc7172ebf3e75e0a83c66973d2d6c874db4ea90ee5beda5b6f415e0efd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69597705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3e1319da42aab56f9a008429503a30a4479268a8cafb219a4aa21d2473e064`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:04:14 GMT
ADD file:c295ac949cf6eaba5c5d52c389db08bd675e330909eff8ffc4830f470e00e191 in / 
# Tue, 31 Mar 2020 02:04:18 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:28:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c022ee991294966f0839f32cefa09d5adb5a31987af7b4230925f0d6dac86599`  
		Last Modified: Tue, 31 Mar 2020 02:11:13 GMT  
		Size: 50.9 MB (50858572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e272a955874c481555018422eaed223cbbb88fb5f995272a28857a9b79b6a0`  
		Last Modified: Tue, 31 Mar 2020 04:45:09 GMT  
		Size: 7.8 MB (7797593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753916d700ebcd3dfc6785ee04467f1efd75f81e7e55e561d8a04b655a2dc738`  
		Last Modified: Tue, 31 Mar 2020 04:45:09 GMT  
		Size: 10.9 MB (10941540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:de1471c713f1d5ae5408b31972d41e5e9202aaf5ac2e91a1c8d7a7a6d253ab69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72496965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d34d6313031595acccbf357525393006d8c2f1e6943370c64a6040ad966fd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:38:46 GMT
ADD file:930e7a44cb4836bcd1f8f50505e46e4bf4fd398eaad8aaddac7c962b60ca7e44 in / 
# Tue, 31 Mar 2020 00:38:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:09:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3243f119e5f4c4b861f26f136c3e132ab2844145f46cb5d7b6cc9602b0086f3b`  
		Last Modified: Tue, 31 Mar 2020 00:44:42 GMT  
		Size: 53.1 MB (53061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e2dd532613df680378f734636580b380c128d4698ca4b3fa4951dfe348eb9a`  
		Last Modified: Tue, 31 Mar 2020 01:27:42 GMT  
		Size: 8.1 MB (8100943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb8ef6d4279b94da7f069e17e431221e259d8eba9ab62fbab1fa2b13b383023`  
		Last Modified: Tue, 31 Mar 2020 01:27:42 GMT  
		Size: 11.3 MB (11334316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:69f0c2981406d811ba0b2d0a23b20c526dd5b2233afc051e0f1ba13d95f931b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75830677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7925b49f09a4b3d6728e193fb64ee676200acb78a2af97e4c6d174cbe5c400d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:30:51 GMT
ADD file:544f960bbf6b0c556a3946247e7163ea2d8976c01f513bb4e7ed8eb8df4d09ae in / 
# Tue, 31 Mar 2020 01:30:57 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:03:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:03:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:de0d878984bf9a338e5828a66a5f63ae0852a3a1838645e030f18c29df6748ed`  
		Last Modified: Tue, 31 Mar 2020 01:42:06 GMT  
		Size: 55.8 MB (55810298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80755c7f1f2b64223e3ae4cbc62d0e4c2a93eda7f1f3734ea3686292ae264420`  
		Last Modified: Tue, 31 Mar 2020 03:58:05 GMT  
		Size: 8.3 MB (8349042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436e4215faaae7e504e17484b61fdfc1a375ec0c1b46b37361c8b0c6de944883`  
		Last Modified: Tue, 31 Mar 2020 03:58:09 GMT  
		Size: 11.7 MB (11671337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:33d2a82018257e9e54e3977cc9d947d67872aac2b6f4b9ab54aac312e28e0cc2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68934499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109517adb8f09043e5d6b50a6154e0f0d2ca46587de9a17fb37bbabafd76be2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:08:23 GMT
ADD file:c425c02ec78c0d94b688067a35be5c57d71687cb603f9103c3c0736e2a469360 in / 
# Tue, 31 Mar 2020 01:08:25 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:18:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:18:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2c5824ffa7966a2d6d1b45b6cc8e3e0e844fd262d0efcd2ef5cf9a9277f65e8a`  
		Last Modified: Tue, 31 Mar 2020 01:12:00 GMT  
		Size: 50.5 MB (50522622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbb2d8d7f0af1e7df5d27f860da9f4382c1c7710f9ae98e792a380cd0cb851`  
		Last Modified: Tue, 31 Mar 2020 02:27:44 GMT  
		Size: 7.6 MB (7591237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3b77d0e2a2b6911e2c546d532b0577fee7321c1bc99cd6a728b04571edcedb`  
		Last Modified: Tue, 31 Mar 2020 02:27:49 GMT  
		Size: 10.8 MB (10820640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
