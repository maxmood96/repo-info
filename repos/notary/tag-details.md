<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.6.1-2`](#notaryserver-061-2)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.6.1-2`](#notarysigner-061-2)

## `notary:server`

```console
$ docker pull notary@sha256:141534ec456d58f96094fd956682b7425bd50e90d3428011f4a069bec0710e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server` - linux; amd64

```console
$ docker pull notary@sha256:43f4409374b91208328c212fdf9363ac1e6dc22412eb7217aac751bc5c489dd2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8592976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162689747d5ac7859de78f9aae1f4ffd15e68bac113e35a855e350a05886234f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:58:36 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:58:36 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:58:36 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 18:58:36 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 18:58:36 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 18:58:52 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 18:58:52 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 18:58:52 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 18:58:53 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:58:54 GMT
USER notary
# Mon, 28 Jun 2021 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 18:58:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:58:54 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77556963ef8a796bf41535d79d06ba6d80883bdaa9cd149853fa0cb7bf99da0`  
		Last Modified: Mon, 28 Jun 2021 18:59:27 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae7947d7e939530ca197852782ce0cf6546b2508f5b7f70a2ae9940803d415c`  
		Last Modified: Mon, 28 Jun 2021 18:59:28 GMT  
		Size: 5.8 MB (5778894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774741ed1bdb890d7e5e37e13c0a5eaada0dd7dde5d7d6c3dcfa47892f8fef4c`  
		Last Modified: Mon, 28 Jun 2021 18:59:27 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ff51d63b11312605581f793afe414169a074b16e9615348f61425edbfded20`  
		Last Modified: Mon, 28 Jun 2021 18:59:27 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abf3b1ab2eca193532a47a956e16b9412aa4a2724dee7c54260fd27d2acbbc3`  
		Last Modified: Mon, 28 Jun 2021 18:59:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:19ce5792b7c9769089fb8b0fd736bf1f084eaf7fa958ce6fd0a9a479c6c9a6bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402814d5a76677d5defb45a7423e84467ca374c481609a52c7b553df3f549414`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 19:03:50 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 19:03:50 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 19:03:51 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 19:03:51 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 19:03:52 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 19:04:18 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 19:04:19 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 19:04:20 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 19:04:21 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 19:04:22 GMT
USER notary
# Mon, 28 Jun 2021 19:04:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 19:04:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 19:04:23 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb0fe1c5eb5b55a63c1f43d072d6473002d6bafddbd5129189736c88b1c4df3`  
		Last Modified: Mon, 28 Jun 2021 19:05:35 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89157730c492f9ff6dc09b4b6d68970b3c38f97382aa413616780b99f16d0150`  
		Last Modified: Mon, 28 Jun 2021 19:05:38 GMT  
		Size: 5.4 MB (5432637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbdc6a98cd1821e80988139e066b22d819cb2428e3a6b7e23fd0687e36c721a`  
		Last Modified: Mon, 28 Jun 2021 19:05:35 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d98817260921113ab52f99676b5469c9eba20989f2ebe16de7244fb7399507`  
		Last Modified: Mon, 28 Jun 2021 19:05:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098fc3ce99653b67ce80a6974bd3b7e19cafe04b93b91bc6b2b794d10793f2ab`  
		Last Modified: Mon, 28 Jun 2021 19:05:35 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:84d37fa149b66ca8f676d231ea0a45a9fa9ee9b0b64c6f1ccd33882fcfe5634d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8049433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaff639380cc586b31a1e46dac0e3b2514e134ffbd03b651630a39a16d3afbba`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:41:01 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:41:02 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:41:02 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 18:41:02 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 18:41:02 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 18:41:15 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 18:41:15 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 18:41:16 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 18:41:17 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:41:17 GMT
USER notary
# Mon, 28 Jun 2021 18:41:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 18:41:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:41:17 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0adeb9de9824c29710e237b61cbcbe6fd3a06ee6d782b196281b43d9f6df8d`  
		Last Modified: Mon, 28 Jun 2021 18:41:58 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872551adbbf0fa99b194c79bf451d61f6737218d54a37eda8452f261299d5efa`  
		Last Modified: Mon, 28 Jun 2021 18:41:59 GMT  
		Size: 5.3 MB (5335286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833deb1d1fddec8beb3c60afa38b604c831f69fadded305c0e3c1f3013d69204`  
		Last Modified: Mon, 28 Jun 2021 18:41:57 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdb1fdfa241c1d8481fd04253374894f79918d98f96d7b5c5d544a89489ec05`  
		Last Modified: Mon, 28 Jun 2021 18:41:57 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e165a9f59ac6310e9902f349c334a4bb56c0744e158a9bf9dcb78063263db3`  
		Last Modified: Mon, 28 Jun 2021 18:41:58 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:e81817925f77d235fa795ae6392ccf0b31c27a053bd8535984123ed70ba3fe87
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84878aa0bc86752b72261a25fda7c3c6b001d9a92244bdb5a0437be09b3a69c8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:42:39 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:42:40 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:42:40 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 18:42:40 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 18:42:41 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 18:43:11 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 18:43:11 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 18:43:11 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 18:43:13 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:43:13 GMT
USER notary
# Mon, 28 Jun 2021 18:43:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 18:43:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:43:14 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901d834306dca5d73c86b1a3e642b9623921b12ace19614b6b851c711ba34e30`  
		Last Modified: Mon, 28 Jun 2021 18:44:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7854fb2fa81e4225857d0903028f8d8b60388e6bc42d1db7fab53e6c00b69f6a`  
		Last Modified: Mon, 28 Jun 2021 18:44:20 GMT  
		Size: 5.5 MB (5492174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd57aef237b519a95608c73287c0f7025c19f6f8685b4a7c3715a37e29bb21e`  
		Last Modified: Mon, 28 Jun 2021 18:44:18 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b71b6aed3eeb286dd02ff8e1f0c537db2c147943ec0fbd066ec4930a26e4d8d`  
		Last Modified: Mon, 28 Jun 2021 18:44:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15732b114c4aed6d8e9f55bfd4e53745154b102cdae6ba7a4b33c54cbed03b4`  
		Last Modified: Mon, 28 Jun 2021 18:44:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:e710cd582687e088fefe628a07dd2505127c6796e66dbcda8326be05cc15894f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8011976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a516df75368365fad1bd7a4a6dc2aa9686e90d3e4caebe6e111e5485a71633a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 19:05:43 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 19:05:49 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 19:05:58 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 19:06:04 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 19:06:12 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 19:06:50 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 19:06:53 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 19:06:59 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 19:07:12 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 19:07:17 GMT
USER notary
# Mon, 28 Jun 2021 19:07:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 19:07:25 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 19:07:32 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774d1c5c4381a471d0330583b591b085ba7721be3c81cd8789feed42d94069f`  
		Last Modified: Mon, 28 Jun 2021 19:09:24 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8624d575f7e1f0cc7af0f836038c0ba18a5a4f28d59b19f7b864af5d2b3165a9`  
		Last Modified: Mon, 28 Jun 2021 19:09:25 GMT  
		Size: 5.2 MB (5196709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2bc8ac9d9839b1b22e79990daa58552a3504fad4d75872e944c14d114436aa`  
		Last Modified: Mon, 28 Jun 2021 19:09:24 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdfca1d1b5189efb3f22d793bdcc0515e3a8046adfe3245891f745cf6aa2c14`  
		Last Modified: Mon, 28 Jun 2021 19:09:24 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7305ee40cd7e7cca0861152b40b859c023212391129fe54bbcae71824bc83`  
		Last Modified: Mon, 28 Jun 2021 19:09:24 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:e3d43fb7dda0343a7ded6d0993a1e708a9e41c4e24d58132ced015c5e739b8d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfdb9f7f7bd3d0d7244783d83e48c5b96d36c043790ee7013daf9636174d768`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:41:45 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:41:46 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:41:47 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 18:41:47 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 18:41:47 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 18:42:05 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 18:42:06 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 18:42:07 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 18:42:08 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:42:09 GMT
USER notary
# Mon, 28 Jun 2021 18:42:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 18:42:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:42:10 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184ca204db36314f27bd03240ef076a859f4b79eb88eb91fc577a23a9272f87`  
		Last Modified: Mon, 28 Jun 2021 18:43:04 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2861cd8ad73ff4769fe4d4486b69d53c3ef482a6f8910c9eb4ca0fe0d905384`  
		Last Modified: Mon, 28 Jun 2021 18:43:06 GMT  
		Size: 5.6 MB (5608457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a16f9d50249d2ecd1d114cef11feff1caae20cc7f78b90b7e0d1db1c6a2fbe`  
		Last Modified: Mon, 28 Jun 2021 18:43:04 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99304ce094ebb21e1986dc45779d9f4e11efe621f41d8bb2f2fee1e08f61edc6`  
		Last Modified: Mon, 28 Jun 2021 18:43:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da8c1de5d2b406d6aa67d960e9de45167c8245853584cfad981b8b08d279ce`  
		Last Modified: Mon, 28 Jun 2021 18:43:04 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:server-0.6.1-2`

```console
$ docker pull notary@sha256:141534ec456d58f96094fd956682b7425bd50e90d3428011f4a069bec0710e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server-0.6.1-2` - linux; amd64

```console
$ docker pull notary@sha256:43f4409374b91208328c212fdf9363ac1e6dc22412eb7217aac751bc5c489dd2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8592976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162689747d5ac7859de78f9aae1f4ffd15e68bac113e35a855e350a05886234f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:58:36 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:58:36 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:58:36 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 18:58:36 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 18:58:36 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 18:58:52 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 18:58:52 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 18:58:52 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 18:58:53 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:58:54 GMT
USER notary
# Mon, 28 Jun 2021 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 18:58:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:58:54 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77556963ef8a796bf41535d79d06ba6d80883bdaa9cd149853fa0cb7bf99da0`  
		Last Modified: Mon, 28 Jun 2021 18:59:27 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae7947d7e939530ca197852782ce0cf6546b2508f5b7f70a2ae9940803d415c`  
		Last Modified: Mon, 28 Jun 2021 18:59:28 GMT  
		Size: 5.8 MB (5778894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774741ed1bdb890d7e5e37e13c0a5eaada0dd7dde5d7d6c3dcfa47892f8fef4c`  
		Last Modified: Mon, 28 Jun 2021 18:59:27 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ff51d63b11312605581f793afe414169a074b16e9615348f61425edbfded20`  
		Last Modified: Mon, 28 Jun 2021 18:59:27 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abf3b1ab2eca193532a47a956e16b9412aa4a2724dee7c54260fd27d2acbbc3`  
		Last Modified: Mon, 28 Jun 2021 18:59:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; arm variant v6

```console
$ docker pull notary@sha256:19ce5792b7c9769089fb8b0fd736bf1f084eaf7fa958ce6fd0a9a479c6c9a6bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402814d5a76677d5defb45a7423e84467ca374c481609a52c7b553df3f549414`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 19:03:50 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 19:03:50 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 19:03:51 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 19:03:51 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 19:03:52 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 19:04:18 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 19:04:19 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 19:04:20 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 19:04:21 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 19:04:22 GMT
USER notary
# Mon, 28 Jun 2021 19:04:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 19:04:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 19:04:23 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb0fe1c5eb5b55a63c1f43d072d6473002d6bafddbd5129189736c88b1c4df3`  
		Last Modified: Mon, 28 Jun 2021 19:05:35 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89157730c492f9ff6dc09b4b6d68970b3c38f97382aa413616780b99f16d0150`  
		Last Modified: Mon, 28 Jun 2021 19:05:38 GMT  
		Size: 5.4 MB (5432637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbdc6a98cd1821e80988139e066b22d819cb2428e3a6b7e23fd0687e36c721a`  
		Last Modified: Mon, 28 Jun 2021 19:05:35 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d98817260921113ab52f99676b5469c9eba20989f2ebe16de7244fb7399507`  
		Last Modified: Mon, 28 Jun 2021 19:05:35 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098fc3ce99653b67ce80a6974bd3b7e19cafe04b93b91bc6b2b794d10793f2ab`  
		Last Modified: Mon, 28 Jun 2021 19:05:35 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:84d37fa149b66ca8f676d231ea0a45a9fa9ee9b0b64c6f1ccd33882fcfe5634d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8049433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaff639380cc586b31a1e46dac0e3b2514e134ffbd03b651630a39a16d3afbba`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:41:01 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:41:02 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:41:02 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 18:41:02 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 18:41:02 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 18:41:15 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 18:41:15 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 18:41:16 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 18:41:17 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:41:17 GMT
USER notary
# Mon, 28 Jun 2021 18:41:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 18:41:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:41:17 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0adeb9de9824c29710e237b61cbcbe6fd3a06ee6d782b196281b43d9f6df8d`  
		Last Modified: Mon, 28 Jun 2021 18:41:58 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872551adbbf0fa99b194c79bf451d61f6737218d54a37eda8452f261299d5efa`  
		Last Modified: Mon, 28 Jun 2021 18:41:59 GMT  
		Size: 5.3 MB (5335286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833deb1d1fddec8beb3c60afa38b604c831f69fadded305c0e3c1f3013d69204`  
		Last Modified: Mon, 28 Jun 2021 18:41:57 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdb1fdfa241c1d8481fd04253374894f79918d98f96d7b5c5d544a89489ec05`  
		Last Modified: Mon, 28 Jun 2021 18:41:57 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e165a9f59ac6310e9902f349c334a4bb56c0744e158a9bf9dcb78063263db3`  
		Last Modified: Mon, 28 Jun 2021 18:41:58 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; 386

```console
$ docker pull notary@sha256:e81817925f77d235fa795ae6392ccf0b31c27a053bd8535984123ed70ba3fe87
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8313192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84878aa0bc86752b72261a25fda7c3c6b001d9a92244bdb5a0437be09b3a69c8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:42:39 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:42:40 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:42:40 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 18:42:40 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 18:42:41 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 18:43:11 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 18:43:11 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 18:43:11 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 18:43:13 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:43:13 GMT
USER notary
# Mon, 28 Jun 2021 18:43:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 18:43:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:43:14 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901d834306dca5d73c86b1a3e642b9623921b12ace19614b6b851c711ba34e30`  
		Last Modified: Mon, 28 Jun 2021 18:44:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7854fb2fa81e4225857d0903028f8d8b60388e6bc42d1db7fab53e6c00b69f6a`  
		Last Modified: Mon, 28 Jun 2021 18:44:20 GMT  
		Size: 5.5 MB (5492174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd57aef237b519a95608c73287c0f7025c19f6f8685b4a7c3715a37e29bb21e`  
		Last Modified: Mon, 28 Jun 2021 18:44:18 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b71b6aed3eeb286dd02ff8e1f0c537db2c147943ec0fbd066ec4930a26e4d8d`  
		Last Modified: Mon, 28 Jun 2021 18:44:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15732b114c4aed6d8e9f55bfd4e53745154b102cdae6ba7a4b33c54cbed03b4`  
		Last Modified: Mon, 28 Jun 2021 18:44:18 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; ppc64le

```console
$ docker pull notary@sha256:e710cd582687e088fefe628a07dd2505127c6796e66dbcda8326be05cc15894f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8011976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a516df75368365fad1bd7a4a6dc2aa9686e90d3e4caebe6e111e5485a71633a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 19:05:43 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 19:05:49 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 19:05:58 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 19:06:04 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 19:06:12 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 19:06:50 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 19:06:53 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 19:06:59 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 19:07:12 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 19:07:17 GMT
USER notary
# Mon, 28 Jun 2021 19:07:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 19:07:25 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 19:07:32 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774d1c5c4381a471d0330583b591b085ba7721be3c81cd8789feed42d94069f`  
		Last Modified: Mon, 28 Jun 2021 19:09:24 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8624d575f7e1f0cc7af0f836038c0ba18a5a4f28d59b19f7b864af5d2b3165a9`  
		Last Modified: Mon, 28 Jun 2021 19:09:25 GMT  
		Size: 5.2 MB (5196709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2bc8ac9d9839b1b22e79990daa58552a3504fad4d75872e944c14d114436aa`  
		Last Modified: Mon, 28 Jun 2021 19:09:24 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdfca1d1b5189efb3f22d793bdcc0515e3a8046adfe3245891f745cf6aa2c14`  
		Last Modified: Mon, 28 Jun 2021 19:09:24 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a7305ee40cd7e7cca0861152b40b859c023212391129fe54bbcae71824bc83`  
		Last Modified: Mon, 28 Jun 2021 19:09:24 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; s390x

```console
$ docker pull notary@sha256:e3d43fb7dda0343a7ded6d0993a1e708a9e41c4e24d58132ced015c5e739b8d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfdb9f7f7bd3d0d7244783d83e48c5b96d36c043790ee7013daf9636174d768`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:41:45 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:41:46 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:41:47 GMT
ENV INSTALLDIR=/notary/server
# Mon, 28 Jun 2021 18:41:47 GMT
EXPOSE 4443
# Mon, 28 Jun 2021 18:41:47 GMT
WORKDIR /notary/server
# Mon, 28 Jun 2021 18:42:05 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Mon, 28 Jun 2021 18:42:06 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Mon, 28 Jun 2021 18:42:07 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Mon, 28 Jun 2021 18:42:08 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:42:09 GMT
USER notary
# Mon, 28 Jun 2021 18:42:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 28 Jun 2021 18:42:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:42:10 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184ca204db36314f27bd03240ef076a859f4b79eb88eb91fc577a23a9272f87`  
		Last Modified: Mon, 28 Jun 2021 18:43:04 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2861cd8ad73ff4769fe4d4486b69d53c3ef482a6f8910c9eb4ca0fe0d905384`  
		Last Modified: Mon, 28 Jun 2021 18:43:06 GMT  
		Size: 5.6 MB (5608457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a16f9d50249d2ecd1d114cef11feff1caae20cc7f78b90b7e0d1db1c6a2fbe`  
		Last Modified: Mon, 28 Jun 2021 18:43:04 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99304ce094ebb21e1986dc45779d9f4e11efe621f41d8bb2f2fee1e08f61edc6`  
		Last Modified: Mon, 28 Jun 2021 18:43:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da8c1de5d2b406d6aa67d960e9de45167c8245853584cfad981b8b08d279ce`  
		Last Modified: Mon, 28 Jun 2021 18:43:04 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer`

```console
$ docker pull notary@sha256:a33cc6c8b2d3581afdfd1589496e195d2584582553853d7f036d7896c1fa3c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:ef452f69cb0136c87ef982cd9865fffb0192804c40173c9c9424ba70f0023e1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8074897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c0d72e66a1e64dfb64930956bd35c02bb493d2e1ef07ad4d22001eec04efe4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:58:36 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:58:36 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:58:57 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 18:58:58 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 18:58:58 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 18:58:58 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 18:59:13 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 18:59:13 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 18:59:14 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 18:59:15 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:59:15 GMT
USER notary
# Mon, 28 Jun 2021 18:59:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 18:59:15 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:59:16 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae06682cc74aa8466b3054395843766c23120c08700730d982412a347acbd357`  
		Last Modified: Mon, 28 Jun 2021 18:59:39 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022ee6e7927e718ca2d541751d63f2ad8566f9e5ef7c0e8796fcc5874462afce`  
		Last Modified: Mon, 28 Jun 2021 18:59:40 GMT  
		Size: 5.3 MB (5260868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d436ae8c1f852ceff180862c1fb9f94c26c0f4e84e247c2d140c16fd33a7cb7f`  
		Last Modified: Mon, 28 Jun 2021 18:59:39 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d5760f441337852538af88eb3dfdeb457f91fc92fd98266abe4a07be6a14ea`  
		Last Modified: Mon, 28 Jun 2021 18:59:39 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4333e4c4880d9a95b9641756fe7b44a8a89f7a4211c90c2b3c2e224ca1acaf87`  
		Last Modified: Mon, 28 Jun 2021 18:59:39 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:1c33d7b2e8a6b906cac8f10144db242d7e6f9e6cbe29ecfa86202e58c49b7f26
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f9caf9a3e0625db3da27658a98220e73f0cd5d1287aeea072fdd31d8fc5daa`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 19:03:50 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 19:03:50 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 19:04:33 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 19:04:34 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 19:04:34 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 19:04:35 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 19:04:58 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 19:04:59 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 19:04:59 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 19:05:01 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 19:05:01 GMT
USER notary
# Mon, 28 Jun 2021 19:05:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 19:05:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 19:05:03 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9b161eefead0cec701cdcf3c1624977a39a72c1cda681a936c15194e466bf`  
		Last Modified: Mon, 28 Jun 2021 19:05:51 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1159b671f0ade7168f2d01d5be2cd420e797b451e422c48e2295b5fd2b69b494`  
		Last Modified: Mon, 28 Jun 2021 19:05:54 GMT  
		Size: 4.9 MB (4946838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cf26f824896e9a8a49ad7f17fbbbf4dc103573a2622ff39e49daa14d6fc89d`  
		Last Modified: Mon, 28 Jun 2021 19:05:51 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9ee6854652602cc106acc56c9a3378d20aecd3befc403e258aff23c0e1eff8`  
		Last Modified: Mon, 28 Jun 2021 19:05:51 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4deb73581688018a5740aeddf0f589d819a74491be05a89ed1ebad3308fec6df`  
		Last Modified: Mon, 28 Jun 2021 19:05:51 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:e19752489373db10f56262f344c89be563600cddb33e8c5d4a3abbc9acc5670e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2254205dd7846938c0ac120f7dbea8e1e599587ea179df8844cb31f07ff75ff8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:41:01 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:41:02 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:41:24 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 18:41:24 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 18:41:24 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 18:41:25 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 18:41:37 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 18:41:37 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 18:41:37 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 18:41:38 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:41:38 GMT
USER notary
# Mon, 28 Jun 2021 18:41:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 18:41:39 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:41:39 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e0fa12a850c2f663003533004002c3664154fb7307d828429951110aea9687`  
		Last Modified: Mon, 28 Jun 2021 18:42:10 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67cc19b70d16f873d8a25077e7bd2500fb24d123420d888749ffc0d11f7d59a`  
		Last Modified: Mon, 28 Jun 2021 18:42:12 GMT  
		Size: 4.9 MB (4859004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0cd0fde5328be58b614777c8091540330fd526e335bde638d0b9d821466686`  
		Last Modified: Mon, 28 Jun 2021 18:42:11 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc841fa62e30dfe11784ad16c822ba548417e18f4e6107ef0df194e876e28b62`  
		Last Modified: Mon, 28 Jun 2021 18:42:10 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2c83faeb5b5184924d2676aec91258a21b56491aad1a5d32fbd57150b15f7`  
		Last Modified: Mon, 28 Jun 2021 18:42:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:a77c5117d447096a45dfdbc9c96f8dceb7ac812af2313b3f5ef318d5a9ab6be0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7827291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fd81c0349dc3ae9d3c371739ac979143231a119f8d0c6ba9a4fed520a29b1f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:42:39 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:42:40 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:43:24 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 18:43:24 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 18:43:24 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 18:43:25 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 18:43:51 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 18:43:51 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 18:43:51 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 18:43:53 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:43:53 GMT
USER notary
# Mon, 28 Jun 2021 18:43:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 18:43:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:43:54 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d582fd18e358e07f4b30fada572cdf6e1e982085d7817893216ab3869c1b6e9`  
		Last Modified: Mon, 28 Jun 2021 18:44:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f58a11c6ddc2c120eb603e6a5f89be19a72fdc1b3a4689c7c1283e795f956`  
		Last Modified: Mon, 28 Jun 2021 18:44:34 GMT  
		Size: 5.0 MB (5006330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c9c0b37a49135e20513806760b105056477a33ce4e73d61fad7d66e755afef`  
		Last Modified: Mon, 28 Jun 2021 18:44:33 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cc9cacf53edb0f2cc407630af58061218c31aacee52b18a5e99aa909ddf5af`  
		Last Modified: Mon, 28 Jun 2021 18:44:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61176d5608e956b55974fc3102a3779c89d4b397e32dbe2e8375ec84392a6831`  
		Last Modified: Mon, 28 Jun 2021 18:44:33 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:46b18b5acabda88a85f8e0d66ae6017eedad7a3c0023bf005e6f7fded9097793
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7549912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1faafeea274430d76f5eeba2b73ab3795d7d2c18646fe853f5525c981f7d5b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 19:05:43 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 19:05:49 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 19:07:49 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 19:07:52 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 19:07:55 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 19:08:00 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 19:08:26 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 19:08:32 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 19:08:34 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 19:08:48 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 19:08:53 GMT
USER notary
# Mon, 28 Jun 2021 19:08:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 19:08:59 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 19:09:02 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc28f4919ab07e53b0b37321d204f7a4d50d7927e071f1ca67dbe2f86270d794`  
		Last Modified: Mon, 28 Jun 2021 19:09:38 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d10c05e32efba3172abfd0d2afb4b59e67e18a4a70919e91ad5bf6f87fff9f7`  
		Last Modified: Mon, 28 Jun 2021 19:09:39 GMT  
		Size: 4.7 MB (4734713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8233b4aec87ad0d2f1a223e046095fb2c8d9da6ec74b3431669ec0f6cb60e14`  
		Last Modified: Mon, 28 Jun 2021 19:09:39 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13aec91f57e142578ec0d689c7b778dd9e0fbc40dbfb81380f83925c5febdc1d`  
		Last Modified: Mon, 28 Jun 2021 19:09:38 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472760a7fb11369fadd46e374ea826026791ba6df0fc28c2deb679375658a16a`  
		Last Modified: Mon, 28 Jun 2021 19:09:38 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:b7ad38f580bf5e6f1a597401a4be89ea20e58de6da2a2395ba17e08bc35ae25b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7712169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebfc5f0a0590c25445b2f1c6c607af3a3c750d491f9749c9cd0ee990f3e1692`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:41:45 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:41:46 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:42:18 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 18:42:18 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 18:42:19 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 18:42:20 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 18:42:37 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 18:42:38 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 18:42:39 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 18:42:40 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:42:41 GMT
USER notary
# Mon, 28 Jun 2021 18:42:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 18:42:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:42:42 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cce7e45c0520ea4b7c81353d7da232d60ef9db27080ac960d8e1710f96e53ff`  
		Last Modified: Mon, 28 Jun 2021 18:43:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0845cbb40b0ab3a40c4a2bd9f330b619fa09ebff05018a6a67314aa8fce8e1ea`  
		Last Modified: Mon, 28 Jun 2021 18:43:15 GMT  
		Size: 5.1 MB (5107458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3a22a2563022491f4f40b5493c1d3cbf2c29c9b39897753958bebdb8c445a2`  
		Last Modified: Mon, 28 Jun 2021 18:43:14 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c162698fdae52d938a3f50d7c0b81594c45ccc44d86b4c917dd2c140f5a38432`  
		Last Modified: Mon, 28 Jun 2021 18:43:14 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a3ec179744b0d4b21107f45d247eedba585c0ead200486d099110985088b11`  
		Last Modified: Mon, 28 Jun 2021 18:43:14 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer-0.6.1-2`

```console
$ docker pull notary@sha256:a33cc6c8b2d3581afdfd1589496e195d2584582553853d7f036d7896c1fa3c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer-0.6.1-2` - linux; amd64

```console
$ docker pull notary@sha256:ef452f69cb0136c87ef982cd9865fffb0192804c40173c9c9424ba70f0023e1d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8074897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c0d72e66a1e64dfb64930956bd35c02bb493d2e1ef07ad4d22001eec04efe4`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:58:36 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:58:36 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:58:57 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 18:58:58 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 18:58:58 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 18:58:58 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 18:59:13 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 18:59:13 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 18:59:14 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 18:59:15 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:59:15 GMT
USER notary
# Mon, 28 Jun 2021 18:59:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 18:59:15 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:59:16 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae06682cc74aa8466b3054395843766c23120c08700730d982412a347acbd357`  
		Last Modified: Mon, 28 Jun 2021 18:59:39 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022ee6e7927e718ca2d541751d63f2ad8566f9e5ef7c0e8796fcc5874462afce`  
		Last Modified: Mon, 28 Jun 2021 18:59:40 GMT  
		Size: 5.3 MB (5260868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d436ae8c1f852ceff180862c1fb9f94c26c0f4e84e247c2d140c16fd33a7cb7f`  
		Last Modified: Mon, 28 Jun 2021 18:59:39 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d5760f441337852538af88eb3dfdeb457f91fc92fd98266abe4a07be6a14ea`  
		Last Modified: Mon, 28 Jun 2021 18:59:39 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4333e4c4880d9a95b9641756fe7b44a8a89f7a4211c90c2b3c2e224ca1acaf87`  
		Last Modified: Mon, 28 Jun 2021 18:59:39 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; arm variant v6

```console
$ docker pull notary@sha256:1c33d7b2e8a6b906cac8f10144db242d7e6f9e6cbe29ecfa86202e58c49b7f26
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f9caf9a3e0625db3da27658a98220e73f0cd5d1287aeea072fdd31d8fc5daa`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 19:03:50 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 19:03:50 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 19:04:33 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 19:04:34 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 19:04:34 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 19:04:35 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 19:04:58 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 19:04:59 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 19:04:59 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 19:05:01 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 19:05:01 GMT
USER notary
# Mon, 28 Jun 2021 19:05:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 19:05:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 19:05:03 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a9b161eefead0cec701cdcf3c1624977a39a72c1cda681a936c15194e466bf`  
		Last Modified: Mon, 28 Jun 2021 19:05:51 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1159b671f0ade7168f2d01d5be2cd420e797b451e422c48e2295b5fd2b69b494`  
		Last Modified: Mon, 28 Jun 2021 19:05:54 GMT  
		Size: 4.9 MB (4946838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cf26f824896e9a8a49ad7f17fbbbf4dc103573a2622ff39e49daa14d6fc89d`  
		Last Modified: Mon, 28 Jun 2021 19:05:51 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9ee6854652602cc106acc56c9a3378d20aecd3befc403e258aff23c0e1eff8`  
		Last Modified: Mon, 28 Jun 2021 19:05:51 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4deb73581688018a5740aeddf0f589d819a74491be05a89ed1ebad3308fec6df`  
		Last Modified: Mon, 28 Jun 2021 19:05:51 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:e19752489373db10f56262f344c89be563600cddb33e8c5d4a3abbc9acc5670e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7573089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2254205dd7846938c0ac120f7dbea8e1e599587ea179df8844cb31f07ff75ff8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:41:01 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:41:02 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:41:24 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 18:41:24 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 18:41:24 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 18:41:25 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 18:41:37 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 18:41:37 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 18:41:37 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 18:41:38 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:41:38 GMT
USER notary
# Mon, 28 Jun 2021 18:41:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 18:41:39 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:41:39 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e0fa12a850c2f663003533004002c3664154fb7307d828429951110aea9687`  
		Last Modified: Mon, 28 Jun 2021 18:42:10 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67cc19b70d16f873d8a25077e7bd2500fb24d123420d888749ffc0d11f7d59a`  
		Last Modified: Mon, 28 Jun 2021 18:42:12 GMT  
		Size: 4.9 MB (4859004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0cd0fde5328be58b614777c8091540330fd526e335bde638d0b9d821466686`  
		Last Modified: Mon, 28 Jun 2021 18:42:11 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc841fa62e30dfe11784ad16c822ba548417e18f4e6107ef0df194e876e28b62`  
		Last Modified: Mon, 28 Jun 2021 18:42:10 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd2c83faeb5b5184924d2676aec91258a21b56491aad1a5d32fbd57150b15f7`  
		Last Modified: Mon, 28 Jun 2021 18:42:10 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; 386

```console
$ docker pull notary@sha256:a77c5117d447096a45dfdbc9c96f8dceb7ac812af2313b3f5ef318d5a9ab6be0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7827291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fd81c0349dc3ae9d3c371739ac979143231a119f8d0c6ba9a4fed520a29b1f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:42:39 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:42:40 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:43:24 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 18:43:24 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 18:43:24 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 18:43:25 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 18:43:51 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 18:43:51 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 18:43:51 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 18:43:53 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:43:53 GMT
USER notary
# Mon, 28 Jun 2021 18:43:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 18:43:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:43:54 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d582fd18e358e07f4b30fada572cdf6e1e982085d7817893216ab3869c1b6e9`  
		Last Modified: Mon, 28 Jun 2021 18:44:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f58a11c6ddc2c120eb603e6a5f89be19a72fdc1b3a4689c7c1283e795f956`  
		Last Modified: Mon, 28 Jun 2021 18:44:34 GMT  
		Size: 5.0 MB (5006330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c9c0b37a49135e20513806760b105056477a33ce4e73d61fad7d66e755afef`  
		Last Modified: Mon, 28 Jun 2021 18:44:33 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cc9cacf53edb0f2cc407630af58061218c31aacee52b18a5e99aa909ddf5af`  
		Last Modified: Mon, 28 Jun 2021 18:44:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61176d5608e956b55974fc3102a3779c89d4b397e32dbe2e8375ec84392a6831`  
		Last Modified: Mon, 28 Jun 2021 18:44:33 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; ppc64le

```console
$ docker pull notary@sha256:46b18b5acabda88a85f8e0d66ae6017eedad7a3c0023bf005e6f7fded9097793
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7549912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1faafeea274430d76f5eeba2b73ab3795d7d2c18646fe853f5525c981f7d5b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 19:05:43 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 19:05:49 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 19:07:49 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 19:07:52 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 19:07:55 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 19:08:00 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 19:08:26 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 19:08:32 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 19:08:34 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 19:08:48 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 19:08:53 GMT
USER notary
# Mon, 28 Jun 2021 19:08:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 19:08:59 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 19:09:02 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc28f4919ab07e53b0b37321d204f7a4d50d7927e071f1ca67dbe2f86270d794`  
		Last Modified: Mon, 28 Jun 2021 19:09:38 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d10c05e32efba3172abfd0d2afb4b59e67e18a4a70919e91ad5bf6f87fff9f7`  
		Last Modified: Mon, 28 Jun 2021 19:09:39 GMT  
		Size: 4.7 MB (4734713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8233b4aec87ad0d2f1a223e046095fb2c8d9da6ec74b3431669ec0f6cb60e14`  
		Last Modified: Mon, 28 Jun 2021 19:09:39 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13aec91f57e142578ec0d689c7b778dd9e0fbc40dbfb81380f83925c5febdc1d`  
		Last Modified: Mon, 28 Jun 2021 19:09:38 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472760a7fb11369fadd46e374ea826026791ba6df0fc28c2deb679375658a16a`  
		Last Modified: Mon, 28 Jun 2021 19:09:38 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; s390x

```console
$ docker pull notary@sha256:b7ad38f580bf5e6f1a597401a4be89ea20e58de6da2a2395ba17e08bc35ae25b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7712169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebfc5f0a0590c25445b2f1c6c607af3a3c750d491f9749c9cd0ee990f3e1692`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Jun 2021 18:41:45 GMT
ENV TAG=v0.6.1
# Mon, 28 Jun 2021 18:41:46 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Mon, 28 Jun 2021 18:42:18 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 28 Jun 2021 18:42:18 GMT
EXPOSE 4444
# Mon, 28 Jun 2021 18:42:19 GMT
EXPOSE 7899
# Mon, 28 Jun 2021 18:42:20 GMT
WORKDIR /notary/signer
# Mon, 28 Jun 2021 18:42:37 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Mon, 28 Jun 2021 18:42:38 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Mon, 28 Jun 2021 18:42:39 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Mon, 28 Jun 2021 18:42:40 GMT
RUN adduser -D -H -g "" notary
# Mon, 28 Jun 2021 18:42:41 GMT
USER notary
# Mon, 28 Jun 2021 18:42:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 28 Jun 2021 18:42:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 28 Jun 2021 18:42:42 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cce7e45c0520ea4b7c81353d7da232d60ef9db27080ac960d8e1710f96e53ff`  
		Last Modified: Mon, 28 Jun 2021 18:43:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0845cbb40b0ab3a40c4a2bd9f330b619fa09ebff05018a6a67314aa8fce8e1ea`  
		Last Modified: Mon, 28 Jun 2021 18:43:15 GMT  
		Size: 5.1 MB (5107458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3a22a2563022491f4f40b5493c1d3cbf2c29c9b39897753958bebdb8c445a2`  
		Last Modified: Mon, 28 Jun 2021 18:43:14 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c162698fdae52d938a3f50d7c0b81594c45ccc44d86b4c917dd2c140f5a38432`  
		Last Modified: Mon, 28 Jun 2021 18:43:14 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a3ec179744b0d4b21107f45d247eedba585c0ead200486d099110985088b11`  
		Last Modified: Mon, 28 Jun 2021 18:43:14 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
