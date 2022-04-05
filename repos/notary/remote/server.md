## `notary:server`

```console
$ docker pull notary@sha256:230da2dd813166262d862bd6d0f2fa26265f3b3e3512618ee3037cae17e6efbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server` - linux; amd64

```console
$ docker pull notary@sha256:6b31bfa488d68eeec5b00dbb10d2e9478c39d68c6185bca1bb35f787c667b7c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8208595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3d36b2afa65b96aff75628e9f60aea0136135045717043b35aad1920ec7514`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:29:46 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 10:29:46 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 10:29:46 GMT
ENV INSTALLDIR=/notary/server
# Tue, 05 Apr 2022 10:29:46 GMT
EXPOSE 4443
# Tue, 05 Apr 2022 10:29:46 GMT
WORKDIR /notary/server
# Tue, 05 Apr 2022 10:30:01 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Tue, 05 Apr 2022 10:30:01 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 05 Apr 2022 10:30:01 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 05 Apr 2022 10:30:02 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 10:30:02 GMT
USER notary
# Tue, 05 Apr 2022 10:30:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 05 Apr 2022 10:30:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 10:30:02 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce7872a467c81c2cebbf77c57a630500a0ccbbef8dcd892ffdca4bb0ee792c0`  
		Last Modified: Tue, 05 Apr 2022 10:30:32 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fdbc4096710704d136b0fa30e267f2474e0ffe99773c87955b8bab4780743d`  
		Last Modified: Tue, 05 Apr 2022 10:30:33 GMT  
		Size: 5.4 MB (5387173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9c1737b7b8f8d5419d60f8ecdbb82f2b9b079cf1a2dac3f492dc27661293ab`  
		Last Modified: Tue, 05 Apr 2022 10:30:32 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd630de30c259a81493f2d644cb43f0b9cf72aa612fcc6b9e6dafcda261970`  
		Last Modified: Tue, 05 Apr 2022 10:30:32 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30072905120a5c734bca8c05907d004ac9c6a6ac82c205a66b29ce5057b2d849`  
		Last Modified: Tue, 05 Apr 2022 10:30:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:9d01ff58d9a93a6e3f3312b36707b6bbe5a25eaeac244c93119a8c462ebd41d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c378e605ec35afbb940128565e45ae828a74212bb38e3a027930d1c7e2b6b10`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:41:44 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 06:41:45 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 06:41:45 GMT
ENV INSTALLDIR=/notary/server
# Tue, 05 Apr 2022 06:41:46 GMT
EXPOSE 4443
# Tue, 05 Apr 2022 06:41:46 GMT
WORKDIR /notary/server
# Tue, 05 Apr 2022 06:42:09 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Tue, 05 Apr 2022 06:42:10 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 05 Apr 2022 06:42:11 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 05 Apr 2022 06:42:12 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 06:42:12 GMT
USER notary
# Tue, 05 Apr 2022 06:42:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 05 Apr 2022 06:42:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 06:42:14 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4479acb877d9ed71ac9cb807fc9765aa7b938f534fa63edd59a1a706deebe9f1`  
		Last Modified: Tue, 05 Apr 2022 06:43:23 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a61a1045f987826fb23d5c5bdc815f5f63b7c330657db350bf5b8da7dac78d`  
		Last Modified: Tue, 05 Apr 2022 06:43:26 GMT  
		Size: 5.0 MB (5039524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f85ea69762fd87547f3df804b22c9183e21aea68bd15c767ff2d5b12213af6`  
		Last Modified: Tue, 05 Apr 2022 06:43:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55600985e48c157a1b6dd5a28ea08643d6d488ceda2a0604613233bb594c1f1`  
		Last Modified: Tue, 05 Apr 2022 06:43:23 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5917846216dc5f7f45ca5d3892fc06482aecd40257c0c26519de264edc92c99d`  
		Last Modified: Tue, 05 Apr 2022 06:43:23 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:ea7e41eae9f2943165c0fcddb602b2b3cc05f19d90d1db3477f2c42c9add49e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7657170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fc22f2d30bf1c82a8b4b3aeb6756bf01d185b8b429718997e1b714c3a26b3a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:20:06 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:20:07 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:20:08 GMT
