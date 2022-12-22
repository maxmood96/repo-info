## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:9d82564af17be98abfc9102a22445ac6a72dd042ac65d60a424fd181ea4f4e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:56146ea5d6b392e4dce8f44766d9251703f013af7254faf0f7b6c1e4149ea451
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80520720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ff34c476bcbe14e850955115eeec13acdeefb549018982b8a476d19302e5dc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:50 GMT
ADD file:3a69ab43af761d2eea701ad591edccb2b1f84ff63a25059ad9d5bc53358dedc1 in / 
# Fri, 09 Dec 2022 01:20:50 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:27:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Dec 2022 19:27:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a13f57ee816c77bd77798d728a3d73246552cac763e9c613b26aecd8441e43e6`  
		Last Modified: Fri, 09 Dec 2022 01:22:25 GMT  
		Size: 27.5 MB (27505626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb206e2c65ae53b38b00dbe71e2c1e6bb7b54b88640624201c2b86a1f5847b8`  
		Last Modified: Thu, 22 Dec 2022 19:32:28 GMT  
		Size: 6.8 MB (6780053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d01a823ce10ce5db3cb9c09adcc98b1c550a3ffa8adab1c26c5ae3eda5c0e65`  
		Last Modified: Thu, 22 Dec 2022 19:32:28 GMT  
		Size: 3.7 MB (3657390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4c43da0c86244888b0b84f7c0a7f0e0c892e4926cf101cce101bfd3af10574`  
		Last Modified: Thu, 22 Dec 2022 19:32:44 GMT  
		Size: 42.6 MB (42577651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:22047f52a775e61b50513529548568f86aea50be839b09f196bb58ed1a2ae8e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79388399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcd0ce1dfe116457b68d716fa1381469afe392cf6b113ba4e9b5e73235f1c9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:47:11 GMT
ADD file:7e5379395d9cd9ee04e9f4dcd8e394c2d1c29e9491757a29f4e37f807d3635c9 in / 
# Fri, 09 Dec 2022 01:47:11 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:46:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:46:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Dec 2022 19:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6101eb5b766f68aef80c6b84dc902199e26926e7dc981aa0ac38cb1c3075b5ef`  
		Last Modified: Fri, 09 Dec 2022 01:48:40 GMT  
		Size: 26.8 MB (26825777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d47c5b275711c889982121dbce8e6eb1df30a49c0cda62485bca0531a1823f6`  
		Last Modified: Thu, 22 Dec 2022 19:52:52 GMT  
		Size: 6.6 MB (6609996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1aa323bbd3d0e560aa576969c1bf8bbaaf5ef7b2c159c053e97229a8f208a2`  
		Last Modified: Thu, 22 Dec 2022 19:52:51 GMT  
		Size: 3.6 MB (3619166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328677d06c80ebbc7a99cd646b992d671cfbbfbf4c1a39a51a34ba9f63eb101b`  
		Last Modified: Thu, 22 Dec 2022 19:53:06 GMT  
		Size: 42.3 MB (42333460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2f6d20352cf371b2502c7f4ae2c3b722b90817c0d58c46faf884372bb585af47
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91456138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08ce0187f7b9840e3ce3c7c186062b71cfd0abad0238fb1d061e6105ff6024d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:28:29 GMT
ADD file:fc908ee01c16840b84760d5041e467ede6748c61754d04faa691f9fb6ddf1686 in / 
# Fri, 09 Dec 2022 01:28:31 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:41:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Dec 2022 19:42:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:08a75ad1a4a23cbc8eccc791fdfae97d71a324379cb275562275520611a56654`  
		Last Modified: Fri, 09 Dec 2022 01:31:25 GMT  
		Size: 32.1 MB (32104472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c870358a362895034ccb4359831dc39366f11c4609b717d9c3a44e0282b11b`  
		Last Modified: Thu, 22 Dec 2022 19:49:56 GMT  
		Size: 7.8 MB (7754835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0d292dfd312b20bb9ad0a639938aaa822a0e0a09f07b775ef818d1c3483fd4`  
		Last Modified: Thu, 22 Dec 2022 19:49:55 GMT  
		Size: 4.4 MB (4378575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7296a8f280368b3eaf64dc4cc52332f529dc23a9622eef822ef0bf1ac366c8b8`  
		Last Modified: Thu, 22 Dec 2022 19:50:20 GMT  
		Size: 47.2 MB (47218256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f34a4832e21f7b3a34722518124c697a7afbf5fafbecbce91c354b06039927b5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81001866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7817103c111c67c4d91cd18ebbd8ff7a21123c3adbcfd062acc761f64fb53c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:17:04 GMT
ADD file:dd674b2aba3f7d1f5bb21fe7f9173314f05007fa6b78d8efec97661a9bf7c748 in / 
# Fri, 09 Dec 2022 01:17:06 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:12:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:13:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Dec 2022 19:15:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ced4571d7775ec15e8b89c410d607207d53803f56e764a02dbbde02cd345dd4`  
		Last Modified: Fri, 09 Dec 2022 01:40:36 GMT  
		Size: 25.7 MB (25674343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb4476ae2074d1e5bb1f9442f0da2cf6977a81ea5526eea5879a654cbd20eeb`  
		Last Modified: Thu, 22 Dec 2022 19:21:32 GMT  
		Size: 5.9 MB (5927559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd258f4dab88306e41aad9845768a49cd66889bc363a5f1a5cd03af38a7bb7a`  
		Last Modified: Thu, 22 Dec 2022 19:21:28 GMT  
		Size: 3.9 MB (3903143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d977602dbe08ebbaf095d49185456792528adf3e22b7d605f7a85bc019287`  
		Last Modified: Thu, 22 Dec 2022 19:22:38 GMT  
		Size: 45.5 MB (45496821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2ad0df7ab017197cc643330fcfc73b3047421d48095106d668df0207cb3b1db6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78564212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db7ffd5ce3b608d19caf11e78aa4b6fe52b044ed4ec021111e86071706d2b43`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:53:35 GMT
ADD file:34ba36266e3f51a04f8105b97312cec6ad0e02db549c1a40af7b2b9b8b4527fb in / 
# Fri, 09 Dec 2022 01:53:39 GMT
CMD ["bash"]
# Thu, 22 Dec 2022 19:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 19:53:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Dec 2022 19:53:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40f085afd82295659f70518a511d2ea24258833fac78ee993694322605814e97`  
		Last Modified: Fri, 09 Dec 2022 01:55:38 GMT  
		Size: 26.1 MB (26064347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4ff57ac87df71f9147afd569d5c780b3c46584d3ae2a7ca33d038e5b2603c3`  
		Last Modified: Thu, 22 Dec 2022 19:59:01 GMT  
		Size: 6.5 MB (6463110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dcb825ede09e4c615483b46aaf77e56e707f1a2e30ae7027eaf43484859483`  
		Last Modified: Thu, 22 Dec 2022 19:59:00 GMT  
		Size: 3.6 MB (3643218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f27c39d9c3fda7daacd85705c51fab24e164f5ee1e884b24c4afce7b770dc1`  
		Last Modified: Thu, 22 Dec 2022 19:59:13 GMT  
		Size: 42.4 MB (42393537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
