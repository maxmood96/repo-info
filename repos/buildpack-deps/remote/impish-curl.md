## `buildpack-deps:impish-curl`

```console
$ docker pull buildpack-deps@sha256:40969d345ea67b862a72d9d24144395ddea299a517a4c456f060cf108f177c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:dd6c280b99daea86543d074f477b5b196e3136433686b6848dc654663bb60e58
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37847491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883360346d84b6140d17a89c82dded9c76d0c86eda04909badf532a6d40fcfd9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:12 GMT
ADD file:355a5f56bf0136597bcd90b01ff73fc517b6bf7e76f45b65bf1af1136f434462 in / 
# Tue, 31 Aug 2021 01:21:12 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:02:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:03:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:25907b3add375d4f44a3bf4bfc3544b51ff9f4a23fe8c186f3b20e54b37d19ae`  
		Last Modified: Tue, 31 Aug 2021 01:22:53 GMT  
		Size: 30.6 MB (30602781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ef40c83a42d65ce37ce8bc08e06a0c4b994512527cad13196aca51586d9bd7`  
		Last Modified: Tue, 31 Aug 2021 03:14:51 GMT  
		Size: 3.7 MB (3692694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a871edcbb988433606f5a8d03efc8f0d9d49a4cd78a5d506401ec3b7854a2162`  
		Last Modified: Tue, 31 Aug 2021 03:14:51 GMT  
		Size: 3.6 MB (3552016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9a3d5880ea36b8866fa5d8f9d4b3604048c83a329f3e4a4ea6aba5eed872f1fc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34495049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e2e9a9304e887c58fb5516661169e2e18ea005307279c2d8d325a22f638621`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:42 GMT
ADD file:0abcd0c1c6aecb3d5af2aa5d9c631949d716076e338faccdd7802906b4979bd6 in / 
# Tue, 31 Aug 2021 01:41:43 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:21:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:22:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:be5e7fb59932c05a5acf0221847ae12179d4f81037fdeb44f8c408bc27ec1511`  
		Last Modified: Tue, 31 Aug 2021 01:46:11 GMT  
		Size: 27.3 MB (27313903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558c8f5e7395b48e26211a363f2c66ea0e729fa5f4ce1e980a22a70c47eacbf1`  
		Last Modified: Tue, 31 Aug 2021 03:40:47 GMT  
		Size: 3.4 MB (3438915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30125ee4f15b1f56a8279e5c1f488ef77c51231b62f4da3cb1a03b8a32fdae7`  
		Last Modified: Tue, 31 Aug 2021 03:40:46 GMT  
		Size: 3.7 MB (3742231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a443fd6e3736e490f466797038af04904d36fc0129968f8a26a2d0c0f5411654
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36244513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651cadc9706f04ce4ca19d0656ea6e725e8b0099e4f8ac8a95e0c9db590029d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:02 GMT
ADD file:ed3a8c55fbedc627dd5d33aecf52df10becbd9bd492f7c3f4f0a710b15629618 in / 
# Tue, 31 Aug 2021 01:41:03 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:13:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:835dcfefc46e2b5551a40002ffed802b6b70970071e61e3f9dce0dd0404c2a12`  
		Last Modified: Tue, 31 Aug 2021 01:43:19 GMT  
		Size: 29.0 MB (29033527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff76d237fe2a405ec5c0175da7117764a3725e495a5280fa68824281d0209f48`  
		Last Modified: Tue, 31 Aug 2021 02:21:58 GMT  
		Size: 3.7 MB (3677477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972cd7eb9f3f8f76c354e0777c1e299b4979c519af36ee25c5a4b5176d14c93b`  
		Last Modified: Tue, 31 Aug 2021 02:21:58 GMT  
		Size: 3.5 MB (3533509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:838cee7286d3baa3d78a9117036d5697643c8db2337680cedb6d584405b7ba53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44393554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7088c04b44397a9f243f59f8046529d76d35591ab07d0f3564045047c59cd2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:11:28 GMT
ADD file:776487dfd6a31c5a5d57d6924dd11136cb94d2e661eb085c76b14213c2220e3f in / 
# Tue, 31 Aug 2021 02:11:33 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 04:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 04:21:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7f23233eca55841e558566a0a689d1261b17a023a5d0ed1e0ee267da33ff84a9`  
		Last Modified: Tue, 31 Aug 2021 02:15:11 GMT  
		Size: 36.1 MB (36055099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10a1f2d8a9c3bf4f6060f088986f3f74fbf50acda4d6016dfd6d1115fbf3a9d`  
		Last Modified: Tue, 31 Aug 2021 05:27:38 GMT  
		Size: 4.1 MB (4096829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd26809db5804495bc5bf81be1fbeae7b7a82215d30ff3e0c59d3353cc857206`  
		Last Modified: Tue, 31 Aug 2021 05:27:21 GMT  
		Size: 4.2 MB (4241626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:97bd04e7cd9db63b4fdfd2f347aa020ccedf795d142138f5bc2fbd99b3405f27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34478604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221e715de9dc218092a332bbdf4433b434c800e4703c3f3ab14ad8b5106fbae8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:19:36 GMT
ADD file:84d3daa77b3c4590ccb1b2c1bdfa7b2ea2629a8e289c7e0df33678a72ef40f4c in / 
# Tue, 31 Aug 2021 01:19:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:16:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2027d80189558886be09b6f8194607cd27258802c79f3c3f228e92404c40c304`  
		Last Modified: Tue, 31 Aug 2021 01:35:47 GMT  
		Size: 27.2 MB (27192169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ccb43db8246e726e33f90f4887b26c5c6e5c0eb9b7c4fd223c18539a9963369`  
		Last Modified: Tue, 31 Aug 2021 02:53:01 GMT  
		Size: 3.5 MB (3483280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a66489e611edd2a918d67c7aa380888b297b1b1170487f8cf4d412010e9da74`  
		Last Modified: Tue, 31 Aug 2021 02:53:00 GMT  
		Size: 3.8 MB (3803155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b3f1c9e13e18f3a6e5662bf31762ed9c77414c91bab87c7de91de6a71e1935e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39220762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc85733e213410e8138f3ac19e6603d3c39f436a8584a4f0df250ce43cb4d2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:54 GMT
ADD file:4748ab039bb7c33cbda2bba944346ecf2e0e6238971d842acc53ec7e8c77df92 in / 
# Tue, 31 Aug 2021 01:42:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:39:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b2abd65908848180c8f2b1a3f2a6493d9c7c22253fc30bc557fce0bbf12327e7`  
		Last Modified: Tue, 31 Aug 2021 01:44:45 GMT  
		Size: 31.3 MB (31308069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f61cb11476011700fc2feeb76881a7eeceb9638e97fa4c33603d64dab544155`  
		Last Modified: Tue, 31 Aug 2021 02:47:40 GMT  
		Size: 4.0 MB (3950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7802bd74770db74806622bc0f14aa9cc4666241c5b47c5aee05c1b85aa17ebe5`  
		Last Modified: Tue, 31 Aug 2021 02:47:40 GMT  
		Size: 4.0 MB (3962603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
