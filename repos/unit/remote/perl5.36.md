## `unit:perl5.36`

```console
$ docker pull unit@sha256:f5bbb8cf5b0b9aaca7403a0d5593ee77c0425edda34acc781fd1c7fd41061785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `unit:perl5.36` - linux; amd64

```console
$ docker pull unit@sha256:3e44f444cf54062591199d948acc9bba051fb4f2b225a83236b2fa47a393b36f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344782858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35b76970f6244f0192fcd3b23d85b5083149a853cf87b81762755798bc85937`
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
# Thu, 30 Nov 2023 20:45:21 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.3.tar.xz -o perl-5.36.3.tar.xz     && echo '45a228daef66d02fdccc820e71f87e40d8e3df1fc4431f8d4580ec08033866bd *perl-5.36.3.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.3.tar.xz -C /usr/src/perl     && rm perl-5.36.3.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 30 Nov 2023 20:45:22 GMT
WORKDIR /usr/src/app
# Thu, 30 Nov 2023 20:45:22 GMT
CMD ["perl5.36.3" "-de0"]
# Thu, 30 Nov 2023 23:07:38 GMT
LABEL org.opencontainers.image.title=Unit (perl5.36)
# Thu, 30 Nov 2023 23:07:38 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 30 Nov 2023 23:07:38 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 30 Nov 2023 23:07:38 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 30 Nov 2023 23:07:38 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 30 Nov 2023 23:07:38 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 30 Nov 2023 23:07:38 GMT
LABEL org.opencontainers.image.version=1.31.1
# Thu, 30 Nov 2023 23:08:27 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Thu, 30 Nov 2023 23:08:27 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Thu, 30 Nov 2023 23:08:27 GMT
COPY multi:44b909b4ee0b15a0820a0f95f866a48ec9fbcb6e3c46d6d937842c09126ebe93 in /usr/share/unit/welcome/ 
# Thu, 30 Nov 2023 23:08:27 GMT
STOPSIGNAL SIGTERM
# Thu, 30 Nov 2023 23:08:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 30 Nov 2023 23:08:28 GMT
EXPOSE 80
# Thu, 30 Nov 2023 23:08:28 GMT
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
	-	`sha256:ebcbf195a363d7dd4df5dd68ce8a8239c86b518c61bb0aeebc4bb7793a498293`  
		Last Modified: Thu, 30 Nov 2023 22:35:32 GMT  
		Size: 15.2 MB (15231042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0719fb2a66259155a5504090102ad65db1011efc75a016dfbb59d69f6ccb5325`  
		Last Modified: Thu, 30 Nov 2023 22:35:29 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae3a7e05c5551b67f5fb4d1cabaa2b218bf9b0b32a2b135eaafa5518038e7c1`  
		Last Modified: Thu, 30 Nov 2023 23:10:31 GMT  
		Size: 7.3 MB (7251009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba18efc91738465ea1819797649ad06a6050ca8fc5a5f3b4c59cb1832c4f05`  
		Last Modified: Thu, 30 Nov 2023 23:10:30 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a929236637e6869504317be9d0bc05a5488b1e3b90d3c5d6860e7af9d48e63`  
		Last Modified: Thu, 30 Nov 2023 23:10:30 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `unit:perl5.36` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:b368757ad0e06f348e769461a5542636aa7a153d98d571e0d17d79bc8611038d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 MB (336263731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868529f6448562023b5fc0497a248579f081645e0c4bd6bf5a576a53a153e7cf`
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
# Thu, 30 Nov 2023 20:48:58 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.3.tar.xz -o perl-5.36.3.tar.xz     && echo '45a228daef66d02fdccc820e71f87e40d8e3df1fc4431f8d4580ec08033866bd *perl-5.36.3.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.3.tar.xz -C /usr/src/perl     && rm perl-5.36.3.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 30 Nov 2023 20:48:58 GMT
WORKDIR /usr/src/app
# Thu, 30 Nov 2023 20:48:58 GMT
CMD ["perl5.36.3" "-de0"]
# Thu, 30 Nov 2023 22:56:34 GMT
LABEL org.opencontainers.image.title=Unit (perl5.36)
# Thu, 30 Nov 2023 22:56:34 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 30 Nov 2023 22:56:34 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 30 Nov 2023 22:56:35 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 30 Nov 2023 22:56:35 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 30 Nov 2023 22:56:35 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 30 Nov 2023 22:56:35 GMT
LABEL org.opencontainers.image.version=1.31.1
# Thu, 30 Nov 2023 22:57:15 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates mercurial build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && hg clone -u 1.31.1-1 https://hg.nginx.org/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stdout /var/log/unit.log
# Thu, 30 Nov 2023 22:57:15 GMT
COPY file:8b65557c2137d1a3946148e09ddd45af0b855e40210dabb5a9bd6c36fac22006 in /usr/local/bin/ 
# Thu, 30 Nov 2023 22:57:15 GMT
COPY multi:44b909b4ee0b15a0820a0f95f866a48ec9fbcb6e3c46d6d937842c09126ebe93 in /usr/share/unit/welcome/ 
# Thu, 30 Nov 2023 22:57:15 GMT
STOPSIGNAL SIGTERM
# Thu, 30 Nov 2023 22:57:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 30 Nov 2023 22:57:16 GMT
EXPOSE 80
# Thu, 30 Nov 2023 22:57:16 GMT
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
	-	`sha256:0be332de5dd572bc3d450f863bf2472b94710083f42cf025db3b616dfcbf0202`  
		Last Modified: Thu, 30 Nov 2023 22:21:00 GMT  
		Size: 15.2 MB (15174829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ae05673004e92c16b716ff0d040171926d0c55d271d4a5f3ac4ab3879facdb`  
		Last Modified: Thu, 30 Nov 2023 22:20:58 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe83d4b0cda264dbcbfa3438c257aeda18ce5656f6bd25465616a2c307c5fc`  
		Last Modified: Thu, 30 Nov 2023 22:58:57 GMT  
		Size: 7.1 MB (7127377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349c8637c38d56b72f2e91dd8dcb66094416edf75e14caa90f95b010005db992`  
		Last Modified: Thu, 30 Nov 2023 22:58:56 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37547d311d794deb090da08441a4969813c40efa45eebc8b495df54154e58d`  
		Last Modified: Thu, 30 Nov 2023 22:58:56 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
