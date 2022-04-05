## `notary:signer-0.6.1-2`

```console
$ docker pull notary@sha256:b92a4e7c50ec43d2434ddfbe713be7dad7a103a2833cef4b117d92841f8913ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer-0.6.1-2` - linux; amd64

```console
$ docker pull notary@sha256:44f117f30922793e76f4d48c38ea7e48801ffd70b6718b0bb8504e4c7dd63ce5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7690976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785cf5694e3a633c4fe81218642e11df3f9a891c5bb3fbf493357cc343dd5454`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:29:46 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 10:29:46 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 10:30:05 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 10:30:05 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 10:30:06 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 10:30:06 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 10:30:20 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 10:30:20 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 10:30:20 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 10:30:21 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 10:30:21 GMT
USER notary
# Tue, 05 Apr 2022 10:30:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 10:30:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 10:30:21 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb410511d0d5e78ad31c5f248da2b0f0d7e88a25d2c6b58051dcf8b7fa3722b`  
		Last Modified: Tue, 05 Apr 2022 10:30:42 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74f6af36413f34a740b7a0ba1706a95db01175d2086fe02ecaae4bfa273d99b`  
		Last Modified: Tue, 05 Apr 2022 10:30:43 GMT  
		Size: 4.9 MB (4869606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074f61631574424b1185ce7e2c35720cd690dbb57c46fb7e493403fb51fafda7`  
		Last Modified: Tue, 05 Apr 2022 10:30:42 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0336feabce1e13b60b87793e745349d0e54f3424a15bb00223cf5b0bdb7f62`  
		Last Modified: Tue, 05 Apr 2022 10:30:42 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf7c16c3a9208773e09ddcd08178231872e84a5d6dd14c096a4b8264ebc023b`  
		Last Modified: Tue, 05 Apr 2022 10:30:42 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; arm variant v6

```console
$ docker pull notary@sha256:d1631ce42d7d46f07ac750643100dc17dc17377fb2b0a2e21068bbb716731a9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7182333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0120661b76e9d5a482d47dcffc5546d01455ae2458c46befada9e3f2fcf08a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:41:44 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 06:41:45 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 06:42:25 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 06:42:25 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 06:42:26 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 06:42:26 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 06:42:49 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 06:42:50 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 06:42:50 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 06:42:52 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 06:42:52 GMT
USER notary
# Tue, 05 Apr 2022 06:42:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 06:42:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 06:42:53 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a6edf6e31f19499935c3a76441187fcd92466739f87b8ea2583089574efa13`  
		Last Modified: Tue, 05 Apr 2022 06:43:37 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b3a89b1d6bec2d87129fa631facb69d2cefd43a3bdd7953ee43fd5490c87a5`  
		Last Modified: Tue, 05 Apr 2022 06:43:40 GMT  
		Size: 4.6 MB (4555132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d676f849034fec3a503bafc9bc46ab26e65a6910f1cdc7bbfbff56e607614ab`  
		Last Modified: Tue, 05 Apr 2022 06:43:37 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59df2725d042919c5b6b9846a0750838d7ca1f5fcfa3664a91ed3aa598fbc99`  
		Last Modified: Tue, 05 Apr 2022 06:43:37 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9357ddb4523a1181e8ce7cb7dd6ba669ae79bededc06ef673085779140af3`  
		Last Modified: Tue, 05 Apr 2022 06:43:37 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:5dbf103c67811b30038b3b8dfdbbae4583755f2273a6f11df29f89601b4c3a3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eb0ad8e2cbe3ea5fb8f00624eb2c54b9df96819474aa54fb6570dbfd92626e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:20:06 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:20:07 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:20:37 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 04:20:38 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 04:20:39 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 04:20:40 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 04:20:50 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 04:20:52 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 04:20:53 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 04:20:53 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:20:54 GMT
USER notary
# Tue, 05 Apr 2022 04:20:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 04:20:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:20:57 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6469eb955e2ff78803a49c305daee9f8c7d822f4dad3ef5e7a038762c5481ef6`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d6490184b518304c9183e97b397c747c44b61d6f7fbbff25b4cb9a085a65e6`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 4.5 MB (4455769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b93c98b085b6c25682339ea64ff49350b11739eaa962cf834feebf8af0e113`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abecf4b5d027264415cd1c595cace4c7b11fd6c3ef56d1b5ba8403194af017fa`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d88c446898ad5ead0c9dbb7ffe0f3e84bc4cd0106185a42fb36d14ad28c2be`  
		Last Modified: Tue, 05 Apr 2022 04:21:27 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; 386

