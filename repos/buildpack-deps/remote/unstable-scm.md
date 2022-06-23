## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:6cefd8f9c924873204da3a145cbb478739bfad45718579f77e6c06341da5eff7
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e29b1d0e636faaaab0d309b057b744605d424501fd3789917230f511c2a426ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131784236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6b8717186a33e6b3db8fe42c54e93bdc3c94c440ac713b4f488ec60c85caf0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:21:33 GMT
ADD file:5d253befef9729db59927d6e0d60fc3d68d46edea7e014babd24f72ac3a437bf in / 
# Thu, 23 Jun 2022 00:21:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:53:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:53:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 00:53:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d3673f28ea1768e72855620961143c989d7f371e6bca9954aea151e92c37b180`  
		Last Modified: Thu, 23 Jun 2022 00:28:29 GMT  
		Size: 53.2 MB (53218973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ae65eee62be843f104a65e140f50abf4d3ec55a20e85b9e3f7d2cfad04120d`  
		Last Modified: Thu, 23 Jun 2022 01:00:54 GMT  
		Size: 9.3 MB (9292311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6091239aaf7cc50884c05faa6c40bbdf0de0a133524daaebd95e5128d36a0d9`  
		Last Modified: Thu, 23 Jun 2022 01:00:54 GMT  
		Size: 11.3 MB (11264406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e0035db86f2c4cb2e7be73d8634723047f8cca5c7260b8e2792b5d7a795402`  
		Last Modified: Thu, 23 Jun 2022 01:01:13 GMT  
		Size: 58.0 MB (58008546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3f88fbadc739e07eac0d2674c0aee342f3f4160a828633c094b434d540e579c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126253539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac37bf086fa55f7d53c87b574dbdedc5bd46b01266eeafa3cd8f2acf7b1dd60`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:06:33 GMT
ADD file:e64ba6aa11d10902c0a4ef8d3e05a21ff17f500ec2beb0d0704f12a033eecd07 in / 
# Sat, 28 May 2022 02:06:34 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:15:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:16:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84223462af5a86d80ca0b6ee4295740a256dc6c036fd9bf8911e3d45aac34d9e`  
		Last Modified: Sat, 28 May 2022 02:23:20 GMT  
		Size: 51.0 MB (50961426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f88c92295b4fa5d01d5c7dd27b573f1426efbbe47348df31dc55de977a42f8e`  
		Last Modified: Sat, 28 May 2022 03:36:29 GMT  
		Size: 8.7 MB (8725167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb95b40f6f03c3c9f4041396fccdad464a167dcdabf7faa4ce59545b10eff9e`  
		Last Modified: Sat, 28 May 2022 03:36:30 GMT  
		Size: 10.9 MB (10927897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af801cca276fe8a8c2fa1f3f2f395ef1bf390a44b25cbcd5f6c27c81ee430fe5`  
		Last Modified: Sat, 28 May 2022 03:37:20 GMT  
		Size: 55.6 MB (55639049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f6bf52d8b4ec798004c8caf4dea72484ad827e47d2a35fd354f51f4381347b1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121223856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ef01a0f272ce41bdbc63946e5a099585429d87cfca89546e3955bf3f12f5da`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:03:25 GMT
ADD file:8021dbeb20862f976e9f6edfab38dfb8756a92dd1ede73d49af4c657334e675d in / 
# Sat, 28 May 2022 01:03:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:50:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:50:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:51:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0e42766a606a457d26f0182502f6f1920959f31aa96f3bea8438d9c1662a0e5`  
		Last Modified: Sat, 28 May 2022 01:19:59 GMT  
		Size: 48.7 MB (48693491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c18451f312662604904a27a75c2a619f95996c3f8953c2894835994ef1938f`  
		Last Modified: Sat, 28 May 2022 03:14:46 GMT  
		Size: 8.4 MB (8394033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ababb74aefd4519ecdc1de94bab8271fdc2ba7a6a0b2288e65d7452f33cf91a`  
		Last Modified: Sat, 28 May 2022 03:14:46 GMT  
		Size: 10.6 MB (10572851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a64aad191116b0a523175f0713d0852be12924ca13142989d6feaecc7dd86`  
		Last Modified: Sat, 28 May 2022 03:15:34 GMT  
		Size: 53.6 MB (53563481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d3303a17c94ae966f4734754be9d2d091b2e55d9c0694e1b1a3a4fa36d1dda3b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130453704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62edf6792cff0f27d834f133d7c23ca4b2901aa0a24290171c1800afc156d48`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:42:04 GMT
ADD file:f08e8dd302c69f11b0631751a00fb9468d4bd358c6e3c34e364eae4601f0a325 in / 
# Thu, 23 Jun 2022 00:42:04 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:14:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:14:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:14:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:40490949eb8203de1427980faef5b6b648ec81967b0cb93ef80fb4a09d798555`  
		Last Modified: Thu, 23 Jun 2022 00:50:02 GMT  
		Size: 52.3 MB (52287486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd1881ca7c4691be4824f0eddf333c4f2ab5f1ac743ee1c8c554a75da079933`  
		Last Modified: Thu, 23 Jun 2022 01:24:16 GMT  
		Size: 9.1 MB (9132621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852bea5bd7a74a6867d8c61780e5bdaaad07e160db0bada549bc1b04e63e489`  
		Last Modified: Thu, 23 Jun 2022 01:24:16 GMT  
		Size: 11.0 MB (11041937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bb12213e9f6fc3859b16595e8478ff8f3156869e99a0f9352d29da9911e50e`  
		Last Modified: Thu, 23 Jun 2022 01:24:36 GMT  
		Size: 58.0 MB (57991660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e1f1bc3f1310339b07caf890d9ea7cd0230c7380f848425153526681209a16d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134606360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6232b96a9f3559f92841699393871a63ec25303a3a10b4f7432e93377cb7aa7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:59 GMT
ADD file:8e587a340c6b6c6dfa097954552e77cf8a794c99a1462d0c2062dd4f3b905687 in / 
# Thu, 23 Jun 2022 00:41:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:15:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:15:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:15:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:82252cde47e9fb82645e6353c13b39594115b4ab4b96e5a602245359036bb69f`  
		Last Modified: Thu, 23 Jun 2022 00:49:29 GMT  
		Size: 54.2 MB (54181034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a804107ac0ac6b959662ec593acb07f7f7900f2753d01cc321b3f498797ff54`  
		Last Modified: Thu, 23 Jun 2022 01:24:44 GMT  
		Size: 9.5 MB (9465816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3278139543c9edfb79cec19d272bb6af19642454308507ba2015c252c4b5462`  
		Last Modified: Thu, 23 Jun 2022 01:24:43 GMT  
		Size: 11.5 MB (11464249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553753d1d94d5a84b19b44ef5dd89152d8c95834466d6f78894d6f8d41a1c878`  
		Last Modified: Thu, 23 Jun 2022 01:25:05 GMT  
		Size: 59.5 MB (59495261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

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

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b997f364233a3e1e4fa01fe36128a1be13f639765c90d9862f4231b7fa6c4520
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142079779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93322eb05603c6d18f31e03c23ab9a86c73203aa1a419d058c089e4b0a88ed2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:25:12 GMT
ADD file:ae9857e5f5e911c083920a02f175061f1626b33e8244c6b286b16a61fb6326ab in / 
# Sat, 28 May 2022 01:25:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:23:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:24:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:25:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:37e804d95f71e07756995895c16c589fb7c512c0b5fda75c9e57d4ba10ea4c27`  
		Last Modified: Sat, 28 May 2022 01:34:49 GMT  
		Size: 57.4 MB (57378472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7461effc372e5ee4bd7909ed036e44f7b839da66ba136f7add0d1221c18cbd`  
		Last Modified: Sat, 28 May 2022 03:38:27 GMT  
		Size: 9.9 MB (9880924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3a54c3d4f16e2101943055448a74b563c54f32ad957a68eb5dba4c980373c3`  
		Last Modified: Sat, 28 May 2022 03:38:27 GMT  
		Size: 12.1 MB (12065230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d030f83cb04ad5b06d1396bcda4925db17a6880b92c2161c73a4a52615c076f`  
		Last Modified: Sat, 28 May 2022 03:38:52 GMT  
		Size: 62.8 MB (62755153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6b1367d956b5dfbfbb71443192cd4f601f842b30696ff4ea55674e2c8ae3dc4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122382331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7fe5db8fa7d99cede7b23cca134144ddecf885f6a1d29fb58f7838c08f69ac`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:14:59 GMT
ADD file:e8683ebd7fe3c7f8d36edee19a4eb44173d2c0533a248bb49edfe18fbbec52c4 in / 
# Sat, 28 May 2022 01:15:02 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:03:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Jun 2022 07:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5fcc51d6aaca235d0204fa542679e8c928a4f929dacf2d472c004f8bef16292b`  
		Last Modified: Sat, 28 May 2022 01:33:36 GMT  
		Size: 49.4 MB (49398978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11875dbcf4bf154b85cc0b226364129a3a766fd9696699dece93ac84fc30ecff`  
		Last Modified: Sat, 28 May 2022 02:44:06 GMT  
		Size: 8.4 MB (8388372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcaa3fee1a4ad6e285aa0e16f72b33694c419b2821bdeec5341875dc49f47c6`  
		Last Modified: Sat, 28 May 2022 02:44:07 GMT  
		Size: 10.7 MB (10650485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e27ca9c7481f28619ddde6f60a59911202108797689731eb9c1350eec0ebba`  
		Last Modified: Tue, 21 Jun 2022 08:11:45 GMT  
		Size: 53.9 MB (53944496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

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
