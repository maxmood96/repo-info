## `unit:perl5`

```console
$ docker pull unit@sha256:924ed02ffbfe691f61e3f79286d91917759e5da3bfca8810dd8f3fd65fa09a01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:perl5` - linux; amd64

```console
$ docker pull unit@sha256:21c91c9277a7bea481dff947df78fd1622fcc455e6a4b3a5bc9d8bbc6fb9a4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 MB (385768712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6688924ae9a1b19d51f290797e6c60a97efa04df42b3d14fec716dc9bc0feaf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
WORKDIR /usr/src/perl
# Mon, 03 Mar 2025 18:37:38 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.3.tar.gz -o perl-5.40.3.tar.gz     && echo '4c155b4e6160682b38919b55ac319081b898db11857cf18a7d9ffed2648ccaff *perl-5.40.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.3.tar.gz -C /usr/src/perl     && rm perl-5.40.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
WORKDIR /usr/src/app
# Mon, 03 Mar 2025 18:37:38 GMT
CMD ["perl5.40.3" "-de0"]
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.title=Unit (perl5.40)
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.version=1.34.2
# Mon, 03 Mar 2025 18:37:38 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.2-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
STOPSIGNAL SIGTERM
# Mon, 03 Mar 2025 18:37:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:37:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Mar 2025 18:37:38 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6ffe3614ab4a262aa4bc4f9759e9ec47c42ce5bb3321f0023815974344cb9b`  
		Last Modified: Tue, 12 Aug 2025 22:50:00 GMT  
		Size: 211.4 MB (211394364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5de7913a534bb0928273d04d20ff2dc669e664d7dc8552aec1300923c893e`  
		Last Modified: Mon, 18 Aug 2025 18:06:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4315c7155a42c9e42146cee90d9fbc64aea081986a96b3c72f65e4e47dbbdab9`  
		Last Modified: Mon, 18 Aug 2025 18:07:04 GMT  
		Size: 15.8 MB (15826766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d97c6f33ae16c2d563420c68fefcb1cae0349f366617d506b02ac77aef3bdf`  
		Last Modified: Mon, 18 Aug 2025 18:06:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1db0e3b9f84dcfe8e5e8c80241827ecc279237b5c5cf17e6f1c96a7ef2259d`  
		Last Modified: Mon, 18 Aug 2025 18:11:17 GMT  
		Size: 21.6 MB (21629192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec76445c21ef6d268a5f3aa354c4a60b8fa321d85e0fe4b89bfa1f10318bc802`  
		Last Modified: Mon, 18 Aug 2025 18:11:15 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5309db097ec6ea29834377b5fa979b167c97eaa75b5cc357baf5b68c0ec4ea3`  
		Last Modified: Mon, 18 Aug 2025 18:11:15 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:perl5` - unknown; unknown

```console
$ docker pull unit@sha256:5fb2c8d796eb88a3ab794d97853a77372865f6c0bb2153a67e1681c0a0423281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b775d09af70d99774a0b52ed51c9526c4bc6b928187ace7f8b785d0bbdb4e3a7`

```dockerfile
```

-	Layers:
	-	`sha256:fefedf6e802aa14d5afdd3f754cf63dccb1b82f8a71fcbbcddb6bf22335e575b`  
		Last Modified: Mon, 18 Aug 2025 20:45:25 GMT  
		Size: 28.2 KB (28153 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:perl5` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:1d6c0e7cb94ad31dd9864fa1518dd79708d75cc7c17dbc5753e1afd44e019630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.9 MB (375926667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99228cb725644d5e1fcea27d4892d9b115c2961d75f93cf3fab3aa9c90e8c889`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
WORKDIR /usr/src/perl
# Mon, 03 Mar 2025 18:37:38 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.40.3.tar.gz -o perl-5.40.3.tar.gz     && echo '4c155b4e6160682b38919b55ac319081b898db11857cf18a7d9ffed2648ccaff *perl-5.40.3.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.3.tar.gz -C /usr/src/perl     && rm perl-5.40.3.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
WORKDIR /usr/src/app
# Mon, 03 Mar 2025 18:37:38 GMT
CMD ["perl5.40.3" "-de0"]
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.title=Unit (perl5.40)
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 03 Mar 2025 18:37:38 GMT
LABEL org.opencontainers.image.version=1.34.2
# Mon, 03 Mar 2025 18:37:38 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.2-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure perl     && make -j $NCPU perl-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure perl     && make -j $NCPU perl-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && /bin/true     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Mon, 03 Mar 2025 18:37:38 GMT
STOPSIGNAL SIGTERM
# Mon, 03 Mar 2025 18:37:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 03 Mar 2025 18:37:38 GMT
EXPOSE map[80/tcp:{}]
# Mon, 03 Mar 2025 18:37:38 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8325efcffd02810e02c94ef0cf141d88f021fdac3fd247613e996624eb84fb23`  
		Last Modified: Wed, 13 Aug 2025 21:52:42 GMT  
		Size: 202.9 MB (202855055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631d0eb85b74d0d7990a8e8bb6bc6085cac4842a96a0ef7b7a6f5e840ab781bc`  
		Last Modified: Mon, 18 Aug 2025 18:04:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b52e182640f78ed3e4de832ea38ececc95e2359c3ece5d9d5add0b99a4f98f`  
		Last Modified: Mon, 18 Aug 2025 19:06:12 GMT  
		Size: 15.8 MB (15785598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a2346f6e4306f364a68d715980a98fd38fd6945d41c731206be921e62bb7dc`  
		Last Modified: Mon, 18 Aug 2025 19:06:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c075e996fc7ba754a5aa8b4a9c84bacd4fba0b91bec3a02ba252877e01be8846`  
		Last Modified: Mon, 18 Aug 2025 22:40:42 GMT  
		Size: 21.0 MB (21003731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b695aed6d3d28af015a0dee09e93a0d82947d73c3bd62093b86f3a93c56ef20d`  
		Last Modified: Mon, 18 Aug 2025 22:40:40 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692bf73632aa330d80c111db1491eeed4e0286107233e6bd7431a425d115c4b6`  
		Last Modified: Mon, 18 Aug 2025 22:40:40 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:perl5` - unknown; unknown

```console
$ docker pull unit@sha256:11ea7a6ef3f00d6f78191795ebe20c9be0009834fbe1359eba5d007643b3c7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 KB (28258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8fa77737a1966a72e67e9c25c0e299f577a11f3da336f018cdcf364fda57fa`

```dockerfile
```

-	Layers:
	-	`sha256:1d1d8544e44379cd2a6539a3c20f412e9643b2080cc4a5bd1ffdd9c08e4ddae4`  
		Last Modified: Mon, 18 Aug 2025 23:45:39 GMT  
		Size: 28.3 KB (28258 bytes)  
		MIME: application/vnd.in-toto+json
