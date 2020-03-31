## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:b6177f82d16c59f81ffc4cb9929d483b7cc4c1762af7987b8c4f537ee4635805
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:407c7f5c02b085ad163494adf2ee810c442b2f09b7a74f4f29d91fd79997f788
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 MB (126094979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295f6752e407d8e19f93d1b77bc2dcc4393d38a2dd6116d46c6fddc1f567135c`
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
# Tue, 31 Mar 2020 01:54:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7075d49fde8d153b51250bca15556db66dcc9e8295b7c43f49937bef0f1f9e9e`  
		Last Modified: Tue, 31 Mar 2020 02:09:12 GMT  
		Size: 55.3 MB (55305270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:543439eb397891819f44b0029fe7c8e861c57d094baa2af3f1b1927c4cec2359
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.0 MB (121035595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc68a3990d9715c37db8c228b84e601accabaf57db08a7daf345680cbb88a2f`
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
# Tue, 31 Mar 2020 03:20:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1b7480e7f26a4fddbd2129e9273b18dfd1c9e33989b1cf84be529e4861c12598`  
		Last Modified: Tue, 31 Mar 2020 03:46:07 GMT  
		Size: 53.0 MB (52964859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0de28bb1b4d4be49171edc78c19643cbb0040015ebb27c406e0867341975d757
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115836051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace5b2a8bd06e87d59a71b576b70bb2f2b484ec513d264d0bfc65f6567e678b7`
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
# Tue, 31 Mar 2020 03:34:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4cd835fb29b9b7f225747fb4c8d6d5a1a2c6b074b1ea1d0bc743b66317ab1d2b`  
		Last Modified: Tue, 31 Mar 2020 03:58:55 GMT  
		Size: 50.7 MB (50662894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bf14100742ccce2fdd762900ca1ef268df2194a919af1f33bc17a0ac553766f4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125081532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b67c6df911cae01f53f9665910ffc0eba562f6bb2c8ccac1a5a24360486605f`
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
# Tue, 31 Mar 2020 04:29:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7f98057de3552869b2e8f34819456b26adb5ef78d1979c7f755979777d799f0c`  
		Last Modified: Tue, 31 Mar 2020 04:45:34 GMT  
		Size: 55.5 MB (55483827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c1db16337c66921df78a06bd3de413d91e7878cac727f1fe38eec0980c35cadc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129663892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0163ece584e91810a2856ff51bc98b406a1354b02036c4a8df4f5d094388f7`
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
# Tue, 31 Mar 2020 01:09:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e9e841cf9c625cfcbef38746fbb539d5caa4a613cdd12452b81811f57855f5f0`  
		Last Modified: Tue, 31 Mar 2020 01:28:03 GMT  
		Size: 57.2 MB (57166927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:81bce8c761c528906d6667b55a4fd42dc83c7b89b15d2fb8e93dfaad0133a342
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136482723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d80775d604a083b970c3af100343b0e9ffacccdcee01e82787e22da5aedf91f`
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
# Tue, 31 Mar 2020 03:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:37ec1de538484d05e151adf76315f07e1874120a05c2fec146d2e7440407137b`  
		Last Modified: Tue, 31 Mar 2020 03:58:51 GMT  
		Size: 60.7 MB (60652046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3c36251798065c44b8311fd5109aca4e1d2457b41df535d0ff73c8503ea8b0e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123505097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff63be9f05fa42e256ec6f19a290f091c147122f9de1ff62d47e44b7112a2f35`
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
# Tue, 31 Mar 2020 02:18:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:6fc3853981ce94e376dc6f9e8834504cd7bf393525dc859aeac81143c19cc07c`  
		Last Modified: Tue, 31 Mar 2020 02:28:03 GMT  
		Size: 54.6 MB (54570598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
