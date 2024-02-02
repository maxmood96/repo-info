## `unit:minimal`

```console
$ docker pull unit@sha256:23d83ef1f4958a34b9688f8d9932aae5c4453edf536a50dadecc8d4796f7152a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:minimal` - linux; amd64

```console
$ docker pull unit@sha256:057fd5f5d0c1989444b383bcd78dc58b464110d1f5bdf32ec1f460ec8df68c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40261846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f68082b8b590fb07680aba0e95389f5f0a9a6c9f0869e3767e730910ab907df`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Oct 2023 10:47:22 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["bash"]
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.title=Unit (minimal)
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.version=1.31.1
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure      && make -j $NCPU version     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure      && make -j $NCPU version     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
STOPSIGNAL SIGTERM
# Thu, 19 Oct 2023 10:47:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Oct 2023 10:47:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1518ac400fabc3037e27a4ffca2105b1698a7693df7222d8395de1af1d59a8`  
		Last Modified: Thu, 01 Feb 2024 00:09:37 GMT  
		Size: 8.8 MB (8841304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc48fee51e78b456fddd2f50ef6b3a20e2fe2754638b8af742b11c5610b43aa5`  
		Last Modified: Thu, 01 Feb 2024 00:09:37 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4846bf34d0de5de1a8e28471b7daada4a8e5681756d81bec4553a6c3c89caf66`  
		Last Modified: Thu, 01 Feb 2024 00:09:37 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:minimal` - unknown; unknown

```console
$ docker pull unit@sha256:9e80a1bcd73c36f559625c430bb8e0b7689e57b6fc71918e3a7abec880475a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2de219ccac0994b08660b0404f86f76a4fe5ac913f054a802400fa95a83a0e`

```dockerfile
```

-	Layers:
	-	`sha256:c43482c5460f1ac09f943c66886193f9eb30c2811cbe791a2ec87f3d6a126269`  
		Last Modified: Thu, 01 Feb 2024 00:09:37 GMT  
		Size: 2.2 MB (2230058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1815107ea47744ccf84df2bf08421da102b46425146d0063da73f13c0f5e37`  
		Last Modified: Thu, 01 Feb 2024 00:09:37 GMT  
		Size: 20.5 KB (20536 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:minimal` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:a026d67018108f099ee63760a1dafc3c29a4d6c1074541410275ac9afb787a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38769637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a256807d101b3f92b516263990b24254d53895d6efc18aae6b057367218d4d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Oct 2023 10:47:22 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["bash"]
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.title=Unit (minimal)
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.version=1.31.1
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure      && make -j $NCPU version     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure      && make -j $NCPU version     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
STOPSIGNAL SIGTERM
# Thu, 19 Oct 2023 10:47:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Oct 2023 10:47:22 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0d5a53b374b2ec45d93c965d2871c5575c594dbfbe55130ce525721a85a5f`  
		Last Modified: Thu, 01 Feb 2024 21:42:03 GMT  
		Size: 8.7 MB (8702582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a425e720b289dd4a2b7155a358215aa6d56f208079bec852b7d112c7c05b3238`  
		Last Modified: Thu, 01 Feb 2024 21:42:02 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee104c49ff96fd8d2a38a9a503f3dd88aa7b0ed1ea43fd284976525aae0b91e4`  
		Last Modified: Thu, 01 Feb 2024 21:42:02 GMT  
		Size: 1.5 KB (1459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:minimal` - unknown; unknown

```console
$ docker pull unit@sha256:7baf4df58533637c3b8d84975ec94da6849b9265695531f09d02bb43e725f845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473e5efa44c6dbc46c48755d09b4ec0d6ffdd708673ae8384989204526b1e864`

```dockerfile
```

-	Layers:
	-	`sha256:0518f25aaba11e6964530ed54f1eafe4e26334a5a4f70fa398c9fbc8165262ab`  
		Last Modified: Thu, 01 Feb 2024 21:42:03 GMT  
		Size: 2.2 MB (2230381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:040e64ae75e7d51ab715ef7073d71642e01e1d4f0e70e81eea1d2018c87784c1`  
		Last Modified: Thu, 01 Feb 2024 21:42:03 GMT  
		Size: 20.4 KB (20377 bytes)  
		MIME: application/vnd.in-toto+json
