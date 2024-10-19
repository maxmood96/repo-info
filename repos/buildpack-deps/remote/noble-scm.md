## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:2cf19cb7d6c1692fb84e950592909719b1e5229f2fc550bdb015b987c95d4dfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

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
$ docker pull buildpack-deps@sha256:99381b633665998b79690396699aeecda8a6021ba7f48ef5dc0b11d61d8f0977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87636078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de004308e59e863c2497e47864e8d59c4739b921649cdbf16ebb5dcc4d490bb4`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4950c6def722ac96f41618bdff1f82e38c2b3d5849ce2c07b4049db764444b`  
		Last Modified: Sat, 19 Oct 2024 05:23:22 GMT  
		Size: 13.5 MB (13452782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3b9ee069311be4d8fca64a1f65e93cf73601746ef5283dfcbda615585143a`  
		Last Modified: Sat, 19 Oct 2024 06:27:05 GMT  
		Size: 45.3 MB (45297451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c537019769318d6441a1a0ccde858638029672a31a138cdea08c817a02d85a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0417cb63caa30943de8542749d15b831605f70f171fb340489aa486804153b0d`

```dockerfile
```

-	Layers:
	-	`sha256:6564a5d55c888b25e3b018c49e151e8df03e9f22c64b33c89509fc90c86a0d6f`  
		Last Modified: Sat, 19 Oct 2024 06:27:04 GMT  
		Size: 5.1 MB (5083278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74f6858d965dcd2c8366c220ab6a8e4c2213babf582ac0bdc402982d06317bc`  
		Last Modified: Sat, 19 Oct 2024 06:27:03 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5fa4b463c6bad8c325cf2a680beae1b5bdedf56de3341022116b1cacbe932088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100881127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de165e6533312f2db04bbb6972e5c0c6e9bf6b9572b6e1356fe2934adc94bcb`
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
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bb7422168207a94659a7d755a71642577184a266af0a8a3afb47316450f6c`  
		Last Modified: Sat, 19 Oct 2024 04:14:07 GMT  
		Size: 16.0 MB (15990504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48479dfc2b7d427cb9b67d6c2ae25148b5cdad254e89920f302994550cebd409`  
		Last Modified: Sat, 19 Oct 2024 05:30:15 GMT  
		Size: 50.5 MB (50501654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:489d19de386867de888327079b1653eb5c2145f06deb5463336a053265851639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ec07f3c69822c7b50ff6231d02fa11ef9873228a0ee554cda3b170d2c5f41a`

```dockerfile
```

-	Layers:
	-	`sha256:a42262aa516f6d496beeb73cfcd4241bca3fdef81c466f632fab58c0d5a6784e`  
		Last Modified: Sat, 19 Oct 2024 05:30:13 GMT  
		Size: 5.1 MB (5083769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e14fa4672f84ec2b48325ebcbe2b010f0936ce050f44bc4ba250e171457eb`  
		Last Modified: Sat, 19 Oct 2024 05:30:13 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cfe4a44771a4894331c387dfbfd41699d4082635a6d03edf2941e0a316b4d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99073365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edee905bdc81d5092eafd62cb7be9c063fa42d60d447d2cc14041cbdf81c0e6`
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
ADD file:008d2e9e73153005eafa485b2ecca3ca9fd6996da5b5c99a52a7376427350f8d in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53300d777b1a34c849b57f3a3ccdc52f3ad795ea045079e7bcca5f63efab0327`  
		Last Modified: Fri, 11 Oct 2024 05:07:42 GMT  
		Size: 31.0 MB (30951587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a51cb0bf7686a8c2782160996192e9d89c09949101fc6d8c09083eb1013e91`  
		Last Modified: Sat, 19 Oct 2024 04:08:40 GMT  
		Size: 14.3 MB (14320414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0a2eaf274204c5bf93c79db9bc33e24b045b07aacb49995d18798544f6f56f`  
		Last Modified: Sat, 19 Oct 2024 05:41:12 GMT  
		Size: 53.8 MB (53801364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1c88e5543520ba78e7e211adf00aab3892c369fcf8456da61a453ed97ba8b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dba033ffdf0708f27422d708abdda6f4c7605566d9f1d37e2125e8c12426e23`

```dockerfile
```

-	Layers:
	-	`sha256:5e58895d95772019ad0fdcbe6b4be69f49a47be40659f1043c291ca842db57e0`  
		Last Modified: Sat, 19 Oct 2024 05:41:05 GMT  
		Size: 5.1 MB (5066623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7fac63c0870d1c2791b08f5b05f46d2480ad4a0bc9c88d45b5d99d94de2d5f`  
		Last Modified: Sat, 19 Oct 2024 05:41:04 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1ed21863e54c46bb6a3e2a234ea3fa2be1aefa81129997fb2ce3ddf556d4b2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91917558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845a06f98ce3734e6f2f38f914787f29ed85439d1730e933b3a44bdb334c6638`
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
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3d2abe11fb3bab133e95a31c3eeb04ba27eaed096cd5d4d3baeb8f12c3473633`  
		Last Modified: Fri, 11 Oct 2024 05:07:47 GMT  
		Size: 30.0 MB (30019614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1e22806c936cf352e8613a36cc00e41a5fc02ec3a1756fa36d836ba0f8dd58`  
		Last Modified: Sat, 19 Oct 2024 03:51:58 GMT  
		Size: 15.0 MB (14974773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3949ce1635c27257c28d76c25291d89d75979fb73e8177e9220f5e051d01fddf`  
		Last Modified: Sat, 19 Oct 2024 05:13:20 GMT  
		Size: 46.9 MB (46923171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64971ad19818eaa5aec413e6610f11a061fbca500b06d502ed9ae51be25b0b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcadac4f51c1e199a96b69a99209a7b38d7d773d63d289914616fda48513d23`

```dockerfile
```

-	Layers:
	-	`sha256:618826a9976b9b06ed1c6f291f504f0edb80abfff6d55911eb84ed2e273db8d6`  
		Last Modified: Sat, 19 Oct 2024 05:13:19 GMT  
		Size: 5.1 MB (5078416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08e90487ee45bafeb6e1dce6760b32074eb2786e00670505a3efa62c24f56e3`  
		Last Modified: Sat, 19 Oct 2024 05:13:19 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