```console
$ docker pull notary@sha256:c517416d0b0dbc3c15ffaf46105076e75637a3b09a480093871692adb85e808e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213048bd3ff08817186da1bc64b37e2e3bcfc0ba88265511ea161de9575b070b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:38 GMT
ADD file:caa278dc5cc6257518d542227fef491a89b0b4a7fc4dcb87632c2b786b65752a in / 
# Mon, 04 Apr 2022 23:38:38 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:16:38 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:16:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:17:09 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 04:17:10 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 04:17:11 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 04:17:12 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 04:17:24 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 04:17:26 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 04:17:27 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 04:17:27 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:17:28 GMT
USER notary
# Tue, 05 Apr 2022 04:17:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 04:17:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:17:31 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:54c95c2f58283907ca735a3fe8d3ac4a49a63dc20092eb6fddd7bad2429e3f67`  
		Last Modified: Mon, 04 Apr 2022 23:39:46 GMT  
		Size: 2.8 MB (2820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200ef45146319efcdecd60d517a8c61a2089c481a8449dcce89a92d1f04fc978`  
		Last Modified: Tue, 05 Apr 2022 04:18:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b0bfadc04bb02930de67b428075c382c95951ce913e2ddd7e8462bf02c18b6`  
		Last Modified: Tue, 05 Apr 2022 04:18:02 GMT  
		Size: 4.6 MB (4613397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a7a5dd0a2be99efa7a91689ab5526eea77055eb0de94e8d7a176728d183126`  
		Last Modified: Tue, 05 Apr 2022 04:18:01 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af15ea7412390861f7d24856cf33145bfd8880cc705b75818e4192cdcf807fb1`  
		Last Modified: Tue, 05 Apr 2022 04:18:01 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8fa97a166eed333075e1b99395c5888757006665f8eda4991a90a1637160b1`  
		Last Modified: Tue, 05 Apr 2022 04:18:01 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; ppc64le

```console
$ docker pull notary@sha256:11f853f0ab53e1ed5939953e13fb2fcb91447f7ac1833648512eb816b9d8b0f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e58ed464da460d79e4acb9b1dc906baaefdae68b12785381b59eee94f6b4a90`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:56 GMT
ADD file:a9d5347a58c095f620406d9afc12b5ae4fd6c3994ea7e88e6415db7b09725289 in / 
# Tue, 05 Apr 2022 00:24:00 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:19:13 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 11:19:15 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 11:20:24 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 11:20:26 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 11:20:30 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 11:20:33 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 11:20:56 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 11:20:59 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 11:21:00 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 11:21:07 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 11:21:10 GMT
USER notary
# Tue, 05 Apr 2022 11:21:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 11:21:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 11:21:23 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:afbded953e7f469508815262f0ff60fc06823cc1701e4b7aa211eb10bca545bd`  
		Last Modified: Tue, 05 Apr 2022 00:25:18 GMT  
		Size: 2.8 MB (2814791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ed3d483d5b28cbb5ddbb7617f627ac98cb1be502de16f9f2142bf90be77ba4`  
		Last Modified: Tue, 05 Apr 2022 11:22:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f82a5122c73ebe87551600dedc06ef6346fa50d153d4c317ff178bdee27e6fc`  
		Last Modified: Tue, 05 Apr 2022 11:22:04 GMT  
		Size: 4.3 MB (4337769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab602ec3b6f8d575b40e9883a1d1e0dda91c5ab7a07f1df9b746b9dc3c88584e`  
		Last Modified: Tue, 05 Apr 2022 11:22:03 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec900c07dc4fd312c906966fdd0bf95ed247cdd7fe12c0dd87f66b0c663923ed`  
		Last Modified: Tue, 05 Apr 2022 11:22:03 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0337124674433fd9a3fa73816a42e56ee36b5a7de1de4b8f3c33c3dbafe6202b`  
		Last Modified: Tue, 05 Apr 2022 11:22:04 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; s390x

```console
$ docker pull notary@sha256:84879e97cc7abfa76e42bd92d5d987f618dcf1679091c9b6e2922e53afd0f70d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ab04d2464b2a7b73bde2a36faa51916a3790e99232336d1ee332a76cae7f1e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:55 GMT
ADD file:0f7653032bb9c65a5643cc31ad93fca7bd018ca0466a2d1c4ccadc5db00ad0f0 in / 
# Mon, 04 Apr 2022 23:41:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:09:32 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:09:32 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:09:53 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 05 Apr 2022 04:09:53 GMT
EXPOSE 4444
# Tue, 05 Apr 2022 04:09:54 GMT
EXPOSE 7899
# Tue, 05 Apr 2022 04:09:54 GMT
WORKDIR /notary/signer
# Tue, 05 Apr 2022 04:10:04 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 05 Apr 2022 04:10:05 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 05 Apr 2022 04:10:05 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 05 Apr 2022 04:10:06 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:10:06 GMT
USER notary
# Tue, 05 Apr 2022 04:10:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 05 Apr 2022 04:10:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:10:06 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:22b3eb8fdd3cabd13718400a1a4d1e75330e6e512d556cdd902359adeb0b014a`  
		Last Modified: Mon, 04 Apr 2022 23:42:54 GMT  
		Size: 2.6 MB (2605058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5cfceb0623aa4b77376a2b0943c3f6ad639bb23399311c58f149db56acb6d1`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a23bb6474155371d7265c465752a84b037ab18d0b42c89829b8f7882da58f0`  
		Last Modified: Tue, 05 Apr 2022 04:10:32 GMT  
		Size: 4.7 MB (4706646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d732b0ce88d1b86635ede17c577fd772ea20c726d4fce09af29d5c1946abeea`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd809709510a90d3548f93ff9a1cdc757565859ef825247e106c24c0755277aa`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a18a490d4f9aec625e87d72f9df174b123b33a2197cae2d329bc4835baed09`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
