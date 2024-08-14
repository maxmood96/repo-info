## `unit:go1.21`

```console
$ docker pull unit@sha256:313c1aa4f3643c9096b5e3b1aab2370766660d2a849a41a45bb6e7ee0cdbcb8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:go1.21` - linux; amd64

```console
$ docker pull unit@sha256:dee6f034e4f541c88f2e7372e9bb32ac418fbfe2850a81cdf3ac9d774716aa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285602269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e64daf92b7b3aad4fbdcb34b3cf45af9201dc537beba87934ad48288b3c91b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 26 Mar 2024 13:57:15 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GOLANG_VERSION=1.21.13
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GOPATH=/go
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:57:15 GMT
COPY /target/ / # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
WORKDIR /go
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.title=Unit (go1.21)
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.version=1.32.1
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.1-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
STOPSIGNAL SIGTERM
# Tue, 26 Mar 2024 13:57:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:57:15 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665b6f4bd774e6a4c9738f0532ee622cf3bc07679e5a4449ba05c1f395e4f75`  
		Last Modified: Tue, 13 Aug 2024 00:51:07 GMT  
		Size: 54.6 MB (54588802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a818415ef02f582c87c5f378d9303dc6e2d2129563a28669c6dbfb6feba43b8f`  
		Last Modified: Tue, 13 Aug 2024 02:05:32 GMT  
		Size: 86.0 MB (85957696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bf7053e2d96c2c7f4637ad7580bd64345b3c9fabb163e1fdb8894aea8a9af0`  
		Last Modified: Tue, 06 Aug 2024 22:56:15 GMT  
		Size: 67.0 MB (67010746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc3eeb8d0994f3f39f914c543f5a0a2afc353306a1322a4a3193ebb99622f95`  
		Last Modified: Tue, 13 Aug 2024 02:05:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127d37bbec61061d9a2f316070cc098560117bc12980c4b6cfcb7c0b851108d7`  
		Last Modified: Tue, 13 Aug 2024 03:02:50 GMT  
		Size: 7.2 MB (7193220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13032068aa81eb20550b656864cfcfab4ba8bfe0de19d4bbb1acaf9aa7f5becb`  
		Last Modified: Tue, 13 Aug 2024 03:02:50 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a2cb011a1453f6ecba567028c48a3f9cf1c900a68ca57a841f0e64bf90e420`  
		Last Modified: Tue, 13 Aug 2024 03:02:50 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.21` - unknown; unknown

```console
$ docker pull unit@sha256:66c077cce1b34affdd1c74c1a9372b879563c682334910cfdbdac057a2f05eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 KB (24152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e840bf428e2455eada4855387cf17c6cb95006001acbdd2ade1aebd5334156`

```dockerfile
```

-	Layers:
	-	`sha256:57be235728cd9b83133f9e4ca40c1ed389d8ddeb82d8ee2d8f01603cea874e49`  
		Last Modified: Tue, 13 Aug 2024 03:02:50 GMT  
		Size: 24.2 KB (24152 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:go1.21` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:453a54d006886b676ecf3c6823846f5a437345a42a27e90f8faefaa4300ecc68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276699652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23afc26d093c719d31e1dd2e350cd11fef94896ef504126660ef9adb0ab95ce8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 26 Mar 2024 13:57:15 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GOLANG_VERSION=1.21.13
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GOPATH=/go
# Tue, 26 Mar 2024 13:57:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:57:15 GMT
COPY /target/ / # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
WORKDIR /go
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.title=Unit (go1.21)
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.version=1.32.1
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.1-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
STOPSIGNAL SIGTERM
# Tue, 26 Mar 2024 13:57:15 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 13:57:15 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5265d6983e8ed11fd8dc48e17209d3479015214ac92f89f4ac51b2e65060840`  
		Last Modified: Tue, 13 Aug 2024 01:10:33 GMT  
		Size: 54.7 MB (54694302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d185dc793c8db3008fdd70d76dd66a025410d301d6255f72364424d849ca8c57`  
		Last Modified: Tue, 13 Aug 2024 16:03:31 GMT  
		Size: 81.4 MB (81367325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6022646f09ee78a83ef4abd0f5af04071b6563cf16a18e00fb2dcfe63ca0a3`  
		Last Modified: Tue, 06 Aug 2024 22:58:56 GMT  
		Size: 64.1 MB (64107897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb51f7d4526a783f7edbeda955b148fed5032eaf485f44c0a974ba830379a6e9`  
		Last Modified: Tue, 13 Aug 2024 16:06:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfbafe20fef8aa8a211699819da432edd943deae1550d7f77461b73717c8167`  
		Last Modified: Tue, 13 Aug 2024 21:55:30 GMT  
		Size: 7.0 MB (7047825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1336692884927651a45f33a2b147f7e3a0b01b62784b30e51b491037cde95dd`  
		Last Modified: Tue, 13 Aug 2024 21:55:29 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124975e26a92156ea87fa3fbbcb9553311fa04c9d38f53eb0c9089d1c33b4fb`  
		Last Modified: Tue, 13 Aug 2024 21:55:29 GMT  
		Size: 1.5 KB (1457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.21` - unknown; unknown

```console
$ docker pull unit@sha256:c7cbd555c59ee6694e8edcb1d6b78ba456cf0174f7cd01e06679db140e9e3e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 KB (24313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049405dcb25b60dcc20f772580cd30c0c21c02e029a3af434b7e8d2e3d1c837f`

```dockerfile
```

-	Layers:
	-	`sha256:531b2e62a556b739373018f7ae8c65891b64f0dfe64029c9c287abbce3ebc874`  
		Last Modified: Tue, 13 Aug 2024 21:55:29 GMT  
		Size: 24.3 KB (24313 bytes)  
		MIME: application/vnd.in-toto+json
