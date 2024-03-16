## `unit:php8.2`

```console
$ docker pull unit@sha256:12f5caf7c6c474b34fb46c7b7f8e9dbb9ca358b660f11b31d18314d726d6146a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `unit:php8.2` - linux; amd64

```console
$ docker pull unit@sha256:c417032a32ce2cb278954a9b4fd4765614dd0e392be98399fc6dd8d02177daa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176893934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f224e86c74d0157465eae276cce967cf27311ba43ea233425b50539f22634f3c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 27 Feb 2024 15:15:42 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 27 Feb 2024 15:15:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_VERSION=8.2.17
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 27 Feb 2024 15:15:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 27 Feb 2024 15:15:42 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 27 Feb 2024 15:15:42 GMT
RUN docker-php-ext-enable sodium
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["php" "-a"]
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.title=Unit (php8.2)
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.version=1.32.0
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure php     && make -j $NCPU php-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure php     && make -j $NCPU php-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && ldconfig     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
STOPSIGNAL SIGTERM
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 15:15:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a110dcb6d2f3bea8c7f86c44dda941c22c88034e199a40fa904ec2e203a23dee`  
		Last Modified: Tue, 12 Mar 2024 05:26:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a676cd3cc4aa867242bce97f4a71ef07fbe9d401ce8f56bef633008f42c9b07`  
		Last Modified: Tue, 12 Mar 2024 05:27:05 GMT  
		Size: 91.6 MB (91639971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0074f28e265cef1b2a0480f04003205964be45768281d74af416ccdda13de198`  
		Last Modified: Tue, 12 Mar 2024 05:26:52 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34ae204057db2a1c6915403005c484620199b12d759595d689d02e7c5cba551`  
		Last Modified: Sat, 16 Mar 2024 02:39:48 GMT  
		Size: 12.4 MB (12411343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db52e87e604cb5d7f29d25682f38c79c469dde48f94f7be47b1a4a045bff7a28`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df59523d803c3219a234851a6aa0912eb8c1ccaa93b0448fd83965b0951350e2`  
		Last Modified: Sat, 16 Mar 2024 02:39:52 GMT  
		Size: 34.5 MB (34511479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f44aff3be1a8ec6564aad47c0c086c709689ca7458b6bab92fdd395e395773`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef071615fd64752edc86ce2e176124c27586e0034cefe7b3dee992c64fd1d7ea`  
		Last Modified: Sat, 16 Mar 2024 02:39:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73afb71483c00396988762a605056bbab167708051522370a5acf9dd47c1d5d8`  
		Last Modified: Sat, 16 Mar 2024 02:52:01 GMT  
		Size: 6.9 MB (6902243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827996dcdf695435cd80e9214acc899fe4c7188c5498750654276c88d6142f89`  
		Last Modified: Sat, 16 Mar 2024 02:52:01 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb6b8093a47c65d6ff3d40630f4af017db8089ae5cdb5aa8a018fc0ca856a22`  
		Last Modified: Sat, 16 Mar 2024 02:52:01 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:php8.2` - unknown; unknown

```console
$ docker pull unit@sha256:c2cc8104e6b7dfcf7360159e09d52f5c2e264273706e7add4dc777def33746d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6367095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c938ee9479b4d6504e9f22433faecd89a7f3ca5dfc0028340d7f2cce806ae594`

```dockerfile
```

-	Layers:
	-	`sha256:1fb9c12586ca4a5043d2e8fa9bf5849dfb7e38a81077c679105db3d5f6e30a8d`  
		Last Modified: Sat, 16 Mar 2024 02:52:00 GMT  
		Size: 6.3 MB (6339601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2048dfe6f9c890d1cc2189e74f60c18e076d473f846b6f03adc51dfd0074db14`  
		Last Modified: Sat, 16 Mar 2024 02:52:00 GMT  
		Size: 27.5 KB (27494 bytes)  
		MIME: application/vnd.in-toto+json

### `unit:php8.2` - linux; arm64 variant v8

```console
$ docker pull unit@sha256:8f4a2d6c21f034cfbf45a3f7215761d08d26d11e6e3b8e3247334ae760db221c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170638232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63febc957706f93f6202335fc4621fd754093be527fe1e614c83c185c27291ca`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["unitd","--no-daemon","--control","unix:\/var\/run\/control.unit.sock"]`

```dockerfile
# Tue, 27 Feb 2024 15:15:42 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["bash"]
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 27 Feb 2024 15:15:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_VERSION=8.2.16
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Tue, 27 Feb 2024 15:15:42 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 27 Feb 2024 15:15:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--enable-embed 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 27 Feb 2024 15:15:42 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Tue, 27 Feb 2024 15:15:42 GMT
RUN docker-php-ext-enable sodium
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["php" "-a"]
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.title=Unit (php8.2)
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.description=Official build of Unit for Docker.
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.url=https://unit.nginx.org
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.source=https://github.com/nginx/unit
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.documentation=https://unit.nginx.org/installation/#docker-images
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.vendor=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 27 Feb 2024 15:15:42 GMT
LABEL org.opencontainers.image.version=1.32.0
# Tue, 27 Feb 2024 15:15:42 GMT
RUN set -ex     && savedAptMark="$(apt-mark showmanual)"     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y ca-certificates git build-essential libssl-dev libpcre2-dev curl pkg-config     && mkdir -p /usr/lib/unit/modules /usr/lib/unit/debug-modules     && mkdir -p /usr/src/unit     && cd /usr/src/unit     && git clone --depth 1 -b 1.32.0-1 https://github.com/nginx/unit     && cd unit     && NCPU="$(getconf _NPROCESSORS_ONLN)"     && DEB_HOST_MULTIARCH="$(dpkg-architecture -q DEB_HOST_MULTIARCH)"     && CC_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_CFLAGS_MAINT_APPEND="-Wp,-D_FORTIFY_SOURCE=2 -fPIC" dpkg-buildflags --get CFLAGS)"     && LD_OPT="$(DEB_BUILD_MAINT_OPTIONS="hardening=+all,-pie" DEB_LDFLAGS_MAINT_APPEND="-Wl,--as-needed -pie" dpkg-buildflags --get LDFLAGS)"     && CONFIGURE_ARGS_MODULES="--prefix=/usr                 --statedir=/var/lib/unit                 --control=unix:/var/run/control.unit.sock                 --runstatedir=/var/run                 --pid=/var/run/unit.pid                 --logdir=/var/log                 --log=/var/log/unit.log                 --tmpdir=/var/tmp                 --user=unit                 --group=unit                 --openssl                 --libdir=/usr/lib/$DEB_HOST_MULTIARCH"     && CONFIGURE_ARGS="$CONFIGURE_ARGS_MODULES                 --njs"     && make -j $NCPU -C pkg/contrib .njs     && export PKG_CONFIG_PATH=$(pwd)/pkg/contrib/njs/build     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd-debug     && make clean     && ./configure $CONFIGURE_ARGS --cc-opt="$CC_OPT" --ld-opt="$LD_OPT" --modulesdir=/usr/lib/unit/modules     && make -j $NCPU unitd     && install -pm755 build/sbin/unitd /usr/sbin/unitd     && make clean     && /bin/true     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/debug-modules --debug     && ./configure php     && make -j $NCPU php-install     && make clean     && ./configure $CONFIGURE_ARGS_MODULES --cc-opt="$CC_OPT" --modulesdir=/usr/lib/unit/modules     && ./configure php     && make -j $NCPU php-install     && cd     && rm -rf /usr/src/unit     && for f in /usr/sbin/unitd /usr/lib/unit/modules/*.unit.so; do         ldd $f | awk '/=>/{print $(NF-1)}' | while read n; do dpkg-query -S $n; done | sed 's/^\([^:]\+\):.*$/\1/' | sort | uniq >> /requirements.apt;        done     && apt-mark showmanual | xargs apt-mark auto > /dev/null     && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }     && ldconfig     && mkdir -p /var/lib/unit/     && mkdir -p /docker-entrypoint.d/     && groupadd --gid 999 unit     && useradd          --uid 999          --gid unit          --no-create-home          --home /nonexistent          --comment "unit user"          --shell /bin/false          unit     && apt-get update     && apt-get --no-install-recommends --no-install-suggests -y install curl $(cat /requirements.apt)     && apt-get purge -y --auto-remove build-essential     && rm -rf /var/lib/apt/lists/*     && rm -f /requirements.apt     && ln -sf /dev/stderr /var/log/unit.log # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
COPY welcome.* /usr/share/unit/welcome/ # buildkit
# Tue, 27 Feb 2024 15:15:42 GMT
STOPSIGNAL SIGTERM
# Tue, 27 Feb 2024 15:15:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 27 Feb 2024 15:15:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 27 Feb 2024 15:15:42 GMT
CMD ["unitd" "--no-daemon" "--control" "unix:/var/run/control.unit.sock"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95434312c87bbfb0c1c0428101ecb9ad5da0f27b23e0bab2cfa9aef467e4d9e`  
		Last Modified: Tue, 12 Mar 2024 06:58:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465e10561b205308476d133ec1a862daf9138d09b954ce86d35fd888baaa8727`  
		Last Modified: Tue, 12 Mar 2024 06:58:46 GMT  
		Size: 86.9 MB (86934539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3beb929c6bc3ebeb0fbc6e8e3ce3ecda6ee33da58ad63dafdead658eed3e34`  
		Last Modified: Tue, 12 Mar 2024 06:58:37 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7485e890eb883243663c0dbd3a549d5196f43acaae9137340fedfc2350d89afd`  
		Last Modified: Tue, 12 Mar 2024 07:06:19 GMT  
		Size: 12.4 MB (12403872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f911fbbfdfe49db04c83d6eba87f9a8f19b9486ce2890d40552472c991adf0`  
		Last Modified: Tue, 12 Mar 2024 07:06:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dc27f16a88dfc539683db9102096de2d6de869719cb964cd5cbfb0f440b847`  
		Last Modified: Tue, 12 Mar 2024 07:06:21 GMT  
		Size: 34.4 MB (34449482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99af6085a0d0b02ca430eb124ae6db5f052490797fb22e7e289a042f215d5430`  
		Last Modified: Tue, 12 Mar 2024 07:06:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7760f346cca221ae0bdc718853d497ac78f0536cd465f2ef8303e4e4c0c46df0`  
		Last Modified: Tue, 12 Mar 2024 07:06:17 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8917a5853bcac49d072f04ae579b802d66d3fac833a4bdb63c6ffffbab92a`  
		Last Modified: Wed, 13 Mar 2024 06:20:56 GMT  
		Size: 6.8 MB (6772819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191ce9c14e03499e48913d93f21e7fa9f79a986c7f9e57bee99a4ba0f42428ff`  
		Last Modified: Wed, 13 Mar 2024 06:20:56 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e95d9b913d4b5d8be4a0a84ba19eab5a6cf85aa5aede2ddad4ba8abdd807f9a`  
		Last Modified: Wed, 13 Mar 2024 06:20:56 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `unit:php8.2` - unknown; unknown

```console
$ docker pull unit@sha256:46c80b14a283cf7fa339e014d8b6084a70924fd2f92924f56194926cbca12d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6370075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec235c49da0b673c77f1de36324a560ade44bc0d3ea094877f46ada5f53cae6f`

```dockerfile
```

-	Layers:
	-	`sha256:6753f92848e93f85185dab692fab80967ea6fba318d9ea32e57a8d2fa0cbfd1d`  
		Last Modified: Wed, 13 Mar 2024 06:20:55 GMT  
		Size: 6.3 MB (6342576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96b4e25195d971c33026d43cafa60faab0b451c7e49b5983f94e895e54af110`  
		Last Modified: Wed, 13 Mar 2024 06:20:55 GMT  
		Size: 27.5 KB (27499 bytes)  
		MIME: application/vnd.in-toto+json
