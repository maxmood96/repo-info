## `unit:go1.22`

```console
$ docker pull unit@sha256:1b6f3e9ad65ea0127941ecaf7c543b5013d0dbf0f4336f3b3c4536f912e89b0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:go1.22` - linux; amd64

```console
$ docker pull unit@sha256:0062b19a3ead3447d25a81335cace4cba91d2dac699bcf7ccfadac5fffaec0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288094886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5e70ec4dea465e743e216b509f2d43676265949b9c1c3143a58b0f7e4de7dd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 27 Feb 2024 15:15:42 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 27 Feb 2024 15:15:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 27 Feb 2024 15:15:42 GMT
ENV GOPATH=/go
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 15:15:42 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
WORKDIR /go
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.title=Unit (go1.22)
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.version=1.32.0
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
STOPSIGNAL SIGTERM
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 15:15:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd73e3517bc8fa1e9863e448b6ad3b54c5482345b15ce6ad28439cf1f017523`  
		Last Modified: Tue, 12 Mar 2024 16:05:11 GMT  
		Size: 86.1 MB (86114119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8b7674f6c3067682860f7a62b4b9d5fa441b5daebea480559d4e62557637a5`  
		Last Modified: Tue, 12 Mar 2024 16:05:11 GMT  
		Size: 69.3 MB (69347675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd4913374228f0d58e0cdb9081980604d1f5fc688e3df2a139dd83092bfab2`  
		Last Modified: Tue, 12 Mar 2024 16:05:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567900d7515538ab71191fdbe563c5e404061d0aa0b60c4e3034e8dc448c313d`  
		Last Modified: Tue, 12 Mar 2024 17:10:15 GMT  
		Size: 7.2 MB (7193233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495a13370a517bf1dc5654d44ada488aca3df035f2176f02d26581bc112d0da3`  
		Last Modified: Tue, 12 Mar 2024 17:10:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d794271dc382e4b7749923cbf8517879c179229133f643a5d10a28e9b05f654`  
		Last Modified: Tue, 12 Mar 2024 17:10:15 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.22` - unknown; unknown

```console
$ docker pull unit@sha256:3d0e025f72d4c9dcd5d35a6c2a75851bd4193156e65d6087ce5fce7f22211e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10368571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072e47607e1e0c07d3b93c64e4b7649acc4f716c6f18b9b01829318661acc81b`

```dockerfile
```

-	Layers:
	-	`sha256:5d456da4c573e8fee04ea61b308d3c8ae0aeb10caa41c172e883995a9bb07f94`  
		Last Modified: Tue, 12 Mar 2024 17:10:15 GMT  
		Size: 10.3 MB (10342562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ac03863b56fa07f42cbf20a42c176fc96718bd08a46e66e6b3e64ffa673c716`  
		Last Modified: Tue, 12 Mar 2024 17:10:15 GMT  
		Size: 26.0 KB (26009 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:go1.22` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:782177af7f1269b4b5375755868c789c150082559a796daea43f206bda8a0d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (278990386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d9f4aa704907309179238443c34657b2cb4091170cc862da3442260e2964c6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 27 Feb 2024 15:15:42 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 27 Feb 2024 15:15:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 27 Feb 2024 15:15:42 GMT
ENV GOPATH=/go
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Feb 2024 15:15:42 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
WORKDIR /go
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.title=Unit (go1.22)
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.version=1.32.0
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
STOPSIGNAL SIGTERM
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 15:15:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1a55d94f7d8a528deb7e730df7ff17f400c24a7a40074da413de7a5e2b8e90`  
		Last Modified: Tue, 12 Mar 2024 10:19:19 GMT  
		Size: 81.5 MB (81527400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475213ba525cec461dc49d18bfb1b613491f445e29944188cd2e2776e8727c80`  
		Last Modified: Tue, 12 Mar 2024 10:19:20 GMT  
		Size: 66.2 MB (66246664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4d58e72a17780bf23c1b9b29a2c545fc3903f126227e696722f479b1ec2a7a`  
		Last Modified: Tue, 12 Mar 2024 10:19:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e939fc0972143d1626f94dbf8b202eda584fc14e33f22c55cc979552302e3b`  
		Last Modified: Wed, 13 Mar 2024 06:14:39 GMT  
		Size: 7.0 MB (7047790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9942f4741220dffcda087282267c47708cf98c948f170682c58bda249d858f6b`  
		Last Modified: Wed, 13 Mar 2024 06:14:39 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bb8568ac6720f17e911baeba266c62c2c8c4d78c312ca50a617cddbb23e519`  
		Last Modified: Wed, 13 Mar 2024 06:14:40 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.22` - unknown; unknown

```console
$ docker pull unit@sha256:bc07c1cf2650d791eab3643c3c6114e71d51ba1c6f1b779d02dbd7b29f1d9d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10370384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f5ca98a4d64b41a40335cabd8d99f76fc47d1d1b70a0c0d0aaa550b379a1a9`

```dockerfile
```

-	Layers:
	-	`sha256:d6a68044ad0a9b10d90f13970b11e20aea5f8b962e474d3846beb15a39f27b37`  
		Last Modified: Wed, 13 Mar 2024 06:14:38 GMT  
		Size: 10.3 MB (10344366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dc99bde3be9902e603a6a68436d0ceb918ca74dce02d765f9b9b0f2f748bf8`  
		Last Modified: Wed, 13 Mar 2024 06:14:38 GMT  
		Size: 26.0 KB (26018 bytes)  
		MIME: application/vnd.in-toto+json
