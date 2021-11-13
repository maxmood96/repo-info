## `notary:signer-0.6.1-2`

```console
$ docker pull notary@sha256:4bee7e92a3b1c46978141c6b6afca61acc87b6e3af28891a40465327c28c9a21
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
$ docker pull notary@sha256:a3024c444f372965bb9e02409cbd51cf83cf64e34eb6c2cb59cda240ca1df125
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7688013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26aad70f50d38c07bd7f33356fcb4df3bdaaec3a4831c088d8b272bda896ccef`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:13:51 GMT
ENV TAG=v0.6.1
# Wed, 01 Sep 2021 03:13:51 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Wed, 01 Sep 2021 03:14:17 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 01 Sep 2021 03:14:17 GMT
EXPOSE 4444
# Wed, 01 Sep 2021 03:14:17 GMT
EXPOSE 7899
# Wed, 01 Sep 2021 03:14:17 GMT
WORKDIR /notary/signer
# Wed, 01 Sep 2021 03:14:36 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Wed, 01 Sep 2021 03:14:36 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Wed, 01 Sep 2021 03:14:36 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Wed, 01 Sep 2021 03:14:37 GMT
RUN adduser -D -H -g "" notary
# Wed, 01 Sep 2021 03:14:37 GMT
USER notary
# Wed, 01 Sep 2021 03:14:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 01 Sep 2021 03:14:38 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Sep 2021 03:14:38 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0640cea0fffa153e8a43f0cc1bba1b442e6294eba3a414a7326a92ae1774d9e`  
		Last Modified: Wed, 01 Sep 2021 03:15:03 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3826f26db296ff4a05ad4906679d7baae10106106a52ebe02a1d5eade5d6177f`  
		Last Modified: Wed, 01 Sep 2021 03:15:04 GMT  
		Size: 4.9 MB (4871876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e403c8609bed446927d18879dab4a45d49fa3bfac062d23d1f193b6912542a`  
		Last Modified: Wed, 01 Sep 2021 03:15:03 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2d426533852ba181bb1c0526d7e9d9947021478043d28a381f7252ced4a368`  
		Last Modified: Wed, 01 Sep 2021 03:15:03 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70ee8e69aa78933fce9ce6c3d810dee7282f82b7277216c5129e46719bc091d`  
		Last Modified: Wed, 01 Sep 2021 03:15:03 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; arm variant v6

```console
$ docker pull notary@sha256:94a6194b7f7b65743f0222dd458b930025c28a770911640c79fad7ca26034b52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7182693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75506eef87a7ee2f483c5172bef11d439f155faebc2b51e581f746c187e02e38`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 05:40:38 GMT
ENV TAG=v0.6.1
# Wed, 01 Sep 2021 05:40:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Wed, 01 Sep 2021 05:41:21 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 01 Sep 2021 05:41:22 GMT
EXPOSE 4444
# Wed, 01 Sep 2021 05:41:23 GMT
EXPOSE 7899
# Wed, 01 Sep 2021 05:41:23 GMT
WORKDIR /notary/signer
# Wed, 01 Sep 2021 05:41:47 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Wed, 01 Sep 2021 05:41:47 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Wed, 01 Sep 2021 05:41:48 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Wed, 01 Sep 2021 05:41:49 GMT
RUN adduser -D -H -g "" notary
# Wed, 01 Sep 2021 05:41:50 GMT
USER notary
# Wed, 01 Sep 2021 05:41:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 01 Sep 2021 05:41:51 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Sep 2021 05:41:51 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84200730013aecb1dcbb2f93f6f7b5c2077317205083389d1ab8544b6c1809`  
		Last Modified: Wed, 01 Sep 2021 05:42:37 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d1061ec4ca2d75dcb091b4aaf6ca4fcc558e626a50113ae6876a02841a3e6c`  
		Last Modified: Wed, 01 Sep 2021 05:42:39 GMT  
		Size: 4.6 MB (4556877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db861ba970aa473981dd5c166a69c29cae305e43fb9742de19c7723eac82079d`  
		Last Modified: Wed, 01 Sep 2021 05:42:37 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba3cdee7eedcaf8d17f5e5291b723564fb8ff012432b70654f56c5451a40e0c`  
		Last Modified: Wed, 01 Sep 2021 05:42:37 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d66f578ac7a54250a9c6b87880a389618b43fb59cd18f3432e5468d962f0daa`  
		Last Modified: Wed, 01 Sep 2021 05:42:37 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:6fefe152b56505b59cfd4e97cebbfd7514d1e8685dc9810c756f79fa6f697c9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7182203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ade0436dde6056ffa83df7107a2af83084291618c1e1d4749b943e2b42f0250`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 00:13:38 GMT
ENV TAG=v0.6.1
# Sat, 13 Nov 2021 00:13:39 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Sat, 13 Nov 2021 00:14:09 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 13 Nov 2021 00:14:10 GMT
EXPOSE 4444
# Sat, 13 Nov 2021 00:14:11 GMT
EXPOSE 7899
# Sat, 13 Nov 2021 00:14:12 GMT
WORKDIR /notary/signer
# Sat, 13 Nov 2021 00:14:25 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Sat, 13 Nov 2021 00:14:27 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Sat, 13 Nov 2021 00:14:28 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Sat, 13 Nov 2021 00:14:28 GMT
RUN adduser -D -H -g "" notary
# Sat, 13 Nov 2021 00:14:29 GMT
USER notary
# Sat, 13 Nov 2021 00:14:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 13 Nov 2021 00:14:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 13 Nov 2021 00:14:32 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73c68a67445be4c877ecd7986db3857403f81b0cbe4b276300309b7c953d1bd`  
		Last Modified: Sat, 13 Nov 2021 00:15:04 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8ad0750bbda32429d887e25820911a19ef9034a569020bae511ba5425fd7f9`  
		Last Modified: Sat, 13 Nov 2021 00:15:05 GMT  
		Size: 4.5 MB (4460538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb140f321bcfa502e9644d0bbdefa46dbb3c613c4d15846be69394dbf49bdef`  
		Last Modified: Sat, 13 Nov 2021 00:15:04 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c4c1544d842ec5effc5fa006170c896ffc224754c701b25c089d89caa2bfae`  
		Last Modified: Sat, 13 Nov 2021 00:15:04 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97f073fab2f7a16c2b02d0032b3a3b108086dca2d0b8f1c9beb95630caa5888`  
		Last Modified: Sat, 13 Nov 2021 00:15:05 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; 386

