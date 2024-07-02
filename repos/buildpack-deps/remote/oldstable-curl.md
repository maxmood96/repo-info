## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:2664effe6f3b6843422ae1929c4877948c6417f69a869f2884ec55832604532e
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ae423f26d315d668192d2b84696e337454f5d209e0438cecb02ecfe7d965d8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70845534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8bdda2c6064087e7233bfc346b1f8d75613454dbd1e7db1a4c976d5991f9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:93f351e82d4a8b05e60de5c8a75e254454b933e3572ebeab3591cb89b1f4a291
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67960936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e35a6c91c9c810a49e01aa80edfa4d85c0c03174ab68b477f542cb66fd4875`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:35 GMT
ADD file:cb32078a57dd8b6e640717e8afff9bcae9ea1cf42a7bd24509f83795da6d69ed in / 
# Tue, 02 Jul 2024 00:48:36 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0255beb3242b94aeac85f21472bd3eefc33bdbbaa166c0613587099443695f98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65118329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770c1352c76530f665658d2979a67c6e602015e2aef9d8ca872b18d13082cd30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:11 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Tue, 02 Jul 2024 01:00:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4bc65dbdf99b85e1d096a0b5fe82b7e18e999520ad8326df8dc8ef225adab48b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69471218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe19f2cd286b38892de1f8a24683cd9aec0ca038b7058f752e0298ab3262774`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c735b3a94a4984965fc9cd7b2c3f6a854f66a60c6cd18ad85b0a032cd84ea626
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72332838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c0f2880a9e91116a2c4c49f245c10090831981a9139a060b44251acfc7f995`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:05 GMT
ADD file:e6fa59569d6234c463e39f7c2465f2984240a5e8cd613c1ffdc14ab3abb4a7ad in / 
# Tue, 02 Jul 2024 00:39:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1e74df0d98406e6b343e1c6e13059275cb2efa1d8ee93d2d34e1717d09ae0354
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69040918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b4da15b0210ee093f56fb660b105c314ecac2cc7b6a857c5dfe95986747e8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:58 GMT
ADD file:c27c9e3b89ea2f05df44728fc1fc46f994aa335600846cab7240fdd415afec7a in / 
# Tue, 02 Jul 2024 01:19:04 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:71c61aaf5ded77878049b8e4bc43e5dd7cff7180c3dff04682f5429bb5621a6a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75716265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20aa294ef4b12b21e67f8409d999d9a0c48f1e4220b10b65829ffd947d15cbb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:47 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Tue, 02 Jul 2024 01:17:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:47:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:13fe48d9bae2e358f656f3ff3f18053305fbe1786579871634f4dc1cb2b0eee0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68961642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef19b1cfab848b38c33569a0acbfa1748aa61ef89c30ec6f9a3afccf7c598dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:57 GMT
ADD file:5752d26037cbb262eeafd1819ecd77ecf8a8cd0019683c05fb92c50c6a458861 in / 
# Tue, 02 Jul 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
