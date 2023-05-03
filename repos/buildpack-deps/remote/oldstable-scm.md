## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:c930de23511cccf4af61bf52ff7bed60c2c442b83ae90a1ec90e08a6a7aa2531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:59aa732d6a99f3c3497e5cdeddfd4f6ef5363407c17bae1fbd828869f4f78e0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119907883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2647275e3f34306c699cf7eafb5ecbd4b4dd845cf31f7afc65e39ac956e048d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:14:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19b5081b1db3d1f9cb6b976463daaf186eb48aa03d63ea69a4b09f3506e6839`  
		Last Modified: Tue, 02 May 2023 23:39:53 GMT  
		Size: 17.6 MB (17580546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fab42f58c1ef3e6849f7c792aaa60c56b53a70e77977fca6fd201578b6295b1`  
		Last Modified: Tue, 02 May 2023 23:40:08 GMT  
		Size: 51.9 MB (51878611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:840401a938a7bae6476fd63359b2b29e659da496628604ce2f32beff32760f2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109519880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0478392093fada8ea9a9e2adb646edd728985d6091e90500dcb34cba5bee3d1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0100aae2782ccdf7a55cdfc65368dfa31bea8ad211255263c57da584967eb2e9`  
		Last Modified: Tue, 02 May 2023 23:36:57 GMT  
		Size: 16.2 MB (16211233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46e28591afdcb4ab771b00597a0d617f18f15f51dfd82d4c118b9031067fb6c`  
		Last Modified: Tue, 02 May 2023 23:37:19 GMT  
		Size: 47.4 MB (47392446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:96e03d67380daeace99ddc589fb25df608d86e8a2d78ef9d4635323c7774934b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119166062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2ed8743d8648e388b28b2c5274b320ccc3352bca03a56d3d0b65c133c5acf9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:08:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 01:08:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208fd617b499747daceba851b67da426c285d1e306b316a193f06968123f49da`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 7.7 MB (7732136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadebfda1423d1b70a0e991e9ff8bb2e3fe0b08d55562359a004c265fc7c86`  
		Last Modified: Wed, 12 Apr 2023 01:14:12 GMT  
		Size: 10.0 MB (10003581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe7e7c438113f5e58417f97e7eb0a755b17ee63eebd85a7c3b86a2aad4c993e`  
		Last Modified: Wed, 12 Apr 2023 01:14:27 GMT  
		Size: 52.2 MB (52191713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a16fd4acdc4794f5bae5d36740f91b0e59776009c559ca94d12138d2ecb1e00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122777728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054d039e9910e760cab0d90325cada2ce5fc39d7197a477c304c2002211d634d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:44:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd99c81a486e88f0f0651f64eb17ab23ef66618d2702b301568e0dedde54f37`  
		Last Modified: Tue, 02 May 2023 23:56:17 GMT  
		Size: 18.1 MB (18097666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb713ce4d6df9acc34bad743fb201e85ffd28c4667280dd9af9bdf5f80f2a46`  
		Last Modified: Tue, 02 May 2023 23:56:36 GMT  
		Size: 53.5 MB (53473895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
