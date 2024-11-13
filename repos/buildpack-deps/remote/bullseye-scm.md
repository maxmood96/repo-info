## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:da5b63b001c7fd1e3848311c92018c1ae23dea341002a7e34546c586107e4a32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:540e7a62b63872321d2c383afd57c95a18ae18b2f5ceb5bcc0cdd6df05db8576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125402461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd55a9e99939cf7c5acf4c269136ff35f63aaa9a844090e0b1371e26552ae01c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7aa7ab778ad756a4f5b94a9de226627f55235ccdf11496a0d182f3bc0ee3f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bcf6ce98fa3bc15782ab2f19e9d7e2b0086c50da9d6bb74813f7de64b3a923f`

```dockerfile
```

-	Layers:
	-	`sha256:a1e5ea0b3a869821c16ffa4ba2bf5f7cac5d4d91a864463741aed3d1441e916e`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 7.7 MB (7720136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f7d1a03ede92d8e8005d05cde3f0bc5596c387c4c736f94ba3a94d1aa52014`  
		Last Modified: Tue, 12 Nov 2024 03:14:05 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0b27afdfd77d75f7daa15242cc63d12c81c15bef9bfdf3389220b78e4b71c5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115732934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fea1c1109f52736fe3129fe2d91df3883572414c5c1c122f693e794c1cca2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d17122d5550612fcfb8bdb86e3884095b4bb789a98d27dec66b7b6363b515ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7728923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a8a3069eb6e9c82d3c4c18ddb245fd1e026f21f27ffd7382878abd6e0251e7`

```dockerfile
```

-	Layers:
	-	`sha256:6875125c6a3662c299a57970ecff8767213464540a3f4b2443f46582d4b59612`  
		Last Modified: Sat, 19 Oct 2024 06:37:58 GMT  
		Size: 7.7 MB (7721498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c133ef3869a8610514a32152844f53057e7d5043e5788c21cc57d2487ebb1a5`  
		Last Modified: Sat, 19 Oct 2024 06:37:57 GMT  
		Size: 7.4 KB (7425 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fad764dca1afb9d5ed0c4a860ade11f9bf47e382ffef6c27585b54f76d1c1f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124142744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eebaef5f9ec18d565a0443d4a966e2bc5993c9b3c08fecbe3c128e5b11f2435`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9e545ff305fe56558a94b064a901c16b373a3501daf5519f82ec19db6a3655`  
		Last Modified: Tue, 12 Nov 2024 11:16:34 GMT  
		Size: 15.5 MB (15543588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952be101e4ab063ff4eafa1d2809245e9ac9e713c342da9f201d2280d4a6c9b`  
		Last Modified: Wed, 13 Nov 2024 02:42:41 GMT  
		Size: 54.8 MB (54842084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ecf1d6096ee569b3305ca895d03f0cf4ed6853b5f2b012860cecd5f2ec9a0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7733308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa18e52374bf24b029c1eace5a916de6aca3fb9c70c7172d02810ab66ce5bbd`

```dockerfile
```

-	Layers:
	-	`sha256:6aad38936d8c50842283a826822caf2b85d3b0dd0cc9a1c657b1e75edcf44881`  
		Last Modified: Wed, 13 Nov 2024 02:42:39 GMT  
		Size: 7.7 MB (7725875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:224e45f9c93f64a7486b029f1a1a8f448f6aa6fb5143c96fabb7cc39e27208a5`  
		Last Modified: Wed, 13 Nov 2024 02:42:39 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:abdacb8dd3629c36873bb6565bb5355bb43e35599717521edddba9275708ca78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128187827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3519d81e879877e50e48707a4c989ea967331bf5b66e4edbd4517f2f68c0c5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f57fdf5c9316bd657fa92242f94a7a45fc7b72ff77e45c1afb81c50264750afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7722954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7c49e19c31ee997e83662326c7457752c1ae0084f5cf1d96e437c0a414b61a`

```dockerfile
```

-	Layers:
	-	`sha256:cac73e9dd9c0a64923bfc98da0ae2d1e496fc28c574c818636b78b29f41a46f8`  
		Last Modified: Tue, 12 Nov 2024 03:14:13 GMT  
		Size: 7.7 MB (7715624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5177cad227d9b19951172f747480276aa38502fbfbca8407d68577dff7fc57`  
		Last Modified: Tue, 12 Nov 2024 03:14:13 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json
