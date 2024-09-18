## `unit:go1`

```console
$ docker pull unit@sha256:52b188628832f79218c7cf8f011aeb4e2d1d463c07822ff29b07d29b7bb167a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:go1` - linux; amd64

```console
$ docker pull unit@sha256:6b358acd55388ca598aa78360fdd7e18ce189f097a5f28a017af5cbaa2c728c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334201357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0814f4cf229d7e44107f302139597662b6c136ba56a7c9b7581f646cf11d38`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 16:50:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Sep 2024 16:50:05 GMT
ENV GOPATH=/go
# Thu, 05 Sep 2024 16:50:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:50:05 GMT
COPY /target/ / # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Sep 2024 16:50:05 GMT
WORKDIR /go
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.title=Unit (go1.23)
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.version=1.33.0
# Tue, 17 Sep 2024 21:10:58 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.33.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure go --go-path=$GOPATH     && make -j $NCPU go-install-src libunit-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
STOPSIGNAL SIGTERM
# Tue, 17 Sep 2024 21:10:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Sep 2024 21:10:58 GMT
EXPOSE map[80/tcp:{}]
# Tue, 17 Sep 2024 21:10:58 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627963ea2c8d5e7f344e68dce05f9013c8104d06e6e0d414fcbb261cc0b6bbde`  
		Last Modified: Thu, 05 Sep 2024 22:03:10 GMT  
		Size: 92.3 MB (92260964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bff916ab0c126c9d943f0c481a905f402e00f206a89248f257ef90beaabbd8`  
		Last Modified: Thu, 05 Sep 2024 22:02:55 GMT  
		Size: 74.0 MB (74003284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1ad979d054ab0c2824c196b59074e31870426326f3e359ca9ee12d0fcb999`  
		Last Modified: Thu, 05 Sep 2024 22:03:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db67a7fca1811f19a21d1afbce7aaacc5431d1819b9ca7e7066bdfbc0d56f804`  
		Last Modified: Wed, 18 Sep 2024 00:01:15 GMT  
		Size: 30.2 MB (30176355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb730621e056b10edd7b76d80b4d49e3ee50855b010954ac75ad38d4fe1a970`  
		Last Modified: Wed, 18 Sep 2024 00:01:15 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dda14ad7747273c0054f3baf99878362b55e7fb804095ce5159ffe8acf6706b`  
		Last Modified: Wed, 18 Sep 2024 00:01:15 GMT  
		Size: 1.5 KB (1457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1` - unknown; unknown

```console
$ docker pull unit@sha256:a78046bc888882c1dc2ad8eba046a2224400e20aa2e903b7140b60bfa1bebc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bb33c9d2527d1b27ff74250d7ba7902cc307a322040af33cae37e898884a64`

```dockerfile
```

-	Layers:
	-	`sha256:5baf715f9eb85143889f8f9e8378c5d33706df690f670ccb2a051805387e12a6`  
		Last Modified: Wed, 18 Sep 2024 00:01:15 GMT  
		Size: 24.7 KB (24728 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:go1` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:faab56496715a86570bc5071d69b007efc69c1124ab791f7901c6730a956ba9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (279019991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32060354498c70be500564b5a0178b4b68bad73f95b52c01c895c45ca0c02e4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 26 Mar 2024 13:57:15 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
ENV GOLANG_VERSION=1.22.7
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
LABEL org.opencontainers.image.title=Unit (go1.22)
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
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6321cc2f68c817a276b509dea0b6abbcca8b3bfcab0c79b3d01cada5b1b80b5`  
		Last Modified: Thu, 05 Sep 2024 12:05:56 GMT  
		Size: 81.4 MB (81366514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e22f72b836bf3633103ff91c50db9b36ba220b58376e9f5fc91490e0e05fd33`  
		Last Modified: Thu, 05 Sep 2024 22:11:49 GMT  
		Size: 66.3 MB (66288032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a0bf12b13f857020abec85cd5e27932e93295e5e62fffc3270163caea3e1a7`  
		Last Modified: Thu, 05 Sep 2024 22:12:23 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850209d8b64f6234a87877d9a9d0b99cb98123aebe78e49b9ff7d759d8e99dcd`  
		Last Modified: Thu, 05 Sep 2024 23:31:34 GMT  
		Size: 7.0 MB (7047791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b528ee81e3bda5c6c414ed259202150a4be23a0f1e9e6a4171a9b38a1530a`  
		Last Modified: Thu, 05 Sep 2024 23:31:33 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163dc049fb9dfb9e5258833258e3aaf3a6b8d026a76ef21bdbc492beb1bf1932`  
		Last Modified: Thu, 05 Sep 2024 23:31:33 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:go1` - unknown; unknown

```console
$ docker pull unit@sha256:811c65ef9c745cbd89f42efee3427915dc7646aef073276219f308f32b0fbbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8561812cdf96871ba9bb724d9b4ca656da4930ab662f478e94981464aaf6c6c9`

```dockerfile
```

-	Layers:
	-	`sha256:eacdf24638133c72803bf9c32097d39834b4c82175e9f858e9bfdd423964334c`  
		Last Modified: Thu, 05 Sep 2024 23:31:33 GMT  
		Size: 25.2 KB (25182 bytes)  
		MIME: application/vnd.in-toto+json
