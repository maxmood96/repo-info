## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:63dceb420dd1f35491eddb52c7aec1eaf6335e6bddc552aeee2eae211b3a7434
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8eab756f646b732a7dc889ae8b8edc6b7910c99a726dbfef4d55b84e097001c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88704738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc073b53d6ac3a55820ef7f37b3b01f8eab8d306c872ee6dd8cc8c3273bfb59a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10f2d793001e79ccc6be8c28ad194b0142e46f3ea6c14095699bb7ba44ef3c`  
		Last Modified: Sat, 19 Oct 2024 02:06:23 GMT  
		Size: 13.6 MB (13616706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed9a6a1726d06e0402223e684a198aad45fe01804a81aa58967a03d085b6dd`  
		Last Modified: Sat, 19 Oct 2024 02:52:33 GMT  
		Size: 45.3 MB (45337669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2a09e9dc33036b61d80e379ffd5129d921c9af74fa05aac5fca717149fb56f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cebdd3000d8052a20f7ae88451c5cd8ccf95751b8cbbd1374dd8c343905396`

```dockerfile
```

-	Layers:
	-	`sha256:fb57808df518ee10975192da49d52cf1942c3a864b2a5633e74b8359dc522a03`  
		Last Modified: Sat, 19 Oct 2024 02:52:32 GMT  
		Size: 5.1 MB (5076079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3045d24ebd20c1b16edafcb0f97642f4592eece82164dc9a906540d80177a4e`  
		Last Modified: Sat, 19 Oct 2024 02:52:32 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a06d232a7e643f4daa3c698adada949fc17a0fd20f47b1debeb8504404577af0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89538068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a39be091951674a4cbb94634063aca7bf984a766831b1fe21c8ad39c1b6b27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:49:10 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:49:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:49:10 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:49:14 GMT
ADD file:eba80434f5df435e13e0c4a971c865a8fe930d18d36089192130267316506ded in / 
# Fri, 11 Oct 2024 03:49:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02c8f8f0873a74c67ece25c25d14882bda4d283742faf5b1b57c79636c7bb7a3`  
		Last Modified: Wed, 16 Oct 2024 01:28:34 GMT  
		Size: 27.7 MB (27734804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59877cb0baed413a6f7f191bceb85156aae185047f8a4191514a949478e74899`  
		Last Modified: Wed, 16 Oct 2024 01:28:31 GMT  
		Size: 12.8 MB (12775197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c34db50907d073cf30d59433a5b4eae93a48fa52ede9ea3b913d0b753160ad`  
		Last Modified: Wed, 16 Oct 2024 01:28:49 GMT  
		Size: 49.0 MB (49028067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6936451af0ed0a91229fc21e2c2c429ed854077e5b6360fae94e8089dea36fbd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88843450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9ddea909fdbb18cd569092953e76b7a61efb90a9c6aed2db4c7e8ff835c81f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:25:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437f1ae3840d0d52b5ee6c8725a6f8d1a0536cd1c9a3eb2c0f372603443d8d93`  
		Last Modified: Wed, 16 Oct 2024 01:30:38 GMT  
		Size: 13.5 MB (13453267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b150961a20a0a06d6f810da85fa0f3e06e5942258e8d0f0ba7003e35f0fd02c5`  
		Last Modified: Wed, 16 Oct 2024 01:30:50 GMT  
		Size: 45.4 MB (45437380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3038197fed25007eda3256f4b2a57b81d6e897193c650a3809533a5b713f6b9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102142893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f197312de325f9248d1193327d98608528ff57eebaa5475f93ffa70840537d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:56:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:57:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7231a69ac9743a365979e5be9d932fc4406b48dd5b449dd3e4e31f8b083fde8f`  
		Last Modified: Wed, 16 Oct 2024 02:02:09 GMT  
		Size: 16.0 MB (15991302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0b2b4d7e49ecab28973a1234e450767a55095ee5c46d9f6c5fda68a69d661f`  
		Last Modified: Wed, 16 Oct 2024 02:02:26 GMT  
		Size: 50.6 MB (50640454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:58bfee3b37ade385bd6d4489243657d8d601d1e5acac4ba402f472cd02c7236e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100207463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed1ee396bd81d04e194c94f7be101f93dfa563fd21a6f0ff9b34aecfc8fd3d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 04:10:39 GMT
ARG RELEASE
# Fri, 11 Oct 2024 04:10:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 04:10:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 04:11:12 GMT
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Fri, 11 Oct 2024 04:11:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 03:15:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 03:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:204f07d74c824e98a1cfb23ed6770fe82046746e00606a5575c65c44415d86c7`  
		Last Modified: Wed, 16 Oct 2024 03:23:55 GMT  
		Size: 31.9 MB (31946420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8083d881e7983d0ac4992dc5b5733293b09a9fe0502fc7e7bb46a26d095483`  
		Last Modified: Wed, 16 Oct 2024 03:23:43 GMT  
		Size: 14.3 MB (14321281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866f7e1c8a9b4315a0ed15211421dba0019460f8a9083a212fa9fc751b5b81ec`  
		Last Modified: Wed, 16 Oct 2024 03:24:51 GMT  
		Size: 53.9 MB (53939762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:670d048ac22ccac1fed74cfb5714c7e94b6258c1efc866c41da1395b3a26b83a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92700086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66fe8c0be99d7249a1f123ad94ec058fcd4204c0c34167e176e2edebcbe287a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:28 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:28 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:29 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Fri, 11 Oct 2024 03:48:29 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:13:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Wed, 16 Oct 2024 01:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97babcf495d74dff8479c7173a459ffe71f3e6016a2917626a2902468e3d22ce`  
		Last Modified: Wed, 16 Oct 2024 01:17:42 GMT  
		Size: 15.0 MB (14975939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fe4420f7cc31e2e71a763e82cb5891ae4caf5f1904fbbe4513bb4cd423b516`  
		Last Modified: Wed, 16 Oct 2024 01:17:57 GMT  
		Size: 47.1 MB (47062541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
