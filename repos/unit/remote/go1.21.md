## `unit:go1.21`

```console
$ docker pull unit@sha256:91a0b5bb40b782b4b63bb58f35943c454e20f6dc1ae0c629a0948bddc8c26c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:go1.21` - linux; amd64

```console
$ docker pull unit@sha256:9efdcf275b8a4db50a224de5bae5ebf48699ea95aad1f7b22273f7a5a664f8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285757933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06a774ea4732e6e937d382df3320ea8b0d06af9cdc15b4831c89e9ea74bf061`
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
ENV GOLANG_VERSION=1.21.8
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
LABEL org.opencontainers.image.title=Unit (go1.21)
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
	-	`sha256:0635831cef590cc18d45a50a86211bcdbb7e2dc2aeac5a3d19671604e6b7e3d9`  
		Last Modified: Tue, 12 Mar 2024 16:05:58 GMT  
		Size: 67.0 MB (67010703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579c95fc9df09d4b635a801a036ce19e0793e293b61b4621bac859996c4bbd47`  
		Last Modified: Tue, 12 Mar 2024 16:05:48 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c23e38451710badd1a42db1733f335da433a68d067e7d9d52b208db944689ce`  
		Last Modified: Tue, 12 Mar 2024 17:10:08 GMT  
		Size: 7.2 MB (7193251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefbb92e8042abfc657f3b769352abbe3ed1006fba78f89101c1226db78e9536`  
		Last Modified: Tue, 12 Mar 2024 17:10:10 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19922867646a8a01af588ec2a08b063168babe44190e88d90877cbb4b1a6eba2`  
		Last Modified: Tue, 12 Mar 2024 17:10:09 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.21` - unknown; unknown

```console
$ docker pull unit@sha256:b25bb9cc5187ceca223132f76963dc0b914027b5d0a75ed28bdc9133e9779a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10367483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ff50531e282e6a8a930748b94fc0f22cb44659f73b1cd5ac111f044d6da7b9`

```dockerfile
```

-	Layers:
	-	`sha256:d1ee85a309e1a6750d61f20d42dbf257318b07a56d70a5c80856b2d1a7918f4d`  
		Last Modified: Tue, 12 Mar 2024 17:10:08 GMT  
		Size: 10.3 MB (10342048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9edae8e3c89972eb9d36f51453a1aceacda326a4d05e158cbd1add6d504903b9`  
		Last Modified: Tue, 12 Mar 2024 17:10:08 GMT  
		Size: 25.4 KB (25435 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:go1.21` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:14c6414c8865f10a596e53215a96f4a40b6267d77480825495b7ba92d970a231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276854964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5245ca14bf0a159f3f7e94e788523e4f24d38753a55cc186a849cf2b0ac60e`
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
ENV GOLANG_VERSION=1.21.8
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
LABEL org.opencontainers.image.title=Unit (go1.21)
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
	-	`sha256:d0cd7d9f24ddd2530514bc3389758941ba11ca443df9de002bad636f940a3834`  
		Last Modified: Tue, 12 Mar 2024 10:20:00 GMT  
		Size: 64.1 MB (64111192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52b884d3994af21e4155f276b96ca2da9b969818b590c3b88db0a04d9df017d`  
		Last Modified: Tue, 12 Mar 2024 10:19:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53f947fa6e5078d945ae0a2bc9e5e97c99f7c94d6b4c4b71183b09be33eface`  
		Last Modified: Wed, 13 Mar 2024 06:15:50 GMT  
		Size: 7.0 MB (7047842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa8bce5570caf272b394c430c97c5e373e5fba0604c808ee211d39827145e1`  
		Last Modified: Wed, 13 Mar 2024 06:15:49 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f06ed043e050bb57209d7517b85e4e2df59d4e278b01259efdab9ecc35331d6`  
		Last Modified: Wed, 13 Mar 2024 06:15:50 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1.21` - unknown; unknown

```console
$ docker pull unit@sha256:ac237a385cefe29cb2da26030e78c2b8be5594003e207949c03696f2fbae0e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10369289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ef8da62ecb33b3f888b9a8c9d11810092e9815c6440ddb47b790ffab62655`

```dockerfile
```

-	Layers:
	-	`sha256:4c3232694f6c553a68d9eef45af6725ff4f0f76a10974177af73b5329ddd0243`  
		Last Modified: Wed, 13 Mar 2024 06:15:50 GMT  
		Size: 10.3 MB (10343848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc7ae6023ae4e545bfe7307929a68a6008c8ae3a76761e1799bf39eb432e6ba`  
		Last Modified: Wed, 13 Mar 2024 06:15:49 GMT  
		Size: 25.4 KB (25441 bytes)  
		MIME: application/vnd.in-toto+json
