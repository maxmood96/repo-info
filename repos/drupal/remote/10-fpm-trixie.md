## `drupal:10-fpm-trixie`

```console
$ docker pull drupal@sha256:807aeaa2963794c2c8c306ab8a9eae471cbe8e5eedf9b2394b805b500a4ed2e1
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

### `drupal:10-fpm-trixie` - linux; amd64

```console
$ docker pull drupal@sha256:0049e1199b4ec061cb84bf4cbfe22fafcb9be043b0300d76874bcbffc41c8439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208880043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6b27b01a8a57547695681ae39a2fe0d74727c02b01037c7f807b79d4e933d2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:22:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 24 Jun 2026 01:22:22 GMT
ENV PHP_VERSION=8.4.22
# Wed, 24 Jun 2026 01:22:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 24 Jun 2026 01:22:22 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Wed, 24 Jun 2026 01:25:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:25:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:28:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:28:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:28:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:28:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:28:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:28:27 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:28:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:28:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:28:28 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:28:28 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:25:01 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 01:25:01 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:25:01 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:25:01 GMT
ENV DRUPAL_VERSION=10.6.12
# Thu, 25 Jun 2026 01:25:01 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:25:01 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:25:07 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:25:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e2719559bdcd9ac3459aae392020b09eca80afb1ee8dd5ccb38d2a412807f2`  
		Last Modified: Wed, 24 Jun 2026 01:25:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415de87f8879dbce10e3b86223460bc0ed3f63c3b822b90dccede2741af557fb`  
		Last Modified: Wed, 24 Jun 2026 01:25:37 GMT  
		Size: 117.8 MB (117839751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fdb60786769d4c81c1a378487d7f26851caafcd815ec099821006cdbffcf8f`  
		Last Modified: Wed, 24 Jun 2026 01:25:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9539b54aa4afcf702dd1b13b8b2b6353eb290ef97bdce4dd9ad6d99a32e8c08e`  
		Last Modified: Wed, 24 Jun 2026 01:28:38 GMT  
		Size: 13.9 MB (13879592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031955f909d30229a052399747c16f66efa3341d4e2af9d4096025b91c8f29c8`  
		Last Modified: Wed, 24 Jun 2026 01:28:38 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044304fb6aee2850a0e9d30ca9122c2e5c76f8c447c2f29f08c4eef234594d66`  
		Last Modified: Wed, 24 Jun 2026 01:28:38 GMT  
		Size: 13.8 MB (13809279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669b938b66abfe4444ccf7edf55a71112b3cd2ac12cd57df470336eb6b8a652a`  
		Last Modified: Wed, 24 Jun 2026 01:28:38 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db45aeb37769270ca314263d88c5fcd0a4339d96a714e810021712d188427e15`  
		Last Modified: Wed, 24 Jun 2026 01:28:39 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2de7f060e017fa2dd172201ae99f9301f23ec7c9c5f169439e2ff88837f7deb`  
		Last Modified: Wed, 24 Jun 2026 01:28:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2aac3b1211d9695278ef2e00aebae737f5868a1fe31d844e959f095226d3eb`  
		Last Modified: Wed, 24 Jun 2026 01:28:40 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9994ee57e9c93d68909b5478aeb4633146d67cb512c18e1e92034d7d083a98a0`  
		Last Modified: Thu, 25 Jun 2026 01:25:24 GMT  
		Size: 10.8 MB (10790318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5e95bc81815de8fee6d8ac15e348b9b40a102a735e4b45948167a6ccafbca`  
		Last Modified: Thu, 25 Jun 2026 01:25:24 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a75f658f86d1fdb4a44eff662cf92ef2e08f1166a1a5ef9025e0d07362bcef`  
		Last Modified: Thu, 25 Jun 2026 01:25:24 GMT  
		Size: 823.3 KB (823339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72138b9d481a50605e16ae1ad6a82e2a8b87a45b42d112f9b6c5f369e655e397`  
		Last Modified: Thu, 25 Jun 2026 01:25:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6388f38e9c7e84e1317b6380f912be2711b4b39c67d07caf2cd2a9e4e23c91c9`  
		Last Modified: Thu, 25 Jun 2026 01:25:26 GMT  
		Size: 21.9 MB (21938737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:0ca9537037b4ffa7f456ade353def1fa65736a52468109209ecc8029d431b6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6961744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27636bc9b4853d25dd92df1955a689fe852dbdc3be08b1ca6cece71b8b4ca65c`

```dockerfile
```

-	Layers:
	-	`sha256:e741ecdc6488f31e929cc084d346cc541b3fb9c163bbec48d108324c9173b350`  
		Last Modified: Thu, 25 Jun 2026 01:25:24 GMT  
		Size: 6.9 MB (6924644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9055a0bfaa82026ebe12c9194acad558f217baa5b64c18acc54ee2d408a7b0a`  
		Last Modified: Thu, 25 Jun 2026 01:25:23 GMT  
		Size: 37.1 KB (37100 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; arm variant v7

```console
$ docker pull drupal@sha256:19f30ed09fe67276a7d163fae873e3f540405c4ab33c42323304747c3491eb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167340526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e438d724511fff958d6c3dcabadfd7c8dc2e545e657c736b55ae7619b5df92`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_VERSION=8.4.22
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Wed, 24 Jun 2026 01:29:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:29:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:32:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:32:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:32:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:32:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:32:27 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:32:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:32:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:32:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:32:27 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:40:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 01:40:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:40:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:40:24 GMT
ENV DRUPAL_VERSION=10.6.12
# Thu, 25 Jun 2026 01:40:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:40:24 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:40:32 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:40:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaae95db0a85ff82847a66047248eac221c6c4fc2a0b259b974df3f7a6ce7ea`  
		Last Modified: Wed, 24 Jun 2026 01:25:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592cf4ef542b80f3a01efa46026d4120e17bece16f1f3ce29241d7b67731b110`  
		Last Modified: Wed, 24 Jun 2026 01:25:47 GMT  
		Size: 86.3 MB (86256007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb17027a57328ec40c6ea7b9fec64d931e5ca1c8ac245604f5e0e45f83abfe5`  
		Last Modified: Wed, 24 Jun 2026 01:25:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540f4766be8f5472124405d9d0d160f04ab9d2a76a48044558737e7176d27a26`  
		Last Modified: Wed, 24 Jun 2026 01:32:38 GMT  
		Size: 13.9 MB (13877002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a89af9cd89d7b60a18724e44e50f2ff3728d8d962d7f226b5a96e6a03c32430`  
		Last Modified: Wed, 24 Jun 2026 01:32:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1670f2c79a8dfd8da5a12bd318ca70a60d203356c74941288e3748fa05719b0c`  
		Last Modified: Wed, 24 Jun 2026 01:32:37 GMT  
		Size: 11.7 MB (11654206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53987155d72ac9db55bd1fac2882da25c2ab6a3e5bad39689c7111679bcb6c74`  
		Last Modified: Wed, 24 Jun 2026 01:32:37 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4d3934db685816e140c8c235e9f5cbe0249c1e73661025430ed30f7959e553`  
		Last Modified: Wed, 24 Jun 2026 01:32:38 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfef38c662724d17064b5a3b2dbb38a56120c51fbc61e6f0efdb47e6ee9fc41`  
		Last Modified: Wed, 24 Jun 2026 01:32:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8dd3981f70bd3a600c69e97f3a1de4986d9d271c1948c713b6f1920ab9f0fe`  
		Last Modified: Wed, 24 Jun 2026 01:32:39 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d6b6270bb320d5189c7e72d79bb9becd65d2231f3dcee2e1706db61ae6336a`  
		Last Modified: Thu, 25 Jun 2026 01:40:49 GMT  
		Size: 6.6 MB (6566602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23ead064686914f2fce9f1c994a591c237b50015d331373981fdb21f12e8e8d`  
		Last Modified: Thu, 25 Jun 2026 01:40:49 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9de2dc3c726c36dea4654a0f476daa92af9e3064b90abd3a09425138e9d402`  
		Last Modified: Thu, 25 Jun 2026 01:40:49 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ee66d3f68a40665b96084452c33dbef866039245889cabff0e5bf53697a885`  
		Last Modified: Thu, 25 Jun 2026 01:40:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5a2d0276d7db47d282e8fe71982777b9720724f515170d6aa8587e7d692447`  
		Last Modified: Thu, 25 Jun 2026 01:40:50 GMT  
		Size: 21.9 MB (21938700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:3528717cd85b9dc4106eb2071a7fac0e2abac86ee9e8a5a48d7037919accea20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6766082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae9b074fd5ffafafd955471c0bbe64151d86dad92133266ed2da783ddbc6d1`

```dockerfile
```

-	Layers:
	-	`sha256:0d9d33f31cd3e42e927fb75d55e047282155ff759a5a3689069178e175f1657f`  
		Last Modified: Thu, 25 Jun 2026 01:40:49 GMT  
		Size: 6.7 MB (6728800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9886f787e710fe9d2e1ce41ebd5b4e6027b2a60b17a84e1fd97faa3b4818a616`  
		Last Modified: Thu, 25 Jun 2026 01:40:49 GMT  
		Size: 37.3 KB (37282 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:bc8809e960f97749bffa68b9ee06d4dc98dd0c5e58dff1019f087af49553c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199751024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5d6d155569b2fef1a3a5d335b2a932e8b511afb7930c994335e582e7f91a44`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:22:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 24 Jun 2026 01:22:48 GMT
ENV PHP_VERSION=8.4.22
# Wed, 24 Jun 2026 01:22:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 24 Jun 2026 01:22:48 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Wed, 24 Jun 2026 01:26:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:26:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:29:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:29:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:29:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:29:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:29:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:29:52 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:29:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:29:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:29:52 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:29:52 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:25:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 01:25:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:25:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:25:49 GMT
ENV DRUPAL_VERSION=10.6.12
# Thu, 25 Jun 2026 01:25:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:25:49 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:26:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:26:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc36bb53cbf10000ddf0839d5ed488060ca9d5a341e4fbad0d70517a1d0d3219`  
		Last Modified: Wed, 24 Jun 2026 01:26:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c67174322f358bd67056275446570fe413c9d268049022098f2ff2ddbb6884b`  
		Last Modified: Wed, 24 Jun 2026 01:26:32 GMT  
		Size: 110.2 MB (110169497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea7372798ce941f2cbf56ecc26a161959544c8aeb6c7ad8f2db9c181cf8da12`  
		Last Modified: Wed, 24 Jun 2026 01:26:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88af0f4c30f1cb5780af8e4771c047d2aa0b0765532cf1223c6be3f2c48217a4`  
		Last Modified: Wed, 24 Jun 2026 01:30:03 GMT  
		Size: 13.9 MB (13879156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200a5375ede727b56d1592e884342b9f64e28812eb330f432e60c0ec2c3587f`  
		Last Modified: Wed, 24 Jun 2026 01:30:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe905697637d6636829e8d09a212e53166832167fe21d7724a3c50a8ab1766f8`  
		Last Modified: Wed, 24 Jun 2026 01:30:03 GMT  
		Size: 13.5 MB (13476388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027df3a970e03298b51770bb23cfd669d4c37cc92f447be95a0e4dc3c99474c3`  
		Last Modified: Wed, 24 Jun 2026 01:30:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd11c5b3f13b12497840682e1660192e5da270aebae37ca7c634c3b932b012`  
		Last Modified: Wed, 24 Jun 2026 01:30:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e060e0739d545747df19444678b5611e0c69a584b05fb8791987663589f632`  
		Last Modified: Wed, 24 Jun 2026 01:30:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12f561a867f60170199f030769b775f581199394045f95d1f9a26a47e4882e7`  
		Last Modified: Wed, 24 Jun 2026 01:30:05 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4426d5b2a0e442d0f2b6e6d79d7f5011799df9f75fed4f1393a1a7902b11d5`  
		Last Modified: Thu, 25 Jun 2026 01:26:19 GMT  
		Size: 9.3 MB (9301531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f6327c7cb137df4f74e8dafe4cfab8be0d1ef3a32c45cc4c771a57a009f75b`  
		Last Modified: Thu, 25 Jun 2026 01:26:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79a67d06f24197383c75e6b8f0a9dff1e073f7370b9d50fa5e51fa92df324d`  
		Last Modified: Thu, 25 Jun 2026 01:26:19 GMT  
		Size: 823.3 KB (823347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce1a6e2a3cfadc3da8bc0b015ad65cf8e4fe551c203908642fdf2bde9c4a837`  
		Last Modified: Thu, 25 Jun 2026 01:26:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d559713bd5851ea64afd4404780d2b5597935a8a75615e2ce96718d6119e3f`  
		Last Modified: Thu, 25 Jun 2026 01:26:21 GMT  
		Size: 21.9 MB (21938941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:1e2146d066dbafb41fbd299f40c538383ceccc6912ee044206836516db5c19a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7059467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebf148eb363681f4707c1a600c0f06f77a44e948d2e092d195578a85fda3777`

```dockerfile
```

-	Layers:
	-	`sha256:f32379859609ac304b961361cbf8d3218742f9fab54a84c54511219fb19b3391`  
		Last Modified: Thu, 25 Jun 2026 01:26:19 GMT  
		Size: 7.0 MB (7022115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bdf5f9b440ffe6538838fc3b2d698b1b8704d81730be6a179b379f68333c5b`  
		Last Modified: Thu, 25 Jun 2026 01:26:18 GMT  
		Size: 37.4 KB (37352 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; 386

```console
$ docker pull drupal@sha256:779f3d8939765f31e9f2f844c02738c4284c4a3a437de1d4b1c534a924fcc98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206648804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451a58fa42b041a52db0c68cbea700915945498fd7ce04b95de6eb4a2dbc5eb1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:17:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:17:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:17:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:17:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:17:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:17:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:17:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 24 Jun 2026 01:17:59 GMT
ENV PHP_VERSION=8.4.22
# Wed, 24 Jun 2026 01:17:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 24 Jun 2026 01:17:59 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Wed, 24 Jun 2026 01:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:22:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:25:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:25:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:25:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:25:20 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:25:21 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:25:21 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:25:21 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:25:21 GMT
CMD ["php-fpm"]
# Thu, 25 Jun 2026 01:25:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 01:25:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 25 Jun 2026 01:25:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 01:25:35 GMT
ENV DRUPAL_VERSION=10.6.12
# Thu, 25 Jun 2026 01:25:35 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 25 Jun 2026 01:25:35 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:25:41 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:25:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc8b327595feb313932525428b9a51cee8c024f3d25e8b170acd66808fe7946`  
		Last Modified: Wed, 24 Jun 2026 01:21:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b06dc83193f7bd380d09fa693ea47f12c2a3d678891b9caf131122119518d34`  
		Last Modified: Wed, 24 Jun 2026 01:21:59 GMT  
		Size: 116.1 MB (116141949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bcdf4793c1818d5c92e08b9445ee7eee33a774d4e651763171becd52071371`  
		Last Modified: Wed, 24 Jun 2026 01:21:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33e3918d9bfed96a00324aaefa27ddc85a3201d402d35329185bca22a4e4d15`  
		Last Modified: Wed, 24 Jun 2026 01:25:32 GMT  
		Size: 13.9 MB (13878474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d555f1cb6d09d2e0a8290d3d58ba24c648efd93112adb9ed0935feb42afb53cf`  
		Last Modified: Wed, 24 Jun 2026 01:25:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac32c609cbac79a80a99326a95c357adceda1ed9ad2573390a7c9cac01107d`  
		Last Modified: Wed, 24 Jun 2026 01:25:31 GMT  
		Size: 14.1 MB (14106555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a2e3b2452e78ca6aaf039fcd7f8db224f9155f2de0f94e0472914ee72a680`  
		Last Modified: Wed, 24 Jun 2026 01:25:31 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7dd2cef5a9dcb842fa0ffd4ec01a82c86666ba1032de0108824d31128ee0a0`  
		Last Modified: Wed, 24 Jun 2026 01:25:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebb52b15520ba1ff7c06f2d496005a46ee9ef3be5b9cb42f81786c42bfc4947`  
		Last Modified: Wed, 24 Jun 2026 01:25:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f80e87a7374f9fff9483ae616480c57786d81a9af1e81be8128676e9716688`  
		Last Modified: Wed, 24 Jun 2026 01:25:33 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555516f4a23cf74e63869374e9273647087d197e00c4fe62760de06d8207b4c`  
		Last Modified: Thu, 25 Jun 2026 01:25:57 GMT  
		Size: 8.4 MB (8445071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9822d47f8c3e29829610d9ba7b33256ba2da219b58fb205a10c92af67533b045`  
		Last Modified: Thu, 25 Jun 2026 01:25:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b0bdb6cddf05d4c65a489920a5370faab23d8e22b457ceda95d638d8c68437`  
		Last Modified: Thu, 25 Jun 2026 01:25:57 GMT  
		Size: 823.3 KB (823347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb511f8414f01477ff02604bfe0af1fc936726d035e5be598264c20bf721fcc`  
		Last Modified: Thu, 25 Jun 2026 01:25:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428514ba23c0f674b2d8289fd0a072cb855778fcb973b9c5c0e5b24c1f0b18ff`  
		Last Modified: Thu, 25 Jun 2026 01:25:58 GMT  
		Size: 21.9 MB (21938583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:6d067bd92465eafe887d2b66a7c6f1a7a206133d9c05cb4e7f0c68f190f96ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6935307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c780d9e21f5815b9438ba238c422bf1fd24b5866f146417fc8f02930c0d79272`

```dockerfile
```

-	Layers:
	-	`sha256:2b64f76acf3b5e0d2b050af1f1b870cc4a59f0b35e6ec28cb415479349eefc13`  
		Last Modified: Thu, 25 Jun 2026 01:25:57 GMT  
		Size: 6.9 MB (6898294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:debd8c4819751c4dc300772a7176c8a7218c3e9ffe102f4290caeac13a01a1fa`  
		Last Modified: Thu, 25 Jun 2026 01:25:56 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; ppc64le

```console
$ docker pull drupal@sha256:b45a62cf248f7d5fa5fbc587fc9d238b6470784bf0b4472b732efe86a8b5bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (203018189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967409aaba10023a30c799301f665e818508637a2aad7a3577db77f242503a50`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:47:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:48:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:48:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_VERSION=8.4.22
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Wed, 24 Jun 2026 02:10:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 02:10:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:19:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 02:19:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:19:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 02:19:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 02:19:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 02:19:03 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 02:19:04 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 02:19:04 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 02:19:04 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 02:19:04 GMT
CMD ["php-fpm"]
# Wed, 24 Jun 2026 09:17:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 09:17:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 24 Jun 2026 09:17:50 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 09:17:50 GMT
ENV DRUPAL_VERSION=10.6.12
# Wed, 24 Jun 2026 09:17:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 24 Jun 2026 09:17:50 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 02:38:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 02:38:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e77efe72bf9ab01112d6628b561df155e58c8abb9a5c50ca8c3c2d3054015`  
		Last Modified: Wed, 24 Jun 2026 01:53:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a885bf66539705f27716480915d14f847c62afd59e7c77b0d7a2ec11fcf9f8`  
		Last Modified: Wed, 24 Jun 2026 01:53:59 GMT  
		Size: 109.6 MB (109598576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6270c259f3728f03e6c19bf8bc89dd6cfe4f6a02bdbe4c4a66ac81d4e83afc0f`  
		Last Modified: Wed, 24 Jun 2026 01:53:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5654d1e5e524f982e7c00379ee8cca9b5ab79596cfda723bc3779fa0fb08b6c2`  
		Last Modified: Wed, 24 Jun 2026 02:14:55 GMT  
		Size: 13.9 MB (13878479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b910cf1256b80804d4f6c6fe94cb8a2f88ca93ec72f89516f35bff47851611e7`  
		Last Modified: Wed, 24 Jun 2026 02:14:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344e22b67a6ac2e6d60a963905ba623dc4b03697ffd374139279942d3a09bca1`  
		Last Modified: Wed, 24 Jun 2026 02:19:34 GMT  
		Size: 14.3 MB (14348286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0dc15ac1f943c583342641dd285bfced05805ea44dd08e0debcc3278948ae`  
		Last Modified: Wed, 24 Jun 2026 02:19:33 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9e7e4665eef92ed954c2898c3c2a0e4f00afa8b958bf41883df72bd4906671`  
		Last Modified: Wed, 24 Jun 2026 02:19:33 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88bbbc4352d3ac859859de221cc60400ad11de3c9ffe3d1cceded63bc6da3dd`  
		Last Modified: Wed, 24 Jun 2026 02:19:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969ab9ca9d4eadbfbd020e500b49d6c41f6938f5ef34551746b2c997dee1444`  
		Last Modified: Wed, 24 Jun 2026 02:19:35 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0064562c3d4cbbd5d29785ee6929ec4fed4035b90f991ccaad6e406bf161197f`  
		Last Modified: Wed, 24 Jun 2026 09:18:47 GMT  
		Size: 8.8 MB (8810865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14ecd4ee4ab4539271371af30c797e2a9888d2b461e0295bd4d30c2295d8bd0`  
		Last Modified: Wed, 24 Jun 2026 09:18:46 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e472549097eb98fa6b69000c148b94ec9f9c1b4f43d91e981b0d0094f9c80eb8`  
		Last Modified: Wed, 24 Jun 2026 09:18:46 GMT  
		Size: 823.3 KB (823344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f06c48f97f47503999c0ac935ab026bee3506d1fc461e37671d0f5fc80b2f6e`  
		Last Modified: Wed, 24 Jun 2026 09:18:46 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844056e214ad091325cd59fd15aae58404f3c20088a4a814766cb9320fb6c9be`  
		Last Modified: Thu, 25 Jun 2026 02:38:47 GMT  
		Size: 21.9 MB (21938625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:c2975f82ee7566323099e4c710b9c2ce6b1bb76d0eea8df52d30a46e94af4c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6962123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acb04442a9809d66265d1b18d1847ed0f7faf9084f0c624568b294124fe236a`

```dockerfile
```

-	Layers:
	-	`sha256:b73e795c83cc06baffbb1577b444601751d02e05610f2a7e610b038fed3b4b1e`  
		Last Modified: Thu, 25 Jun 2026 02:38:46 GMT  
		Size: 6.9 MB (6924922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a78a7b7de156a2f35cea68652c23cd050261409483497a78a4edc530f3bfd713`  
		Last Modified: Thu, 25 Jun 2026 02:38:46 GMT  
		Size: 37.2 KB (37201 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; riscv64

```console
$ docker pull drupal@sha256:cc666233f14887e23f7bc016f41d436df1c67c9d466c1a863e2515ffa874e480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231830662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7845d873581655a97c7d0598a70c0fb9c34efa65fd6f89aed25e4b21ba19a161`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 03:10:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Jun 2026 03:12:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Jun 2026 03:12:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Jun 2026 03:12:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Jun 2026 03:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Jun 2026 03:12:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_VERSION=8.4.22
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Thu, 25 Jun 2026 06:50:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Jun 2026 06:50:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 09:41:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Jun 2026 09:41:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 09:41:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Jun 2026 09:41:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Jun 2026 09:41:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Jun 2026 09:41:20 GMT
WORKDIR /var/www/html
# Thu, 25 Jun 2026 09:41:20 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Jun 2026 09:41:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Jun 2026 09:41:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Jun 2026 09:41:20 GMT
CMD ["php-fpm"]
# Sat, 27 Jun 2026 17:16:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 27 Jun 2026 17:16:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 27 Jun 2026 17:16:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 27 Jun 2026 17:16:18 GMT
ENV DRUPAL_VERSION=10.6.12
# Sat, 27 Jun 2026 17:16:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 27 Jun 2026 17:16:18 GMT
WORKDIR /opt/drupal
# Sat, 27 Jun 2026 18:42:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 27 Jun 2026 18:42:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5857a11081278c6794a11415cb81a403d5e56a1e98d5a05a474e4751b6bbbbab`  
		Last Modified: Thu, 25 Jun 2026 04:15:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f64aa12de76796ba620c1f61dfbf00595d86b22e83c70e23ab80e22f6f224c`  
		Last Modified: Thu, 25 Jun 2026 04:16:17 GMT  
		Size: 146.6 MB (146585183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75d48c7e93a7ac2ea8e95b78d618385a5865f4b0674a6016d1f7a6e51225d7c`  
		Last Modified: Thu, 25 Jun 2026 04:15:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa004b9f5df9297dc43475f2428c93a6f301fffe84a2c09ebb7833e904997565`  
		Last Modified: Thu, 25 Jun 2026 07:47:48 GMT  
		Size: 13.9 MB (13878402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9148599cbe49c1ada31d03b2c087cab81e1038acebc77e19e8fcfe1b75fdd26`  
		Last Modified: Thu, 25 Jun 2026 07:47:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1ec6853936f22d77ba371db16a74b119a845342981ddd6725353539a9e195`  
		Last Modified: Thu, 25 Jun 2026 09:44:17 GMT  
		Size: 13.3 MB (13257890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a8470ddc9fcc4f6a956f43e210912feb912b338943e00e2a27f04ad19a492c`  
		Last Modified: Thu, 25 Jun 2026 09:44:15 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5902b1699d798a119d455a41edb5936f5fbb46a179d34a9506eaf7374eea7ecf`  
		Last Modified: Thu, 25 Jun 2026 09:44:15 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ac0f0f2adff4252f5490df1fcce7e95e507e7b9fec9aa269cf83d46e6257a6`  
		Last Modified: Thu, 25 Jun 2026 09:44:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abacf134075993da3a5ff44ba22ed55c89e53ade7434ca2eb96717ff412921c`  
		Last Modified: Thu, 25 Jun 2026 09:44:16 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2811b09cfe4930f910f90b7e92a5214811e419a480c18cebe3aeaa5973d3dd`  
		Last Modified: Sat, 27 Jun 2026 17:21:58 GMT  
		Size: 7.1 MB (7051297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dcfd42b67e3f0c0222fdeac6e876b363422bf1eb56a05fa6152b6862a5154a`  
		Last Modified: Sat, 27 Jun 2026 17:21:56 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1375bab3c1dced596a11e077df6aea1f4702168fbaa98ee2f1d3d8a36d54d415`  
		Last Modified: Sat, 27 Jun 2026 17:21:56 GMT  
		Size: 823.3 KB (823347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f17934895121bb3ed463523214b4098d948987a77e7b31911b7672d48427df`  
		Last Modified: Sat, 27 Jun 2026 17:21:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b005ac74e4cc38cf1414fb71bd7aa8da8a4480b32b22d48e8797915f2c644eb9`  
		Last Modified: Sat, 27 Jun 2026 18:47:28 GMT  
		Size: 21.9 MB (21938535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:86281be8bf6cf1e8cadc66db1b7e991bcb7cdf14d8e8451c041e272ea0df27b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7033796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d654654d6073693ad57cd74cdd42904eaca46965bb3da7213fdc65eac61b4`

```dockerfile
```

-	Layers:
	-	`sha256:9155a11adf07c60ed3ad6fa123d4fcb3eec21ad0442e992ebab81a8522656f32`  
		Last Modified: Sat, 27 Jun 2026 18:47:25 GMT  
		Size: 7.0 MB (6996595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d462d1604a90e6dbf17a22b0b1cad2785ae6301ac892061bbead904e82006e4c`  
		Last Modified: Sat, 27 Jun 2026 18:47:24 GMT  
		Size: 37.2 KB (37201 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-trixie` - linux; s390x

```console
$ docker pull drupal@sha256:586bd4618649d1f9b7f8e1394b15cbf244b98ae47e8175c4c6675c1f5844162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180024150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ba8f9bc95f3c42705cdb2174b3849263185b77c1cc14e3f7d1c58fc8b5df5c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:19:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:19:53 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_VERSION=8.4.22
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Wed, 24 Jun 2026 01:33:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:33:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:37:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:37:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:37:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:37:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:37:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:37:53 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:37:53 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:37:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:37:53 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:37:53 GMT
CMD ["php-fpm"]
# Wed, 24 Jun 2026 04:32:57 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:32:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 24 Jun 2026 04:32:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 04:32:58 GMT
ENV DRUPAL_VERSION=10.6.12
# Wed, 24 Jun 2026 04:32:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 24 Jun 2026 04:32:58 GMT
WORKDIR /opt/drupal
# Thu, 25 Jun 2026 01:53:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 25 Jun 2026 01:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bb5043cbaffad0e2447070b4a5f2b29ea8f92190db347856d7a7b2afa8db0a`  
		Last Modified: Wed, 24 Jun 2026 01:23:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba630d3700db23d64e3bf4975aae41a0cef309b5e0da02aa4e11522332f82a6`  
		Last Modified: Wed, 24 Jun 2026 01:23:52 GMT  
		Size: 92.6 MB (92572737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d638a07841acb9fde6207fdb8aef39118b24dcc076004311a2f5332cfffa76`  
		Last Modified: Wed, 24 Jun 2026 01:23:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469584d9625f0759a300d696c4684186482a6920711fa82cb9eb99aafb96dcf8`  
		Last Modified: Wed, 24 Jun 2026 01:38:09 GMT  
		Size: 13.9 MB (13877718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab13b331b35bd759e7a76a97f812ecf76c97784bd243c3bb6a7c2e6b1afe0e`  
		Last Modified: Wed, 24 Jun 2026 01:38:09 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463e31f0e3a64d78055109f0c4111c5838a647a9d2507a365a5f7e533214ff8e`  
		Last Modified: Wed, 24 Jun 2026 01:38:09 GMT  
		Size: 13.6 MB (13594614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f00a98adad46881e505bb6177f697a0df0817f57ba73ad3c9319e205838bd5`  
		Last Modified: Wed, 24 Jun 2026 01:38:09 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0714f58541c91070da0ff19bd3f858a2246a7b794b917caa8e708d47e422005`  
		Last Modified: Wed, 24 Jun 2026 01:38:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb546ea14fa2a82a7e8832ace4fd22b5e2c936bfbb66dfece8911a15101dc2e`  
		Last Modified: Wed, 24 Jun 2026 01:38:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9adb625c13af46f0da21770869f4ce75e2f9d4137bb8abbf74f9aacf023462`  
		Last Modified: Wed, 24 Jun 2026 01:38:11 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6babd722bca67425a423b006dbb1a21a94398ae4e1222be21542610debdae7b7`  
		Last Modified: Wed, 24 Jun 2026 04:33:32 GMT  
		Size: 7.4 MB (7351696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d00101efea0ca85faa52234afff5c75570c89a133bf34dbacd507421f798a60`  
		Last Modified: Wed, 24 Jun 2026 04:33:32 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02909cce0e947a415f1da17c0d2e829c665a56725adaaab81a6e00562e1625e6`  
		Last Modified: Wed, 24 Jun 2026 04:33:32 GMT  
		Size: 823.3 KB (823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349677286291ec69f2025daf2aec2176e73b2ba76316646de8efc0dd36be8c41`  
		Last Modified: Wed, 24 Jun 2026 04:33:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60db23e474b6928bf0c1a1048df8930ee5ea7e5f2d8a189e13fca51cddc64d95`  
		Last Modified: Thu, 25 Jun 2026 01:53:54 GMT  
		Size: 21.9 MB (21939052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:08d3f72632d326a1b7067b9c9a45b8089ea315b4c91d8e84bdb7bb23abd63f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6691774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174959f136fcd8ca8971b4f19675114a07531bae84b7bdfe15ce6a91caa0abed`

```dockerfile
```

-	Layers:
	-	`sha256:a8557dc3e066dab7b0421aaa345a978656e6e271d2e4dbf7f963ba3b4e1c57d7`  
		Last Modified: Thu, 25 Jun 2026 01:53:54 GMT  
		Size: 6.7 MB (6656883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d750684b60033c442fb759178c2af6c75d5856c591decb8fecc1f10d2582575a`  
		Last Modified: Thu, 25 Jun 2026 01:53:54 GMT  
		Size: 34.9 KB (34891 bytes)  
		MIME: application/vnd.in-toto+json
