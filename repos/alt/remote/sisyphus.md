## `alt:sisyphus`

```console
$ docker pull alt@sha256:639c2b48d6a30cde3644d50dd389898dee001133dd40322489ed830d3fcdd4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:bcaf63d09de0e1e2e42a04817a2a7e541e94f8858235a03789a6c00c9151c54c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42101073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da81890842f38eac308ec785de82dcfedd5c1b174482e4e7386a3ff537c0bcf5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:20:09 GMT
ADD file:fa6b11057bb920616089ae6766f3d1b7f8d49555a9a7541d533c6c62ff822b11 in / 
# Wed, 09 Feb 2022 22:20:10 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:20:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9cb3d64353589bcb25d988689617e9dda18d6bb15fc228910d1748498c0799a`  
		Last Modified: Wed, 09 Feb 2022 22:20:55 GMT  
		Size: 42.1 MB (42100881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5e87d5a50caa36a0e4c4347cb6717e2728facfe342a1a75d6178215e0047f`  
		Last Modified: Wed, 09 Feb 2022 22:20:49 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm variant v7

```console
$ docker pull alt@sha256:04dbcb41df952df999742e85ca4bfbed9aa9c79d368fe1259d1c035d529d9348
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38560575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992c8ead5fa4dc7a92fc0af6f9aa0b99ae5b8a4d86ca148b756357ce89001e85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Aug 2021 01:09:27 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:58:34 GMT
ADD file:a2ceef9e01c40ad1c8509f438d42924a7bb5c30a535f11ca5fc80caa5ca57d4a in / 
# Wed, 09 Feb 2022 22:58:36 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:58:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a31cbd45aa4ff6b1ab7260e7671d014ae6b92b583f7fd4d2ab19a94fa7e1594a`  
		Last Modified: Wed, 09 Feb 2022 23:00:38 GMT  
		Size: 38.6 MB (38560383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa3efb91db530604e365cf9fd0f478f30d14c2e546f6b353cee9a8ce56866c`  
		Last Modified: Wed, 09 Feb 2022 23:00:14 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:a3e87362d519b2951e6a05424fc9748f12f836a24f33e01c869bcfb4d83f8095
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40739290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a955369e8f599e251b071f01b7a1a2062e6e78407313ab7ba49d7afc33457`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Dec 2021 16:01:29 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:41:35 GMT
ADD file:8ee4a7599d0e3d697995a050c5325c75ba6d1cb4aefae3afabee90c8a069ba6e in / 
# Wed, 09 Feb 2022 22:41:36 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:41:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6aa11d6c759fe44835a556f0192a7f1b23e63010605953ebc0fb8600b893bf60`  
		Last Modified: Wed, 09 Feb 2022 22:42:28 GMT  
		Size: 40.7 MB (40739100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095d5e12d9699cda881a4a8fd6c2f990ec1911f42317593253bdbe80e1ba10b9`  
		Last Modified: Wed, 09 Feb 2022 22:42:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:b0c6578ede21a2e480c1b729e30c933d41adc42c7291c01898fa37f34d48be22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42392516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480b298142a8bd3de6019b59d811d5c3394febdfb31efbad6d13aeb528f31079`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:45:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:39:09 GMT
ADD file:cba6be4baabc9d4cba537262ed6a58e13128b9a57d9564e463c2979d6e64275e in / 
# Wed, 09 Feb 2022 22:39:10 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bf7445c14d0312856a28ab4e4ff966d6534b7b7404b8d15d0ed38f9530ef41d8`  
		Last Modified: Wed, 09 Feb 2022 22:40:10 GMT  
		Size: 42.4 MB (42392324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b91e0f5c401031476f947c1156ac51b8d4bdc4e0897a5a5b444fb96b439901`  
		Last Modified: Wed, 09 Feb 2022 22:40:02 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; ppc64le

```console
$ docker pull alt@sha256:fcd7841be80def833bf20150a44dc36de6bd203edec439839b3eb1e326e93022
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44859644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b92dc0fdf4018d5c678bc2e65e8758f30894313b0c65ee8683496e6a1c3a3f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:29:43 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Wed, 09 Feb 2022 22:24:38 GMT
ADD file:0e95b682787f1ae30d91ad1bad192ffa42728f818fd1cbe8b5f916334b0afdfe in / 
# Wed, 09 Feb 2022 22:24:49 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Wed, 09 Feb 2022 22:24:51 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cda4c58921d124961ae872951d44169f3d545c9e580698137746e448d8da5ab8`  
		Last Modified: Wed, 09 Feb 2022 22:25:56 GMT  
		Size: 44.9 MB (44859453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659f8ae4991b1203646966f80800b9ee37339042f15fc3b51b2d3e6657d7968e`  
		Last Modified: Wed, 09 Feb 2022 22:25:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
