## `unit:perl`

```console
$ docker pull unit@sha256:d8d4516ebc136e03f15760c6545289b4174ef2bfe7de2e930505903e2ef776e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:perl` - linux; amd64

```console
$ docker pull unit@sha256:f62fa22aacd829aa57f9a2a12659086e4da7d03119aece54fde42e163a7c6301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344986913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e08e044f6fce29ec5a1317a6eca9b54535f5e330b5a33ac52af278beebbcf82`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Oct 2023 10:47:22 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["bash"]
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /usr/src/perl
# Thu, 19 Oct 2023 10:47:22 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /usr/src/app
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["perl5.38.2" "-de0"]
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.title=Unit (perl5.38)
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
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log # buildkit
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
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c200adf1811433c67c208599f5f71578e5237cfd9be60d64045c78282562b77`  
		Last Modified: Wed, 31 Jan 2024 23:34:15 GMT  
		Size: 196.9 MB (196898029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4d060f98304ba96ebb36700fdde0ebadfc3304af0922b15271b94c43522c2d`  
		Last Modified: Thu, 01 Feb 2024 00:04:29 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca103ba9dad1f215c40eefc07ef81a2f9b42eedeaef13e293e999ecabbdaba3`  
		Last Modified: Thu, 01 Feb 2024 00:04:29 GMT  
		Size: 15.6 MB (15641851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1fc9d9c38dc63b7442cb0789f1c02433a475e6bc53b9b52c6defa44d5601b1`  
		Last Modified: Thu, 01 Feb 2024 00:04:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af23f3813d211a27edb11b849253ba2372ee539fc02c8b1af00e381c39741c63`  
		Last Modified: Thu, 01 Feb 2024 00:59:33 GMT  
		Size: 7.0 MB (7020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710d5f6fed3dc43e0d7334698f728f48d580b1c3590cf050fc9e8d092deb02fe`  
		Last Modified: Thu, 01 Feb 2024 00:59:33 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb831a429a209ecd4919fcceda1e76954e038d1a17feb1a22ec993de22e2ae`  
		Last Modified: Thu, 01 Feb 2024 00:59:33 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:perl` - unknown; unknown

```console
$ docker pull unit@sha256:a3d8b14824c47b8d9364e2d22069ac5ea487fd61108900bd30e4fb3d6b6eefb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12978079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b73466def953cf0697fbca513afc3cbfe2caf2584cc6756f08d55fdba04e7d`

```dockerfile
```

-	Layers:
	-	`sha256:deef623301a55f5a32710084175d041f679200ec94a9a20e4b7853c8e7102ceb`  
		Last Modified: Thu, 01 Feb 2024 00:59:33 GMT  
		Size: 13.0 MB (12952312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa744f0a644b5651db1a7d57fe126ad979b47d15ce8d8d6102fcb3ce55aefd93`  
		Last Modified: Thu, 01 Feb 2024 00:59:33 GMT  
		Size: 25.8 KB (25767 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:perl` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:e2bf63dae9ac59caed196600005a6eb9630feb03c92b053762bcf1b0ceed7988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336467540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfbba8981155fdb834bdb7d4d36f65e45030760da9c8e750c02c8a529cf1cb5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Oct 2023 10:47:22 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["bash"]
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /usr/src/perl
# Thu, 19 Oct 2023 10:47:22 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /usr/src/app
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["perl5.38.2" "-de0"]
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.title=Unit (perl5.38)
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
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log # buildkit
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
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646806c0e22a1bfa60edc42bcc6170f0ccd02431e5871b9cec1962c34d610232`  
		Last Modified: Wed, 17 Jan 2024 02:59:33 GMT  
		Size: 54.7 MB (54699826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd94a910a6d687fc7621b3af4657f78c1208a07fa463f30e2ed002dadb7e021`  
		Last Modified: Wed, 17 Jan 2024 03:00:10 GMT  
		Size: 189.8 MB (189834377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15170ebec76671bc76b4807a56bbb909e2b2128733f5922d8a7d27d0477d070`  
		Last Modified: Thu, 18 Jan 2024 03:50:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fe2ed51d707e4f80cf3838951a02d628600cb7450e206634794c9a0088ce46`  
		Last Modified: Thu, 18 Jan 2024 03:50:35 GMT  
		Size: 15.6 MB (15572787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b30ac74e2c4aabe9d95705cb54b083d9d4cd74670f8390aaf077575e765dac0`  
		Last Modified: Thu, 18 Jan 2024 03:50:34 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bf52ea1339ea820573a1c7f5be470193283e5bb14365468e8b3ba0ff49323b`  
		Last Modified: Thu, 18 Jan 2024 10:48:11 GMT  
		Size: 6.9 MB (6899004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d6bd96f4a5ed7658e3b6539a90acd5c4943a969a555958fe3a6c7e1942bb19`  
		Last Modified: Thu, 18 Jan 2024 10:48:10 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776b43627a5baaeabcb0b7a9f101d42b142bbd93b01241017ca9f6a0fa03687`  
		Last Modified: Thu, 18 Jan 2024 10:48:11 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:perl` - unknown; unknown

```console
$ docker pull unit@sha256:78119e0ef6eb41f571689f8fda02493ef22b763f981d6534ba2235d45f744f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12980576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5535a62e2002c9426357e5c63fb54b60195751b883ba77c7d6c756e1b271551`

```dockerfile
```

-	Layers:
	-	`sha256:c74aaa101f47c067b8f8657a81251088137bf028a47f8ae344c0f12f4f01f25d`  
		Last Modified: Thu, 18 Jan 2024 10:48:11 GMT  
		Size: 13.0 MB (12954672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7a1d21ac1dc34016d5db5c010c18bb6f418777dd2fdd27af987660bcc08b7f`  
		Last Modified: Thu, 18 Jan 2024 10:48:10 GMT  
		Size: 25.9 KB (25904 bytes)  
		MIME: application/vnd.in-toto+json
