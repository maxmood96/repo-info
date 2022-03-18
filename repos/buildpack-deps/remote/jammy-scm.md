## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:f78edbc36c861bf270ff43de7cad0cd320ba226fffc4446bce85847975ca7d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a30d570e962d40a0e6834dd79937f2a1cdbca0cfd4786a9ada745edfed1a4e9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79771512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b154cd1cd8d96f6ad8fd9b462a4957e84c4867d8f4edeea09ad0d369172a892`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:48 GMT
ADD file:9819681ee3999b437c13bff560a32c11eff16275eebf27adae84e96bcd687c87 in / 
# Thu, 03 Mar 2022 20:19:48 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:58:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:59:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9e826c39a5168edf554e8eafc809c69b421ddb67d281f317701f2e68286572e`  
		Last Modified: Thu, 03 Mar 2022 20:21:20 GMT  
		Size: 30.5 MB (30494980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb206b552ad9a0370938de15f2c458e9c56d77ee5f395419096d50cbb71e3dec`  
		Last Modified: Thu, 03 Mar 2022 21:08:01 GMT  
		Size: 3.8 MB (3817774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f737cc5cf2dcb4287a621d97fd8cbc3b4a9b8e70058583d161eaac583b5f2203`  
		Last Modified: Thu, 03 Mar 2022 21:08:01 GMT  
		Size: 3.6 MB (3559354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95856a5340d77c45fac74b7b9a5da47147559b85588ed8995a11b483c8252f5d`  
		Last Modified: Thu, 03 Mar 2022 21:08:19 GMT  
		Size: 41.9 MB (41899404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fcccecf5a4b9c95f4e8c8207acac6601e54b80d3d7b62b06ae30c796d90b9106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78315723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef11ee4c6aed1b23fe7339467bc639ab1f34a302758536bc5df01c029320d73c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:22:18 GMT
ADD file:0a10344382f1ba734937e8e6730fdbc0f3c70bd476e280a38cdbc3014727d207 in / 
# Thu, 03 Mar 2022 21:22:19 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 03:26:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:26:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 04 Mar 2022 03:27:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a1275d98c22bf682d714805936f9472fc5c80dce170f257ff74996a6fce5ab2`  
		Last Modified: Thu, 03 Mar 2022 21:26:18 GMT  
		Size: 27.1 MB (27064067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b278353823b33d1827168c871378ab20bd5230f8daded3b9566d18f4293d4f4`  
		Last Modified: Fri, 04 Mar 2022 03:44:05 GMT  
		Size: 3.6 MB (3569086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254bcddaf4827926739a64d42bfb16189fc5540d0ff69b089349987576cb2f4`  
		Last Modified: Fri, 04 Mar 2022 03:44:04 GMT  
		Size: 3.7 MB (3712567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c89b9af5eb5159c3eea199ee30ac27e1de7b347ba6b51235ce7efacaa0af42`  
		Last Modified: Fri, 04 Mar 2022 03:44:48 GMT  
		Size: 44.0 MB (43970003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ad77267cb4ea4fd0605486ea29081deb8b1ae6ebbb7a6394e746f72345d368b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77297080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21be0a0e931247d10bfa97f11d0f0499b90bd86957bd2f6318b5747ebd38b1c3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:19 GMT
ADD file:bf6034dcd564f7c5f9ddf620c1dd7e0b870410717176db4e4db91c1bc6ee326c in / 
# Thu, 03 Mar 2022 19:41:19 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:12:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:12:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84df7bf04e98552ca258d4623ba2ee5c455a4f5eee4622923511caceaa69c6a4`  
		Last Modified: Thu, 03 Mar 2022 19:43:18 GMT  
		Size: 28.4 MB (28424704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de81b8d223c70c2ecff8735f6588279de47e4a3c3266d19bf621c5c4ffc048c`  
		Last Modified: Thu, 03 Mar 2022 20:19:41 GMT  
		Size: 3.8 MB (3792303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49986fba69bc0eae7347e2c6882c0b760ce11a31a258fb2694ff83665931577e`  
		Last Modified: Thu, 03 Mar 2022 20:19:41 GMT  
		Size: 3.3 MB (3319390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8402a169943d97ded64a733fe9cd21896e521ec0e8b9fe4524d7ae817818ae`  
		Last Modified: Thu, 03 Mar 2022 20:19:59 GMT  
		Size: 41.8 MB (41760683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:34000f1a6ac105b2403db9d408ce3b2cd6f061d5ea1df3a4f5906fd4482bb089
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77629191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c748ef8b6f6173f4dbf7ad1448226f2d8e4016d23540d2db1cd6fc470215fcd6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:43:01 GMT
ADD file:5596c6fcfdc9d3c4b63db527cacb4cac548690f6631b60dee4972329037237c1 in / 
# Fri, 18 Mar 2022 00:43:02 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 03:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 03:12:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 03:15:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:779c5da60b9290c00c305c706d5d477b0647cc028035cc1723db7e437a962fd8`  
		Last Modified: Fri, 18 Mar 2022 01:01:57 GMT  
		Size: 27.8 MB (27792674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d84b474ce4102d31d6fd8cea63267bfece598ec610fe1f5612b795b0960831`  
		Last Modified: Fri, 18 Mar 2022 03:49:04 GMT  
		Size: 3.6 MB (3611244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4323e0585e69caede2372dd7a23853990eae0fe4e7d87d98456fda8e0f48e7ea`  
		Last Modified: Fri, 18 Mar 2022 03:49:03 GMT  
		Size: 3.8 MB (3775054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c642a2f1f533bed60af71d21875a89773835c6cfc32cd7a8e06aaa82d88f26`  
		Last Modified: Fri, 18 Mar 2022 03:51:17 GMT  
		Size: 42.5 MB (42450219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7b180245a238403946fb394eb07511c2bfdd3d04c13ceb98f08a10913347be2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77948068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856ec75ac69951f61c987080dc62b1e5b7fae9ef6dc6df8818b270e293c6448`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:42:11 GMT
ADD file:e270bb54763417246152bf19cf8c73511429a8b205cf2a2bd94af25bac061f43 in / 
# Thu, 03 Mar 2022 19:42:13 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:38:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:38:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:38:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6caa8a5ada21e95ef49af26f44e5b9c877678b07df85737ef8814d77b47351e8`  
		Last Modified: Thu, 03 Mar 2022 19:43:50 GMT  
		Size: 28.8 MB (28804416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85996336099f18359c21d360ea8d78490be17e76a0a0f5851c75ea270c020696`  
		Last Modified: Thu, 03 Mar 2022 20:44:53 GMT  
		Size: 3.8 MB (3818536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93aed7c66b846b8dc2c3f0e054d16a44d6140c1de0843adad70bac28992a7004`  
		Last Modified: Thu, 03 Mar 2022 20:44:53 GMT  
		Size: 3.5 MB (3470297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e00f42adc53bef1ad03c4575f1ad8cb2afc9881ac631f04c339bf84cb25bb6`  
		Last Modified: Thu, 03 Mar 2022 20:45:06 GMT  
		Size: 41.9 MB (41854819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
