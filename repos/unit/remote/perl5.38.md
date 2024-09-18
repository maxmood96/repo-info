## `unit:perl5.38`

```console
$ docker pull unit@sha256:cf2e87d541436aa74ddfd81a2891698ef0d7a0a59e9df1d031a21dcbb29add9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:perl5.38` - linux; amd64

```console
$ docker pull unit@sha256:65891a57c7a14f76821f1ccc825fafba1b72efc730b3668c4e6608325774eb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.9 MB (394908385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a20b25997ae5d53b8eca24e156916c7a57436a82f02380290c36bfab68a62cc`
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
# Wed, 04 Sep 2024 22:56:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/perl
# Mon, 09 Sep 2024 15:38:32 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 09 Sep 2024 15:38:32 GMT
WORKDIR /usr/src/app
# Mon, 09 Sep 2024 15:38:32 GMT
CMD ["perl5.38.2" "-de0"]
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.title=Unit (perl5.38)
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
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.33.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
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
	-	`sha256:1c8ff076d818ad6b8557e03e10c83657cc716ab287c8380054ff91571c8cae81`  
		Last Modified: Wed, 04 Sep 2024 23:02:08 GMT  
		Size: 211.3 MB (211266623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0685da2111954e2f1d5d55b804141c96cd83da0cc8ff141305458c7462900e4a`  
		Last Modified: Mon, 09 Sep 2024 19:11:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20b6658196b04d243332360f1bac8ec2fb2738b3cc1706210cebbe31114fdbb`  
		Last Modified: Mon, 09 Sep 2024 19:11:52 GMT  
		Size: 15.5 MB (15525985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e6e9fd445216eab2066cf639c7395d99f4d574ea985d5e32b7bf37bf3a0bdf`  
		Last Modified: Mon, 09 Sep 2024 19:11:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d45f84e28d860d2f8fff391b1fc25fd68a17499142eb0e1f1335f9875e61d3`  
		Last Modified: Wed, 18 Sep 2024 00:01:28 GMT  
		Size: 30.4 MB (30354925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4097707e65e702af00649898749917b8366a24a31daf644401352b23dc84a419`  
		Last Modified: Wed, 18 Sep 2024 00:01:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73888fe5269b5b6680b1892a347040ee3a9234615f29f567c1764d1ca75e86d0`  
		Last Modified: Wed, 18 Sep 2024 00:01:27 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:perl5.38` - unknown; unknown

```console
$ docker pull unit@sha256:6c56bb0037c533f39ddcdf8ba8fc27b91add68500b14e7bd6b8b35ce13ee9cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c5129b15200bbb7aa2d7f53a6693e945d4833b845cddad9e03cb3cbd842b8`

```dockerfile
```

-	Layers:
	-	`sha256:5d25465ad2e0e89210ff1c7763329f37a43bc8a2234d937809466d15826e8e3d`  
		Last Modified: Wed, 18 Sep 2024 00:01:27 GMT  
		Size: 23.9 KB (23938 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:perl5.38` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:65d7f22b242e3f9478b21ef2840bf58a822a33148bcd0c763c7b50d16d59ff0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336649502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbffe5c68d869a2ae101f8690ef497290c687cc74cc1450ccc4d4e5a4e26158a`
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
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 26 Mar 2024 13:57:15 GMT
WORKDIR /usr/src/perl
# Tue, 26 Mar 2024 13:57:15 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 26 Mar 2024 13:57:15 GMT
WORKDIR /usr/src/app
# Tue, 26 Mar 2024 13:57:15 GMT
CMD ["perl5.38.2" "-de0"]
# Tue, 26 Mar 2024 13:57:15 GMT
LABEL org.opencontainers.image.title=Unit (perl5.38)
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
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.1-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
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
	-	`sha256:ea2c74c1774e448d6bb324968dd639df704566af4ae9461a86ec79cc6e8de709`  
		Last Modified: Wed, 04 Sep 2024 22:09:38 GMT  
		Size: 190.0 MB (189961799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256618b2d5df5bb1b308524d2e3fb7403a062f3473879488a421c732af283f90`  
		Last Modified: Mon, 09 Sep 2024 23:22:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f8eae32a543d77d8ed417a33feff785f5ac916b7be06eec6fa28565fff0528`  
		Last Modified: Tue, 10 Sep 2024 00:08:22 GMT  
		Size: 15.4 MB (15447144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b57c9e8d26205b134ab69b76bf30d58d74eef7ea89600298041d947f09a51e`  
		Last Modified: Tue, 10 Sep 2024 00:08:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71eae1b6877917f39ccd391d5dd48c6c3ee2912c09f79a60c9dbcb692a53dee5`  
		Last Modified: Tue, 10 Sep 2024 05:42:10 GMT  
		Size: 6.9 MB (6922798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6d788092a2923f9051aa0e04e8bd65aae172ff2d45c619eb82ac30a61d3d44`  
		Last Modified: Tue, 10 Sep 2024 05:42:09 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436445fa25a7e674a4efb1570edf538853ddb5f00bea88777d4eca9eda7da9e1`  
		Last Modified: Tue, 10 Sep 2024 05:42:09 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:perl5.38` - unknown; unknown

```console
$ docker pull unit@sha256:54554a95ed26329d96d110b904b26758a0eab34a3cdf92d9aa6d3012a2de20ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (24998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2475b2b1488f24eab0f3d2bc8b60fa6481f43d075e49c8ce6a24cfb5c7320081`

```dockerfile
```

-	Layers:
	-	`sha256:0b8a301ec0a0b0ce57226912faab5cf88a910b43b5b8ed32db793a0bde00cb46`  
		Last Modified: Tue, 10 Sep 2024 05:42:09 GMT  
		Size: 25.0 KB (24998 bytes)  
		MIME: application/vnd.in-toto+json