ENV INSTALLDIR=/notary/server
# Tue, 05 Apr 2022 04:20:09 GMT
EXPOSE 4443
# Tue, 05 Apr 2022 04:20:10 GMT
WORKDIR /notary/server
# Tue, 05 Apr 2022 04:20:21 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Tue, 05 Apr 2022 04:20:23 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 05 Apr 2022 04:20:24 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 05 Apr 2022 04:20:24 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:20:25 GMT
USER notary
# Tue, 05 Apr 2022 04:20:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 05 Apr 2022 04:20:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:20:28 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d749029e21583966f36211e83a21b915cef23d5fa9b0810c29eb4aa31cb3e7f6`  
		Last Modified: Tue, 05 Apr 2022 04:21:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b65b06888f0dd71a48b397bb482c2c2f3f0883922f88544f8eeb2203a01446`  
		Last Modified: Tue, 05 Apr 2022 04:21:15 GMT  
		Size: 4.9 MB (4934191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a1e98a8934a0ea7083ba0570b377c4a4c9e57df2f5a1440cf4eabcf5543b81`  
		Last Modified: Tue, 05 Apr 2022 04:21:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb7990edf9aaebbbfc47dce6acdc71dad40788d03336cacf2ea2b55a3f3e5c4`  
		Last Modified: Tue, 05 Apr 2022 04:21:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932ddfe8f35fe31d6c2a3246c554ea5593527575b8c3aeccb294ec2b81e7e0`  
		Last Modified: Tue, 05 Apr 2022 04:21:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:df5dabef4d5b397e477ba589ddb913cd89a799b4ddf93e4f31cece82b8fc891b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632c94bdaa2fa7e89dfa0f50effa636a65c0e52eb4374c84d9fc7bda41bdcd6d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:38 GMT
