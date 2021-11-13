## `notary:server-0.6.1-2`

```console
$ docker pull notary@sha256:45fdd756e039d3c42e791b78cb5099d38699b7369bf47960e36b50a263b2928f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server-0.6.1-2` - linux; amd64

```console
$ docker pull notary@sha256:67ffe7a46b7806128d92bda4c1b690b26ea4a2f0ba810a82fbc7142ddb2943cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8207893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca52a83cf1a2a6216ae2be361a5a75be35478313ecc9177fbda0a59af156a2d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:13:51 GMT
ENV TAG=v0.6.1
# Wed, 01 Sep 2021 03:13:51 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Wed, 01 Sep 2021 03:13:52 GMT
ENV INSTALLDIR=/notary/server
# Wed, 01 Sep 2021 03:13:52 GMT
EXPOSE 4443
# Wed, 01 Sep 2021 03:13:52 GMT
WORKDIR /notary/server
# Wed, 01 Sep 2021 03:14:11 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Wed, 01 Sep 2021 03:14:11 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Wed, 01 Sep 2021 03:14:11 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Wed, 01 Sep 2021 03:14:12 GMT
RUN adduser -D -H -g "" notary
# Wed, 01 Sep 2021 03:14:13 GMT
USER notary
# Wed, 01 Sep 2021 03:14:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 01 Sep 2021 03:14:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Sep 2021 03:14:13 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7563319b599f4b2880de541811e7aa09df2d754a7aff1c29f2bd82734f00f63b`  
		Last Modified: Wed, 01 Sep 2021 03:14:51 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a9ac2020932ed3fa1dd909e958fe0de479168166ac890c02f5aababd9e94d6`  
		Last Modified: Wed, 01 Sep 2021 03:14:53 GMT  
		Size: 5.4 MB (5391688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc192082178ba426f4668d919fd331ed9ffadaa27dc421222e4ec486c4794a`  
		Last Modified: Wed, 01 Sep 2021 03:14:51 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6d214a7821c7637a982e72d16658a619473d1d83151e101582ff51bf9d5d9f`  
		Last Modified: Wed, 01 Sep 2021 03:14:51 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3416e2a15f0632f19e8488e51c5016e6f8da1e459ed5b6cc8108bd8f71f01f9a`  
		Last Modified: Wed, 01 Sep 2021 03:14:51 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; arm variant v6

```console
$ docker pull notary@sha256:c9a63790b120cdbfc708dcda2bd2a5e33d0b4b7c24ac091e5188554c4d9b83cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7669520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f6b34f2daf1485b896a6fd665e468b70ba83169a21a3afbc098dbf3e4a5e46`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 05:40:38 GMT
ENV TAG=v0.6.1
# Wed, 01 Sep 2021 05:40:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Wed, 01 Sep 2021 05:40:39 GMT
ENV INSTALLDIR=/notary/server
# Wed, 01 Sep 2021 05:40:40 GMT
EXPOSE 4443
# Wed, 01 Sep 2021 05:40:40 GMT
WORKDIR /notary/server
# Wed, 01 Sep 2021 05:41:05 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Wed, 01 Sep 2021 05:41:05 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Wed, 01 Sep 2021 05:41:06 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Wed, 01 Sep 2021 05:41:07 GMT
RUN adduser -D -H -g "" notary
# Wed, 01 Sep 2021 05:41:08 GMT
USER notary
# Wed, 01 Sep 2021 05:41:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 01 Sep 2021 05:41:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Sep 2021 05:41:09 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9791b32cb2bee0a0b775d8371df3e8c553536fb8eea6b87917960002d729a8d4`  
		Last Modified: Wed, 01 Sep 2021 05:42:22 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1829517afacd837ea27a38cfeb23b911d1800a10c4716a3c0e4f991167e17cea`  
		Last Modified: Wed, 01 Sep 2021 05:42:24 GMT  
		Size: 5.0 MB (5043640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df17778e7033a45144aa86f0dd5a1ca55f56889651c7c018c7002dd39b9c2d1c`  
		Last Modified: Wed, 01 Sep 2021 05:42:22 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67729e596106cdd9114ac21e8c4bfc0fc7ac3d1421fecd99044eefcefdb04909`  
		Last Modified: Wed, 01 Sep 2021 05:42:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721b9740d73d966ff04dd47698ac8ecb6daa1e55a2a087b23c8828cda0c2a4e3`  
		Last Modified: Wed, 01 Sep 2021 05:42:23 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:d058307a78633e4174d099f514df79346330a16b65e66a2bcbc379bb9aebe3a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7661057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211ff0cf0466d36bd9d0821396297d9a04d95012678e1d45f4e236b1a9c18c50`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 00:13:38 GMT
ENV TAG=v0.6.1
# Sat, 13 Nov 2021 00:13:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Sat, 13 Nov 2021 00:13:40 GMT
ENV INSTALLDIR=/notary/server
# Sat, 13 Nov 2021 00:13:41 GMT
EXPOSE 4443
# Sat, 13 Nov 2021 00:13:42 GMT
WORKDIR /notary/server
# Sat, 13 Nov 2021 00:13:56 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Sat, 13 Nov 2021 00:13:58 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Sat, 13 Nov 2021 00:13:59 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Sat, 13 Nov 2021 00:13:59 GMT
RUN adduser -D -H -g "" notary
# Sat, 13 Nov 2021 00:14:00 GMT
USER notary
# Sat, 13 Nov 2021 00:14:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 13 Nov 2021 00:14:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 13 Nov 2021 00:14:03 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5b871c3959ef05d38d452bf8f6b740ec4dd926fe08ebb5f0768bb34b849e0f`  
		Last Modified: Sat, 13 Nov 2021 00:14:53 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffaaeba98ef041f585bd32bec6651174bc246de87abb1a5d8735b8feb82af34`  
		Last Modified: Sat, 13 Nov 2021 00:14:54 GMT  
		Size: 4.9 MB (4939333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce603624efa4750d223cca7ddeddce867dd69b49e8ea51239c729ec607aac79`  
		Last Modified: Sat, 13 Nov 2021 00:14:53 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb556b8eb36fef7fb085be5678af95f78d8e6569281e4e5fe2faf028efcce02`  
		Last Modified: Sat, 13 Nov 2021 00:14:53 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebd9966df2aa85787057ee1da91e8cd549d165d9b4745d50dacfc94db2e95f8`  
		Last Modified: Sat, 13 Nov 2021 00:14:53 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; 386

