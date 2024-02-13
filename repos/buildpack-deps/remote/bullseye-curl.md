## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:dcd9cb8a57e52aaa529a7dd9a614695180080d0869e52395bfc34fa69cba5569
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

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:33e2f726c178caacc3a3230f83bd503fe5d23202237256adf9e2b55af0ed86ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70848370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4230b3e4bcd298bd9ab076e5def770bacf8ca055d26bca243a35a3a4809d17`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c06bc5e596da68e541d1945e2c738494bbc749fee351b2aa949aa71bad6612ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67961817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4a2ec3c57ecae85345a0bcf9597d695fbd108cb75be3ad5cda7475eec249a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d258d0865d6b4269397d1ca385bf94ac78bce402a330982fe9c5cf6cf5e74`  
		Last Modified: Tue, 13 Feb 2024 01:55:14 GMT  
		Size: 15.4 MB (15374936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dbae290c16d068690f41fa20ae4285f139c2706e0146ddf9af72f24ff472205b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65120886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b0ffc707ded7337ff84765b4690514940a640c78d9494ff8730cf14369c2ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:606a04dc618c5b285d40fb7ec84d5732923f38fae0d4c4b7489b942fe35e01a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69470627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a912445217af04d8625a1b0b0e6d8ea4c548702559d8141eb63e00584b001b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:181b00ca45a400f3506725903a0f1bb9204e4a008af41ed8f31db39ac32d89ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72325550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa4f0bf68a9df19c762bb7d1faf854d4ce88305489a3e298bfb9abc459b4edf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b007e9eee1eac08bdb963983b9aeece5c26d2ee98d848406f9e3be6013ce52fb`  
		Last Modified: Tue, 13 Feb 2024 01:30:52 GMT  
		Size: 16.3 MB (16267766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f612116154a8cf673eea8fda22e01dff265d307a3a45f34ee167d6ea414c9456
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69037563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4039f57e6dd822bcbdbef762b1eda72b73357ad98ac20061d2c1977f09e876a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:04:48 GMT
ADD file:f0c2e3e71ce8133518aba22664b25c63fbd8c964a5c5ce64025477e120c8e59c in / 
# Tue, 13 Feb 2024 02:04:54 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8fd455dd9aba699cef01f8ec9dcd521cc60e9d65f6f4a8b4682b184d6d9f01cb`  
		Last Modified: Tue, 13 Feb 2024 02:15:55 GMT  
		Size: 53.3 MB (53303273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3bdef7a4adaf4b26d1c9d17cecf0116391ff83640a2b297c799a3c9ab2486`  
		Last Modified: Tue, 13 Feb 2024 04:23:58 GMT  
		Size: 15.7 MB (15734290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fd015c1f0467981471c9c92bcc21db0a267145b239cb36cec5bd65e5f0a56dfd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75697648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c624aef848904d6e2ac0494e4b4e7ba0d1bafa9ec6ce15c44f771db492d04e3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3b00da3f11b464d553016a1ab9c3bd2f59a79bcc555c40465966cba535158248
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68960598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46db613acfb3f425b19419a4cd8be40519a125cf1784908dad907d7dcea2b4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b73853a3a5d303ce5a91d0496492ac8084773db71a7ca85f6d20e26005340c`  
		Last Modified: Tue, 13 Feb 2024 02:58:56 GMT  
		Size: 15.6 MB (15641273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
