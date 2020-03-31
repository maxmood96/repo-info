## `buildpack-deps:stretch-scm`

```console
$ docker pull buildpack-deps@sha256:7560d820611db89c72b2453460713f0bc59fa4b089b6b7de1705c2337f1fc03d
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

### `buildpack-deps:stretch-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:46fc6c5a495b2c589228d4426421073ff943e666971dad451c58e45fb5a469ec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110584974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8818f8abfdfe8404cfe822d8e185dd1600ab9de89e70f2a40eeb7f9ff473199`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 02:07:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e1e13bd9f6c381f158a5366b3eff242e8b4a4decfa940e915b1d5705ef4a28`  
		Last Modified: Tue, 31 Mar 2020 02:12:58 GMT  
		Size: 50.1 MB (50071604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8705b80030473865b094587234d212a5d2c6d8f07341f5255f46aa6cf7ce7095
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106373876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de639752f78a5430eeb2c66e4d414f2e70c936ad4fccb486c60fbcb6291ef72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:29:01 GMT
ADD file:5a406f17e0981025084e19ed83a5deb90ebcba048fe641c8273f340add75cb3f in / 
# Tue, 31 Mar 2020 01:29:03 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:40:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:40:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:41:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:442790510f4830e8d231c31971c1ad175b7d7fbf094edfb7914e6154fcd31434`  
		Last Modified: Tue, 31 Mar 2020 01:36:31 GMT  
		Size: 44.1 MB (44066449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c87dcd2bd87a418f8e317fa8e6c3f1fddfa90ea5ed4a77e7f1e67e2a0c6e9f`  
		Last Modified: Tue, 31 Mar 2020 03:51:39 GMT  
		Size: 9.9 MB (9866705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85810ebe9c6c3a63905ec14959badf92e7ee22150b33cf41ac37544fddf2b98f`  
		Last Modified: Tue, 31 Mar 2020 03:51:33 GMT  
		Size: 4.2 MB (4159184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e921bb4bc1118cd5b95a78c4031c7bc544941c454384273565546ad9826933`  
		Last Modified: Tue, 31 Mar 2020 03:52:02 GMT  
		Size: 48.3 MB (48281538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:22b43f02e6a100184cb6e6baf435aa67e352b2033bf86465529707a707ef976a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101910175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16082e614d5fba52d5b331dabaaeec3f60dde4b00d157fe068bf79ac33ff710`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:53:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:53:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb68590923b075c8f49c4470341451f9d874afc84c5fc916278815a1064243`  
		Last Modified: Tue, 31 Mar 2020 04:04:43 GMT  
		Size: 9.5 MB (9498284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743981b4cf60d4ed8ddd6610e4d1d75256ddb63a7d83d540a96e1faf8ba8a315`  
		Last Modified: Tue, 31 Mar 2020 04:04:42 GMT  
		Size: 3.9 MB (3918805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b83e2473a635025de9a80900fb966143db79eafc6c7fad950a2ce7e54fc1764`  
		Last Modified: Tue, 31 Mar 2020 04:05:06 GMT  
		Size: 46.4 MB (46392996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:794c20d33697f4acfce2fe4e01d59429af8133410d6b0a7f3a7ea5be2e773520
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105025360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11caf2fb934caad4721a62362a0a32debe08ddd17ce64e75e4998a142212ed6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 04:41:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 04:41:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 04:42:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaedfc9896782bd00cfcf104ca392d0b85363b41be4ecedd7c058c1c183ac01`  
		Last Modified: Tue, 31 Mar 2020 04:49:39 GMT  
		Size: 9.7 MB (9748484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa6bb03021f1e64553e2c40a904ffe7c70a0112c00ba9bf44f67ad27162f2b0`  
		Last Modified: Tue, 31 Mar 2020 04:49:38 GMT  
		Size: 4.1 MB (4094373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4110ff81d02419c6737ebf46680f0afee475f58cf3bd159e0892d8f4ffebaf`  
		Last Modified: Tue, 31 Mar 2020 04:50:00 GMT  
		Size: 48.0 MB (48024387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:52ea676b12ac82fd852ca086b4b5023f81a3f4eaa6e29ee4f50c966d2ab5925f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113078595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7f4fb2674e04b206dfadafebac4640dd33e24e1a49e71b1df2108ebb772b54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:42:34 GMT
ADD file:a2d15d4f5721611194d2e75c068cf76220a1fd273b28e60afc9d97c41920f37b in / 
# Tue, 31 Mar 2020 00:42:34 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:25:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:25:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:25:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e23f42c0de4ea650702adc216b9d71349a24439e774c0bbbb00d2ad19aa304df`  
		Last Modified: Tue, 31 Mar 2020 00:48:31 GMT  
		Size: 46.1 MB (46095182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8aed54eafba002eda33cfdc543523b6ddb486d1a0cbca690ff815f53d50e9`  
		Last Modified: Tue, 31 Mar 2020 01:32:58 GMT  
		Size: 10.8 MB (10818153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a1db665f4b770126afb4ccdc427fae19617bf624b95982ce876d0fdb478291`  
		Last Modified: Tue, 31 Mar 2020 01:32:56 GMT  
		Size: 4.6 MB (4561461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b716c001feda21116c3228663db9da4551f266d173d7526106f39b3c53d27212`  
		Last Modified: Tue, 31 Mar 2020 01:33:17 GMT  
		Size: 51.6 MB (51603799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7627f2bdc844be6e9908506cc193d5f0843a2ccd480e65aae9ab6d564b6cac20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110031336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaedd71782c8493066c5f443e216b868cddf6632db6e5f6d1d7f68fe52c28e08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:36:08 GMT
ADD file:88dd9829c8f6a5ba7164ab347e4b14c986122f77fa3881b5b5f9bd34f8e0a794 in / 
# Tue, 31 Mar 2020 01:36:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:46:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:46:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:48:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a7f28865f7aedbe572d508cc57c37cad5f147864f7c67c67a38458e070687420`  
		Last Modified: Tue, 31 Mar 2020 01:52:56 GMT  
		Size: 45.6 MB (45647140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b575341a09a9b1fed08dca01f194be6db272e3f2d161ea2edf0db64d8e706213`  
		Last Modified: Tue, 31 Mar 2020 04:07:20 GMT  
		Size: 10.0 MB (10002319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28423de192fc0e4ecfc04a57e531587e8876d098a124122748a8f55a842f3213`  
		Last Modified: Tue, 31 Mar 2020 04:07:19 GMT  
		Size: 4.3 MB (4296673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cccdb86da25ba4684a518e5fe94d237bd1d84392cdee077d26f6aed0520237e`  
		Last Modified: Tue, 31 Mar 2020 04:08:09 GMT  
		Size: 50.1 MB (50085204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:88bccf8ac9c920cf46a449efa8fd60a2f6510fbdb3e287f72b548fc20ce6f7b8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110431719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb92b21c4efd0a0f76eacd0e494645d65c4d6965cf5eb1edd03c9d04ad71b42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:10:18 GMT
ADD file:4b10f5f6f8f327b6ad71def930275eb5f518828e8eb19f79d20712e112ca35df in / 
# Tue, 31 Mar 2020 01:10:21 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:24:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:25:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 02:25:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32a0ea7e09635bc86f70dd4db2b929ad05b81856f2418c0f482b647e3ec3453e`  
		Last Modified: Tue, 31 Mar 2020 01:14:05 GMT  
		Size: 45.2 MB (45232869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1670721d9cffd9a8df08200c9776f5df2d9c67b509f1687f6af2cff87cea8736`  
		Last Modified: Tue, 31 Mar 2020 02:30:22 GMT  
		Size: 10.3 MB (10325654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ce62003b28e35153216c5f62da651c3fc87ee53f79914403ed0bfcffb7dc6e`  
		Last Modified: Tue, 31 Mar 2020 02:30:22 GMT  
		Size: 4.4 MB (4372633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b80b20ffe11033ae476419f8b2a73153d8fa2905a690306b441cf34c2cb895d`  
		Last Modified: Tue, 31 Mar 2020 02:30:35 GMT  
		Size: 50.5 MB (50500563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
