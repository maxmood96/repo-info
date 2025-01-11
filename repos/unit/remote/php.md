## `unit:php`

```console
$ docker pull unit@sha256:18e2b86ed74eac1cbed2ddecea5ca93fdda51ce2fb34d28588c2a1916f1f3732
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:php` - linux; amd64

```console
$ docker pull unit@sha256:a10075140f5cdc51e8bf08dcb26d656347b8228b6c04c36dd0b73c125a17f721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188020417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402bc784f166145124e1ad857764d50c0720b1546e53db7c7efe7fb4b2da8123`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 17 Sep 2024 21:10:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Tue, 17 Sep 2024 21:10:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Sep 2024 21:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Sep 2024 21:10:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Sep 2024 21:10:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Sep 2024 21:10:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Sep 2024 21:10:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 17 Sep 2024 21:10:58 GMT
ENV PHP_VERSION=8.3.15
# Tue, 17 Sep 2024 21:10:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Tue, 17 Sep 2024 21:10:58 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Tue, 17 Sep 2024 21:10:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 17 Sep 2024 21:10:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 17 Sep 2024 21:10:58 GMT
CMD ["php" "-a"]
# Tue, 17 Sep 2024 21:10:58 GMT
LABEL org.opencontainers.image.title=Unit (php8.3)
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
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.33.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure php     && make -j $NCPU php-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure php     && make -j $NCPU php-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && ldconfig     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2caf96ae71d9f407739c5c483cf9bf24c4da0757ad40eeecaa4d223e6c46711`  
		Last Modified: Tue, 24 Dec 2024 22:24:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8ab92c1a74f8df0d3f3cbb9184617515b8a662bc194aff481d7ba6f2db40ed`  
		Last Modified: Tue, 24 Dec 2024 22:24:53 GMT  
		Size: 104.2 MB (104150505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097c76ee9a6ba16ef0326faf307ac520367bb10cd8c409ab328559b2bcb35dc`  
		Last Modified: Tue, 24 Dec 2024 22:24:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b26b7cc266ccfbea3cda18f445deadd39cb57558758d07c93d123288e4fc8de`  
		Last Modified: Tue, 24 Dec 2024 22:24:50 GMT  
		Size: 12.6 MB (12634134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc72b30bdd8455354b7cf24adb5efa70d98d34ad9a1f31c36ede3cf1266c42c8`  
		Last Modified: Tue, 24 Dec 2024 22:24:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b800b2cc9c36029fbd709225503557976b2d997d4dfb1251c15e6a0bbed8f77b`  
		Last Modified: Tue, 24 Dec 2024 22:24:52 GMT  
		Size: 36.1 MB (36116839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b68d5786695ef96849c3470d037a1eb1acde42ed8dd1889d78678c8d02c5b`  
		Last Modified: Tue, 24 Dec 2024 22:24:51 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9223dc12ecefa04af107e27d6182cdf8a8054f10c547fcd969cc1952937d0970`  
		Last Modified: Tue, 24 Dec 2024 22:24:51 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121b319c0c225b2347c8e4fb152a115580843a78a9226daaa3494f2e284bdda`  
		Last Modified: Tue, 24 Dec 2024 23:22:31 GMT  
		Size: 6.9 MB (6881014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1fecca649b7cce8aadb56fce9eb943da00fa432b03b09516f0368a41dfa3c6`  
		Last Modified: Tue, 24 Dec 2024 23:22:30 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712a0f756105d280f160d3f75bf1b4da7ffdbfa73d80e6acb92121992c3ff98c`  
		Last Modified: Tue, 24 Dec 2024 23:22:30 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:php` - unknown; unknown

```console
$ docker pull unit@sha256:8a2c93048c359a8716048ecf5a62fce8400368a1b6b74b37aef88f1d05d7043f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e012b314ef9fd9ef6c4eab5c40c2fc0b1a639c046a6e4b262b5963c03d03e9`

```dockerfile
```

-	Layers:
	-	`sha256:b95d073dc82ecacfa53dc1c6b80f4b708fb72e946992cf5e9aec3833483e4534`  
		Last Modified: Tue, 24 Dec 2024 23:22:30 GMT  
		Size: 26.5 KB (26465 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:php` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:392abbfa371988fbbd41cf3bb7c184dd3a63bf9c2abbd0ef3a468a72cafd78dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200631172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537212fe7ab27a48a8e99eb64cd2ba325df01795e84065eb9049b60f3aa16045`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Thu, 19 Dec 2024 18:23:57 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:23:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:23:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:23:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:23:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:23:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:23:57 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 18:23:57 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 18:23:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 18:23:57 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 18:23:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:23:57 GMT
CMD ["php" "-a"]
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.title=Unit (php8.4)
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 19 Dec 2024 18:23:57 GMT
LABEL org.opencontainers.image.version=1.34.0
# Thu, 19 Dec 2024 18:23:57 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y          ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config libclang-dev cmake     && export RUST_VERSION=1.83.0     && export RUSTUP_HOME=/usr/src/unit/rustup     && export CARGO_HOME=/usr/src/unit/cargo     && export PATH=/usr/src/unit/cargo/bin:$PATH     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in          amd64) rustArch="x86_64-unknown-linux-gnu"; rustupSha256="6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d" ;;          arm64) rustArch="aarch64-unknown-linux-gnu"; rustupSha256="1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2" ;;          *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;        esac     && url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init"     && curl -L -O "$url"     && echo "${rustupSha256} *rustup-init" | sha256sum -c -     && chmod +x rustup-init     && ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch}     && rm rustup-init     && rustup --version     && cargo --version     && rustc --version     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.34.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs                 --otel"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure php     && make -j $NCPU php-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure php     && make -j $NCPU php-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && ldconfig     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Thu, 19 Dec 2024 18:23:57 GMT
STOPSIGNAL SIGTERM
# Thu, 19 Dec 2024 18:23:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Dec 2024 18:23:57 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:23:57 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f53a9ba108d0b9e18fa23664c2d5a17f4bbf402acecc3a7248ac7178d2fe87`  
		Last Modified: Tue, 24 Dec 2024 23:07:22 GMT  
		Size: 13.7 MB (13668428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8f45fa647a472e184757b77acf9d491a4fa1430582c5d780e12d4a9433cf62`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fd8ef07bf83a98c063d3a6529e1839593698eb5c75f096cd45f48d2d1b4d34`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 40.1 MB (40134642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5f578e5237bdf2a59c1c3bc8715e2ba5703a40437f445e799fbecf9524e402`  
		Last Modified: Tue, 24 Dec 2024 23:07:22 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da7d5a4057d390769f6f26e58a3bf539a6128bd5dc8484190b77a5b569644b`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1877dea297f27dcd0db3881b439955df9147cf769bceb53bda4f6b4a93f856`  
		Last Modified: Sat, 11 Jan 2025 02:22:35 GMT  
		Size: 20.8 MB (20826796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1d0704f9fde00c3446cdd3e25f9ac97d93f13b41d9100b830b1295460494cd`  
		Last Modified: Sat, 11 Jan 2025 02:22:34 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68be15d2c25343ba9159b124f54086527b88d45ef8d641539a8a63c6996b81c`  
		Last Modified: Sat, 11 Jan 2025 02:22:34 GMT  
		Size: 1.5 KB (1456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:php` - unknown; unknown

```console
$ docker pull unit@sha256:05e9aa7bffd30a062fda06097107bdfac0517f7149128b31f91ce58414c60a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348c41e7d2daaff400dfd2767851496eec327319b89e2dafc2657bd19d92ffbe`

```dockerfile
```

-	Layers:
	-	`sha256:d65aa9251b36532679c8f290705a720a33b12c6b5bd7a1743675018de0085dcb`  
		Last Modified: Sat, 11 Jan 2025 02:22:34 GMT  
		Size: 30.2 KB (30157 bytes)  
		MIME: application/vnd.in-toto+json
