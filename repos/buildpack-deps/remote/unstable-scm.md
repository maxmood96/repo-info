## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:d7ae0c397257afff69b4f143db4e1a5f47e900689afabbd8685368b32adc8a1b
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
$ docker pull buildpack-deps@sha256:42bdfcb48e4acfafbcd7969840b3931935dfc049ad6a11875f7db06126ee39b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131791649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d276c6c0a435226741bc7e8ee231e2339867418a4c397cfce7a622eaf42c830b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:21:07 GMT
ADD file:0aaeb8a0c7fde9f030dc2ab67a03f21f44e9eecad9e4cf1f360dc5f768292460 in / 
# Tue, 12 Jul 2022 01:21:07 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:51:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:51:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a81bc091a3ce5ccc3c89ef56e710ee1854c5ff9fd3d7f148e87cb956b5b78c7`  
		Last Modified: Tue, 12 Jul 2022 01:26:19 GMT  
		Size: 53.2 MB (53226349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b567a2d645b715cf7eced5f75816db7c980c3416be39e599e6e4b0bbc82f9eb8`  
		Last Modified: Tue, 12 Jul 2022 02:57:17 GMT  
		Size: 9.3 MB (9295637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303c4db152401668239f15446f8107b320fcfdc241030fd93f94783340b469ca`  
		Last Modified: Tue, 12 Jul 2022 02:57:17 GMT  
		Size: 11.3 MB (11271765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cf65a8772cd0616a80dfa0049c8ec6ea822121ccf534abed287a6206d6e1ca`  
		Last Modified: Tue, 12 Jul 2022 02:57:36 GMT  
		Size: 58.0 MB (57997898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7714d745bbfd1bee0a659a5662658c4b97f0d4837ded37aed06c03ec7b64ff3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126405974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3011c8b5fd2e2a5933c1801d482c79b1cc2c68e44efbc78e6ae92e90714364bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:53:06 GMT
ADD file:d09e1e4b772f7be41e6f5adcb5a71d86548e6099876e8d5d1bf8eb816a2d8cf9 in / 
# Tue, 12 Jul 2022 00:53:07 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:47:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 01:48:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c8fedff5488db39c94b1a6e628f1dd8a8718a76f0b9f0a65f57e06652448e9f4`  
		Last Modified: Tue, 12 Jul 2022 01:06:36 GMT  
		Size: 51.0 MB (51027952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fdb9c4c566afe6ee79f348756dbd9b7b7752109285ecc12936279d515cc71f`  
		Last Modified: Tue, 12 Jul 2022 02:03:57 GMT  
		Size: 8.7 MB (8725449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece2169f6168d0cd57063262293e9a5e841d140a27a657883596ac7fb3cafeaf`  
		Last Modified: Tue, 12 Jul 2022 02:03:58 GMT  
		Size: 10.9 MB (10940756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50438d01e861fe384e7553119984ecff7f7b3803745a0459dac979d7b2f1825`  
		Last Modified: Tue, 12 Jul 2022 02:04:49 GMT  
		Size: 55.7 MB (55711817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f0c306b7e214d4f02d5b66ca26ad3fa883563678893109aae543ffede2087980
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121298032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359ee98f448a75a647321f5a292d095517e0b633da45957764d554b779f8df53`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:03:16 GMT
ADD file:51a321e16e02701a4130fcd4804ef7e14f5facfab8a82cdef3c2fd228a4ba034 in / 
# Thu, 23 Jun 2022 01:03:17 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:54:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:54:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:55:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2391a5c3a80e9c0555d4b398df748ee8be95db129c7c16e82cb7755d493118a7`  
		Last Modified: Thu, 23 Jun 2022 01:19:50 GMT  
		Size: 48.7 MB (48734709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d1193f1a87016b7e352fd620d9d5e616526a8c1d9ac8cad6c77aeb6559fd09`  
		Last Modified: Thu, 23 Jun 2022 02:18:45 GMT  
		Size: 8.4 MB (8405462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59543246561323586b73771e4cfd176cd7d73ca9c0e20cceba57a93111ba12c`  
		Last Modified: Thu, 23 Jun 2022 02:18:45 GMT  
		Size: 10.6 MB (10572843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb1f9d675028e4babe5d9856696abdc7cfa4b462b98ef48396f316fda0b620f`  
		Last Modified: Thu, 23 Jun 2022 02:19:25 GMT  
		Size: 53.6 MB (53585018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b6f942361c32ac509c6072cd18dd9e331b90968745942d3fa5cc3d6c6f940487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130615124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e9871c0346e9651e8f217b106fa21e1407e8c0be5e30a163241800ef3f9686`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:40 GMT
ADD file:0f18dcfe7e502abae9dd7f72911dda640e4675306760d63f467092f962228ad1 in / 
# Tue, 12 Jul 2022 00:41:41 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:36:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:36:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d3ef27d3c918a6321957a64c33268d09a01ec18590cce79a144625d9c0c8599a`  
		Last Modified: Tue, 12 Jul 2022 00:48:17 GMT  
		Size: 52.3 MB (52331756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f3b169736466d16aa015562be48cd38804707291d997ad0a77f69293eb28a6`  
		Last Modified: Tue, 12 Jul 2022 02:44:53 GMT  
		Size: 9.1 MB (9139825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fef5554fb71c819accf1cb6b60a439cb9c6a8da7ad329ecdfa59582ef1f116b`  
		Last Modified: Tue, 12 Jul 2022 02:44:53 GMT  
		Size: 11.1 MB (11056631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0f540b5927de78a3401234b3c45e6a2af90069da738315da30619808488023`  
		Last Modified: Tue, 12 Jul 2022 02:45:13 GMT  
		Size: 58.1 MB (58086912 bytes)  
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
$ docker pull buildpack-deps@sha256:449a0169809c35be36bb3a36d2ce6d52e19d083682ef815d43b7f1ef13eceb5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128614028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8afeb8a2e1b94e3e1a5fbfa5b2364f8c2dd33add5a5348b1cf8a48bcad17baf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:13:03 GMT
ADD file:ee6af73e7954397e332676cdf91fcc81e58c7039ee0e6b28c76a45bbcd35f878 in / 
# Thu, 23 Jun 2022 01:13:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 02:09:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 02:11:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1122351c74d1f54ed8c97871bc43b5e9e533e877516d1335d49d0b35a135e12a`  
		Last Modified: Thu, 23 Jun 2022 01:23:42 GMT  
		Size: 52.3 MB (52302602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b60fb601ee8b9ce8fdf454454bc04959e78f2245d78fb79c1fd28d74c735fe`  
		Last Modified: Thu, 23 Jun 2022 02:26:28 GMT  
		Size: 8.7 MB (8657901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a790127ad374d0d7dce1e83718b6927775398eff00185730060dfa660ee1c63`  
		Last Modified: Thu, 23 Jun 2022 02:26:28 GMT  
		Size: 11.0 MB (11019511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6364d9f384bb225f74e3d8bf8e4a3192ed0f948fd01551882314335e40caa9`  
		Last Modified: Thu, 23 Jun 2022 02:27:18 GMT  
		Size: 56.6 MB (56634014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d214a6253973e331422ac82033ff47535c2b8fd5e4c8bc23b07143927157e37d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142131235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c2648b8a5deb29847d8e241bb03e6c05fe3e7b54f738b743d162d38886327c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:04:45 GMT
ADD file:c9757ca75462d85dc4d76c948caf7c9441b1f94311712aed484424049dfa236b in / 
# Thu, 23 Jun 2022 02:04:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:36:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:36:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 04:37:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e03a908039ec9067867d0cfb4e2137913335e7055a4de7caa5a17b06fdcfc936`  
		Last Modified: Thu, 23 Jun 2022 02:21:32 GMT  
		Size: 57.4 MB (57413710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012e0f9d40f6756a17c2a26c1540b57aef08309d861a58ee201ce546d8e16f89`  
		Last Modified: Thu, 23 Jun 2022 04:59:07 GMT  
		Size: 9.9 MB (9883975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df9fd6cda08db21eda8015d4fac544f2e705c64a73aa93ac154c59b04ee95f`  
		Last Modified: Thu, 23 Jun 2022 04:59:07 GMT  
		Size: 12.1 MB (12065152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e496ab4ce171004942cb8ef21469520bc06b27da4ba9e5ca43224e9a82dc2b8`  
		Last Modified: Thu, 23 Jun 2022 04:59:31 GMT  
		Size: 62.8 MB (62768398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a554d40bdf614dfd9e405a249dbfe2bff02cb93429ca042ff9db3c8e0b1c3124
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122419082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eef1028664b4597959820e5ea3724c58b7a5eff1763e4f7d9729c7729d13014`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:11:50 GMT
ADD file:e156d172727c94dd7b17970577469d9b556db67960762f454d5b90dad3f746bb in / 
# Thu, 23 Jun 2022 01:11:53 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:58:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:59:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 02:04:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70334332338a08f7ae515b43812936d5898e62e8ffd5fd38ba59761c5ed137d9`  
		Last Modified: Thu, 23 Jun 2022 01:30:12 GMT  
		Size: 49.4 MB (49429796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5fc26886e551b626bc82f99096f4659ee9ee5af689dad0d03fc75d88c37d88`  
		Last Modified: Thu, 23 Jun 2022 02:51:42 GMT  
		Size: 8.4 MB (8394795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6176147b43ca0f721514815cbe526cd0e19723ed30c23a9a3534a95d32d19cb`  
		Last Modified: Thu, 23 Jun 2022 02:51:43 GMT  
		Size: 10.7 MB (10650389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feebc8d66990654882c5fa423a1a4c713b77656fe3fb7540e4e51bbfcd8395d3`  
		Last Modified: Thu, 23 Jun 2022 02:54:14 GMT  
		Size: 53.9 MB (53944102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2b47118b90a37280981e27753473870698226c8236b58191eb832721da3affeb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129131202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453ace87d9c651cbfa6003070ecfc31e9bc0a4bb51c4a00bf9ff8d14a0250556`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:46:07 GMT
ADD file:160fd6ac1dd96abed2e1719ac95e75e8a8eeaeef9e04a353e0ba4a23cbd1c1e4 in / 
# Tue, 12 Jul 2022 00:46:14 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:45:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jul 2022 02:46:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4ac3f896d9c36c21fdbee9a7ab2637136d4d09ef6db30c3b2b4ab10c48abbe7`  
		Last Modified: Tue, 12 Jul 2022 00:55:11 GMT  
		Size: 51.8 MB (51757401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7d0c4835633a8b04da06d28abb8af4b5557ef25b136337b6872fd92b710b70`  
		Last Modified: Tue, 12 Jul 2022 02:55:25 GMT  
		Size: 8.9 MB (8939218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabdcf7f5d4d109945eb55d7a1fda36ddcf55c65eaff794d0456ee0e0e2e30f`  
		Last Modified: Tue, 12 Jul 2022 02:55:25 GMT  
		Size: 11.2 MB (11162924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bdd31018381fccdd1cda9c7f537afeb37f464aeb418cc92baa60a4b3a165ab`  
		Last Modified: Tue, 12 Jul 2022 02:55:41 GMT  
		Size: 57.3 MB (57271659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
