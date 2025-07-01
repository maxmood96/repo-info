## `postfixadmin:3-fpm`

```console
$ docker pull postfixadmin@sha256:a85bc8080f5faa51db7fa0b3431144fd0ccbf24c2f18150137404bfaa60a0c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postfixadmin:3-fpm` - linux; amd64

```console
$ docker pull postfixadmin@sha256:404281a48e2b590833596c8eaf549dcea3095a125f22a208a7df13aca25ae4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176972105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0c7cb45d662e9e4c940b755df3bf1deda5be16af6783dc84e0ec5b91f0b33`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.22
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b986b853c7d68a21200eb17378b1ca8d0a57da767bf7fdbf916191b0a2d8633f`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295a75a3a91ff5f91f34813195a00644615dabcbdc8f30cbf8b03cc8630f4dc1`  
		Last Modified: Tue, 01 Jul 2025 02:24:14 GMT  
		Size: 104.3 MB (104331414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb72165b0b8e94fc9fad05eea2c3a4087a92a3bd0e4c866d595dde9d4192c49`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c01f77a2a658fa343656433f231651db8467c242861a9208fd098083f02e743`  
		Last Modified: Tue, 01 Jul 2025 02:24:08 GMT  
		Size: 12.7 MB (12664684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48c1a91367e569651114a78a6ff0ade0c3c140a99b1c3b8aec68db2cbe41a70`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3b46f190097194a6dc87cb5cf5a29045dc322bdea0cd170b2d77866aeca2ef`  
		Last Modified: Tue, 01 Jul 2025 02:24:09 GMT  
		Size: 27.8 MB (27827470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02da033c551838608e675a692849a97bee0806d4b21228d80ed703af8c018f`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eda985a7091d402a5c5c562b3606cec3c4eaf73470ebf832190b740bf414e4f`  
		Last Modified: Tue, 01 Jul 2025 02:24:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a967c5de143dbe20425ef844a3647654e96ea8a8ec85996673624d00699bf`  
		Last Modified: Tue, 01 Jul 2025 02:24:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb04038cc4a9b13940a242856f2881f7ec666347560085c664b1ba8adee5d8`  
		Last Modified: Tue, 01 Jul 2025 02:24:08 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019a67f7e03ec777fd9aea432c532f5acf90ba6e88ab41a58d9455aa69581c17`  
		Last Modified: Tue, 01 Jul 2025 03:19:54 GMT  
		Size: 1.1 MB (1069215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2aab9a2250ea534f8fb7088f05fbce886e306c8ecee82556cd3875b94cec87`  
		Last Modified: Tue, 01 Jul 2025 03:19:55 GMT  
		Size: 973.0 KB (972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fcc4a996f857878bf5d5f25d65eaa210383427cce880c5e443363f731669ba`  
		Last Modified: Tue, 01 Jul 2025 03:19:54 GMT  
		Size: 1.9 MB (1861467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32456af5a895251419f35938b5782ec33a73b32bd5b8391c28c3619d7e58131d`  
		Last Modified: Tue, 01 Jul 2025 03:19:54 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:4f1ef0cdce7df1447e400ac39b350cb74d85953a57be1eea41a3b92b1edfb541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15885e94dab4a7154d7938a604fc6a5dd8dada38c3677345c971cdf498691315`

```dockerfile
```

-	Layers:
	-	`sha256:f6f6a411e4a40c8939c9c1aaaf5a2c487f5db066c8b4a8ac4e8ecc466a9f79f9`  
		Last Modified: Tue, 01 Jul 2025 05:11:07 GMT  
		Size: 27.3 KB (27317 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:511733143475802c72a4a818747b7c2732f43295586dc7ec20bb508d32217bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150533182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c3536ecde0538227c7fd22f1e7cc263dbae085a5d2363878af0a4937f5994`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.22
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b05322491f7f224fdb6afd1a4feb0c269fe0910bd44e82e37a846aec3e465c`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b493a89b33667d984de07320c027ba0599d73427f434c8ec42c944a6bd4aa`  
		Last Modified: Tue, 01 Jul 2025 03:03:27 GMT  
		Size: 82.0 MB (81973614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef43b7ed80f2af53848f0179316741b5f6d73203876a5f0f62b038d570f6c8`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae01bf44a186a5dd593e5200a008bf6d3ea34fba3a2efb813c75da57508eb8e1`  
		Last Modified: Tue, 01 Jul 2025 03:48:34 GMT  
		Size: 12.7 MB (12662659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1db2166fad4250aea738304d0ad773d3afd3c1e644b85a83a5da6896db76c0`  
		Last Modified: Tue, 01 Jul 2025 03:48:23 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c17af07d401cbac6b90f5b289bd8047ae53967637b1b24212375368b115b719`  
		Last Modified: Tue, 01 Jul 2025 03:55:31 GMT  
		Size: 26.3 MB (26305723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680c38b6318d6dd4ec441fef57444a979a28b0f52ba9818e1177c7d010087a50`  
		Last Modified: Tue, 01 Jul 2025 03:55:29 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38e4042670e33bc4a8b95ad9a36c00fd2543a22bed5d4a9e7286fd97b36ab34`  
		Last Modified: Tue, 01 Jul 2025 03:55:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b62317e4e5dd829f11b615c476ffa064b4f802014f299c5d69923acc20a587`  
		Last Modified: Tue, 01 Jul 2025 03:55:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab49dc222c7d606ca874b858a843e30c4c626a36b310112308c1960e87f26b9b`  
		Last Modified: Tue, 01 Jul 2025 03:55:30 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9f1503965fe7a09fd318b2af58caadcc4b074648783672535661657de21db5`  
		Last Modified: Tue, 01 Jul 2025 09:06:12 GMT  
		Size: 1.0 MB (1042304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f78d8871f0dd61646de30deca1cceb3d171a93d75b5d8307102a0e5cc30466e`  
		Last Modified: Tue, 01 Jul 2025 09:06:12 GMT  
		Size: 910.2 KB (910197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa70bf790e755787706e552acf5a525a8a51d880c893890e0318771ac208b44`  
		Last Modified: Tue, 01 Jul 2025 09:06:13 GMT  
		Size: 1.9 MB (1861471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a91546956a4e75665af7415f033c4997b9c77380be628feed69d9ae1232253d`  
		Last Modified: Tue, 01 Jul 2025 09:06:12 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:f79898d9cc3673ad582561c69515f7bee6e60cf576f3caa3e1695326c5275666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd23d04ff8fb3a7849408900a31a237d0e7edf3a3edc084649b87b8d6734cf6`

```dockerfile
```

-	Layers:
	-	`sha256:5258961b5f334840fe1e9fdbec0e1982feffaf9a28fa9f3a0ecf143488830816`  
		Last Modified: Tue, 01 Jul 2025 11:10:50 GMT  
		Size: 27.4 KB (27414 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:eeacf6b72d2bc5c7f38032ae62a418044f3ba672a80733374ef701d7d7304f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141927084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff3cbe5d2bcc7e00c5eddec26931e19ed9ad94243cb13d406da0dec91ad5621`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.22
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef237a39acf4f8b50140ea0e65e44fb78759dd5c3014dea07a2e868cbaea5448`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d1f66f2aaac83b6eaf2006cda16a0feae7d183fb4de3fc7f021a3b94f4d2f5`  
		Last Modified: Tue, 01 Jul 2025 02:37:09 GMT  
		Size: 76.1 MB (76149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834cb9f18ec360ae1dafdba9049fa98c9a4c9dff8f407122be76f6644c8deb27`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd8dd9272c2deda3fe0036b7d36309c16f89e8e7e27eccc8a03fb68cdd395d`  
		Last Modified: Tue, 01 Jul 2025 04:00:35 GMT  
		Size: 12.7 MB (12662620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d0825cfe99539098b6cae5cdca3c89bdbe27b5d79d449068433330dccc5ce2`  
		Last Modified: Tue, 01 Jul 2025 04:00:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892a49c324b105a0450f4f731e40be52375945f984f84ba9b3dcb0eba714caf`  
		Last Modified: Tue, 01 Jul 2025 04:07:50 GMT  
		Size: 25.4 MB (25405949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a046cead5c72b8df9aebf052241961b2424d2232ec90665e9a5c23e6f046108`  
		Last Modified: Tue, 01 Jul 2025 04:07:39 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9983fc55315a3fa43b57af631cf207858b1c8704023bf7c39eb15eec17ad04f`  
		Last Modified: Tue, 01 Jul 2025 04:07:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2f932421f6dd295486c1d874ed60d136db8b585a9479442005d0a011c01f48`  
		Last Modified: Tue, 01 Jul 2025 04:07:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4982234eaf27e3b41ab1119bc802204b1c01e913f2b32091fbca08118e7bf01`  
		Last Modified: Tue, 01 Jul 2025 04:07:43 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca02e467dc2152a0217d24b0400c51bba46ea7c47362dcbe256365868f399c11`  
		Last Modified: Tue, 01 Jul 2025 18:06:19 GMT  
		Size: 1.0 MB (1035359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447cd2cb358ee572b9fef3ce9b02cc11ed5dc43cad13f00f853e770fb2fb4d77`  
		Last Modified: Tue, 01 Jul 2025 18:06:19 GMT  
		Size: 858.6 KB (858563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fea476a6fc8a6ef4be102b827b2beee0864ce5bcc0ab1df69269c3b274f121`  
		Last Modified: Tue, 01 Jul 2025 18:06:19 GMT  
		Size: 1.9 MB (1861467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d443df5a7d0cd8b9ac323c178b2a1e4c21186dde294b5c75dd2c1649e05335`  
		Last Modified: Tue, 01 Jul 2025 18:06:18 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:617cb595d14ccd035a6524933b6be0e81badb3ecffc3c0a231195487206f8810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284bdbd8766878f065d9961c41c7f42f4411c84576205e8c2682c6768949d219`

```dockerfile
```

-	Layers:
	-	`sha256:7bcfd65bc5215c852932d34b27e15eff0959e1edc69ec8d27803b7c72ea12986`  
		Last Modified: Tue, 01 Jul 2025 20:10:35 GMT  
		Size: 27.4 KB (27414 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:5503b6656d29738630c97a462f379e74abddc79ab5f5e0ba5d142a67bfeb78ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170527408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694047aab183c9eba0b831c87a60a2023ee990b9fe98b2fc3bea0a399a62a5a2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.22
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11709a68ca8c2093073c9a1d4b656c3cf0443563f219a68b0b4d26313c3ea1`  
		Last Modified: Tue, 01 Jul 2025 03:15:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5584d1cd13b2f94aca836225a1f54b5de7c1c9943fe27f25088a0be3a7059a`  
		Last Modified: Tue, 01 Jul 2025 03:16:04 GMT  
		Size: 98.1 MB (98130658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f9696b074c2e8b1d467becd89db85a06286c5c522e385d7dfe3d5c3e8c565`  
		Last Modified: Tue, 01 Jul 2025 03:15:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5d77ea42fe176a612fa325478c432fd60345a9d1c25cfd2596bb9f769deddb`  
		Last Modified: Tue, 01 Jul 2025 04:40:35 GMT  
		Size: 12.7 MB (12664531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3381f88af4e5bb2188e1c741e7fa55a98fdea51611706fd139998ec449626593`  
		Last Modified: Tue, 01 Jul 2025 04:40:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba6733ce2400d959dc9de9319c809e7c9367861cc3e7f0d83c93c03cf596249`  
		Last Modified: Tue, 01 Jul 2025 04:48:57 GMT  
		Size: 27.8 MB (27815721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46232951dcae3827b80a484c987955a7f63f2db2207bd332b96a013d2a294c8`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c35e5c8c4524ad3a2aaa8b03892ab1b5537a981a0f51aa8c095b17e9407e05a`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ebf3dc2bdfbd742fb067e2890e93aa40783c69ece95f52d45325df80b43849`  
		Last Modified: Tue, 01 Jul 2025 04:48:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00adee5529ea98b4886bce6e9250cadd330cc16d7e4822fc72835cf28d07d83e`  
		Last Modified: Tue, 01 Jul 2025 04:48:55 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329b2d112df22ae94a24a7e9d9d8363b3d5acd4884e3c513d8bed214c04eebc4`  
		Last Modified: Tue, 01 Jul 2025 13:06:56 GMT  
		Size: 999.3 KB (999348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d619fc06b965a2a8c67c744e6d5ed2c9c1c05606dc2c246ae158cb329414d7`  
		Last Modified: Tue, 01 Jul 2025 13:06:56 GMT  
		Size: 963.3 KB (963257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd97f8a419901beafb06cfc6fda1103275427a43976e6288b4765206641b2956`  
		Last Modified: Tue, 01 Jul 2025 13:06:56 GMT  
		Size: 1.9 MB (1861469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659140511f2e1a67d7e5311606ff84a57de228ecc91a31f3199a48c34270a8f`  
		Last Modified: Tue, 01 Jul 2025 13:06:56 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:df672244e88e1687edd60627716f04642662ed0c45cc9f1c1b1998ef52efada3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e103e1e4e8f763daeeffe5547e0c3514da613f3975622fc5562f96b3e7cf76`

```dockerfile
```

-	Layers:
	-	`sha256:a9e0909c6cb912618ed0173b5d5e0c1810093477f3d80d5878b72e565714a754`  
		Last Modified: Tue, 01 Jul 2025 17:10:30 GMT  
		Size: 27.4 KB (27442 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; 386

```console
$ docker pull postfixadmin@sha256:456b3593e94bc009d9f09ac91af83274430a58db29ec8a13f5fd2fe857951354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175649484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae151980b33fe7074bbf91b1e65755e00398b38848f728e86d2646c57deaa377`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.22
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208d45de7dfd917ed8f40d4093b493768c4b0cbcf35577fe1ac13fdbde5b18c9`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b51fe9cca38fc5f045d0e6194c628fd9a8ddc008549837701f6a4fac3fed9e`  
		Last Modified: Tue, 01 Jul 2025 02:20:04 GMT  
		Size: 101.5 MB (101515122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a98c8659e1991fd6d00c45097475da18db9e844662a8b7e8770c42227abe64`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d195a01c27282f0402501b094be9b79c346a1d1916c690336cec605c0f708b9`  
		Last Modified: Tue, 01 Jul 2025 02:20:00 GMT  
		Size: 12.7 MB (12663750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621b9f51c243086ac493b9f8fd60802178a550a854f59c82de039bcc2e2e2d1c`  
		Last Modified: Tue, 01 Jul 2025 02:19:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29845d7b28a1879fe589cf9305eb39744c1003bc131fb9382134fc1f037986a`  
		Last Modified: Tue, 01 Jul 2025 02:20:00 GMT  
		Size: 28.3 MB (28337321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31f3912fb44c5493fb0452eafb243b2c426ef5e622ec08f6e9adbcc4451c8bd`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a0743a834d375589bd01c1e82fc50cb558e95114bed621713235dae1ae0ba3`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dff81f7275f0fa98afc1eb8b1119fd1e01696bcc01bd5c0b4a90fedd959e72e`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4344be67fdc968ae25fdde02e2c6c17f3b07ee12b0f5761b8dface7a336c1db7`  
		Last Modified: Tue, 01 Jul 2025 02:19:59 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fec8eeca72c06b0c7bc20e92593a3d94053c16417a76b2e29dc79ab905da844`  
		Last Modified: Tue, 01 Jul 2025 03:19:55 GMT  
		Size: 1.1 MB (1054082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23ffb1e1d094105e0f8e1fe0d0696504c80d5f70c40f232922da6273f280b79`  
		Last Modified: Tue, 01 Jul 2025 03:19:55 GMT  
		Size: 990.6 KB (990562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49769f837d94eac19101ce00236fe6bf4c9d2dfb7426c07642ae3fe35b3bcc1`  
		Last Modified: Tue, 01 Jul 2025 03:19:56 GMT  
		Size: 1.9 MB (1861467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c98b3338739bfba1defbec6bb28766ed3852c2bce7503432a8c71c08847c63`  
		Last Modified: Tue, 01 Jul 2025 03:19:55 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:12b08876f84909579ca8c72bc8efe71d45722565f5fd7de0935d3ec80166cfe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ec818d292932a29ca3229fb835ae69b9e8a7823dd6da0bb3ce954e7d9be84d`

```dockerfile
```

-	Layers:
	-	`sha256:76a24d28e9eff521263a510c9f862bbfb01b552d1dcc0bc0b2445ada2110bf86`  
		Last Modified: Tue, 01 Jul 2025 05:11:20 GMT  
		Size: 27.3 KB (27281 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:d18367ee2756252eee50f1985994f024790b17a3a0df38da5b63780915b0eeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152527998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aee2c2b316c1fda39dc16dbacd1cdf7bdce793395a833e2cc92048e18d30a3b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.22
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbaad9c575de27a78ec9ecda6c0f021d7843e351bd682abc01e8edfe52f3239`  
		Last Modified: Wed, 11 Jun 2025 01:37:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6a316d668681533c7b3478f23726ec4bacd15c983a623a42fa361b70101e1b`  
		Last Modified: Wed, 11 Jun 2025 01:37:09 GMT  
		Size: 80.7 MB (80670453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cd671d1ab5d1868581d736fae7d6e8644a5d539113a35ec3166149f5fc9c9`  
		Last Modified: Wed, 11 Jun 2025 01:37:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4212d7fefddbcc05d6c8358c4d91e28a3c30e10d2a5dfd2fff6150fe61730ba7`  
		Last Modified: Wed, 11 Jun 2025 05:04:09 GMT  
		Size: 12.7 MB (12662164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745d24827e7bcb5be8a9c249a9904b0a2663563a8a8470d0570fa26db04c85b`  
		Last Modified: Wed, 11 Jun 2025 02:51:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68ab17a83857fd9143fa3999ca86eb8f2c0b1b960e76cda8b7e1fe8ce998d6`  
		Last Modified: Wed, 11 Jun 2025 03:23:13 GMT  
		Size: 26.9 MB (26917016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31715d80e0a3bacbcce8bcb5fb31955713daad52be416cfc87e25ce59789dc7`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d7cb0fa97846ee1c404a5371ba305b4e795358d2db6ef8cf67a34e62c49bd7`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77c7606a1859a7de246c75b0c847e81fad6b8b4360bed40732a6b9acc2afb8f`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ac771756fac3bafedcf21bfefe04160a455c1a7319e09b7eb2465e40a57733`  
		Last Modified: Wed, 25 Jun 2025 19:56:24 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4547f343c951e65553ab068dbbed4b892b00921af2eabcee2c17e7f8b41f4d`  
		Last Modified: Wed, 25 Jun 2025 22:12:12 GMT  
		Size: 950.6 KB (950559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d523a4a9a56f324017744363c7ca101719778b677533e25ce81853a548841df7`  
		Last Modified: Wed, 25 Jun 2025 22:12:13 GMT  
		Size: 934.8 KB (934838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0b1f607461a41f77669bfe664f647008863cb137f8e2b16a4bc2b90a36b87f`  
		Last Modified: Wed, 25 Jun 2025 22:12:13 GMT  
		Size: 1.9 MB (1861473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a02035f4a7960bd3954b7a049d93b4473727ed3dd459af7866b8dc3eeafc7b0`  
		Last Modified: Wed, 25 Jun 2025 22:12:12 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:a74b3f4eebcdecd8c5712a6a75336d5cf8d7b10f1a893d5e2f1f18182ddd609e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18159515f4b3e26d29427947cb61b1818d5a24c3f76e89f32ac31826719a81e`

```dockerfile
```

-	Layers:
	-	`sha256:5fc2e5e8982a956d665a39da20cb08c8e7ea50be46a802e66b7f3ec4c891c66f`  
		Last Modified: Wed, 25 Jun 2025 23:11:17 GMT  
		Size: 27.4 KB (27380 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:d1090ae2d14110f5a9971d66dfce9935f3cbdccb2631c2c16c67b9eb60de9a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180924571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ed2dc2c9a5d4b841b92ddae0d874d07f9ef6ca60dee8c5847ba246a8aec0a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.22
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceff3d73088eb90a29a3888d344cedd86858df29b36df7932d3fe0d16eda4e7d`  
		Last Modified: Tue, 01 Jul 2025 02:58:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08259e2c7cacc0405f0da4ea7142f0be36234c1b63d584779538944c8319235f`  
		Last Modified: Tue, 01 Jul 2025 02:58:21 GMT  
		Size: 103.3 MB (103326709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fcb5df575fa0806e458d09147e66250dc80c744fe65c46881d5d2395c98374`  
		Last Modified: Tue, 01 Jul 2025 02:58:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed11498eee63906d06a0d4f4eb4f2f82fd8c136b83c10cf0ff318d8f1842d4`  
		Last Modified: Tue, 01 Jul 2025 03:46:05 GMT  
		Size: 12.7 MB (12664075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bd8237575b0bc18f7c1a004275025cdfebf43c3f6280a2a7a6222d6ac2053e`  
		Last Modified: Tue, 01 Jul 2025 03:46:04 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9057d3e1b39a6343b4e2c6ef433175c143f6bf367a4f20ef79de7d9b29b320b`  
		Last Modified: Tue, 01 Jul 2025 03:54:08 GMT  
		Size: 28.9 MB (28894401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e480cee0386b2ef518dc619d80b651cfae5171bc6fea791d47f270723b7bf9da`  
		Last Modified: Tue, 01 Jul 2025 03:54:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702178c015d87efb844dbaff0d3aecd971dd92f3342296d38fdbc2fbce8bba41`  
		Last Modified: Tue, 01 Jul 2025 03:54:01 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa2381189dee0ebf13131823e08eb6a1cf8c43cce44e49869b7188b4c040ac5`  
		Last Modified: Tue, 01 Jul 2025 03:54:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dbdca9dfee4dcf2604ef3810826a5e568264b320a38cc110c668a4b12627d6`  
		Last Modified: Tue, 01 Jul 2025 03:54:01 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a308cd18104e4a66e268a6d0c112fa71cd5f93d8c71d3ff4ca4166ed75527348`  
		Last Modified: Tue, 01 Jul 2025 09:34:41 GMT  
		Size: 986.2 KB (986158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd99d96a1938a43b7e29f717286a2645a2293df8bd0859673fd9cbfe31794fb`  
		Last Modified: Tue, 01 Jul 2025 09:34:40 GMT  
		Size: 1.1 MB (1104185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e974aeac4ff43ce932359a60c5b733d42abed228f14c406dff1aab1ab9366de`  
		Last Modified: Tue, 01 Jul 2025 09:34:41 GMT  
		Size: 1.9 MB (1861469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8acfd7b484fb64d8b10a85c8fb4857f133ca852c9389ef577ce728e7186ff0`  
		Last Modified: Tue, 01 Jul 2025 09:34:40 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:3a36869cfe9a2a26c1f0e945b90338cf3a223eb351a488ab111c709458eea9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170b110fd2b307ea2d42f3a6e73bced7be70701f1b485b89877412c22a8611c7`

```dockerfile
```

-	Layers:
	-	`sha256:906de48dee402702cb874ad7c2089585681a084bbf4f2be4b20c9f46c2c23e62`  
		Last Modified: Tue, 01 Jul 2025 14:10:53 GMT  
		Size: 27.4 KB (27363 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; s390x

```console
$ docker pull postfixadmin@sha256:1c68af57274b14a63f7c0640dba733c83fc74afcee647cf3fa4c737d00aee387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151178294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5782b3d1c14e6d75e36af1cb9bec55c7f9b6cd9f2501ce077c6a3ad69b5dfc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.22
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.22.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=66c86889059bd27ccf460590ca48fcaf3261349cc9bdba2023ac6a265beabf36
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9c297e4e0ff6968c351ba2bf1e5702e339d74da6d2ee401d883eb8eac205b`  
		Last Modified: Tue, 01 Jul 2025 02:42:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2414908a592d42e715071983fa5a673dbdbf81c963b83bc36a868149c796848a`  
		Last Modified: Tue, 01 Jul 2025 02:42:09 GMT  
		Size: 80.8 MB (80825948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7f41513cce80c0dd493bac0e1dfabcb8d66fd1eda3cc802fee9e00d745a700`  
		Last Modified: Tue, 01 Jul 2025 02:42:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a710affcdf491a329bc925c8c87aa62de4b3bd7d946933c08973b1caced9d3a7`  
		Last Modified: Tue, 01 Jul 2025 03:23:31 GMT  
		Size: 12.7 MB (12662980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe47688d0e94200a5b4cdc46404b2fd582481e8e83dbbbe7873b0c5a42e5e53`  
		Last Modified: Tue, 01 Jul 2025 03:23:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a562dcf13254244ee1693ecd265dd678746774c7994fb9b5dfb7ddb312d8237b`  
		Last Modified: Tue, 01 Jul 2025 03:33:35 GMT  
		Size: 26.9 MB (26928296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf827c18b3aaea085cf26d29bde281c198b7db1b12f24d1687a0731f0f795a52`  
		Last Modified: Tue, 01 Jul 2025 03:33:34 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4f7db203f56678bfe531b40b5ac8d8f5a471e9a4a601fdf36c5981bb9c6e69`  
		Last Modified: Tue, 01 Jul 2025 03:33:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6416e77ac7c89b8026d07ddc7dd6b6428a1aab64e126cb955a45f5b4af7365ca`  
		Last Modified: Tue, 01 Jul 2025 03:33:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e524b6e5230c48621e2a229f1aec11a8b9c902274c6daf8fe7a59c622bc4ee2e`  
		Last Modified: Tue, 01 Jul 2025 03:33:33 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef570f8b5e1177c07c261eebf1862c57ee556a8e9e8506c4af1bb56594b686e`  
		Last Modified: Tue, 01 Jul 2025 08:38:57 GMT  
		Size: 1.0 MB (1034653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a68c531d17ced55e74a0f1f29bca5a96e5a8021dc992a9ce551f8ad0454c49`  
		Last Modified: Tue, 01 Jul 2025 08:38:56 GMT  
		Size: 962.4 KB (962391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e46564a3ff419c48e20301d5ab69669de572e99547dfb91ef1ad345ea27ba0`  
		Last Modified: Tue, 01 Jul 2025 08:38:57 GMT  
		Size: 1.9 MB (1861468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9946b7d47591b368a1386b5772f983018b501cd61e9ee8072825e947e1990396`  
		Last Modified: Tue, 01 Jul 2025 08:38:57 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:05bd33b905363f8353c181355634c13138e6112f5cc00443c9a2f58d3817b238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5603ed3e44bc3e8d37880802d36f730c9cbd1a93c5eb70ed617b568de752d2`

```dockerfile
```

-	Layers:
	-	`sha256:cb02a08a3de0c8c787e00d8279e6985041df0445711534025848e0687e3a5959`  
		Last Modified: Tue, 01 Jul 2025 11:11:02 GMT  
		Size: 27.3 KB (27312 bytes)  
		MIME: application/vnd.in-toto+json
