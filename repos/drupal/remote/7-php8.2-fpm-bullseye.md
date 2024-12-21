## `drupal:7-php8.2-fpm-bullseye`

```console
$ docker pull drupal@sha256:7937aae94c1e63330e6d3d45b5c858bafd5efa51fc9099770352b5108c5e874b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `drupal:7-php8.2-fpm-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:6d56458fc039cd9e9629d76c33f6bd88f966754260888b0f348f7704faa07307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165621487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34b05e21e3f4a0b3719341d31f557a48dcb560059a35a48d479084f4d79167c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.2.27
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee741af502444100f842a8999706b68aebd727d0c4c174e079c12ecafcfff026`  
		Last Modified: Fri, 20 Dec 2024 21:35:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f166bf770138defc2ea1657357ccd69abd19a10b2b5fb105f0064465d6a4dd`  
		Last Modified: Fri, 20 Dec 2024 21:35:32 GMT  
		Size: 91.4 MB (91448160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af7d7ddd48355714613885bbf97560b20588f8a322f360ad50fa3a9250ea54c`  
		Last Modified: Fri, 20 Dec 2024 21:35:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c161b74ac01b0473611ea6d16e0481707e9e85d0a6e0815c479bd4f2615be278`  
		Last Modified: Fri, 20 Dec 2024 21:35:30 GMT  
		Size: 12.3 MB (12254389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b98e22e9cfa132c56dbce56a35fe7185e19f149a2b65a8517f2bf42bcc4b35a`  
		Last Modified: Fri, 20 Dec 2024 21:35:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229828450323a0384d13b34f4297b8bbd61fe1c3971c8d30ed0d4c76261eaa67`  
		Last Modified: Fri, 20 Dec 2024 21:35:32 GMT  
		Size: 26.3 MB (26319784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18e41014d393b296cd1d021c408075766aeba3601cb876d56c443d1ede4b207`  
		Last Modified: Fri, 20 Dec 2024 21:35:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e704f4efefc8941b89eafe209bc04ce419a832634692d85d96248026920b810`  
		Last Modified: Fri, 20 Dec 2024 21:35:31 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c37c0df239806cc44e6b21b863272b33b45a9fa75c6aba9ce0144e7b11e9a4b`  
		Last Modified: Fri, 20 Dec 2024 21:35:32 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7934f5581ef62eb5c1c44e7d4ba2b9c78a1cbe3ea9a46bfddeddfbb3f0a6ec49`  
		Last Modified: Fri, 20 Dec 2024 22:34:31 GMT  
		Size: 1.9 MB (1904336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f80ad5c2293b853c7687a79bd2f6346b2dedd122654a5ba284c449af4f8b12`  
		Last Modified: Fri, 20 Dec 2024 22:34:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fc8fa6d4db57741dd62a611f663b0433d530d61526d84a0ae5277d56efcfb9`  
		Last Modified: Fri, 20 Dec 2024 22:34:31 GMT  
		Size: 3.4 MB (3429002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:7b4e4ddda42358d1246e454a16e9213060987e785d9a8c89ed49ba2e20e46a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6444291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd454b8b1a58d7a8b6893830a29046a219ef001a7ec23ff7b7a6dc1abb4b9ec`

```dockerfile
```

-	Layers:
	-	`sha256:18e5733f41a9dbd58508340e0bbf573c4034dc2138d71c13a86e7a3472cf9888`  
		Last Modified: Fri, 20 Dec 2024 22:34:31 GMT  
		Size: 6.4 MB (6421084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:280be162ad5e6e24e56f31ff75524ae25c0a312a7b9d0ed9cbdfa269aaba363a`  
		Last Modified: Fri, 20 Dec 2024 22:34:31 GMT  
		Size: 23.2 KB (23207 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:556f86bff59e0191e9bf8ac7a6f9e1623117937b0a334012be247925f1d3381c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135655014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f6a24659574f44bfdcd687b5cd2fc113bfebd047d1aaa40b56a861662e5c60`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 21 Nov 2024 04:48:20 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 04:48:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_VERSION=8.2.26
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 04:48:20 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Nov 2024 04:48:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 21 Nov 2024 04:48:20 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:79ae44024aa8e358b5fbaad284a41a7c359d47ad28af854839c0e44435b875ba`  
		Last Modified: Tue, 03 Dec 2024 01:28:54 GMT  
		Size: 25.5 MB (25533944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f4cd0ed182c41a7840e3bd6aeb9858708e8c6b99baae88a51faf80b4559a51`  
		Last Modified: Tue, 03 Dec 2024 03:00:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682dddbc2d895e7263b87741543ce754592ab412d0d97e492925c117dfb408e3`  
		Last Modified: Tue, 03 Dec 2024 03:00:19 GMT  
		Size: 69.1 MB (69119217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f7c0f9947f1b2a09b6fb724d5e29aec91c63413c8b1ab8510d897d0b179b52`  
		Last Modified: Tue, 03 Dec 2024 03:00:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91435c65d53c5934859fc8cf5067a92b88e2dbc48374f66052f49ff5f3da00f`  
		Last Modified: Tue, 03 Dec 2024 03:55:16 GMT  
		Size: 12.2 MB (12240140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d112292f30287d40f6f5074f230551f473e55ffe862d582e7e9c61e8be67ea`  
		Last Modified: Tue, 03 Dec 2024 03:55:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1ecf30c1e7f7c8c6624555f1c38ac04a863f671cd853017b490c8b2941dbba`  
		Last Modified: Tue, 03 Dec 2024 04:00:50 GMT  
		Size: 24.0 MB (24035693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b19e355096d1e1fd214be784e207f65d0fe31ce34134f3c278ff69055850174`  
		Last Modified: Tue, 03 Dec 2024 04:00:49 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470f9a3d51d1cb87ac587539e36bfd21f123cfe7690934851a57af225462ae25`  
		Last Modified: Tue, 03 Dec 2024 04:00:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5837f2308ba7cd388b5cb447e35bbfa096bee7d549264f89c996b82e9788e3e`  
		Last Modified: Tue, 03 Dec 2024 04:00:50 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7705cfcb3781fe35edca1b1f56feeb4e2633bb0da909dd2ffc7ad4f9ef5d264`  
		Last Modified: Tue, 03 Dec 2024 17:34:31 GMT  
		Size: 1.3 MB (1283874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e8cb3617da526aa7a4e79602df3bccaefd5d881f16198e5753eb2a49cf476a`  
		Last Modified: Tue, 03 Dec 2024 17:34:31 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b488adf6d5eee4ab58089ee6c8b44291a5d795b7e4bbe9a3e96b6628bf51c2e7`  
		Last Modified: Wed, 04 Dec 2024 20:31:24 GMT  
		Size: 3.4 MB (3429001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:070fc7d75b18144d5d69862159e4646e7abaaa962c90b2998f8d1877906a2739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6cc68813bf7a26f7b6072f9dbac279b4053ce641e26588bb5d5147965e2d5b`

```dockerfile
```

-	Layers:
	-	`sha256:99b8e7771174c840bbb379a883abe723d320f3dc5f957cf593006406a2b09ae9`  
		Last Modified: Wed, 04 Dec 2024 20:31:24 GMT  
		Size: 6.2 MB (6238014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f2585c93f3f38ce9e0217b9580e41dfe8714d707b11c5a4af5062f25dee746`  
		Last Modified: Wed, 04 Dec 2024 20:31:24 GMT  
		Size: 23.3 KB (23293 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:9e3070ca71e529ea99082c8a4694d3449d8bf0cffa8e58cd3fb7e2ab9e104b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159706180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09aa84cb4527a94ff241029131bff65351a02342bd70e53950ef9338337d686`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 21 Nov 2024 04:48:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 04:48:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_VERSION=8.2.26
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Thu, 21 Nov 2024 04:48:20 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 04:48:20 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 04:48:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 21 Nov 2024 04:48:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Nov 2024 04:48:20 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 21 Nov 2024 04:48:20 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaa51b96f45aeeeac0da5ce8bef54768006d2f3f15d75cc62bf2f673af4c4ee`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf1193220d0cc95806c6408988e7d5348f9ad83ddfb796cd2261f04ce83160a`  
		Last Modified: Tue, 03 Dec 2024 03:14:50 GMT  
		Size: 86.7 MB (86734618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80085106d7b6b1e2208214a2555ef1f1d0e5a1cfb68b48454784f2843f1cdc7e`  
		Last Modified: Tue, 03 Dec 2024 03:14:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af539b47c15bc3600d5c3cb5b4bf16fa550292a28d73c2541cb0979afc9583`  
		Last Modified: Tue, 03 Dec 2024 04:12:39 GMT  
		Size: 12.2 MB (12241118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45a6bf38470f4542229ceb53645e4e50cde9e43198bbbbe23de4e5ceddc6d42`  
		Last Modified: Tue, 03 Dec 2024 04:12:38 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062b95182c4eefb4326fe307e611d5c51062d432c2ed9e2bd005084c33781b70`  
		Last Modified: Tue, 03 Dec 2024 04:19:16 GMT  
		Size: 26.4 MB (26373746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4d4a5cba9ef09c6f25b0b96bd654d6ab1ca84d7478c915c98bce05d3b941e8`  
		Last Modified: Tue, 03 Dec 2024 04:19:15 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559d462a0105f40daa9a22856f46bbeb1c8e8c4c007c155a641eafe724bfa3d4`  
		Last Modified: Tue, 03 Dec 2024 04:19:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3861a15201e462d44f33043656fbdb48306e9b5d248c358ea1d6c431989fe36`  
		Last Modified: Tue, 03 Dec 2024 04:19:16 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad5bcdfce6e4dc708d0b9eea8810f83c691afa356c2d8190b9656ea46e92db8`  
		Last Modified: Tue, 03 Dec 2024 12:10:51 GMT  
		Size: 2.2 MB (2169615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7cbb119da617cb4109e0a9848568ecf9e2ebcab4d9bb732745a04cf913e0c0`  
		Last Modified: Tue, 03 Dec 2024 12:10:51 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164ce70aa6b0e9bcd7bda48bba0ba8fc2b57f0fa682dfba74ffd97ad5b816ded`  
		Last Modified: Wed, 04 Dec 2024 20:29:57 GMT  
		Size: 3.4 MB (3429007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:e5897969bfa443db42d64496776a6a67d90de895497717b90e33d23010cd9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6455499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7c7f2d54448a935904663ffecd260b62cc852f910571c8d6bd0eeca5be2679`

```dockerfile
```

-	Layers:
	-	`sha256:e56d5ffd03181b312cbfbc0e02d112b73d1af0f52bf1abe37b4644a929932050`  
		Last Modified: Wed, 04 Dec 2024 20:29:56 GMT  
		Size: 6.4 MB (6432182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ffc61c4443b851383d3ca9d67f15001389257d272428c2a549a419e1863adf`  
		Last Modified: Wed, 04 Dec 2024 20:29:56 GMT  
		Size: 23.3 KB (23317 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:be994f4359a6ddef6ce6a279795eb10f45725910b410a052d7793395538758bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168181030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c206a75040ae2edbb3feb49b683c61531cc66bb62027ae1fe8aa857a6472979f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Dec 2024 16:27:27 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_VERSION=8.2.27
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Wed, 04 Dec 2024 16:27:27 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Dec 2024 16:27:27 GMT
WORKDIR /var/www/html
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Dec 2024 16:27:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 04 Dec 2024 16:27:27 GMT
CMD ["php-fpm"]
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_VERSION=7.103
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.103.tar.gz
# Wed, 04 Dec 2024 16:27:27 GMT
ENV DRUPAL_MD5=9330ed0dd9926e82b06afb9cf236d5f6
# Wed, 04 Dec 2024 16:27:27 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5758d8b0f01ae434c15ea899ac175dada65636225d718b63744e68dbbd988f9b`  
		Last Modified: Fri, 20 Dec 2024 21:39:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e30a60ce5d17311a3ec892e6f1d159b0375eac699203cb34267c3f6ed37fc6`  
		Last Modified: Fri, 20 Dec 2024 21:39:41 GMT  
		Size: 92.5 MB (92521410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2a501911e8a2fbd630dc4b11f3ddf3297bdd4826948bb19be3c28d3a76f359`  
		Last Modified: Fri, 20 Dec 2024 21:39:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad6a134f2126b6cfc8d69a0dac76da175a1cfb3c23fc110ce20ab5fd1f3407`  
		Last Modified: Fri, 20 Dec 2024 21:39:39 GMT  
		Size: 12.3 MB (12253685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0708fded9161f0941475a9ad59f96e6f2c48d81cf83ea22c1e15702c870385af`  
		Last Modified: Fri, 20 Dec 2024 21:39:39 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a83ed48ed16955b35bd6593cfe05e601fc7377338d9a813b55d7f7b91b40f5d`  
		Last Modified: Fri, 20 Dec 2024 21:39:40 GMT  
		Size: 26.8 MB (26814035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba19a6d8cfa3b1e3c1edff5860c0f385044cb5a7354cf5fee5abd9414b38e16`  
		Last Modified: Fri, 20 Dec 2024 21:39:40 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17cd124c851cd8ef73424a5a5c220461509ac1b8632dc2cab050e7df9d9bd14`  
		Last Modified: Fri, 20 Dec 2024 21:39:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1f5b5b74e3efa7dbcd460697ce18369740b9706da62d1f70d6eac4de7dd2ac`  
		Last Modified: Fri, 20 Dec 2024 21:39:41 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b614db73ecd2764538e5a68c5cdce0f3231b48fc457855918345a99e9fd949ba`  
		Last Modified: Fri, 20 Dec 2024 22:31:15 GMT  
		Size: 2.0 MB (1970675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4281dd71dfcd350037702e98a2e1173bccbf39985dc28a4c6665996b928e375f`  
		Last Modified: Fri, 20 Dec 2024 22:31:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9113eb1bebd40a4e78de5569cc487453adf1b1db165100d3a8d9dce50cc0fd79`  
		Last Modified: Fri, 20 Dec 2024 22:31:15 GMT  
		Size: 3.4 MB (3429000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:925efda62d282daa0895d78ac4caae1fac5173f3066a346849e8c584d7c8b53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6434929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11a30a360f62b3daa7c970a8ac256b54a91230f3de661c483160e7c622e3dbd`

```dockerfile
```

-	Layers:
	-	`sha256:56e3db2f6a19a2a7c09671ed3a9a572d68fa60d189f9e0dfe0e6b26f4b450171`  
		Last Modified: Fri, 20 Dec 2024 22:31:15 GMT  
		Size: 6.4 MB (6411748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20eba213823f8fb42d080e63db40696790121f6133fee21471c4fa8e1ff93f34`  
		Last Modified: Fri, 20 Dec 2024 22:31:15 GMT  
		Size: 23.2 KB (23181 bytes)  
		MIME: application/vnd.in-toto+json