ADD file:caa278dc5cc6257518d542227fef491a89b0b4a7fc4dcb87632c2b786b65752a in / 
# Mon, 04 Apr 2022 23:38:38 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:16:38 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:16:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:16:40 GMT
ENV INSTALLDIR=/notary/server
# Tue, 05 Apr 2022 04:16:41 GMT
EXPOSE 4443
# Tue, 05 Apr 2022 04:16:42 GMT
WORKDIR /notary/server
# Tue, 05 Apr 2022 04:16:55 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Tue, 05 Apr 2022 04:16:57 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 05 Apr 2022 04:16:58 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 05 Apr 2022 04:16:58 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:16:59 GMT
USER notary
# Tue, 05 Apr 2022 04:17:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 05 Apr 2022 04:17:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:17:02 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:54c95c2f58283907ca735a3fe8d3ac4a49a63dc20092eb6fddd7bad2429e3f67`  
		Last Modified: Mon, 04 Apr 2022 23:39:46 GMT  
		Size: 2.8 MB (2820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccbfcedc33f7b7a795aac692e856ae7872b305d9d0b216364dff0d349a05b48`  
		Last Modified: Tue, 05 Apr 2022 04:17:50 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e670cc5ddc0a16c08a50bc8f9c958bdecc849d624c59e6f9bf00c11ff15d2c`  
		Last Modified: Tue, 05 Apr 2022 04:17:51 GMT  
		Size: 5.1 MB (5099262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd4fa628a46e3813583739e749f3aa16b61ca4a37ff07619502ea844f5560cb`  
		Last Modified: Tue, 05 Apr 2022 04:17:50 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5132d12084b7c781681561b2e0bb070fd59070c101ef088c668c3b5fd3ed41f`  
		Last Modified: Tue, 05 Apr 2022 04:17:50 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9d70b69c5085475c62fa256caf43badf9dc83817f20f9f8bfb06628348bbf6`  
		Last Modified: Tue, 05 Apr 2022 04:17:50 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:d246f52706baa526e2471411daceaac18c1cdfad58a0a9a88f281afddb20ff27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7618819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc442e8f20de6045d499b07abb4a3e3731be1f28d0a9f24ce587dd000549f631`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:56 GMT
ADD file:a9d5347a58c095f620406d9afc12b5ae4fd6c3994ea7e88e6415db7b09725289 in / 
# Tue, 05 Apr 2022 00:24:00 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:19:13 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 11:19:15 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 11:19:18 GMT
ENV INSTALLDIR=/notary/server
# Tue, 05 Apr 2022 11:19:21 GMT
EXPOSE 4443
# Tue, 05 Apr 2022 11:19:23 GMT
WORKDIR /notary/server
# Tue, 05 Apr 2022 11:19:52 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Tue, 05 Apr 2022 11:19:53 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 05 Apr 2022 11:19:55 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 05 Apr 2022 11:20:04 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 11:20:07 GMT
USER notary
# Tue, 05 Apr 2022 11:20:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 05 Apr 2022 11:20:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 11:20:13 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:afbded953e7f469508815262f0ff60fc06823cc1701e4b7aa211eb10bca545bd`  
		Last Modified: Tue, 05 Apr 2022 00:25:18 GMT  
		Size: 2.8 MB (2814791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9d4b101d59127772fe29076100ab8c2da0bfe8471a86c6ca52943d1d64ece6`  
		Last Modified: Tue, 05 Apr 2022 11:21:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb281cb6061176b1cb2452285c2ec0a492d680d8cc3dcb7e939a6c349ef585fb`  
		Last Modified: Tue, 05 Apr 2022 11:21:49 GMT  
		Size: 4.8 MB (4801899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39350c84f3706e68b11642143abbae09e84547430b8e0c64ba8de9a90369800e`  
		Last Modified: Tue, 05 Apr 2022 11:21:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569b8c01cf16565735cd83f76e05f4f45d6c3207541907ea27dc8b59bc0e6f15`  
		Last Modified: Tue, 05 Apr 2022 11:21:48 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c023b243258d7c44f7b8311d3835f477e093714c35afdb24deb0adf35c83ffd`  
		Last Modified: Tue, 05 Apr 2022 11:21:48 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:c4325701906e5481d84e6fe8c12beb33826cd7654d602b833e8f2ea03cb5f996
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7813144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d302c9267695d87d102e35f56d96fdea7b7d5c54731c6f168276fc20afd126c3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:55 GMT
ADD file:0f7653032bb9c65a5643cc31ad93fca7bd018ca0466a2d1c4ccadc5db00ad0f0 in / 
# Mon, 04 Apr 2022 23:41:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:09:32 GMT
ENV TAG=v0.6.1
# Tue, 05 Apr 2022 04:09:32 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 05 Apr 2022 04:09:33 GMT
ENV INSTALLDIR=/notary/server
# Tue, 05 Apr 2022 04:09:33 GMT
EXPOSE 4443
# Tue, 05 Apr 2022 04:09:33 GMT
WORKDIR /notary/server
# Tue, 05 Apr 2022 04:09:45 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Tue, 05 Apr 2022 04:09:45 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 05 Apr 2022 04:09:45 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 05 Apr 2022 04:09:46 GMT
RUN adduser -D -H -g "" notary
# Tue, 05 Apr 2022 04:09:46 GMT
USER notary
# Tue, 05 Apr 2022 04:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 05 Apr 2022 04:09:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 05 Apr 2022 04:09:47 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:22b3eb8fdd3cabd13718400a1a4d1e75330e6e512d556cdd902359adeb0b014a`  
		Last Modified: Mon, 04 Apr 2022 23:42:54 GMT  
		Size: 2.6 MB (2605058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818aa24101a696a79626ade78060355eab638f240ddaacf2a329a4777dde59c2`  
		Last Modified: Tue, 05 Apr 2022 04:10:24 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c2a583ec7d4a26a30b982202be1ffd1abca8f4f0a100abac4820e68d45e94e`  
		Last Modified: Tue, 05 Apr 2022 04:10:25 GMT  
		Size: 5.2 MB (5205961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ff52d29bc1b9d095c15d4ff8328f258458a9711905ea88f5b8526a35099873`  
		Last Modified: Tue, 05 Apr 2022 04:10:24 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee722db8f5a5dca2d8689915528646d995be73e4c3bd7bf78a2825adb800dc33`  
		Last Modified: Tue, 05 Apr 2022 04:10:24 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c3b90ca6a4fa7bf437a1a1034c711400af8c4be705e6339b24ef747a6bdde9`  
		Last Modified: Tue, 05 Apr 2022 04:10:24 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
