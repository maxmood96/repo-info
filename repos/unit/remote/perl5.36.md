## `unit:perl5.36`

```console
$ docker pull unit@sha256:5f512d4d1c8d728fdc4ba92ce1108731ae7fc2b607cd801a48b62a50b4bf69fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:perl5.36` - linux; amd64

```console
$ docker pull unit@sha256:ef5b22906c2ee3deb1b697f5dbbb26edc8d155bb67ee6a9b131472089b60351b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344582261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae4913c5b0cf4799e9c7e16bb44457915ff178b74af74896475c56de810a261`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Oct 2023 10:47:22 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.36.3.tar.gz -o perl-5.36.3.tar.gz     && echo 'f2a1ad88116391a176262dd42dfc52ef22afb40f4c0e9810f15d561e6f1c726a *perl-5.36.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.3.tar.gz -C /usr/src/perl     && rm perl-5.36.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /usr/src/app
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["perl5.36.3" "-de0"]
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.title=Unit (perl5.36)
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
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24098c8d74fae9a314e70517566e785db7b39341cbc4bd63adf14c330728677c`  
		Last Modified: Wed, 17 Jan 2024 02:01:11 GMT  
		Size: 54.6 MB (54601537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6374b4ceb7a33a2609d9577d1f8cb5133e782949ab21f31086c1de775cb6843`  
		Last Modified: Wed, 17 Jan 2024 02:01:44 GMT  
		Size: 196.9 MB (196898503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4f23af31c941cc804c81151bbf47fc0d1b8cc493b0e5b5a30956c3b4f72054`  
		Last Modified: Wed, 17 Jan 2024 03:55:37 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e53c6127e559b871a1160c11919dd368eef6b2dfd1f9f846b69ae7a180de7c`  
		Last Modified: Wed, 17 Jan 2024 03:55:37 GMT  
		Size: 15.2 MB (15246184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa09cdf28c3f184c2e0c4a81f6a91926cffa6dcd7376df4da670e610a473b24`  
		Last Modified: Wed, 17 Jan 2024 03:55:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90ec4970c1c65f4d8000e83c2167dd2f89354d421310ab179cb1820dcd4b2b9`  
		Last Modified: Wed, 17 Jan 2024 04:49:36 GMT  
		Size: 7.0 MB (7010223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1454ce7e0abd565a23ec5d79b075eecf009a0520a8567b47aa0a10970a51b2f`  
		Last Modified: Wed, 17 Jan 2024 04:49:36 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c84458fc08f6fb8a7dca30a18628fff746904da3a83f3df8794e8cea9ebafd`  
		Last Modified: Wed, 17 Jan 2024 04:49:35 GMT  
		Size: 1.5 KB (1451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:perl5.36` - unknown; unknown

```console
$ docker pull unit@sha256:5600961d233436399819c2e213661c6549b797e80f059bc8308abd688ac19b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12976916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcbc114c29ab4ac69e7d978111783f1c15e10b19a10da9cd609303f32b2c49f`

```dockerfile
```

-	Layers:
	-	`sha256:b49660f6252ce8ba9ca25dc52645629505d8f45baa53f299e09f28bfd6b419d0`  
		Last Modified: Wed, 17 Jan 2024 04:49:36 GMT  
		Size: 13.0 MB (12951730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede5b699c137d3c67bb86b76e891a0b9ed69ca1a25f4232164e9a2d8d0407d39`  
		Last Modified: Wed, 17 Jan 2024 04:49:35 GMT  
		Size: 25.2 KB (25186 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:perl5.36` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:31eb9f4dfacc1a89252a327546e5f0148a01f50ba8e4c59d57a52ec7e6ee3029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336071239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2374fbfb1b6e12998563c35337a70036f2066a8f46296f10af104d1eadb7cf46`
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
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /usr/src/perl
# Thu, 19 Oct 2023 10:47:22 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.36.3.tar.gz -o perl-5.36.3.tar.gz     && echo 'f2a1ad88116391a176262dd42dfc52ef22afb40f4c0e9810f15d561e6f1c726a *perl-5.36.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.3.tar.gz -C /usr/src/perl     && rm perl-5.36.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 19 Oct 2023 10:47:22 GMT
WORKDIR /usr/src/app
# Thu, 19 Oct 2023 10:47:22 GMT
CMD ["perl5.36.3" "-de0"]
# Thu, 19 Oct 2023 10:47:22 GMT
LABEL org.opencontainers.image.title=Unit (perl5.36)
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
	-	`sha256:826044e8ec1545c4af5dfe71ab63bce600198330f150aa968074bb86e78cd154`  
		Last Modified: Thu, 11 Jan 2024 09:35:17 GMT  
		Size: 54.7 MB (54699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb605b1d0205817191fda1aebbfb24bc89220d168a2231b4a4b44c0c48e4e627`  
		Last Modified: Thu, 11 Jan 2024 09:35:43 GMT  
		Size: 189.8 MB (189834619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c39682001daa1567615530df83ff0ffb4e745ebc43424e356017ac3086b266`  
		Last Modified: Fri, 12 Jan 2024 09:38:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b0fe9213ed70eec1e577729aa43ba546d080a989a1d48a8446c49be668dc4f`  
		Last Modified: Fri, 12 Jan 2024 11:41:58 GMT  
		Size: 15.2 MB (15188447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b04fcfd62d767f9360c44f162ef94ff38372441a52bf925e7ea2a63e57d0ad`  
		Last Modified: Fri, 12 Jan 2024 11:41:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cff532a967866f9824c9ef805d8d5ae251c28fa2090af3ce08d86b6ad06ba9`  
		Last Modified: Fri, 12 Jan 2024 21:01:36 GMT  
		Size: 6.9 MB (6886756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ede555fe4e7ed37bea0de65c74bb3f562bc26f87cfcd8efa5cc736a85cc3ab0`  
		Last Modified: Fri, 12 Jan 2024 21:01:35 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ad5e03e144519731acf0eff2bad705db31f30d08c95a1be568b5ac978c5c6b`  
		Last Modified: Fri, 12 Jan 2024 21:01:36 GMT  
		Size: 1.5 KB (1458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:perl5.36` - unknown; unknown

```console
$ docker pull unit@sha256:788b4ef11b7021d1eb44feacb5d8dbcc2646cc24f84d995f57cbe52fcff748af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12979403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6bf7aa96caf0006d2dc6df2cbc845116076913861f74cb2c317e7def04326d`

```dockerfile
```

-	Layers:
	-	`sha256:065756624131a2f6b1e55bc93a9790084884ecef599ad595ddc1705aac5ba56f`  
		Last Modified: Fri, 12 Jan 2024 21:01:36 GMT  
		Size: 13.0 MB (12954086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15439103e6f23b5875a7abe83209fd6bc107060882bb9f2282d0b21debd2f3a9`  
		Last Modified: Fri, 12 Jan 2024 21:01:35 GMT  
		Size: 25.3 KB (25317 bytes)  
		MIME: application/vnd.in-toto+json