```console
$ docker pull notary@sha256:7bd21d589d36965d05f8ea2c22cb3f1f4927559f0c7cd93beb1d6007c72457c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed58ef6de2cc5ba00a2e02b0ccd753e0ea362c744c8c8ad4ff9f1b9203e704b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 23:39:54 GMT
ENV TAG=v0.6.1
# Tue, 31 Aug 2021 23:39:54 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 31 Aug 2021 23:39:54 GMT
ENV INSTALLDIR=/notary/server
# Tue, 31 Aug 2021 23:39:55 GMT
EXPOSE 4443
# Tue, 31 Aug 2021 23:39:55 GMT
WORKDIR /notary/server
# Tue, 31 Aug 2021 23:40:14 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Tue, 31 Aug 2021 23:40:14 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Tue, 31 Aug 2021 23:40:14 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Tue, 31 Aug 2021 23:40:15 GMT
RUN adduser -D -H -g "" notary
# Tue, 31 Aug 2021 23:40:16 GMT
USER notary
# Tue, 31 Aug 2021 23:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 31 Aug 2021 23:40:16 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 31 Aug 2021 23:40:16 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f309a72780c0ae33127f3d9648feaa3dd524ff498129bc563de603752c5825`  
		Last Modified: Tue, 31 Aug 2021 23:41:05 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28501c64e3369880c178e46a15a6e74b8afb5623d2de0f4ba2155c0a9c84689`  
		Last Modified: Tue, 31 Aug 2021 23:41:06 GMT  
		Size: 5.1 MB (5102327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887ed1e71237dd3118e189e7b0b716daa96d6358eb59c33eb4c2ce1afb9b8d1a`  
		Last Modified: Tue, 31 Aug 2021 23:41:05 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4debc595f02ce78ea65231fc7907840b8888dc35f4811bcb5d0cc3e8dcc2d5b2`  
		Last Modified: Tue, 31 Aug 2021 23:41:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5679870d8918954f4852fa7e70aa4cc8a33feee628d5a035446a67eed3398cd`  
		Last Modified: Tue, 31 Aug 2021 23:41:05 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; ppc64le