```console
$ docker pull notary@sha256:f1c03eb045dc97ea17197a0c1cb777c201234ba78a0b54b4df42209369d0df3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4fee68e4fe3c14a89ac9b77ae2d4512de54f2e5123bfc1a0feed63bdbe2855`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 23:39:54 GMT
ENV TAG=v0.6.1
# Tue, 31 Aug 2021 23:39:54 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Tue, 31 Aug 2021 23:40:21 GMT
ENV INSTALLDIR=/notary/signer
# Tue, 31 Aug 2021 23:40:22 GMT
EXPOSE 4444
# Tue, 31 Aug 2021 23:40:22 GMT
EXPOSE 7899
# Tue, 31 Aug 2021 23:40:22 GMT
WORKDIR /notary/signer
# Tue, 31 Aug 2021 23:40:42 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Tue, 31 Aug 2021 23:40:42 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Tue, 31 Aug 2021 23:40:43 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Tue, 31 Aug 2021 23:40:43 GMT
RUN adduser -D -H -g "" notary
# Tue, 31 Aug 2021 23:40:44 GMT
USER notary
# Tue, 31 Aug 2021 23:40:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 31 Aug 2021 23:40:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 31 Aug 2021 23:40:44 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081c6e54401247246c2ca4756cf927b72d3e7fe0475427eadf3336126ce70fe8`  
		Last Modified: Tue, 31 Aug 2021 23:41:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab536c085215585c4faa4355b6337e17697a20c900ae81f252fb5ffc08f33c31`  
		Last Modified: Tue, 31 Aug 2021 23:41:19 GMT  
		Size: 4.6 MB (4618168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3590fe1d8ea9b1aa7ce1509eff698d62dde081fc7e7747ce9d7997aed7af424f`  
		Last Modified: Tue, 31 Aug 2021 23:41:18 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f255fd7b742ec8e3a6ffbb7edc13de9a72bae61b6944b8d6a34d17aedf9f6451`  
		Last Modified: Tue, 31 Aug 2021 23:41:18 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b07363a7b86ee845044145d80b1f3c112a0316d572fd6ec35d130a4a7b38e5`  
		Last Modified: Tue, 31 Aug 2021 23:41:19 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; ppc64le

