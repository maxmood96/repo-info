## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:fbbddbf5f22ac7c7c8ecc9fcc471d8949cee637b3644bfbd7ee2cd153da554fd
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

### `buildpack-deps:trixie-scm` - linux; amd64

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

### `buildpack-deps:trixie-scm` - linux; arm variant v5

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

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:90a681e8e90b6720921b8f7ac6294c41fdbdb0b3352a3898522409425e690f5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129588885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ef0b823d873fb6d43427a124bdb38b6738c0afee2a830b1d27b87b454468ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 03:59:58 GMT
ADD file:59809e0abebdd1dc9132ad810fe8f3f2944fb2b6fa8df3e129a60d19cf0a0235 in / 
# Tue, 21 Nov 2023 03:59:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 14:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 14:11:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a13157ca2b3325f6cfce85c5d417fa81a8cf7c5536e5efd4164b11bece6ea33f`  
		Last Modified: Tue, 21 Nov 2023 04:06:34 GMT  
		Size: 45.0 MB (45025780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16faa22bdfe8beba1cf1ebd5a35e015985f50707921bfd4676c129f65c1a8e9`  
		Last Modified: Tue, 21 Nov 2023 14:18:13 GMT  
		Size: 23.9 MB (23949711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9b87af5a0303242349bd3387e8e710da8c4bed4c8b6c9248b7adbe02282821`  
		Last Modified: Tue, 21 Nov 2023 14:18:32 GMT  
		Size: 60.6 MB (60613394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

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

### `buildpack-deps:trixie-scm` - linux; 386

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

### `buildpack-deps:trixie-scm` - linux; mips64le

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

### `buildpack-deps:trixie-scm` - linux; ppc64le

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

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c1151634c7e3a017b784f1eb9a20d31ca5b19e61af07410c71d068ffca257b06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142290545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585f78d00d4e7d5176cfb4e20e019ad8271fa52f40eae6313924bd54827c4bde`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 05:07:59 GMT
ADD file:d0b90d4f8aa4259bbd6e1887bf2da65394e444995622363495d2e13ad00154bf in / 
# Tue, 21 Nov 2023 05:08:07 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:12:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b094bae18b4460a8208634d7220fba165e3979b123ddcbdd060fb9c73c37f2b`  
		Last Modified: Tue, 21 Nov 2023 05:12:26 GMT  
		Size: 49.0 MB (48970235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e58498ddda5b5285e62304a232a3204b2c0d769172de15744b3afdda3b07cb`  
		Last Modified: Tue, 21 Nov 2023 06:18:57 GMT  
		Size: 26.8 MB (26829362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09114f0213626e79784208aa286e09335b4ba1f291eb0eca1b085809f09d3a4`  
		Last Modified: Tue, 21 Nov 2023 06:19:11 GMT  
		Size: 66.5 MB (66490948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