```console
$ docker pull notary@sha256:5ebfcc4e2ce9fba290bb3dce5f72828507f4b391a86824248f20d276628b8bc4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7625145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc726b8e6fdee456c512b7b4669685327a649b5c8336a23499f941f3f6d850e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Wed, 01 Sep 2021 02:42:40 GMT
ADD file:07a51f1a2f818bd1c1651832ce63cb1e0046a57994724cda6a20ff1a2a685295 in / 
# Wed, 01 Sep 2021 02:42:41 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 11:31:28 GMT
ENV TAG=v0.6.1
# Wed, 01 Sep 2021 11:31:32 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Wed, 01 Sep 2021 11:31:38 GMT
ENV INSTALLDIR=/notary/server
# Wed, 01 Sep 2021 11:31:43 GMT
EXPOSE 4443
# Wed, 01 Sep 2021 11:31:47 GMT
WORKDIR /notary/server
# Wed, 01 Sep 2021 11:32:09 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Wed, 01 Sep 2021 11:32:10 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Wed, 01 Sep 2021 11:32:11 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Wed, 01 Sep 2021 11:32:19 GMT
RUN adduser -D -H -g "" notary
# Wed, 01 Sep 2021 11:32:20 GMT
USER notary
# Wed, 01 Sep 2021 11:32:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 01 Sep 2021 11:32:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Sep 2021 11:32:26 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:39d9bf63205258fe1d085fd596101e6fc46ff796cda8d3ba2983e166a25b74db`  
		Last Modified: Wed, 01 Sep 2021 02:43:53 GMT  
		Size: 2.8 MB (2814813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c975bde7d3c508db3b7430faa12453ba1fcb4b38930168a6c482c5f16122adfe`  
		Last Modified: Wed, 01 Sep 2021 11:33:51 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1bbe6c8c639d47e3a0363729bb630caf92f6eb77f8c27186dbf9c1ffb61490`  
		Last Modified: Wed, 01 Sep 2021 11:33:52 GMT  
		Size: 4.8 MB (4808212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d167ff7519a7e7657df22f676e7b6693d1845213f43feeac7f8b504985ccfb6`  
		Last Modified: Wed, 01 Sep 2021 11:33:51 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de91a48bec8aa3318a6ffb570b17be8ae9cece4ddf092e0d4cd80461ff8acf2`  
		Last Modified: Wed, 01 Sep 2021 11:33:51 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf45fde51aee48def303ba9b620770e78af2bb1281c50a4841ac1d7025f7ee1`  
		Last Modified: Wed, 01 Sep 2021 11:33:51 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.6.1-2` - linux; s390x

```console
$ docker pull notary@sha256:6c43379addb89d560e7cab01d84855b22bd2c82e5cc2e36801f14838c700c279
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7825095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b18dc5db474643b19fdf62273306c35c1c45ff86f4b82d08c468f41e646f5f6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--help"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:44 GMT
ADD file:637f327c9b07758709ef7dbc42eb472c888d221acde89b1c3775553864334d5c in / 
# Fri, 12 Nov 2021 16:41:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:28:05 GMT
ENV TAG=v0.6.1
# Fri, 12 Nov 2021 19:28:05 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 12 Nov 2021 19:28:05 GMT
ENV INSTALLDIR=/notary/server
# Fri, 12 Nov 2021 19:28:05 GMT
EXPOSE 4443
# Fri, 12 Nov 2021 19:28:05 GMT
WORKDIR /notary/server
# Fri, 12 Nov 2021 19:28:17 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --help
# Fri, 12 Nov 2021 19:28:17 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 12 Nov 2021 19:28:17 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 12 Nov 2021 19:28:18 GMT
RUN adduser -D -H -g "" notary
# Fri, 12 Nov 2021 19:28:18 GMT
USER notary
# Fri, 12 Nov 2021 19:28:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 12 Nov 2021 19:28:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 12 Nov 2021 19:28:18 GMT
CMD ["notary-server" "--help"]
```

-	Layers:
	-	`sha256:b872f056719bde6e6722091afb2a3376d720c69c142b91ac352050080dd79615`  
		Last Modified: Fri, 12 Nov 2021 16:42:54 GMT  
		Size: 2.6 MB (2611155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f678c2054f7f61ec9de39904e129a2cdf5fc3d5426a7baabba2759476f19e7`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fdd4ef13b2fa79ee53546c4ea6f6818eb1734907894e05ea859c2dbfb980a`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 5.2 MB (5211824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b738a8c0c4be5e7dfd345c86d78a0d2d197ca1b75fce8c9c2f0f1d33a38b4e8`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71170955a75304f163bcc48c4dbe43164ee6f1a17c33a38f711459b475b96a1b`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8145397afd5cfbb2a1082fddeaf7f0f58ed97c7017183595e5391fe76c7c55e`  
		Last Modified: Fri, 12 Nov 2021 19:28:55 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
