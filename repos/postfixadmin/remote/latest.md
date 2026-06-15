## `postfixadmin:latest`

```console
$ docker pull postfixadmin@sha256:c21e4b358b2ecc8871913053ff5de6622dfe70fadc0742e4a4e817241c6533f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postfixadmin:latest` - linux; amd64

```console
$ docker pull postfixadmin@sha256:5d6fd52c4a3525e8cc739573010c57983307cb736a47009d6c2cc18e7a89c2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205015069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ff500241c27529253a1e9ca1ee4a17602dac217b01d4e01077b35e7846bbf`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:24:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:24:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:24:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:24:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:24:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:24:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:28:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:28:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:28:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jun 2026 00:28:12 GMT
ENV PHP_VERSION=8.3.31
# Thu, 11 Jun 2026 00:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 11 Jun 2026 00:28:12 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 11 Jun 2026 00:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:28:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:31:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:31:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:31:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:31:23 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:31:23 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:31:24 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:31:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:31:24 GMT
CMD ["apache2-foreground"]
# Mon, 15 Jun 2026 21:54:05 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Mon, 15 Jun 2026 21:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 21:54:22 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:22 GMT
ARG POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:54:22 GMT
ARG POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:54:22 GMT
ENV POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:54:22 GMT
ENV POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:54:22 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 15 Jun 2026 21:54:22 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Mon, 15 Jun 2026 21:54:23 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Mon, 15 Jun 2026 21:54:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:54:23 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:54:23 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 15 Jun 2026 21:54:30 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 21:54:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8087aab715a642138f96cc56d017f6602e06f83936c428343b167226ff0334`  
		Last Modified: Thu, 11 Jun 2026 00:27:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df42c2da9f1661337ee3c91e9db6269b11bed810ba1a907c9428b205de7d881`  
		Last Modified: Thu, 11 Jun 2026 00:27:57 GMT  
		Size: 117.8 MB (117840421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ec0ae568c7ef5b26e7f05810ec34f8ef60b250aeb0fd095a4dd276aca32a3`  
		Last Modified: Thu, 11 Jun 2026 00:27:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2190843fe6b0ddea7af0a62be75ff1ba658beb0ff4c6426c4f734f83285ebd`  
		Last Modified: Thu, 11 Jun 2026 00:31:35 GMT  
		Size: 4.2 MB (4227916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3684cf1a7d298df33763c038af71c634123d42b057525a8fc8029416993a416`  
		Last Modified: Thu, 11 Jun 2026 00:31:34 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb1e1109915ce026ef3195364a00cb99b776937daa03f0facba4bab1af05ab8`  
		Last Modified: Thu, 11 Jun 2026 00:31:35 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f345c9987c93cbc280a8199d1ec417d5b48bb20bd76ffd1c031867e65a60ad`  
		Last Modified: Thu, 11 Jun 2026 00:31:35 GMT  
		Size: 12.8 MB (12770149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840aa0903cad03d257226e9ffb3b8d296681eb76996b031431d1a7dea2e75766`  
		Last Modified: Thu, 11 Jun 2026 00:31:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dd647780b7c900938a7ae0a499f2ca52ce6b1acea49bf08da746e3b9aa30c7`  
		Last Modified: Thu, 11 Jun 2026 00:31:36 GMT  
		Size: 11.7 MB (11715410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fe4dcacdc0c5cd0de5c9affe473ee1bea2e110a03489f5163901b08ab779c9`  
		Last Modified: Thu, 11 Jun 2026 00:31:36 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ed1ded06886d567832e5162180c6c40170b650b7d95de8f4e89f4aa7a929ea`  
		Last Modified: Thu, 11 Jun 2026 00:31:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b9b7578e538d99a22488f4f3edcc7e9fb4e7c6eba96729bf6fe7aff2f7a522`  
		Last Modified: Thu, 11 Jun 2026 00:31:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce8c764daab41d3e4b3cbf9c6dc3213a4c2cc0088b57a96eef9c3737ce5a1bb`  
		Last Modified: Thu, 11 Jun 2026 00:31:38 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba180d51ee2f2dcf5e9eba59e98a70527188e360a436b92324ffef1f7b1af3e2`  
		Last Modified: Mon, 15 Jun 2026 21:54:36 GMT  
		Size: 1.4 MB (1352216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7644b06ed6e758852775ca46b3f93abccf7fe53b7106d5558620a17a5137a2`  
		Last Modified: Mon, 15 Jun 2026 21:54:36 GMT  
		Size: 466.9 KB (466947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaf90e72a96b53d6e03cae7404444a709fe8c736d3ac6952bff48759505747c`  
		Last Modified: Mon, 15 Jun 2026 21:54:36 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0287d9fd3ac9f8fdeb51e5ee41f7555047cd4ed7557518207e7456b61b8f74ab`  
		Last Modified: Mon, 15 Jun 2026 21:54:37 GMT  
		Size: 2.6 MB (2602974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55938ef94925959b4a3bbad2e790c7b8d233b469f11d7ac879db1efca78dd51`  
		Last Modified: Mon, 15 Jun 2026 21:54:38 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afd9aec2924c1cb7af2b5a9c827f6195ed03fb841925abf899b98bd1818cc52`  
		Last Modified: Mon, 15 Jun 2026 21:54:38 GMT  
		Size: 823.3 KB (823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609b94708f88971df77e69aef27077e18e0281cc6a7bdecf014a3a1454ae1936`  
		Last Modified: Mon, 15 Jun 2026 21:54:38 GMT  
		Size: 23.4 MB (23415435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:5b9b9e32003bcf0429fa1a3df37522b7576843b55e2597f7bcfed7883ed23984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 KB (49974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46927f44c9e586e9c11352042a55e766edbbd4e8a30dcc8c0e60aa9c7011c4e6`

```dockerfile
```

-	Layers:
	-	`sha256:32a8d8e7e7e005c8a373de474e0f13dfaf6263bb615f6c0fc14968cc7599db9c`  
		Last Modified: Mon, 15 Jun 2026 21:54:36 GMT  
		Size: 50.0 KB (49974 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:d8e108792019c0d8d724af88d9c02d48f7d6b46b32538e7931ab0c8cd9eaa239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167631068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6259e72ce5eb9471d1bd5bb5cd3e4d8075e9e5d871faf3dcfe6fcf1c817d5d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:24:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:24:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:24:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:24:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:24:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:37:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:37:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jun 2026 00:37:48 GMT
ENV PHP_VERSION=8.3.31
# Thu, 11 Jun 2026 00:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 11 Jun 2026 00:37:48 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 11 Jun 2026 00:37:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:37:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:40:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:40:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:40:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:40:38 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:40:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:40:38 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:40:38 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:40:38 GMT
CMD ["apache2-foreground"]
# Mon, 15 Jun 2026 21:53:47 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Mon, 15 Jun 2026 21:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 21:54:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:12 GMT
ARG POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:54:12 GMT
ARG POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:54:12 GMT
ENV POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:54:12 GMT
ENV POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:54:12 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 15 Jun 2026 21:54:12 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Mon, 15 Jun 2026 21:54:13 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Mon, 15 Jun 2026 21:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:54:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:54:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 15 Jun 2026 21:54:24 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 21:54:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6483b1ff32791a5e01344329589dd2d3245327e467caa1c2ca0acc9e8ae20205`  
		Last Modified: Thu, 11 Jun 2026 00:27:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb7146680508f622139aae64cd7cf004a7e101911f72f4bb2e25a6c45289870`  
		Last Modified: Thu, 11 Jun 2026 00:27:23 GMT  
		Size: 86.3 MB (86256050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cbfa8ee038f286b8e76a13b94fd58d9bd74f37f8eef7dd9f44e3480dcbe41c`  
		Last Modified: Thu, 11 Jun 2026 00:27:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fa78b8ec57f7aa9f3cfde53cbbd35c98595c8f94a58bc91536853326f37e65`  
		Last Modified: Thu, 11 Jun 2026 00:40:49 GMT  
		Size: 3.8 MB (3756637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ffad4d3e68b82453b2a4498b0eaac1aaf3b5b99b33cef381702881d24c0a00`  
		Last Modified: Thu, 11 Jun 2026 00:40:48 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923ad9e18740ecc68c21ac6d90a803cdd5a215b418a4ffc91804164b3442a59`  
		Last Modified: Thu, 11 Jun 2026 00:40:48 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b2835bdcde2311fb61fa930fc76c1242a3bab241b1c730c1a8c7a832a9f3f`  
		Last Modified: Thu, 11 Jun 2026 00:40:49 GMT  
		Size: 12.8 MB (12767745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73fee8e32087d743319df1f7abd97632b0cd1d04ccd6013e4c6ff8d0b735db5`  
		Last Modified: Thu, 11 Jun 2026 00:40:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52a0666f1486abae27faf7a80904d1066cecfe264fd1fd172f66d99158c18a8`  
		Last Modified: Thu, 11 Jun 2026 00:40:50 GMT  
		Size: 10.1 MB (10074064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c0b51bd800308768411146c4f35e17b9288beeb38b61a915eb3a544a2a13c7`  
		Last Modified: Thu, 11 Jun 2026 00:40:50 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20af4caf9f34fa53b0dcf243608186ec617d3d8e1801ab7a485ff4253c48812e`  
		Last Modified: Thu, 11 Jun 2026 00:40:50 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8ddc8001c6140ac51e4d774924ef81e300eccd2a92121631135f2ff340f78e`  
		Last Modified: Thu, 11 Jun 2026 00:40:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd199efd76c788d36efd91e0cfa15e3ef7afc644004f30d5c9f364243dbad49`  
		Last Modified: Thu, 11 Jun 2026 00:40:51 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ff31dd4d909adc56045fb4831722d272b8b38a2dac826a0fce646d876519f6`  
		Last Modified: Mon, 15 Jun 2026 21:54:30 GMT  
		Size: 1.3 MB (1289486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5dd31350acd30b058fa981bd22c5298dfda36468031e2818d1f209565d8c75`  
		Last Modified: Mon, 15 Jun 2026 21:54:30 GMT  
		Size: 421.7 KB (421673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45019924b9900567cf9fd8456ff0fcb010102aaa6aec462bd2788c82064406fd`  
		Last Modified: Mon, 15 Jun 2026 21:54:30 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dfa0d5a696ff21fb7887346aa7d5bb9c4241a2a015ab6c7c89bb6e31981f1d`  
		Last Modified: Mon, 15 Jun 2026 21:54:30 GMT  
		Size: 2.6 MB (2602978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1becc3f2a1eb4ed0a499be2c1450ab8e9a51579a47bdfab08bfde748666a51ca`  
		Last Modified: Mon, 15 Jun 2026 21:54:31 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be87f3ccec404fd17fd085df3b79c3b1a4d84f48d5c13aff6ef867169fcadd5`  
		Last Modified: Mon, 15 Jun 2026 21:54:32 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15d0bd381c121310daa58aa23d6808d54252fa587273fa2c748ac3b5866ab5f`  
		Last Modified: Mon, 15 Jun 2026 21:54:32 GMT  
		Size: 23.4 MB (23413213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:b98107e0bc24c3d6d6ffcbc4333600b4cd8e30c360b7067a2730ee58394a29c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a6c0d141db0a2caae88766786defbd9cd7e99541719072dc2a6cee166b285d`

```dockerfile
```

-	Layers:
	-	`sha256:0d275ca8a465c3ea39008ee14d4bada4a178db5efec4875142250e62eed4837f`  
		Last Modified: Mon, 15 Jun 2026 21:54:30 GMT  
		Size: 50.2 KB (50152 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:ea53637d59f348099a098e28e67961fcb5c788aba6964acbb3853fffc66aced4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197716010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f917b9ab672c0c92af0efd4b2732a0da969d69b067564a3e84ef5324d1d3239`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:28:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:28:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:28:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:28:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:28:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:28:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:28:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:28:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:28:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:28:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:28:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:28:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:28:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jun 2026 00:28:55 GMT
ENV PHP_VERSION=8.3.31
# Thu, 11 Jun 2026 00:28:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 11 Jun 2026 00:28:55 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 11 Jun 2026 00:29:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:29:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:32:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:32:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:32:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:32:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:32:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:32:46 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:32:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:32:46 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:32:46 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:32:46 GMT
CMD ["apache2-foreground"]
# Mon, 15 Jun 2026 21:54:20 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Mon, 15 Jun 2026 21:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 21:54:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:43 GMT
ARG POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:54:43 GMT
ARG POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:54:43 GMT
ENV POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:54:43 GMT
ENV POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:54:43 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 15 Jun 2026 21:54:43 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Mon, 15 Jun 2026 21:54:44 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Mon, 15 Jun 2026 21:54:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:54:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:54:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 15 Jun 2026 21:54:52 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 21:54:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a88fa296e8bb585995adc04f532701875bc1881e3404b503d5107fa1f3643b`  
		Last Modified: Thu, 11 Jun 2026 00:33:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e68f282164f5281b6449864a848e297a4d3af03c0cea213bc1a6f4a30434d`  
		Last Modified: Thu, 11 Jun 2026 00:33:11 GMT  
		Size: 110.2 MB (110169662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2338c0dd5a9600ba5379291529c129bbda1a7145abd38a0ac4b162baad30a495`  
		Last Modified: Thu, 11 Jun 2026 00:33:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b908a0625ed9962bc3b3667f4cc2b27f6f0d105599051de1cb604bc8ba41db89`  
		Last Modified: Thu, 11 Jun 2026 00:33:09 GMT  
		Size: 4.3 MB (4308276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5488bea1a6d56ee8d9533a4cda827ff325dce59280ca3b1bba07051c927b137f`  
		Last Modified: Thu, 11 Jun 2026 00:33:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1739a98c05bae8520378f4cc869b74324503d49b2fb5e81697148ed9b20b27eb`  
		Last Modified: Thu, 11 Jun 2026 00:33:10 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d805fdc5a0dd3f8da8d6c519b4cb5f163fbafb420b715aae24981a94a69c477b`  
		Last Modified: Thu, 11 Jun 2026 00:33:11 GMT  
		Size: 12.8 MB (12769742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8dd80693b17424ef7b1bcf10891fc839f776c152aeaa1ee5920943ea511cc6`  
		Last Modified: Thu, 11 Jun 2026 00:33:11 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad62adaa0bcfe0115eeedb5912ffc150c88a376d86053ed358b2b9c9480122d7`  
		Last Modified: Thu, 11 Jun 2026 00:33:11 GMT  
		Size: 11.7 MB (11734663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883ad7a9de545d3cfe5534a9d15483aa46729bad4458c1aee205a19f92e47bda`  
		Last Modified: Thu, 11 Jun 2026 00:33:12 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ea0853824913ecc74e4e32226285182bc1c4590e93c2833658909fd67ec9ea`  
		Last Modified: Thu, 11 Jun 2026 00:33:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11896591ec9c109686e8798bff7072e8697184bfc66e4c81cf3f710bfcd2e854`  
		Last Modified: Thu, 11 Jun 2026 00:33:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d3645cd3a3af35de2ff2ee735cbc75fa3db7336a0582e638b25ba00f978416`  
		Last Modified: Thu, 11 Jun 2026 00:33:14 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9185ad1bc56c729493c539503af3e07354f1d2070430b9b46af7f4e4be5ef6`  
		Last Modified: Mon, 15 Jun 2026 21:54:58 GMT  
		Size: 1.3 MB (1266086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd9db72b6fe899cdfb16c7dc657f83c0f42770fb088a4922ba71362d8895609`  
		Last Modified: Mon, 15 Jun 2026 21:54:58 GMT  
		Size: 462.7 KB (462740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115476bfb40804876250bafc469ccdd2b73530db550a7018a7d8e32aeb424f9a`  
		Last Modified: Mon, 15 Jun 2026 21:54:58 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fdf164c16bacf94d76602f088809758aad73eec285fc757323eb57b43f1c55`  
		Last Modified: Mon, 15 Jun 2026 21:54:58 GMT  
		Size: 2.6 MB (2602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ff2b0ba91ff24b947e4ed085f808591713c16d117e8e337e24dbc18944bfa5`  
		Last Modified: Mon, 15 Jun 2026 21:55:00 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91147335bd3aa6648eaf24e0f6585280b0e35c66f41ce2ad96ab20979db811fc`  
		Last Modified: Mon, 15 Jun 2026 21:55:00 GMT  
		Size: 823.3 KB (823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dd44f480a72e7565dc0cb91092ae9b519c39ad7a3146ab552b8d740f4f3769`  
		Last Modified: Mon, 15 Jun 2026 21:55:00 GMT  
		Size: 23.4 MB (23415143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:734cd6917ec0667b591d6a6379df736e05c22f327b18b9c7dd8f71b7db5f00f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11c8f15dfbb4d18910ddb396ccdc090f33eb685ed2303cb0dfab7aed1d51462`

```dockerfile
```

-	Layers:
	-	`sha256:593cddea79ce3fcddab5e1273322ecdff1460c906a1f68f82a7fac99d69a3490`  
		Last Modified: Mon, 15 Jun 2026 21:54:58 GMT  
		Size: 50.2 KB (50213 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; 386

```console
$ docker pull postfixadmin@sha256:8e8f794ad68362240d10cbbd4ce206a1e8cf754f43c6fcbeca18983af751fde7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205250633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84a91767cac09c18d0d0a492a0309e22b51f0bdb7a1c59837ce660a8cb23b4b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:18:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:18:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:18:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:18:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:18:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:18:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:25:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:25:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:25:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:25:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:25:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:25:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:25:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jun 2026 00:25:41 GMT
ENV PHP_VERSION=8.3.31
# Thu, 11 Jun 2026 00:25:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 11 Jun 2026 00:25:41 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 11 Jun 2026 00:25:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:25:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:28:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:28:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:28:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:28:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:28:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:28:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:28:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:28:31 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:28:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:28:31 GMT
CMD ["apache2-foreground"]
# Mon, 15 Jun 2026 21:54:10 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Mon, 15 Jun 2026 21:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 21:54:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:30 GMT
ARG POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:54:30 GMT
ARG POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:54:30 GMT
ENV POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:54:30 GMT
ENV POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:54:30 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 15 Jun 2026 21:54:30 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Mon, 15 Jun 2026 21:54:31 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Mon, 15 Jun 2026 21:54:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:54:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:54:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 15 Jun 2026 21:54:38 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 21:54:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17fc7f919f95a72293bf052bb27a17c9d15c32dc814a08b349b09e2a5605a5a`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b81ad9ca6036d33b964953f5a7777818ed14d0d4719032caed5fc0ea304f88a`  
		Last Modified: Thu, 11 Jun 2026 00:22:14 GMT  
		Size: 116.1 MB (116142537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf4bfc39b9bd3b5205f39d18e5be8bbda36e7a2ad888e2a176e27af6daaf1b8`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d75b262f915086462ed3a49660d0851d37a27e92b10e7d555a6a1a93cbe98f`  
		Last Modified: Thu, 11 Jun 2026 00:28:41 GMT  
		Size: 4.5 MB (4459145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf6cb3bbf9b64fe6c0bfeaae7e778dd7d3959ed6ac4918048132604c697dcb7`  
		Last Modified: Thu, 11 Jun 2026 00:28:40 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf65af3f2c913896809f2d8dbc5f9ac8dfc17ee8b674b0baf73320c6e93a9603`  
		Last Modified: Thu, 11 Jun 2026 00:28:40 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e531bd9fcad706d42d0a530bc6117355dfad0411dcc4acf3ea7aafb0871302`  
		Last Modified: Thu, 11 Jun 2026 00:28:41 GMT  
		Size: 12.8 MB (12769174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba698eb1f542d65363420693313311719261a88601c79d707e91cc584ce57790`  
		Last Modified: Thu, 11 Jun 2026 00:28:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b54ae9ca74109c2ae9b447804dd7305a7bd8291921b7b1c93aa13a63b9cd58`  
		Last Modified: Thu, 11 Jun 2026 00:28:42 GMT  
		Size: 11.9 MB (11928935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5212394ea6ad14a33baea78d1e96b5e2880ecccd1c8f44ed0c95646c9ae503`  
		Last Modified: Thu, 11 Jun 2026 00:28:42 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a782af7f729f18c60174e2f77270db7e3b75a194e120be9e7da0575d2833e63`  
		Last Modified: Thu, 11 Jun 2026 00:28:43 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e051778bc07affc1d778772f397be232adf33ef857edbebfe01767a84b9929df`  
		Last Modified: Thu, 11 Jun 2026 00:28:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c1917d95fc881199b154389822ce35eb9e3f8a64e3327ab6852e606bc9b0a1`  
		Last Modified: Thu, 11 Jun 2026 00:28:43 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73fb3a8c47ece7cb0c9aeae80454d10857a23becfa23f6c960716d588dea6f6`  
		Last Modified: Mon, 15 Jun 2026 21:54:45 GMT  
		Size: 1.3 MB (1311156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28bf712a01201e293d79f7b36eaddcd4d7a474657eb7428cfd5590a288ef5c0`  
		Last Modified: Mon, 15 Jun 2026 21:54:45 GMT  
		Size: 482.6 KB (482607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514c24303b55b1ebb175d5c6235a6e11630c09946f49b9f19744ecd399e5c688`  
		Last Modified: Mon, 15 Jun 2026 21:54:45 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e484fce39a98e3175d2a434ea7fe92ba3768225f8793c2fd17ef3743fce628db`  
		Last Modified: Mon, 15 Jun 2026 21:54:45 GMT  
		Size: 2.6 MB (2602975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a3bcec5e8d89b667e9dd031b596ab396692b0869624274590231740e31898`  
		Last Modified: Mon, 15 Jun 2026 21:54:46 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb031a1aa3a3e97b849fae7c64293045acd52f2abd7b52673c0813d24d5fae6`  
		Last Modified: Mon, 15 Jun 2026 21:54:46 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe33a4d40b94989035fd324aa2d433ee42fdc6ae8fd03012573c34247034140`  
		Last Modified: Mon, 15 Jun 2026 21:54:47 GMT  
		Size: 23.4 MB (23414694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:07ce744bfd5fe445549c57061f41fbfd2b4b6f8d834db20685306522e4b116db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 KB (49907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7971272ab88b0b6607ba5c08b943ff2c0ae316b9a5bd5cee418d4c1ee2ca7789`

```dockerfile
```

-	Layers:
	-	`sha256:3247d9ee402091bc380244e689d4fd31ad244642bc878c04430e695a0b784b86`  
		Last Modified: Mon, 15 Jun 2026 21:54:44 GMT  
		Size: 49.9 KB (49907 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:a556c6ba2e46e47c99197257f0c53e1c09b7f25ebc15f1768051eb9481aca959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201608972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d73e8411f8efbf1594b69534120c6e730ef79a949814f7382c8e7a33ee7ec56`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:00:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 03:01:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 03:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:01:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 03:01:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 03:01:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 03:01:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 03:04:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 03:04:37 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 03:04:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 03:04:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_VERSION=8.3.31
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 11 Jun 2026 03:45:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 03:45:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:49:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 03:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:49:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 03:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 03:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 03:49:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 03:49:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:49:55 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 03:49:55 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 03:49:55 GMT
CMD ["apache2-foreground"]
# Mon, 15 Jun 2026 21:53:06 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Mon, 15 Jun 2026 21:53:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 21:53:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:53:48 GMT
ARG POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:53:48 GMT
ARG POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:53:48 GMT
ENV POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:53:48 GMT
ENV POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:53:48 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 15 Jun 2026 21:53:48 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Mon, 15 Jun 2026 21:53:49 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Mon, 15 Jun 2026 21:53:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:53:51 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 15 Jun 2026 21:54:08 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:54:08 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 21:54:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76942a34176bffe275c52bbf371c6a83affed73bab30526f495165cbc094b557`  
		Last Modified: Thu, 11 Jun 2026 03:06:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d446e1e0a4b12d658b3e858628249ee37b9a22d29bee0c2dd4686159c2e43988`  
		Last Modified: Thu, 11 Jun 2026 03:06:22 GMT  
		Size: 109.6 MB (109598344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e8bcde33298859f8eb941222505617b97a665c07395dc23100212e1d7a25d8`  
		Last Modified: Thu, 11 Jun 2026 03:06:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7d51c61734b9f5fbda00c651630c71a2ba54dd9247e49484c77277fe2ce0c`  
		Last Modified: Thu, 11 Jun 2026 03:09:41 GMT  
		Size: 4.9 MB (4883580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b6856b13dd8027fcf9d867bed35ded648e583baea3696392c17d0fa8bcaf36`  
		Last Modified: Thu, 11 Jun 2026 03:09:40 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8920a67f463e815da5e5dbdfa3a5ee6626ca03e2d3a8f2c577e66b82002ed9`  
		Last Modified: Thu, 11 Jun 2026 03:09:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecf3323b62e990c37c1f8e3206f5b43160c4f64622d842508a2b87bb6cced9b`  
		Last Modified: Thu, 11 Jun 2026 03:50:18 GMT  
		Size: 12.8 MB (12769266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5921a42a649de100b6b345df6239f3ed13a1c7153368ea4ab3c0aad43644657`  
		Last Modified: Thu, 11 Jun 2026 03:50:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790470697b7432c50aedb6d2289af5d4e247dffc40015a65483b5e726dfa054d`  
		Last Modified: Thu, 11 Jun 2026 03:50:18 GMT  
		Size: 12.1 MB (12125179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aefb5053629b2435a546abc407b1aa7032ae971c9c63ded37c63edfdb5620f`  
		Last Modified: Thu, 11 Jun 2026 03:50:18 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c829d94229f4e531f4eb50de7911ec76c043e08e088d75e09c88d57650550db4`  
		Last Modified: Thu, 11 Jun 2026 03:50:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fdd1768d1692eb82ef43b3ba35cdd744408bd76a18c2264952ba7eae3ad2a4`  
		Last Modified: Thu, 11 Jun 2026 03:50:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9221d667a58b53daffe99020f1c3745fd3628516133d674b0981a8432f02545`  
		Last Modified: Thu, 11 Jun 2026 03:50:21 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4651829ad8b1a2ec726b245573bd273388838d1fa2a0ceef19e191a78c1d194b`  
		Last Modified: Mon, 15 Jun 2026 21:54:19 GMT  
		Size: 1.3 MB (1268498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9837325c80a800935ca8db8072b252b4d806aa6482f13021c50b88d34edcfc41`  
		Last Modified: Mon, 15 Jun 2026 21:54:19 GMT  
		Size: 501.8 KB (501752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b349f4f3c14939bca9faff73a53e2397ade2db2deded759ace8c8f918a70b1f`  
		Last Modified: Mon, 15 Jun 2026 21:54:19 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee05bf0799cbe9402080ce07640f7541d1e552d34997b206bdc0f359384670e`  
		Last Modified: Mon, 15 Jun 2026 21:54:19 GMT  
		Size: 2.6 MB (2602972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6f2e0c42cb405c73a096635e05527268d61acd953ab53a88d3413d13c1ccc1`  
		Last Modified: Mon, 15 Jun 2026 21:54:20 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2cad97b490442fa37882abf4bf87fd22bff3933c603bdc2c926e4568dd25b3`  
		Last Modified: Mon, 15 Jun 2026 21:54:21 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80cfc7438a12b7115f2457a2033580166a82aa4b20e573b8cf9e00834109eda`  
		Last Modified: Mon, 15 Jun 2026 21:54:21 GMT  
		Size: 23.4 MB (23414827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:05d2c700983953a3dd4d866838b2a756de0d10215bac9a7e9c473936077edd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5436efca3199ae8c7f83cc4edd5abe7b1cf143161c780937f8bf8290f52b677c`

```dockerfile
```

-	Layers:
	-	`sha256:691fb10b993bdbc00e48c234c28ba95d6cae0570fd0d0033ad52f6c4147ae90f`  
		Last Modified: Mon, 15 Jun 2026 21:54:20 GMT  
		Size: 50.1 KB (50061 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:27c1266009d0a89f68d378b1b1d39db3cb45c65dd7b22cfdb0720a0d5e096f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231526729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b137c68a3e4a70114c8f29b15ca076afa08b75dc4986b1e0600c394b546d81e1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 11:59:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 May 2026 12:01:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 May 2026 13:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 May 2026 13:07:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 May 2026 13:07:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 May 2026 13:07:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_VERSION=8.3.31
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 20 May 2026 20:49:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 May 2026 20:49:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 May 2026 21:38:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 May 2026 21:38:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 May 2026 21:38:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 20 May 2026 21:38:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 May 2026 21:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 May 2026 21:38:30 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 May 2026 21:38:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 May 2026 21:38:30 GMT
WORKDIR /var/www/html
# Wed, 20 May 2026 21:38:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 May 2026 21:38:30 GMT
CMD ["apache2-foreground"]
# Fri, 29 May 2026 01:09:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 29 May 2026 01:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 May 2026 01:14:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 29 May 2026 01:14:06 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 29 May 2026 01:14:06 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 29 May 2026 01:14:06 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 29 May 2026 01:14:06 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 29 May 2026 01:14:06 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 29 May 2026 01:14:06 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 29 May 2026 01:14:09 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 04 Jun 2026 20:34:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 20:34:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jun 2026 20:34:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jun 2026 20:35:41 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Thu, 04 Jun 2026 20:35:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 04 Jun 2026 20:35:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3f1ce6bdb422619d5f28f3d354ac88efadf525446aa4cc0a2cf6d208358da0`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2278d8aba6744e8388864d93d2ccd060b4b5b706da0855420292afc7562eef8`  
		Last Modified: Wed, 20 May 2026 13:05:36 GMT  
		Size: 146.6 MB (146584901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f680f6a3aa4a44306703b8a92e46d186729d6e1435771fbfda06e18de5ebcc5`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887cf26ec25a917a3969775023d91d64e52e0fc30b0f1e2c5a326ce664b36942`  
		Last Modified: Wed, 20 May 2026 14:08:12 GMT  
		Size: 4.0 MB (4031581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e116995318a8f16f6dd281e40820dba3f5cec3ccbf8b001b5f77cc47621731c`  
		Last Modified: Wed, 20 May 2026 14:08:10 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72c0690c9ca74d867f3cd4b9dd3884b132b21d1a7e60c2dfcd33fecaa0fb76f`  
		Last Modified: Wed, 20 May 2026 14:08:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f141c427a46f1759713dd715f2b2791ede42c5999242efd0c63766804280c65`  
		Last Modified: Wed, 20 May 2026 21:41:36 GMT  
		Size: 12.8 MB (12784261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee06ce4dcedcd83bfb671ba90b0f3a5d9864ea66e2df3c3fc9863439f06e844b`  
		Last Modified: Wed, 20 May 2026 21:41:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c074bd4815919a1ea293f5d0e9860a75d0d85a8517f686b8d664ab6b9884b4`  
		Last Modified: Wed, 20 May 2026 21:41:36 GMT  
		Size: 11.3 MB (11255979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e03a1d9fb0c37e61eb1dbf72bc1a8cd205940124bf0f4d6a16857c6e59c7a4`  
		Last Modified: Wed, 20 May 2026 21:41:31 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f503077b0fb46c4efc42977e7d8e3dc3c5652f85e40d21d688e0bd5cc48806b`  
		Last Modified: Wed, 20 May 2026 21:41:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885921ea102fba979369e756898326a8244f68e27534c75bb87792e5d7cbbea8`  
		Last Modified: Wed, 20 May 2026 21:41:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6b617233e6367ce4f70f391ff5cc68c4d273f816494a37326f5f6e80607a0f`  
		Last Modified: Wed, 20 May 2026 21:41:35 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bf3b909767751dce0485dc66ea189ddf329f13096f995fea859472ee640aaa`  
		Last Modified: Fri, 29 May 2026 01:16:44 GMT  
		Size: 1.3 MB (1265668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff01a38143a485d9a552b333b75e6c09ba7d68d88c5060773635ce7dc2264b`  
		Last Modified: Fri, 29 May 2026 01:16:44 GMT  
		Size: 456.1 KB (456090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7660bccae2e00f7bd4403114dc85245aad95c494fcfce6757ff3992625b13ea`  
		Last Modified: Fri, 29 May 2026 01:16:44 GMT  
		Size: 7.5 KB (7480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b019cd275d7f205e563e59d695c2a63afc524533d9222786f4ee2b0ff1c89c59`  
		Last Modified: Fri, 29 May 2026 01:16:45 GMT  
		Size: 2.6 MB (2602184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaf21b7e9ddcf61185d8d8719bdf00d222b60f84732b59e9697fdf72c0c2fbd`  
		Last Modified: Thu, 04 Jun 2026 20:36:53 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cede4bd0ae532b8cfce8639d3fcb15069baaef17d29291ad63b3a0e53431a6c`  
		Last Modified: Thu, 04 Jun 2026 20:36:53 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381b768b6bc3c4e727395fef901eea315c3df91e251d2ca6a1fbcf7dae2201ca`  
		Last Modified: Thu, 04 Jun 2026 20:36:57 GMT  
		Size: 23.4 MB (23430237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:eca3a194b2fe170d130e57a4aeaf1158d2e7e8e5bb58bf3a5f29c5e02f37abe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c7add5b6e2ac6a8d571b7a36713a8c1853d2d484ce3f82482bac2660368cdf`

```dockerfile
```

-	Layers:
	-	`sha256:875ab7d38e79503d3cb3f74840298e33831253120b7190df6bc538db5cbd3e28`  
		Last Modified: Fri, 05 Jun 2026 16:38:03 GMT  
		Size: 50.1 KB (50061 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; s390x

```console
$ docker pull postfixadmin@sha256:c5ff6bc34e67a37c6db9367dd0f0fe620377c762543d4f56cc105e4dff935eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179734595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244b80b0e91d9b33472d56f7deaa07eda4c33e83b868ecf6917653691929b6e8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:23:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:23:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:23:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:23:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:23:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:23:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_VERSION=8.3.31
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 11 Jun 2026 00:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:48:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:48:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:48:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 00:48:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:48:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:48:09 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:48:09 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:48:09 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:48:09 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:48:09 GMT
CMD ["apache2-foreground"]
# Mon, 15 Jun 2026 21:53:04 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Mon, 15 Jun 2026 21:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jun 2026 21:53:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:53:25 GMT
ARG POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:53:25 GMT
ARG POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:53:25 GMT
ENV POSTFIXADMIN_VERSION=4.0.3
# Mon, 15 Jun 2026 21:53:25 GMT
ENV POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
# Mon, 15 Jun 2026 21:53:25 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Mon, 15 Jun 2026 21:53:26 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Mon, 15 Jun 2026 21:53:26 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Mon, 15 Jun 2026 21:53:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:53:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 21:53:26 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 15 Jun 2026 21:53:35 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.3 POSTFIXADMIN_SHA512=b1f0261bf9cab0529ea43fb502bdef595c81350671c0e4b3fc6609335448552a3d7b649d8f4612473cc07bfe4bd1c6ba7800dc080a0fdf4247f5d81718ff2360
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 21:53:35 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 21:53:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f12811ca8054d10a6d855c99328a1f0623889381d202bba7392d112bc3de481`  
		Last Modified: Thu, 11 Jun 2026 00:28:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c3c60b41e88a2039142613d746976cbbd5c2d61145b36679028c24bf550936`  
		Last Modified: Thu, 11 Jun 2026 00:28:29 GMT  
		Size: 92.6 MB (92573159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39530e62e350f67cad534ea575f3024d4018b676be4212ebd0ff185c2f12e154`  
		Last Modified: Thu, 11 Jun 2026 00:27:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af8a8d7637b102b0927b2fe4838bd66d078d8497c6b8daf69a1af6de3c05716`  
		Last Modified: Thu, 11 Jun 2026 00:28:28 GMT  
		Size: 4.3 MB (4331367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81831958195a79868b988dbf00474aa90e83a65b5efa30da45faafb7f722895e`  
		Last Modified: Thu, 11 Jun 2026 00:28:29 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d9f6ef9d8cf0e08bf1a5c2cde718210376f9ed42f8dfe2ea97190ae4a2709b`  
		Last Modified: Thu, 11 Jun 2026 00:28:29 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cf9fd6c46e0f22b8412e26c1183e39f1f7e442b809f95863e444baec0429da`  
		Last Modified: Thu, 11 Jun 2026 00:48:28 GMT  
		Size: 12.8 MB (12768533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bd262f530ae6ca9614b41fe46daeee9aabf53618312e7c75e0857b1e7d21ca`  
		Last Modified: Thu, 11 Jun 2026 00:48:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4af958c055689ca8f760c811f2b32b226f18680d0ec21715d7bf90bfeaa1d9`  
		Last Modified: Thu, 11 Jun 2026 00:48:28 GMT  
		Size: 11.6 MB (11573210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f5cb38322eda038d3b18fa59c60ebb923e0ffad1ad7719a162b97c77f11724`  
		Last Modified: Thu, 11 Jun 2026 00:48:27 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cd107e5419bcc4d782e3cbaf793b079550e5296e37dbdb3343fd6239c3da16`  
		Last Modified: Thu, 11 Jun 2026 00:48:28 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7011873d099435e6e516642de8bd940b7794fdb1aeb1938a010c59aeae7b36a9`  
		Last Modified: Thu, 11 Jun 2026 00:48:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecf45e7183dddcf1c86dfdb6985c5b589bad40f25ac9b6257a3b4a28ae5ad54`  
		Last Modified: Thu, 11 Jun 2026 00:48:29 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d61ea0ae627f5f6b07bbe5b5b452ac33231da3a91dfb36825dff0e294645839`  
		Last Modified: Mon, 15 Jun 2026 21:53:45 GMT  
		Size: 1.3 MB (1307497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e3f62cac53128529ebb8ba810a18e40721ba98d95d4285d57924464f7aeb9e`  
		Last Modified: Mon, 15 Jun 2026 21:53:45 GMT  
		Size: 474.6 KB (474563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4019deb5b71e9caf97e81b4696c48d9737678ad9a6a841c1dca132b385af6d`  
		Last Modified: Mon, 15 Jun 2026 21:53:45 GMT  
		Size: 7.5 KB (7481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e324968b3f7fac5bdeecdfaf3b305665f863d8fd3450237da6ba06ac46257048`  
		Last Modified: Mon, 15 Jun 2026 21:53:45 GMT  
		Size: 2.6 MB (2602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b084e3e36380102221e13ed2119aa1fc168a950a755abcd7d16bfabb4748854`  
		Last Modified: Mon, 15 Jun 2026 21:53:46 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9cf145b215a0e6dc48583676b1f11c10376b77cc9ab3dd0ca31361e169d61f`  
		Last Modified: Mon, 15 Jun 2026 21:53:47 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670791241d5736a5f473b1268e87ccd003478c7c9490d8453380792645133796`  
		Last Modified: Mon, 15 Jun 2026 21:53:47 GMT  
		Size: 23.4 MB (23413733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:af5fb8c6ea21eadd805ba8f1a9d9de4a14ad585038efcc3773a98edebb171f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 KB (49967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902badd5f5869191fa2f63d93690d9cd81cecebaaae3b13073d3f28eb9ff769b`

```dockerfile
```

-	Layers:
	-	`sha256:ef7c79ecb721700e5383f046dce26ad04b6adf688956d13120ae0282c5be1cdb`  
		Last Modified: Mon, 15 Jun 2026 21:53:45 GMT  
		Size: 50.0 KB (49967 bytes)  
		MIME: application/vnd.in-toto+json
