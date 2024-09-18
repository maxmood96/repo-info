## `unit:latest`

```console
$ docker pull unit@sha256:c0ce086ac605454510abc8fa571e604e79d6355c1bf88ea9908dc42e35795876
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:latest` - linux; amd64

```console
$ docker pull unit@sha256:c1cd3071f76b2f152e53c004e2170364e0b1586b9ea8ff16f2e7cf768698b446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41245110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f6fdeb043eaa6328587d8bdde38bd8c3e0ea70f6d4b9c34467a6373cb29c73`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.title=Unit (minimal)
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
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.33.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure      && make -j $NCPU version     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure      && make -j $NCPU version     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9736afedb45d98f3e9df43a68a20b20efb3834a11604b695647ae9f680a232b`  
		Last Modified: Wed, 18 Sep 2024 00:01:29 GMT  
		Size: 12.1 MB (12115907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6d0175ed798c04b5509180f704385ae915a4de1e6e4dd6157c5830cf5fd143`  
		Last Modified: Wed, 18 Sep 2024 00:01:29 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5886e38afd0df3e2280112226c01cf337d5e5fc4c24b27447a2388e85d5079`  
		Last Modified: Wed, 18 Sep 2024 00:01:29 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:latest` - unknown; unknown

```console
$ docker pull unit@sha256:14b8b6ba0e534179d65d65defdef6c7314c48628cfce780af6c98bcb51bc5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdae43ddf5e5171bac3291280e72cb7c519e306be79348382baabf2d02e12ce5`

```dockerfile
```

-	Layers:
	-	`sha256:196d209f8cf4bdf4458bda801374dca7487069a496bf7b4a31e54e2df6eaeb90`  
		Last Modified: Wed, 18 Sep 2024 00:01:29 GMT  
		Size: 20.2 KB (20227 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:latest` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:bdaef5bbad6248db1673a08145ba26b1e40c6c1e38b503c9d83d8121c910a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38792493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485aab7059bad7d0b23d0a6e39fd69c76f23fbf48dc3cfbe16e7e3038b9f0eec`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 26 Mar 2024 13:57:15 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.title=Unit (minimal)
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
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.1-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure      && make -j $NCPU version     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure      && make -j $NCPU version     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
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
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de49afd056b094681839378fa3c8fc5385f888811bf3573ea98a0b0e50313da`  
		Last Modified: Thu, 05 Sep 2024 20:40:11 GMT  
		Size: 8.7 MB (8715412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ecb44d780aeda62414cc6df81f61f111cfa2635d71785890a47d8806117f63`  
		Last Modified: Thu, 05 Sep 2024 20:40:10 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817ad066d7c5a7fc40bc5d051e8bd7158b5c14fb1bae0ad2305f4786a6333b4a`  
		Last Modified: Thu, 05 Sep 2024 20:40:10 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:latest` - unknown; unknown

```console
$ docker pull unit@sha256:2e878f02d4d39c56631189de14470dd0168fba7847a250ce361ca07af8bb4452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 KB (20521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3e2d824fde246eea01d86a272678719fe5f8a3041bc4d65d4bc55c4155b5d4`

```dockerfile
```

-	Layers:
	-	`sha256:6082c27d4117a07697dcd6c861f35828be1fb86c8753620bffc5f4b5d2b382ab`  
		Last Modified: Thu, 05 Sep 2024 20:40:10 GMT  
		Size: 20.5 KB (20521 bytes)  
		MIME: application/vnd.in-toto+json
