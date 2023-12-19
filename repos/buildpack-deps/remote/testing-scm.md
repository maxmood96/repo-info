## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:2591701ff76a09f6f0a0a421a0c1600c0df38476e78184140756786298713402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c0671311fe2df63cb6409bfc09fb8981d8340b18f1095bfb33c7526b6a26dd16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142065621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4dd427945b05d85995a35fa4d41637c064ea78cdf1cc59adc53f627d7097623`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:39:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86533899ea4c6a05c0bc99be1cf97d8c7b1864649d1d7b07f04486b15f07cb0`  
		Last Modified: Tue, 19 Dec 2023 04:45:40 GMT  
		Size: 66.1 MB (66061532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:13bceeb03345c9a59eac75e79c3d51e7fcd73ba4f6b510649a033585731dc1d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135833971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c888f7c37c41a6c2475dcea11c0c95537cd1b746e2673e122ae4fb352585c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:29:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66a9a66c86c09cf82b78482882d191231a14e757c4087a6351318a0a4750a2d`  
		Last Modified: Tue, 19 Dec 2023 05:35:26 GMT  
		Size: 63.7 MB (63675825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:09b8c9c77dc2d85b60d4cef70aeac990f34b08f000e2ead506363105e1f36d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130335588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a1249d1d797ccb97cd3fb0ede5f01d03b44f168707353214d26808331f8e97`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:10:03 GMT
ADD file:3a9b07d7d2dd3958b5dd3f5e10d02d2e2f612023edc0a993b72001585b39fffb in / 
# Tue, 19 Dec 2023 02:10:04 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 08:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 08:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5fdfd0725abb7810a629f5d363de8fc6e2d9dcb7251dbd35de649c96745cd052`  
		Last Modified: Tue, 19 Dec 2023 02:16:07 GMT  
		Size: 45.1 MB (45080555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc6f8d845eb2d7a99ad733d60426b1890e2dae97e2c100045f2a994f37727dc`  
		Last Modified: Tue, 19 Dec 2023 08:10:31 GMT  
		Size: 24.1 MB (24059302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaf87f01b13e2c56d32f7922d2c5a19f02303d7e15d431e44ce223f7f3c2bc2`  
		Last Modified: Tue, 19 Dec 2023 08:10:51 GMT  
		Size: 61.2 MB (61195731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9b8986ba543d946187b8c26349ecde3edcb0112fd2c27e08f362b5e1c277b605
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141008154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2406e1f99a452aabbb862577d2e816ff3e79019d35079785c5703e6f89d592`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:50 GMT
ADD file:b661d22b170c983d1f8f6e1899757b3ea7418ea86f47bc616943149dfde25bbd in / 
# Tue, 21 Nov 2023 06:28:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:04:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f05f219707556ec064f3738b8347f22666ebc44f11201375d02acfd29240356`  
		Last Modified: Tue, 21 Nov 2023 06:34:35 GMT  
		Size: 49.6 MB (49571278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48906cee9fa2510e8f3e54f1027f9f1046eb7c9331600c58e2eccc32e1147c20`  
		Last Modified: Tue, 21 Nov 2023 08:09:40 GMT  
		Size: 25.8 MB (25827922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f062b3f69830199094fd9bd9a07a08b65ee4def0bd5c712c6ee103880bff09ac`  
		Last Modified: Tue, 21 Nov 2023 08:09:55 GMT  
		Size: 65.6 MB (65608954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe2f5901d6fe0d1944a3856bd2bedb58332b2f3049ace7138edffb4668c677bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145782750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2fd75b070f0a4c5276459e18f30b018df15fae60a9f1d899cbe1e1782ddfc8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cab3bcda927a6bdf058c09d2eb156aa0af0222312987068a8db4995e0e7b38`  
		Last Modified: Tue, 19 Dec 2023 03:42:10 GMT  
		Size: 67.8 MB (67818215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d1dc0b8fdda160220d48b8e2d0efe0fe602b51705fcdd4a12e81de92e80f6cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139714589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b21ef50f4ae8cd5a1aac2dee9f4573f60c80c927af1e3a651567b79ac682fe8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:16:18 GMT
ADD file:5a5a104714237ebb36fb780708ec93fc6f37e226c70a6cb07acb454559074354 in / 
# Tue, 21 Nov 2023 04:16:23 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:49:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:51:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d49b5078b4e69925915d9f9be6cb94f93e60122ef1d800b354bcd8216ec830be`  
		Last Modified: Tue, 21 Nov 2023 04:27:30 GMT  
		Size: 49.3 MB (49327517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9d3064a22d3ef7862a5268a8afe02ea1fd4667ea569463a73e72e664e09e6a`  
		Last Modified: Tue, 21 Nov 2023 13:08:31 GMT  
		Size: 26.1 MB (26073748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20a1437fbf153264541271f63ca64815b844be642e2c03279cb0e53ad0725bf`  
		Last Modified: Tue, 21 Nov 2023 13:09:24 GMT  
		Size: 64.3 MB (64313324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d10b4a6b3ef635a2b679169bacda8ac4b674df60ae3371a03c8a1f5cc86e7a93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153174776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897ba107c9d649eae78c14111b541fbffa91311376657fbeebbcb7275085fe88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:49 GMT
ADD file:dc6f1d4d555ba3f35237b7e67b320c18ac6e1c8d12a95eedb8a5230f42402844 in / 
# Tue, 21 Nov 2023 04:26:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:03:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7e2ccd81c8e1fab8cf4a7e3dcfcc9c9057946f10830bacc66f9e35e00b25e3`  
		Last Modified: Tue, 21 Nov 2023 04:32:41 GMT  
		Size: 53.4 MB (53437879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da93de48b4e366a300fc98f49a68981fa34793ac393d57b3adda3769aff47f`  
		Last Modified: Tue, 21 Nov 2023 07:10:36 GMT  
		Size: 28.8 MB (28814830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09699f0245492a67f8cf23ca1a57b1830e534c2904c0101f5032102ad5f2c4c1`  
		Last Modified: Tue, 21 Nov 2023 07:10:57 GMT  
		Size: 70.9 MB (70922067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1d100159013e1c8adf66e4d726229c66136a96d35bcf66efc131dc14c7fcdfa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143157876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9fb9cc2b6588aaa49c5519d3d627bf8c3b6d33ff4887f09eeec8f36d2c9a66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:45:30 GMT
ADD file:b16365f9cf7d013b9f58428c1e63b824b4c10cd69e7e4899e47af1a279108581 in / 
# Tue, 19 Dec 2023 01:45:33 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:50:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b824578a72fec7523b71b452ffd659ecf374f66d41368945e63eaefb55285ad8`  
		Last Modified: Tue, 19 Dec 2023 01:49:59 GMT  
		Size: 49.0 MB (49047729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3918e3f5a21f3ff19f3099110f7748b164e79403be43cfceef60cb243c54219e`  
		Last Modified: Tue, 19 Dec 2023 07:56:10 GMT  
		Size: 27.0 MB (27013250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741832ca2803b66ffc8820965eb933fadefd163fd8b192600c3fc4c2733868ce`  
		Last Modified: Tue, 19 Dec 2023 07:56:24 GMT  
		Size: 67.1 MB (67096897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
