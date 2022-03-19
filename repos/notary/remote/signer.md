## `notary:signer`

```console
$ docker pull notary@sha256:cb2c07a1278d44d5bc2dd2d67a4068879a07b426886de78611da64c5473a4984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:7cd15517d615b5af1cda1296f28a31a50d463d2ec4e66d47807ea963a5a9ae0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7688823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6cc8c94cf061e07d741926ded6f6345780868f1d598e31e86ca4f1e5182a0c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:36 GMT
ADD file:51c08645923aa2d3513f66571f0c598a727dd5805e4f2bb87fb660b2f789348d in / 
# Thu, 17 Mar 2022 15:19:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:03:57 GMT
ENV TAG=v0.6.1
# Thu, 17 Mar 2022 18:03:57 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Thu, 17 Mar 2022 18:04:20 GMT
ENV INSTALLDIR=/notary/signer
# Thu, 17 Mar 2022 18:04:20 GMT
EXPOSE 4444
# Thu, 17 Mar 2022 18:04:20 GMT
EXPOSE 7899
# Thu, 17 Mar 2022 18:04:20 GMT
WORKDIR /notary/signer
# Thu, 17 Mar 2022 18:04:46 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Thu, 17 Mar 2022 18:04:46 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Thu, 17 Mar 2022 18:04:47 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Thu, 17 Mar 2022 18:04:48 GMT
RUN adduser -D -H -g "" notary
# Thu, 17 Mar 2022 18:04:48 GMT
USER notary
# Thu, 17 Mar 2022 18:04:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Thu, 17 Mar 2022 18:04:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 17 Mar 2022 18:04:48 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:e1096b72685a2366348e697f5b57e3b8feb41660e3dbe68447e168381515111a`  
		Last Modified: Thu, 17 Mar 2022 15:20:24 GMT  
		Size: 2.8 MB (2817181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9f5ddc70ebf753823067c484e479e7525c999e2864663475e73ef49c4b7fbb`  
		Last Modified: Thu, 17 Mar 2022 18:05:21 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1631c06e13bed06385f804bdaed5bb983016e85648f3e580a79a34961697a6`  
		Last Modified: Thu, 17 Mar 2022 18:05:22 GMT  
		Size: 4.9 MB (4869589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5aaab4e07d0b7bc2e43648cc06fb718e82ef12812eecc98cf986fe7f33f3b`  
		Last Modified: Thu, 17 Mar 2022 18:05:21 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55c99bb7ce6b42af8b1a6729f77f6a758f6a9bf6a3e0cca9d5aa6f5ebc38b18`  
		Last Modified: Thu, 17 Mar 2022 18:05:21 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bc1d1d60e2d7a3d67e21f60aabf81d07d762d0f3ff0bd446f36a9ee1c81ad`  
		Last Modified: Thu, 17 Mar 2022 18:05:21 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:f02b6731b76ee5f30e5863716264c5040ed35f6cae02a3d3689305d9bc7d7598
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2d35e37ca0a874a961232379a5f754678d48cdd957b46c2f7742b3031e3b73`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:48:36 GMT
ENV TAG=v0.6.1
# Thu, 17 Mar 2022 15:48:37 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Thu, 17 Mar 2022 15:49:20 GMT
ENV INSTALLDIR=/notary/signer
# Thu, 17 Mar 2022 15:49:20 GMT
EXPOSE 4444
# Thu, 17 Mar 2022 15:49:21 GMT
EXPOSE 7899
# Thu, 17 Mar 2022 15:49:21 GMT
WORKDIR /notary/signer
# Thu, 17 Mar 2022 15:49:45 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Thu, 17 Mar 2022 15:49:45 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Thu, 17 Mar 2022 15:49:46 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Thu, 17 Mar 2022 15:49:47 GMT
RUN adduser -D -H -g "" notary
# Thu, 17 Mar 2022 15:49:48 GMT
USER notary
# Thu, 17 Mar 2022 15:49:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Thu, 17 Mar 2022 15:49:49 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 17 Mar 2022 15:49:49 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0219162766422e3078573c2bedb3e58a6c382a030a341c0bb5cc7c809483e5`  
		Last Modified: Thu, 17 Mar 2022 15:50:37 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0baa806a6307efe203e4cc07104f988519047d5e54e588eabd17413a65ac63`  
		Last Modified: Thu, 17 Mar 2022 15:50:41 GMT  
		Size: 4.6 MB (4555144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2df18c0e7de69a12d8ed338050d124adb610886e7f132f89b534dc9f4ff08a7`  
		Last Modified: Thu, 17 Mar 2022 15:50:37 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9666ead86a141412e43831ebd717f9899d1d3d36f5d97cc878be13cb584916e`  
		Last Modified: Thu, 17 Mar 2022 15:50:37 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f77d2a1cb189e2a82c3566cee8a48f598a6ba6209f5c562ae8c63de3c721e`  
		Last Modified: Thu, 17 Mar 2022 15:50:37 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:7a186215872f1c3801ca640e32df5bef70f3d4dda626b07f8d1c4578ec127daa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3cefe647af844bbe0906f558647bb943d54c43ffa98ab5367b4bfb557d8c69`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:19 GMT
ADD file:0bbbf3ca52651bbef2547689474beafcef779899da63743efd8166a01d9f3f7a in / 
# Thu, 17 Mar 2022 18:43:20 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 01:06:40 GMT
ENV TAG=v0.6.1
# Sat, 19 Mar 2022 01:06:41 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Sat, 19 Mar 2022 01:07:07 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 19 Mar 2022 01:07:08 GMT
EXPOSE 4444
# Sat, 19 Mar 2022 01:07:09 GMT
EXPOSE 7899
# Sat, 19 Mar 2022 01:07:10 GMT
WORKDIR /notary/signer
# Sat, 19 Mar 2022 01:07:20 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Sat, 19 Mar 2022 01:07:22 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Sat, 19 Mar 2022 01:07:23 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Sat, 19 Mar 2022 01:07:23 GMT
RUN adduser -D -H -g "" notary
# Sat, 19 Mar 2022 01:07:24 GMT
USER notary
# Sat, 19 Mar 2022 01:07:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 19 Mar 2022 01:07:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 19 Mar 2022 01:07:27 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:6b5c040bf1f18956758f68628afdc8e179044ac75bcd411134da39a661a772e0`  
		Last Modified: Thu, 17 Mar 2022 18:44:11 GMT  
		Size: 2.7 MB (2719134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d31637a795a9f059af1f95be8849f6be791dde68237d7c86c01454dd572b52a`  
		Last Modified: Sat, 19 Mar 2022 01:07:58 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6255a8d20621a4455617d12053f107406d4975d78567f8c39b3da448abfb2bb8`  
		Last Modified: Sat, 19 Mar 2022 01:07:58 GMT  
		Size: 4.5 MB (4455766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0160fc393462056b86027a87648ed7fea282ec77af91cef287afb242f901e311`  
		Last Modified: Sat, 19 Mar 2022 01:07:58 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279ee1fa1db3cede4134d5e6f895becf8d3a8fc735510014fc1a38333270ac29`  
		Last Modified: Sat, 19 Mar 2022 01:07:58 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030e2bf09c2d22c09c9c233270e2b5ddd5c4ef8df32d41a0c7ec854801f21ec1`  
		Last Modified: Sat, 19 Mar 2022 01:07:58 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:4a58e6eea69fc848388dca7dde14d188a2a18b0d2620cdfd6282272df75833ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8340a2ee214549fc9e94e989998d45bae9c8482b9cf0b432915d05b67a6182`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Thu, 17 Mar 2022 16:34:42 GMT
ADD file:fbbd764c2b3ce734329c4dc8415d55b9cefc972125c5818e78698f7b894667da in / 
# Thu, 17 Mar 2022 16:34:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 17:41:31 GMT
ENV TAG=v0.6.1
# Thu, 17 Mar 2022 17:41:31 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Thu, 17 Mar 2022 17:41:56 GMT
ENV INSTALLDIR=/notary/signer
# Thu, 17 Mar 2022 17:41:56 GMT
EXPOSE 4444
# Thu, 17 Mar 2022 17:41:56 GMT
EXPOSE 7899
# Thu, 17 Mar 2022 17:41:56 GMT
WORKDIR /notary/signer
# Thu, 17 Mar 2022 17:42:12 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Thu, 17 Mar 2022 17:42:12 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Thu, 17 Mar 2022 17:42:12 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Thu, 17 Mar 2022 17:42:13 GMT
RUN adduser -D -H -g "" notary
# Thu, 17 Mar 2022 17:42:13 GMT
USER notary
# Thu, 17 Mar 2022 17:42:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Thu, 17 Mar 2022 17:42:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 17 Mar 2022 17:42:13 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:4fcf0d6f8c0dc4a27651b1a8218d9febdd0bc510d8a2eb8474b17c87b284c5bd`  
		Last Modified: Thu, 17 Mar 2022 16:35:37 GMT  
		Size: 2.8 MB (2823620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1800e6030f10698439ecde415e5169e45ca3eb886931118fc651de44d7637c`  
		Last Modified: Thu, 17 Mar 2022 17:42:42 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c68a8fa51239b848bd66fbbfda090af0b66341751596346f45352975adac82`  
		Last Modified: Thu, 17 Mar 2022 17:42:44 GMT  
		Size: 4.6 MB (4613629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58dc787e48344b2073d46b54410c0d2a97e0fe9f7d6d7d114159cb63e49ad28`  
		Last Modified: Thu, 17 Mar 2022 17:42:43 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e64a61270a9c3d9a5633f5e17128ba6ad7714efad23c49584c00b7078119f88`  
		Last Modified: Thu, 17 Mar 2022 17:42:52 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8330c46595a8570d280a38cfa426e8a0d232b9944ef7ef7974aadc03fd79931d`  
		Last Modified: Thu, 17 Mar 2022 17:42:42 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:de4c14d3a29714f73f754f969dbbf2beb4ce95db388215fafc90f5d1a30f04ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7157781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3102e51fbf419258c142913b3edb4a3588a019f7f90afac6aeae54c7474e682b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Thu, 17 Mar 2022 18:19:00 GMT
ADD file:06587cebee2131b88da0944eb4be5128053d97f4d51a175881625be110548874 in / 
# Thu, 17 Mar 2022 18:19:03 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 08:43:59 GMT
ENV TAG=v0.6.1
# Fri, 18 Mar 2022 08:44:04 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 18 Mar 2022 08:45:40 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 18 Mar 2022 08:45:43 GMT
EXPOSE 4444
# Fri, 18 Mar 2022 08:45:46 GMT
EXPOSE 7899
# Fri, 18 Mar 2022 08:45:48 GMT
WORKDIR /notary/signer
# Fri, 18 Mar 2022 08:46:10 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Fri, 18 Mar 2022 08:46:13 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 18 Mar 2022 08:46:14 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 18 Mar 2022 08:46:22 GMT
RUN adduser -D -H -g "" notary
# Fri, 18 Mar 2022 08:46:26 GMT
USER notary
# Fri, 18 Mar 2022 08:46:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 18 Mar 2022 08:46:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 18 Mar 2022 08:46:40 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:9ba546239a73b7ff261e6813d8f1cf9e477de8825b6ae341227f315ea3a4cd51`  
		Last Modified: Thu, 17 Mar 2022 18:20:15 GMT  
		Size: 2.8 MB (2817924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6519366b6c543b5c27978b58b1bdbf51a51a1038c4ab4d1aa7002483f4826bbf`  
		Last Modified: Fri, 18 Mar 2022 08:47:15 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a2e73001e44fa11162adab15d4d0b363529ce8439a50dd3ac5762fd8777c90`  
		Last Modified: Fri, 18 Mar 2022 08:47:17 GMT  
		Size: 4.3 MB (4337794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f80ea1b5096245f8380e1415126eab080b4f8d40a0f3e4127ff928d60e49303`  
		Last Modified: Fri, 18 Mar 2022 08:47:15 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e471f9c1dd512097136b165c33d6f00f0a5972d50ff6ece2d34c364aa4546ded`  
		Last Modified: Fri, 18 Mar 2022 08:47:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0282f22781a1e838a98578170128714b6a92e4323547f3026c5c13524c4b81b8`  
		Last Modified: Fri, 18 Mar 2022 08:47:15 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:8e1a224c239605e0b3ff0e45299f029fa955adbea193bd0f18e2416ac23bdd20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7314919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12aa8a2e10c86edbd24bd1d6caf4956f278e2e2dbaad55593c0a56cc7b87414`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Thu, 17 Mar 2022 14:36:02 GMT
ADD file:cc3c2ea972c5b5d1135d0a82f5d1a6cc97fcc81f3006bb6c6b8580f1e9f4c238 in / 
# Thu, 17 Mar 2022 14:36:02 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 16:48:38 GMT
ENV TAG=v0.6.1
# Thu, 17 Mar 2022 16:48:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Thu, 17 Mar 2022 16:48:59 GMT
ENV INSTALLDIR=/notary/signer
# Thu, 17 Mar 2022 16:48:59 GMT
EXPOSE 4444
# Thu, 17 Mar 2022 16:48:59 GMT
EXPOSE 7899
# Thu, 17 Mar 2022 16:48:59 GMT
WORKDIR /notary/signer
# Thu, 17 Mar 2022 16:49:10 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Thu, 17 Mar 2022 16:49:10 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Thu, 17 Mar 2022 16:49:10 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Thu, 17 Mar 2022 16:49:11 GMT
RUN adduser -D -H -g "" notary
# Thu, 17 Mar 2022 16:49:11 GMT
USER notary
# Thu, 17 Mar 2022 16:49:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Thu, 17 Mar 2022 16:49:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 17 Mar 2022 16:49:11 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:3bb5875ccb136d6c7691dcf2927e52a66c831ce80fd5140d92e0a158400a4cfe`  
		Last Modified: Thu, 17 Mar 2022 14:36:53 GMT  
		Size: 2.6 MB (2606212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c965ece0ded347f0522934cfa75df1d2e16714a9443dcc7f5d38b0b7af8041b`  
		Last Modified: Thu, 17 Mar 2022 16:49:37 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dff2e6efbb33014d9f833e935ad719dff7dc9e6c074fac6b629b815030c2056`  
		Last Modified: Thu, 17 Mar 2022 16:49:38 GMT  
		Size: 4.7 MB (4706649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefeffb3ff1831061255068b4e6cba2f0d39ae66375ed18a45d5d52f44e70e4b`  
		Last Modified: Thu, 17 Mar 2022 16:49:37 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55341d4f63ac695e765283a65696d4267e5f55c448e28d93414c41d61d89883`  
		Last Modified: Thu, 17 Mar 2022 16:49:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39329f747ee8ad6602f00a8158f4ab462f51553147a651aedb5f1e763f6279b0`  
		Last Modified: Thu, 17 Mar 2022 16:49:37 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
