## `unit:perl`

```console
$ docker pull unit@sha256:cd633371e658618f3685f1a64b40b9ae6a5413d96a4383fed4ff9db2ff0433f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `unit:perl` - linux; amd64

```console
$ docker pull unit@sha256:b162d7653d0bcf9a87900b1e2c789fe4d89cd8275bfae611b009ff82cdd8bec9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345184263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf5bd869f33b575b60af086ffae2262793a394388a149331b5b80d0d93e6c44`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:54:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:54:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:55:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 21:05:23 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 21 Nov 2023 21:05:24 GMT
WORKDIR /usr/src/perl
# Thu, 30 Nov 2023 19:32:35 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.2.tar.xz -o perl-5.38.2.tar.xz     && echo 'd91115e90b896520e83d4de6b52f8254ef2b70a8d545ffab33200ea9f1cf29e8 *perl-5.38.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.xz -C /usr/src/perl     && rm perl-5.38.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 30 Nov 2023 19:32:35 GMT
WORKDIR /usr/src/app
# Thu, 30 Nov 2023 19:32:36 GMT
CMD ["perl5.38.2" "-de0"]
# Thu, 30 Nov 2023 23:06:39 GMT
LABEL org.opencontainers.image.title=Unit (perl5.38)
# Thu, 30 Nov 2023 23:06:39 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 30 Nov 2023 23:06:39 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 30 Nov 2023 23:06:39 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 30 Nov 2023 23:06:40 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 30 Nov 2023 23:06:40 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 30 Nov 2023 23:06:40 GMT
LABEL org.opencontainers.image.version=1.31.1
# Thu, 30 Nov 2023 23:07:30 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Thu, 30 Nov 2023 23:07:30 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:07:30 GMT
COPY multi:44b909b4ee0b15a0820a0f95f866a48ec9fbcb6e3c46d6d937842c09126ebe93 in /usr/share/unit/welcome/ 
# Thu, 30 Nov 2023 23:07:30 GMT
STOPSIGNAL SIGTERM
# Thu, 30 Nov 2023 23:07:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 30 Nov 2023 23:07:30 GMT
EXPOSE 80
# Thu, 30 Nov 2023 23:07:30 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577ff23cfe55ac8872bc433ce99971a34011e7a15f7c8afa3d6492c78d6d23e5`  
		Last Modified: Tue, 21 Nov 2023 10:02:30 GMT  
		Size: 15.8 MB (15764247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b1e60e9d5a0f16eb1f998245666f7a64a44f8b1f2317bd31e8a658150c23d3`  
		Last Modified: Tue, 21 Nov 2023 10:02:45 GMT  
		Size: 54.6 MB (54595728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beefab36cbfedf8896b5f9f0bc33336fa13c0f01a8cb2333128dd247895a5f3b`  
		Last Modified: Tue, 21 Nov 2023 10:03:16 GMT  
		Size: 196.9 MB (196879850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a474890f1805d2c3d472fc47d13381f8c1b08431e974c9b600277132481ad3`  
		Last Modified: Tue, 21 Nov 2023 22:55:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b9d560ce6b6b1199282991d7e135f41a63d4a2bc5aebe17d494d7d9ba4935e`  
		Last Modified: Thu, 30 Nov 2023 22:31:24 GMT  
		Size: 15.6 MB (15620964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b908e8be92843b55362f440cb0c3663e9071ce93370198c80cb0666c5fcf9358`  
		Last Modified: Thu, 30 Nov 2023 22:31:21 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e7f2b394755e358969a67b5857b52c6f0df5ecb5dea60ba8772a7ecbf1a01d`  
		Last Modified: Thu, 30 Nov 2023 23:10:16 GMT  
		Size: 7.3 MB (7262490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facc1b1a430198cd8a2ae0ba867ad72c9cb978c81e2e7c16ce363372d8a5202a`  
		Last Modified: Thu, 30 Nov 2023 23:10:15 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7f33d3654e9161fea1d4617de608798d3b9c6502d4ff7014d52a4a13023847`  
		Last Modified: Thu, 30 Nov 2023 23:10:15 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `unit:perl` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:f25cc9701384e023ebbf03c6a5fcde279ea95b56a5af611d90ef404e4b452720
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336659786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8576eb6e18f86684efdaf8df9619f7399ae6f23cbffbda4eab352b68c91b0fc2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:59:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:38:00 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 21 Nov 2023 10:38:00 GMT
WORKDIR /usr/src/perl
# Thu, 30 Nov 2023 19:51:06 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.2.tar.xz -o perl-5.38.2.tar.xz     && echo 'd91115e90b896520e83d4de6b52f8254ef2b70a8d545ffab33200ea9f1cf29e8 *perl-5.38.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.xz -C /usr/src/perl     && rm perl-5.38.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 30 Nov 2023 19:51:06 GMT
WORKDIR /usr/src/app
# Thu, 30 Nov 2023 19:51:06 GMT
CMD ["perl5.38.2" "-de0"]
# Thu, 30 Nov 2023 22:55:46 GMT
LABEL org.opencontainers.image.title=Unit (perl5.38)
# Thu, 30 Nov 2023 22:55:46 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 30 Nov 2023 22:55:46 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 30 Nov 2023 22:55:47 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 30 Nov 2023 22:55:47 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 30 Nov 2023 22:55:47 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 30 Nov 2023 22:55:47 GMT
LABEL org.opencontainers.image.version=1.31.1
# Thu, 30 Nov 2023 22:56:28 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Thu, 30 Nov 2023 22:56:28 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Thu, 30 Nov 2023 22:56:28 GMT
COPY multi:44b909b4ee0b15a0820a0f95f866a48ec9fbcb6e3c46d6d937842c09126ebe93 in /usr/share/unit/welcome/ 
# Thu, 30 Nov 2023 22:56:28 GMT
STOPSIGNAL SIGTERM
# Thu, 30 Nov 2023 22:56:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 30 Nov 2023 22:56:29 GMT
EXPOSE 80
# Thu, 30 Nov 2023 22:56:29 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e860a4a6ca9e583881322c2e78baef1911e4d61bc607563e8ad9891e2d91f9`  
		Last Modified: Tue, 21 Nov 2023 08:07:01 GMT  
		Size: 15.8 MB (15750113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9d2006a8ea812285a7be34dfc82465b2a592d6217f4d385d373c298de4642`  
		Last Modified: Tue, 21 Nov 2023 08:07:16 GMT  
		Size: 54.7 MB (54700129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abe2c38c6b934d9d3107cc7ce50d9e852c8ccef92d5cbc324a6f083b5aef0d1`  
		Last Modified: Tue, 21 Nov 2023 08:07:42 GMT  
		Size: 189.8 MB (189800334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f282d1d01501455a79fb9530f97ed3daaaf7d93c691dbc4a4f8688d99dc696`  
		Last Modified: Tue, 21 Nov 2023 13:49:44 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf1e7aa23664fe4d3abb7b62a58c3053db9ec2b3c2f93e30a3d5beab48795a`  
		Last Modified: Thu, 30 Nov 2023 22:16:55 GMT  
		Size: 15.6 MB (15557420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658e16ce3661d1eaca0089b9581900e29d316b7e8112c4788806f37ab66f26bb`  
		Last Modified: Thu, 30 Nov 2023 22:16:51 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb22cab8cd3c6cab70b496e535febffbcfa960e32198cb17c54b492b0700cc0d`  
		Last Modified: Thu, 30 Nov 2023 22:58:43 GMT  
		Size: 7.1 MB (7140838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e0b95476ec7e90393fd5659513b0e3778aa7f0f30cfd26a0a3f51f19c2946c`  
		Last Modified: Thu, 30 Nov 2023 22:58:41 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8609c8056fd431042c53285743dddce776eaf84b50584cdde8de6a24ba468e0`  
		Last Modified: Thu, 30 Nov 2023 22:58:41 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
