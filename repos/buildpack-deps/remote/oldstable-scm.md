## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:c9a4e3ecf3749f27ad5d7bcef0bcac633eb853643f47627a38cab37fbf5b5192
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

### `buildpack-deps:oldstable-scm` - linux; amd64

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

### `buildpack-deps:oldstable-scm` - unknown; unknown

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

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:830b6954c70d048ff92b456e8ffe4dbcf182daca29b6b49bbbad09a984381271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115569782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caffbed5cce66c0c8982d81579513a17c884ca118b20af92b57ab9b49e776a51`
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
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b22721db94b1c5fff4e7c6f09aa650c06de76f3b42c9ec977d76b8bf11c268`  
		Last Modified: Wed, 13 Nov 2024 07:38:50 GMT  
		Size: 50.6 MB (50624136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b23e1865d916cdc8789829a0ee4c44af59b896f84418987afdef383043c7774f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7728947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22ce4c82e846985b53a61c5bf85aeb0485c78d1628b11dc2483be2c3c5f4439`

```dockerfile
```

-	Layers:
	-	`sha256:857879924c2b960fe7b46fc7a8050cc0041f2296d4f0c92eb836f4f1f9e277b3`  
		Last Modified: Wed, 13 Nov 2024 07:38:50 GMT  
		Size: 7.7 MB (7721534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc60bdeb8477a9b6c1efa83a7facc8d429596e00a4ee67eeb1dec64483bab87`  
		Last Modified: Wed, 13 Nov 2024 07:38:48 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

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

### `buildpack-deps:oldstable-scm` - unknown; unknown

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

### `buildpack-deps:oldstable-scm` - linux; 386

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

### `buildpack-deps:oldstable-scm` - unknown; unknown

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
