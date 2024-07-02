## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:ff08d266b8fd2358fc78cd35acf4b4e08ac7031f31badaa20a649495b588e2fc
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2667097b245ebed9c19fab9536c9c95832453f7a966257795797179cd5d7d5eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125434171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a00380ff311262cece625a2d1d12ed8dfbff1a3382f5a283f6d78c71e9c92c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da238dd9d1f579bf4f3cd6589e3ab75747f8ea35be2bf50403f8f3fafa942eea`  
		Last Modified: Tue, 02 Jul 2024 02:01:35 GMT  
		Size: 54.6 MB (54588637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e421248e422f93e3696ad2d583025fbdeb246185d36668a2768c9fbc4336d9b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120289934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bde3d7d0cb989d47b9602a2bd92ea4a503334c6f000d449a6015db83f29b8b5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:35 GMT
ADD file:cb32078a57dd8b6e640717e8afff9bcae9ea1cf42a7bd24509f83795da6d69ed in / 
# Tue, 02 Jul 2024 00:48:36 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:15:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbbd165d7f0cb06245f1b11503844a1b512035157df3061a56ffc65bcd1fb0fa`  
		Last Modified: Tue, 02 Jul 2024 00:51:50 GMT  
		Size: 52.6 MB (52585748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55ce9f73827a53b1d65974ad06aecf88b83eb2b3dbde871489157a0a524be50`  
		Last Modified: Tue, 02 Jul 2024 01:23:51 GMT  
		Size: 15.4 MB (15375188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9122a9bdc64b2bf9d3d2754acd565e00d5cb246e7be6b39e5e2ab6d02e2b3a62`  
		Last Modified: Tue, 02 Jul 2024 01:24:09 GMT  
		Size: 52.3 MB (52328998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:acce8d91d72c0a3cef88346fee422f497074f93ca5907c83c77dcd7d07528085
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115476591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e2880a1dbc912c9a6c38634ffb9cfae02b3f155c15915e6eaf7e066e24fc33`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:11 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Tue, 02 Jul 2024 01:00:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c595e4d8c2d2c7ad66ab723b54c73c6a0aa876b01511358ec8af1aed8c8b94`  
		Last Modified: Tue, 02 Jul 2024 01:40:13 GMT  
		Size: 14.9 MB (14879331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577c5fe1f5243a6910c54b7b4a338cc9cbae0cfeba74a350b011d2a467e49daf`  
		Last Modified: Tue, 02 Jul 2024 01:40:31 GMT  
		Size: 50.4 MB (50358262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:78a1705430080aa1449064e2437d48b39c14b54085a4dbd017e06b336e846b7e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124166275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71dbaf9643ff77b80b3b18db7dea38a1341cacfaaeedbf094d402d8947695c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8ff66c20c22817ea8b9af919feaec04fd453ef7c2d64b36d5195cc6ac64efec2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128260366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e6de2efbb0126ce3cb20efaa6a37a564476938d05f259d0dd952f2d8514e96`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:05 GMT
ADD file:e6fa59569d6234c463e39f7c2465f2984240a5e8cd613c1ffdc14ab3abb4a7ad in / 
# Tue, 02 Jul 2024 00:39:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003014d72f23a9e0b16eb59708032ad565fe8e24244a34ae5b65e72f56314d8d`  
		Last Modified: Tue, 02 Jul 2024 01:15:23 GMT  
		Size: 16.3 MB (16267863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8e3ef3e76ff601cae23732babfc202314066da48aedac550440cd3cdf72f2c`  
		Last Modified: Tue, 02 Jul 2024 01:15:41 GMT  
		Size: 55.9 MB (55927528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f0284d31c8effbb73e3ef1c1859487e4646a00461cfd3f25a8ce31c290311600
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122351954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45093b893dea280977d7efd8422b88b624f37c1bd231cd96d1e7aa73a357b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:58 GMT
ADD file:c27c9e3b89ea2f05df44728fc1fc46f994aa335600846cab7240fdd415afec7a in / 
# Tue, 02 Jul 2024 01:19:04 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:05:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:47b1b1e48b458e7bb52034561a02c3a9df945540ee55d2b8112f6501aaad6d66`  
		Last Modified: Tue, 02 Jul 2024 01:30:13 GMT  
		Size: 53.3 MB (53306204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca902fb3ff705493024175dfa7b750ecd6b69939807e1032182d84553f4e2b8e`  
		Last Modified: Tue, 02 Jul 2024 02:32:52 GMT  
		Size: 15.7 MB (15734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b25e341950d66380e7def2b99a1ad6804e2693911e88a6f3fb36c897514564`  
		Last Modified: Tue, 02 Jul 2024 02:33:35 GMT  
		Size: 53.3 MB (53311036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2cc88c86683ac9fac20d2cd564fe274feea49fe08706d092f4f64de9349d7a52
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134588900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbd152072e2b7e5e8ac25abf936112544070e1bd9dd7c241fbef753721c6c80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:47 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Tue, 02 Jul 2024 01:17:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:47:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8661ff02529d6818e558d6049a746391403c023c68ac6d75816221bd99e3244c`  
		Last Modified: Tue, 02 Jul 2024 02:05:47 GMT  
		Size: 16.8 MB (16765868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93f0edb37745f21593aefba0898d81dbc780a39dfe73cf03491e10c88480878`  
		Last Modified: Tue, 02 Jul 2024 02:06:04 GMT  
		Size: 58.9 MB (58872635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c3530691466b5c9aa5f53e16ffe498847b44793915005fe14a750c1c4669408f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123036957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecbabb04845da06d47e72cae5d31da62e8551ea022a1e7116ce710f7e879272`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:57 GMT
ADD file:5752d26037cbb262eeafd1819ecd77ecf8a8cd0019683c05fb92c50c6a458861 in / 
# Tue, 02 Jul 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:35:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aa9549a3d8effd17bc1f93fd40d83261d2505d37791c5aa837c9f7c0fff5c9e3`  
		Last Modified: Tue, 02 Jul 2024 00:48:47 GMT  
		Size: 53.3 MB (53319825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7860b53e214213e98b388ade5c0d289331e291bb4e43197e4a14a4e8a111583e`  
		Last Modified: Tue, 02 Jul 2024 03:45:25 GMT  
		Size: 15.6 MB (15641817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b8db73130bc88255a98f66627e7258a074a0223eef8b550e6c1084068d24d0`  
		Last Modified: Tue, 02 Jul 2024 03:45:38 GMT  
		Size: 54.1 MB (54075315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
