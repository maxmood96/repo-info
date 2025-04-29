## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:dcd7e6063a52b7502352f4889006bc221c3bbd552d41fa7af49116b761c6643b
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
$ docker pull buildpack-deps@sha256:89e0e8ee18c18bcd557baa3b191a73a65b7903734659bdd2a753ab3369517ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114544235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0065f7b2e17933ec104c9e407a3cfedc8408e967268187f1e2fd0ebb1f7c9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4334dc5f6a657a6699424d6d49382e4c147affc0af7cc3264b211c749c1af9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7719017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61977d91bfdf04bb1c0300937871b138a78d5801b5b7e5fc1a8ee1ab44d5ede`

```dockerfile
```

-	Layers:
	-	`sha256:9b44968b99e9d4ceb5ad497496828848de9aae18c0cad47a4d3ea6cfcd5ee411`  
		Last Modified: Tue, 29 Apr 2025 13:23:49 GMT  
		Size: 7.7 MB (7711604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0bbfa05dbb8376bb3e1ea146cef22cf05d5ad4a272ca78547f8f99a4ff03e5`  
		Last Modified: Tue, 29 Apr 2025 13:23:48 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:223b848bbec4fdaf60f8181a194939b294eaf97559a0d3de2f3fe1dc7434a6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122845088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2d2e27c5a7b613701bcaa68e1cb8a4d5742aa6020e6de13189f9c078abc9d2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a2b567a7a90e2a256addc0e35c6dda160eb4583fc666fe4cad28e46d03751ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7723369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e78fbe9ee21cbb8415f4b5058cd35a3bd88a06c3a4dea5575e77257c884a20b`

```dockerfile
```

-	Layers:
	-	`sha256:2cc216d0dacf6934b7a3ee8753b641642a932b58baace2aee77bf3c64c828502`  
		Last Modified: Tue, 29 Apr 2025 18:37:53 GMT  
		Size: 7.7 MB (7715936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d07e859e7684198bb5a863d8661456a59556c19cffecd4e41a2bf7dd0b81dd6`  
		Last Modified: Tue, 29 Apr 2025 18:37:47 GMT  
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
