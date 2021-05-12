## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:fdf9954356aefaf3bf4ec3ff237e67ffbf34697720ad92c05edd2b2832ea6eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2f11f9a4ca82cc8e1f8f9c0622d1d15431cdd9354a1c94b86fa2a8095724b12d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110770907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89503f94b7f88574822c5deecfd5afedfe370a2aece38d96d78173ee65b3b93f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:23:05 GMT
ADD file:d9e4f6f4fc33703b766642a5642cabb2b01675bb55cf6050f2e91507577ff570 in / 
# Wed, 12 May 2021 01:23:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:59:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:59:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 02:00:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bfde2ec33fbca3c74c6e91bca3fbcb22ed2972671d49a1accb7089c9473cac12`  
		Last Modified: Wed, 12 May 2021 01:29:52 GMT  
		Size: 45.4 MB (45380083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787f5e2f10471c11a2064774062aeeb400f76e9eef1ca768156a23678f005f3e`  
		Last Modified: Wed, 12 May 2021 02:07:25 GMT  
		Size: 11.3 MB (11286410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6173a10eb81a318ed53df74c8b80d29656f68194682e51f46f9b7b24c6ba03`  
		Last Modified: Wed, 12 May 2021 02:07:24 GMT  
		Size: 4.3 MB (4342456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc05be471d511acb4574f2f3630582527220c59d0abf0b8b905769916b550da7`  
		Last Modified: Wed, 12 May 2021 02:07:47 GMT  
		Size: 49.8 MB (49761958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4771cb456f2f8798ae1fdca15494dd76ac23af0e7560980b147486db80be4f21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106572653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed458b157beac13aab41e8d973b36ca926888ab2a8002aba0004d8444db97b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:01:01 GMT
ADD file:f9987935a0f0d3057590a5bfe45c9d8aefa9e442c57db487f8b67540669b57d4 in / 
# Wed, 12 May 2021 01:01:05 GMT
CMD ["bash"]
# Wed, 12 May 2021 02:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 02:39:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 02:40:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a6665c6433be6a95f09c5848a9d88c4bccf7d8279967ab968e389649b956be87`  
		Last Modified: Wed, 12 May 2021 01:12:52 GMT  
		Size: 44.1 MB (44092037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3302a801fe4dd409937e6b92b6e20266d055b35f4a59f90babdc2e2e206ef00`  
		Last Modified: Wed, 12 May 2021 02:49:14 GMT  
		Size: 10.3 MB (10333925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32206e34e189aa99d7c49c7bd5a1d95471b77acce0309357d260203cae17366c`  
		Last Modified: Wed, 12 May 2021 02:49:13 GMT  
		Size: 4.2 MB (4161500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c965fa519fe7c195c998f159c81bb38028dffad89b2231931d113d7640d175`  
		Last Modified: Wed, 12 May 2021 02:49:44 GMT  
		Size: 48.0 MB (47985191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:41fbcc1a77ece08226463e79369d05c6eed4ba014e066b77e69c8f3ffa8e221b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102107338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031b45ec8599b43038ab54ee3ee59bf590f640317e65ec0257bce9363c2ab80d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:11:51 GMT
ADD file:81cfd4e746bdfcc19847240b77012487652be22dbd5741ccb2485a4207f2b73f in / 
# Wed, 12 May 2021 01:11:56 GMT
CMD ["bash"]
# Wed, 12 May 2021 03:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 03:53:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 03:54:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:55b9a6b6b2552c5b2eac0a316e75a7bc18092819ee25c4f1d4d54700bcc1d3dc`  
		Last Modified: Wed, 12 May 2021 01:21:23 GMT  
		Size: 42.1 MB (42120307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9949293f349d0c9019996e174c80df7a8a710fba2d4f1155451c228e33bc1f9e`  
		Last Modified: Wed, 12 May 2021 04:04:11 GMT  
		Size: 9.9 MB (9939912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260f0f7d4174518bdec698aad994bd3fdc95ebc5b34c60ed84955b118cccebb`  
		Last Modified: Wed, 12 May 2021 04:04:10 GMT  
		Size: 3.9 MB (3921255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b560815c9657e548da0f3b44c74b3669291c71ef08e2dcaded2c5dfa6c07393b`  
		Last Modified: Wed, 12 May 2021 04:04:34 GMT  
		Size: 46.1 MB (46125864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:34a58e779a54fae4cab5e6599fd57074e909ae8446b38f45ddefb7796464d95b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105212137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69815fec05bfce31c8bc9fb2f69f6def57b5c821c05050c784ad55d24b5037fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:56:12 GMT
ADD file:9582243afc9973a3708fda530270ae8f23796b20a532a9f07e4faaf245e2cdc0 in / 
# Wed, 12 May 2021 00:56:18 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:41:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:41:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:42:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41f38ce3010a5142300d74e5e19db4dea7694f4771471c330fff27c633f8ba32`  
		Last Modified: Wed, 12 May 2021 01:04:15 GMT  
		Size: 43.2 MB (43177820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ac4bedb842678b3f7ca4713dead8d22045096d5176f53f8d191785b69f236f`  
		Last Modified: Wed, 12 May 2021 01:51:20 GMT  
		Size: 10.2 MB (10201144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6e1b91eb654daaf672ce148b8e9bc5ba6326c274d202bab26c504f0451e73f`  
		Last Modified: Wed, 12 May 2021 01:51:18 GMT  
		Size: 4.1 MB (4096687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d312b156251ad6bb876bd760bf0fd069f10c10554c397edcf563553da2c1914b`  
		Last Modified: Wed, 12 May 2021 01:51:40 GMT  
		Size: 47.7 MB (47736486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d8993b11c1506200d1736a1c7950a3de3a7672ccab7f2cbefd92e481e4d90cb5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113266099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6496b08ff69e05af99d3311ab4cfc5b830450b54026e6c13049d94084616ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:41:41 GMT
ADD file:3b26e2f83a0edf42ea62d20102b47011ee41cd2ab349c9da7487f62ff21b8471 in / 
# Wed, 12 May 2021 00:41:42 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:12:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:13:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a179d76df60628ca372acea241dbf24d4039a86b7dc2ba920d26f64bded15a1`  
		Last Modified: Wed, 12 May 2021 00:49:13 GMT  
		Size: 46.1 MB (46098744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c213a4df67666087b0cfaa22f4d76fa708476c4f91ee848daccd8e1a9059682c`  
		Last Modified: Wed, 12 May 2021 01:21:01 GMT  
		Size: 11.3 MB (11336498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59de6391225c2ff4beecde954f63e31d511a479130b1acd174707008a47f717c`  
		Last Modified: Wed, 12 May 2021 01:20:59 GMT  
		Size: 4.6 MB (4564986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ee2df560b159f574ac071d2b70c54debf87201c8f108268b51b7b83f0cb410`  
		Last Modified: Wed, 12 May 2021 01:21:25 GMT  
		Size: 51.3 MB (51265871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
