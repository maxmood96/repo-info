## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:619181479932d6d581fd77807631d4ba495c85bc35fe0161f252174bb8980f85
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
$ docker pull buildpack-deps@sha256:a74cdbcbd2e4fb8989e9f0659c3fe7c4693daddf5db31a4336d0a9fff7eba5e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142987876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129adc2f7a72789a1a148218ecde13379a552586ced05b0690a00e7c0044a5c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:04 GMT
ADD file:ef50fe9796d01aa6d5f96fd48a91fa7572137f06bc61426966088466af436be1 in / 
# Sat, 30 Mar 2024 20:53:04 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:01a297f066f8fc0bbbe233ce2512fb4efd2ccfdec3a317e7b2f796cfcc8a6851`  
		Last Modified: Sat, 30 Mar 2024 20:55:42 GMT  
		Size: 52.3 MB (52332501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfa6c10db0a79c5f80b9d9dd9d4c7f1aac92357e9f7e2d86820642467e3599d`  
		Last Modified: Sat, 30 Mar 2024 21:43:48 GMT  
		Size: 24.2 MB (24160897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ed217077cbab3a8045ced4bde7cf8f18ce1f44772f12fd815426ba986a514`  
		Last Modified: Sat, 30 Mar 2024 21:44:05 GMT  
		Size: 66.5 MB (66494478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9b202e18370d0b5daf6bd65fdc74b44b9a2beb387dc604e7bf5821079d6ffec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136604131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8096fadd752766e37c0a8eb7436d3abe284d061067230813d29eef0c77c0e187`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:14 GMT
ADD file:610edad9ac2672f29e192282a6bfb0a5bc5909a7410ce328dcee965f697f3e7c in / 
# Sat, 30 Mar 2024 20:52:15 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:17:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e2d9fb5eade7bdb964f6a5e67b4501451648660fd642b9b8493a947178b448bc`  
		Last Modified: Sat, 30 Mar 2024 20:54:36 GMT  
		Size: 49.4 MB (49422214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41a8b4d238b7be08d593a4029f99f33372bcab2e8fdc18f8284effa4d1c0d04`  
		Last Modified: Sat, 30 Mar 2024 21:20:53 GMT  
		Size: 23.0 MB (23041431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b58fc48be57cf2d13ee9a032f9a12e78a89d4e920b01edfc3db1a2244d6fefc`  
		Last Modified: Sat, 30 Mar 2024 21:21:12 GMT  
		Size: 64.1 MB (64140486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:403c95b800e81f8ff214e7b174678a3118cf703b5e9387d66a18e6687dab8d0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130781005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b1d0a45b7c1d0c6284b797e4d6b8c1a10b952b1ee863865c90d0139903aab0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9c6e3e6ce96fb41f02f466b843d37cc564ba933de9a8c733b54cc9095a60c0`  
		Last Modified: Sat, 30 Mar 2024 21:31:53 GMT  
		Size: 61.5 MB (61505430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5a7ba798a132371c9edf1e2136941f258449624e822eb1f7786329a20188cdaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142680898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a220d37191ad7fda6b47cb01ba0b5fda60e218f8b4d53d61c2fb469851490427`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:34 GMT
ADD file:4e62b2db165216904b425ba83d0b0d4c6186d832ff996f8b8c3b063774e053c6 in / 
# Sat, 30 Mar 2024 20:55:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:07df543a1d7c9498d71f3bbefc8b63ef01e65874f69ca50b6719f8aa26631ba2`  
		Last Modified: Sat, 30 Mar 2024 20:58:03 GMT  
		Size: 52.2 MB (52193164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8de779e2187666ead1e28d72960c6006d9591b628ff3bcf5f05debb1f209af`  
		Last Modified: Sat, 30 Mar 2024 21:43:47 GMT  
		Size: 23.9 MB (23879006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae63caa9a5413155875f8588f11232551811490c971f44ce81eb5af6b6772a02`  
		Last Modified: Sat, 30 Mar 2024 21:44:03 GMT  
		Size: 66.6 MB (66608728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eed184f7c0a8d3c5614a63902094e8b29d82dbaea4e9710e2591b9c3cfad513d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146751747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e487430056e803e7f442fafda3fb9030b67eca8226babf68a2a3e8ca55ed5ab`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346270e2a64ccc1d66f8b93818a9e57da01a691477de26749204ec49a036134e`  
		Last Modified: Sat, 30 Mar 2024 21:23:18 GMT  
		Size: 68.3 MB (68287345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:073778b7037e665c7deb59a4f06a254c6be933587f8fb58d705794a27a93e25d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141333448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db4c0353943ea80b7ba5e735727b8a5c912807d88ac7d1804205b190897140`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e46a7c1596412850ec91cc8e73fb58f10bdabe00c3a3878e5c415760e1882c`  
		Last Modified: Sat, 30 Mar 2024 21:50:40 GMT  
		Size: 65.3 MB (65297807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7383cc117938cb6effde90e11e6a0d3577d03642e71279f2df4f6984eb702d9b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154505398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fefcf5e1fd141eea29c1f426e1a805d63a2fb2ad983912acb4204dee42e05e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28cc0d4e61b8cd8c7b7e7f0f32f02fdf18eeb78863a40518a35ae1fa157877`  
		Last Modified: Sat, 30 Mar 2024 21:46:59 GMT  
		Size: 72.0 MB (71999507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6ef5e8408bd072a0ac31f8f64a403c226cfe3ef7da8e0a494dbfc930023532a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144583481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136dee4d4045ab4df58a51a0604007c8690124098bcd865054a422502b810c31`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:17 GMT
ADD file:a763a87b7a749afb8ffcbc72555a671734dd9d842834384eebb8dd784135bfc9 in / 
# Tue, 12 Mar 2024 01:12:19 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:26:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2f13ce6fc956957d2abf0abd272bd88a159c9cdf4a731647c572eb2581973c57`  
		Last Modified: Tue, 12 Mar 2024 01:23:47 GMT  
		Size: 51.7 MB (51738519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4953941dae1a90e29387e6e32120bb7c2ebca24adab5d68977c75cbd85a709bf`  
		Last Modified: Tue, 12 Mar 2024 02:50:10 GMT  
		Size: 25.3 MB (25296799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6744696380aedee2755d9dc38f57a9a70817812b1b1a78dccc3f68e5fe21f170`  
		Last Modified: Tue, 12 Mar 2024 02:50:27 GMT  
		Size: 67.5 MB (67548163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
