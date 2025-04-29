## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:0152cc48ae2d95e8099a2cca65be0bf3da4c983dc043e9b6faaff4335e690962
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
$ docker pull buildpack-deps@sha256:91674b4ce13641337858cc0dbb95b52d51f25603cd6c9f56bf34628ee5dbc44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124267290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5580359fcb4b806eeb7f42c3bf461962963806a6918a25063619c5f5ffe47d73`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d5439f5a946716b4c9de8fa23097613cbe3b9ee583f9aa761c91f7e6aa0547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7717555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8838b48e8169f66c5f2ccd0c8badff0abf4025d9de67396c4e44d71047ba599`

```dockerfile
```

-	Layers:
	-	`sha256:570354adfc921fb736f8fa2635b0ee208663b73d13367a81c1bb1544e4a0b225`  
		Last Modified: Mon, 28 Apr 2025 22:15:29 GMT  
		Size: 7.7 MB (7710202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7c7dcf1ab33669fec376224dda535284367d56bbbd46c57d57a76bf103d272`  
		Last Modified: Mon, 28 Apr 2025 22:15:28 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a7599e11741b3a4cea1ae65781ca1f754d30b34b3eb41de30c3a8f30ca4b42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114534614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c80872d38aebbc923a49595323bf52e41454e7448777f82424ec121f408592d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a8d7ffecec45a7446dbcb6a7c32524d48ecfe3fcd22bffe50a52e165d3045c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7718963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea0edfda4830bf4b3e9c213576bceb9bd18acc6d4f4eb3241c8545faaeb79e0`

```dockerfile
```

-	Layers:
	-	`sha256:7304849978b2c660be9b31c832a33ac189647750bb60d2360f41cfc1bd4c110c`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 7.7 MB (7711550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8333b9cc8106a989db3a76aee88d64028aa2f5043e9ed46dc2d4b7bb19fa966f`  
		Last Modified: Tue, 08 Apr 2025 17:30:31 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:90a79f6f2a751ae8b2315e716f3828ba1ad180148c580f17927fe5909c549aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122853317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b56b4bcde03d08a17d65621355470cb9d4dfc5d893199e281f2dac9e94e4b5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da1e6ea956c4d1ae53505da4ccb571eadb5c4678c979b7d0ca96e4ff01d5c36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7723315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42df8661e7343868a88f667be7c264772fe0cf0006e747edded938733763525b`

```dockerfile
```

-	Layers:
	-	`sha256:1db9eac15b89a36b454fcbb31302cb2cc00a67417c8d578a27f05a4894d47386`  
		Last Modified: Tue, 08 Apr 2025 12:18:41 GMT  
		Size: 7.7 MB (7715882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8338bcce7f2b41c54270ef37c6ba3e877bd811964940388c541b3346296a3c6b`  
		Last Modified: Tue, 08 Apr 2025 12:18:40 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b5a580f4245c4c11a4eb9fb8dfc87fb496d9ba30847ce6500c1e7ee8edb6c465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126997781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51501b77717fa5a0c58c1d56e9eb8e06b484bb768fc90b64b11b9f2b99cccf76`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Mon, 28 Apr 2025 22:14:52 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b525157db8a2e253ad998c04a076fb9317e63c04063e5ceaecb6e576a0f9d45e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7713023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5594e04b02bb15b30092d7c2bac3f822eb583aa51e3d21c27d71e94cd23ed378`

```dockerfile
```

-	Layers:
	-	`sha256:f752b4aac00c1273b3d2aad28fbbd8269a1bd3f8e8ea0782ca16db9a00a069a7`  
		Last Modified: Mon, 28 Apr 2025 22:14:50 GMT  
		Size: 7.7 MB (7705692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee106e6aada708ffe8c8cd116404b4cb408cecfa849fa73c6fb5543ca66417f`  
		Last Modified: Mon, 28 Apr 2025 22:14:50 GMT  
		Size: 7.3 KB (7331 bytes)  
		MIME: application/vnd.in-toto+json
