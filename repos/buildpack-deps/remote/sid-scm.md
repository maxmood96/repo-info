## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:bc4bcbb0795e9b8ce3276ef2dfe6991c03757d5a2cb88707ef6f8e034de612b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6168a2f3df8dd8bc43b1833b1ccc40ff40e3d3c26be6849d3ca1539b2952ac36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131721662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20a4066c8a07bbf67f591d13649093fc1dcd068b3aeda00392a0b5e8c5a8935`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:21:32 GMT
ADD file:dffa51e87e58558bb4b777e117ecb18500d90a9646513d0d8d9724bb5c949dc5 in / 
# Sat, 28 May 2022 01:21:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:43:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:43:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7fa02d3fa6e2ab30d6142a096f5321227237c89c02dd890ff9fa745dbf0790d1`  
		Last Modified: Sat, 28 May 2022 01:27:35 GMT  
		Size: 53.2 MB (53161898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0597a54f85d6fe31261321fa5abdce192dd72a61160f5a30e14cfb698b933373`  
		Last Modified: Sat, 28 May 2022 02:51:29 GMT  
		Size: 9.3 MB (9287856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544dfe1044f9dd59f41f2b606fdedfe343ea2f2e7d6ac305fa10a471e369e8c`  
		Last Modified: Sat, 28 May 2022 02:51:29 GMT  
		Size: 11.3 MB (11264553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1758dc74532aa30f33a69018fed7293e1b1be73f54a3e385d575426ebbc6bbdc`  
		Last Modified: Sat, 28 May 2022 02:51:48 GMT  
		Size: 58.0 MB (58007355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8b257b5aa08adf78986beccc5a0eaab35e8f44e6c540c3f9933195cc00384072
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125035393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a8648008db90e0da2f8875553dc67b7ca3c1ffaaae17542bf93d73ed9db4f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:53:50 GMT
ADD file:4f142f5aefa97fb474a705d0b74abadc5a3efdc7faa28a865e8f774b46affcfa in / 
# Wed, 11 May 2022 00:53:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:15:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:15:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1faa3808d790c86a331ed5dce0a7a8af6a26aa395d982f287f5d3fe6362186a`  
		Last Modified: Wed, 11 May 2022 01:10:36 GMT  
		Size: 50.9 MB (50939831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bd191c3a53704df74788d319588194c3f1115cfa7ce0b029d942621a231b1c`  
		Last Modified: Wed, 11 May 2022 02:36:13 GMT  
		Size: 7.5 MB (7537835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8271993242928fca4b8160659ea37b8a1b4a3ca033c568f9e9c1b99e9a9e04`  
		Last Modified: Wed, 11 May 2022 02:36:14 GMT  
		Size: 10.9 MB (10927528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da3f3eaccabf091adab760ec3c2e8c7aaed5cb736e07943be5b8b69679038c`  
		Last Modified: Wed, 11 May 2022 02:37:07 GMT  
		Size: 55.6 MB (55630199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cee06f9a2656b49c796af7cda37f22d1ceb919e44191a6b220e93222e21d36b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120079356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb11b0cf1dba71685fa0120ef5939ca8ee20e013ea5139cae0d79ea2ac99accf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:52:42 GMT
ADD file:5256a3df37de011e57faaf3b387bbc66fc94fceb82c48ead6b9e5775cbe7bf21 in / 
# Wed, 11 May 2022 01:52:43 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:29:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:29:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:528d9ed2cb56db465cbc360f474c45ab8e5ae05c0a0f596fae936fc1290bc68a`  
		Last Modified: Wed, 11 May 2022 02:09:01 GMT  
		Size: 48.7 MB (48678301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d1a1a1705b16f0412d469f63dae500ab636c3d7d35a70874baa189b03a3579`  
		Last Modified: Wed, 11 May 2022 03:52:19 GMT  
		Size: 7.3 MB (7269475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0226a116d43744d6f9e056ad8e8a6469b2462f8cc039fafca040cfa47dbf0da1`  
		Last Modified: Wed, 11 May 2022 03:52:20 GMT  
		Size: 10.6 MB (10573123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b8551ee0c609b1218c73a583d5c06d28931fab52d37abda11cf0e20b75f2b`  
		Last Modified: Wed, 11 May 2022 03:53:08 GMT  
		Size: 53.6 MB (53558457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1e7bee09876ef0a919aa3b3625070475791b70c89405d61719dbac889afd77fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129119780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72497322cdd50ac82347887d0ee4e716a75f1b7916764a2c328249150e20a34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:48:25 GMT
ADD file:57e11874acd2dc9e0376f854ffe18bfb0b25f8a7a933a3c619d173176c08e412 in / 
# Wed, 11 May 2022 00:48:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:28:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:28:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5489557693077b493aaa820cc173d6947baad433930a473cb7cbbb4883ec94f9`  
		Last Modified: Wed, 11 May 2022 00:56:14 GMT  
		Size: 52.2 MB (52242857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b334af1a397894abf6045ff032026c9b4f342acb68ecfe554c22a6f0f272a613`  
		Last Modified: Wed, 11 May 2022 01:38:13 GMT  
		Size: 7.9 MB (7853722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5604865b4585f274eea230691352b972c26efb7b509f1c89ee586a4c6a3559a`  
		Last Modified: Wed, 11 May 2022 01:38:13 GMT  
		Size: 11.0 MB (11041972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7bbb22e05bd64b1830d1bc074724bb1f87693a3a59566b6c2e1ae211de5c50`  
		Last Modified: Wed, 11 May 2022 01:38:35 GMT  
		Size: 58.0 MB (57981229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:27972202f10bbcb2efc718841a3c8cbac7f1e84371f417e6c3ca1d5c9a96e500
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134562489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e47aafd5bf590af2240ca6d4f8e4fb004dc8f206c0bea0d54195a9376d56f18`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:03 GMT
ADD file:dd10bdbf07bc13b42a7021b48621548cda7b383bf0edb8dff1e35d908f50c392 in / 
# Sat, 28 May 2022 00:41:03 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:14:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e233042357300fc1ac460e8583f90e2b88388d7c2a9016f91be99da315c46fcc`  
		Last Modified: Sat, 28 May 2022 00:49:18 GMT  
		Size: 54.2 MB (54158716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312c6075d7bd54d76868fa2bfad3038339123706e4120edfdacf8be48665b2fa`  
		Last Modified: Sat, 28 May 2022 01:23:48 GMT  
		Size: 9.5 MB (9462060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741e6836ace09c243fa9be77aa56380eeef9635c1dfa4f211ea482b290a4784`  
		Last Modified: Sat, 28 May 2022 01:23:48 GMT  
		Size: 11.5 MB (11464411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81a6911feb95db15f083eaccde4a7497085fd4d68ac9f7f6ceae43f6483b9b2`  
		Last Modified: Sat, 28 May 2022 01:24:12 GMT  
		Size: 59.5 MB (59477302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c8c26a6a62de0bb2d85e5d0eca9ba5519729d2f7afae3f924f74114070ee65d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128578570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a2ae2aa77fe2fd9901ba1a429f54aef890cee8d77674595d357198a6e0af97`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:14:06 GMT
ADD file:1687a4039bc00edb9de7ba18be7ce08c7df3d2cf6a4b7a30cb5bb60f41d3c082 in / 
# Sat, 28 May 2022 01:14:11 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:12:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:13:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:14:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a7336e150b70b2115ef0d770279f4e6f79de8d6e16c87dd256445530c1c68d1e`  
		Last Modified: Sat, 28 May 2022 01:24:53 GMT  
		Size: 52.3 MB (52283200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d31486dae68c1e92361c28f610c582d55f682b8dc91e6fadc6ce7d2f167d0f8`  
		Last Modified: Sat, 28 May 2022 02:30:37 GMT  
		Size: 8.7 MB (8654895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a846f26a733756e5b7a30ab3e72a8147961effdf03d7e9b981808ea3ffc7a6d`  
		Last Modified: Sat, 28 May 2022 02:30:37 GMT  
		Size: 11.0 MB (11019421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f22fde9ffb3511f19f6a84ee5511872740b6a37e844fdb93326adc895f8dde4`  
		Last Modified: Sat, 28 May 2022 02:31:27 GMT  
		Size: 56.6 MB (56621054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e40e3743d0f9443791b631dbd2e880c126f0e0b354f3ddaf616db8aee716b959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140655941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a64297443d9fc0ee9f07a050a732ddf0707059641e5ac53d78c75cccb02940b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:35:07 GMT
ADD file:7d4f085f5fc874b6142d1d0a27c78512d764e68948baffd110bb6e1ff77c725d in / 
# Wed, 11 May 2022 01:35:14 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:23:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:25:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5d4115fab6dd67cca7bafe684609d704cd4e4c3229c7f62f0f1476fe5cfd02`  
		Last Modified: Wed, 11 May 2022 01:45:26 GMT  
		Size: 57.4 MB (57352362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6e8dc2a59c36e07c0ede228c6fdead6ecc03a566fd7328823d686733347f92`  
		Last Modified: Wed, 11 May 2022 03:51:04 GMT  
		Size: 8.5 MB (8492692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6348a08a5fd7953090a3d9ecb22bde8041eae82839726dcf3cfccffe516ee74f`  
		Last Modified: Wed, 11 May 2022 03:51:05 GMT  
		Size: 12.1 MB (12065584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea355dee2bda8ba0c778bfafd143f25e8d2c2ece067b8c73b09037c1734d665a`  
		Last Modified: Wed, 11 May 2022 03:51:31 GMT  
		Size: 62.7 MB (62745303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fd3cc837816d1a0228bd7f768a64c21a714e119aaa698d28294043093b47c94b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121209867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a2ed42ce64de1d0f3896c884c71364e39ee6b518595612d87d16689e4d70cd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:15:02 GMT
ADD file:2406fc75a54a3bdd547095c2a1dba6a536074c482469bd532302201fd8585b5c in / 
# Wed, 11 May 2022 01:15:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:34:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:39:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:642ffa8f974e66e7604ce50484153cb3846bd0cb22b2911d01ae5ea68df5291f`  
		Last Modified: Wed, 11 May 2022 01:33:44 GMT  
		Size: 49.4 MB (49377677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b907969c96c55da8d5b6b71e6af3f13438e5d6fdd5dfe41d51bbedd23697a79`  
		Last Modified: Wed, 11 May 2022 03:17:33 GMT  
		Size: 7.3 MB (7258557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d53965d18bb01a1ca71823c7fcbe5f088068e2ef79d5e1c6a55c4d71c5b4e`  
		Last Modified: Wed, 11 May 2022 03:17:35 GMT  
		Size: 10.7 MB (10650582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942330f4ec5637f6c0393c379b17ad805deb19c2fbe710dcaff8061460659625`  
		Last Modified: Wed, 11 May 2022 03:19:57 GMT  
		Size: 53.9 MB (53923051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4374dd1d27fcc67faf2f4134b4ec71ab327cbd51bea6723f9a6ae17d6e7563e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129096711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cc5d8a837103934b1531ea96605316345d012abee326a141dad1bd9bb59c42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:44:37 GMT
ADD file:03a528116badd98d1660ab1a83ce0462a11168a2dae972be4891032c54483f22 in / 
# Sat, 28 May 2022 00:44:41 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:28:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:28:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0cf941fb152b37e3fda284ae5eceb3dab36c26511fe06a7105ee43081ca68554`  
		Last Modified: Sat, 28 May 2022 00:51:02 GMT  
		Size: 51.7 MB (51703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ecd77e960fd212da3eca4e59b9c918e4d7af7e1ea705150c26c05f5967f79`  
		Last Modified: Sat, 28 May 2022 02:36:52 GMT  
		Size: 8.9 MB (8938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b6e701baf55072de709e3a913641d40af39439387278f3abde5d58deb12714`  
		Last Modified: Sat, 28 May 2022 02:36:52 GMT  
		Size: 11.2 MB (11157585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394d800eeeea5c5491bdadd4fd5e6397e7591cca3df4558fab6201da7b3eab68`  
		Last Modified: Sat, 28 May 2022 02:37:07 GMT  
		Size: 57.3 MB (57296990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