```console
$ docker pull notary@sha256:4bdeca529937e2850a303695eba03e4f9ab2c31628723f9029b741b4673a107d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7158965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76f7a1a7f6c6fd115cc253ddbb2c90a97051427efa82730d437d78661e38192`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Wed, 01 Sep 2021 02:42:40 GMT
ADD file:07a51f1a2f818bd1c1651832ce63cb1e0046a57994724cda6a20ff1a2a685295 in / 
# Wed, 01 Sep 2021 02:42:41 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 11:31:28 GMT
ENV TAG=v0.6.1
# Wed, 01 Sep 2021 11:31:32 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Wed, 01 Sep 2021 11:32:39 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 01 Sep 2021 11:32:41 GMT
EXPOSE 4444
# Wed, 01 Sep 2021 11:32:44 GMT
EXPOSE 7899
# Wed, 01 Sep 2021 11:32:46 GMT
WORKDIR /notary/signer
# Wed, 01 Sep 2021 11:33:14 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Wed, 01 Sep 2021 11:33:15 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Wed, 01 Sep 2021 11:33:16 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Wed, 01 Sep 2021 11:33:22 GMT
RUN adduser -D -H -g "" notary
# Wed, 01 Sep 2021 11:33:25 GMT
USER notary
# Wed, 01 Sep 2021 11:33:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 01 Sep 2021 11:33:29 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Sep 2021 11:33:34 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:39d9bf63205258fe1d085fd596101e6fc46ff796cda8d3ba2983e166a25b74db`  
		Last Modified: Wed, 01 Sep 2021 02:43:53 GMT  
		Size: 2.8 MB (2814813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a2eff0e92e1ad53c9428e166d4364b007ea8dc3f120a46c44e66b1a9793285`  
		Last Modified: Wed, 01 Sep 2021 11:34:03 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62201ab14baff5eca6c77fe9987be6337c33a61be5459a19d3f82519bce46e68`  
		Last Modified: Wed, 01 Sep 2021 11:34:04 GMT  
		Size: 4.3 MB (4342093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d50f16d86cb7eae39bdab52b4419b44fda4c9c49078615634783e6309b8b6b`  
		Last Modified: Wed, 01 Sep 2021 11:34:03 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4c51e955773f2c1779e4e3c9e46078b1dc534f548fd509bafc5104b40737d9`  
		Last Modified: Wed, 01 Sep 2021 11:34:03 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25c98aa2bbaf8a780b35a62035f88c8ec612bf27e2c2136aa7be3a037df0528`  
		Last Modified: Wed, 01 Sep 2021 11:34:03 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.6.1-2` - linux; s390x

```console
$ docker pull notary@sha256:e6f6947d924b122dcb51690332d26424ceda05418e10f3b803a30a275d9b197f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7327235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3761e07526b52455b9cffc179fcf7106a641d7c1384b87cf09ee1c53f329119b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--help"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:44 GMT
ADD file:637f327c9b07758709ef7dbc42eb472c888d221acde89b1c3775553864334d5c in / 
# Fri, 12 Nov 2021 16:41:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:28:05 GMT
ENV TAG=v0.6.1
# Fri, 12 Nov 2021 19:28:05 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 12 Nov 2021 19:28:25 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 12 Nov 2021 19:28:25 GMT
EXPOSE 4444
# Fri, 12 Nov 2021 19:28:25 GMT
EXPOSE 7899
# Fri, 12 Nov 2021 19:28:25 GMT
WORKDIR /notary/signer
# Fri, 12 Nov 2021 19:28:35 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --help
# Fri, 12 Nov 2021 19:28:35 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 12 Nov 2021 19:28:36 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 12 Nov 2021 19:28:36 GMT
RUN adduser -D -H -g "" notary
# Fri, 12 Nov 2021 19:28:36 GMT
USER notary
# Fri, 12 Nov 2021 19:28:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 12 Nov 2021 19:28:36 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 12 Nov 2021 19:28:37 GMT
CMD ["notary-signer" "--help"]
```

-	Layers:
	-	`sha256:b872f056719bde6e6722091afb2a3376d720c69c142b91ac352050080dd79615`  
		Last Modified: Fri, 12 Nov 2021 16:42:54 GMT  
		Size: 2.6 MB (2611155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79567eeea74d41a59f001d5d151c4d04e765141889993d03e61de5e279c4c28c`  
		Last Modified: Fri, 12 Nov 2021 19:29:02 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dec31adf090e3e1c49c2282770f8703464975f40a2f69c7bcb72afc984f794`  
		Last Modified: Fri, 12 Nov 2021 19:29:03 GMT  
		Size: 4.7 MB (4714020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9421ea8709971dd61a13b97364009d352ea9cd2e8152f451f7d89650e3a1cf`  
		Last Modified: Fri, 12 Nov 2021 19:29:02 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ae6189c031409f5ebd4c08d9285eeced61c89b885d30ce723fa22c3a32d5f0`  
		Last Modified: Fri, 12 Nov 2021 19:29:02 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83bcf41fcfe8e0486ace913fa3b816037305b13958b02a0a83f1149e3bb7795`  
		Last Modified: Fri, 12 Nov 2021 19:29:02 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
