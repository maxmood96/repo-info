## `drupal:7-php8.2-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:b450ad2724e3de68e6b1a92f624777ba9bce09816b1df4c918ef7a7f66d201d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:7-php8.2-fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:ce9bffa4c676d79a2ed950c6bd34c87f0ba50ae4e99e7e28b7b5935984c431fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36956782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0152d9e120e83ac365b16263241fc50de626c3836b5ecf0642ef7f6110fd15`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.23
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90ce4000612afa6f02496734ca8182e6e8fb8579399551b0de9baaae42c78ec`  
		Last Modified: Sat, 07 Sep 2024 02:16:03 GMT  
		Size: 2.8 MB (2798817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f0f5e49b7aa130bceca4598e155439e414098a9c7976c011815608f1f7f27`  
		Last Modified: Sat, 07 Sep 2024 02:16:02 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2856bf55ec7b461a369c2144535a11f17a9955ca14cc2b70f773dcf8fe2ccf34`  
		Last Modified: Sat, 07 Sep 2024 02:16:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0137d6fe4f96e89c280ab9cfc3281c0e74065bcd4b071bd4e89d947c2be7ac1`  
		Last Modified: Sat, 07 Sep 2024 02:19:53 GMT  
		Size: 12.1 MB (12139355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb78d94285182053e56b3eabb0059074b65fb0f22ec0b6e9078076fa474a8df5`  
		Last Modified: Sat, 07 Sep 2024 02:19:52 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a5d5e27b991dee7bbfd5ece8bf97cd4edb4d72f45944b151941cf92fa23d41`  
		Last Modified: Sat, 07 Sep 2024 02:20:08 GMT  
		Size: 12.9 MB (12855210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fdbde0fc9b0898edd625ee9d7c6d9ea22fef93d75a699fc6b8a33da27a0247`  
		Last Modified: Sat, 07 Sep 2024 02:20:06 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9da81af747153b7614ced5962efef3b6e6335e129297ad5bb96957f49d41fc`  
		Last Modified: Sat, 07 Sep 2024 02:20:06 GMT  
		Size: 19.6 KB (19558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9812bfee931238b3a39975d26ed1a98c0f2828e54089a246ec9387ac3d1c31`  
		Last Modified: Sat, 07 Sep 2024 02:20:06 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d875b2e4f4be51f2bc3a70262b8f56f6a3bb79aac85f102c7bba31e4638fb62f`  
		Last Modified: Sat, 07 Sep 2024 02:58:15 GMT  
		Size: 2.3 MB (2282607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c9719eab4a94e4af5c61bd25c62d661c7a2293eb483c83d6dd4a780413399a`  
		Last Modified: Sat, 07 Sep 2024 02:58:15 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f4ef9efa0a90ebb8ae0ad2d17aa8c45e0fcae9dd67bc837539f0450990dd29`  
		Last Modified: Sat, 07 Sep 2024 02:58:15 GMT  
		Size: 3.4 MB (3427632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:78ef1f42e2952c0ca8a9ad43f3b0b72998bd0b24aa2d4a21558fd7bf565c423d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 KB (301558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c7c6cf42d13a33a201f374e9c4b9a662bd437d5ce1b91e4d02f80ed830c941`

```dockerfile
```

-	Layers:
	-	`sha256:b694c05a1101c1a19ec0349e34998340158d87ac3889eef0850cf9d34fe5a831`  
		Last Modified: Sat, 07 Sep 2024 02:58:13 GMT  
		Size: 280.2 KB (280220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f010edb7edca86a71b5acc5ec94f4e30169136e00c95b9085d6c29bd97f95b82`  
		Last Modified: Sat, 07 Sep 2024 02:58:12 GMT  
		Size: 21.3 KB (21338 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:0c3d30155ed1a48bd7db0f0d50e6a8f2ab87873d908bc953f0851c13b7663042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35023591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d750bd86d7aa87adf77a22812e581998835ee2bac7f672199171cc54688f08`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.23
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080fcbe137ee32b9152493db0a11b83147216e46a5d126c0a783689576a6259d`  
		Last Modified: Sat, 07 Sep 2024 00:49:55 GMT  
		Size: 2.8 MB (2802371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d469f7c94bdbe032608fcb46ab9d0bc9a7a499e45c5cdb1fce68145f26dded1`  
		Last Modified: Sat, 07 Sep 2024 00:49:54 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c18247add2bbd4eb9f46f3f381558a3863198f9930bfbc655be0a57e7ce49ea`  
		Last Modified: Sat, 07 Sep 2024 00:49:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e502186d2e4264e709cc3bb8d8875de08bb878686500e4195bc4a0af59778f9f`  
		Last Modified: Sat, 07 Sep 2024 00:53:51 GMT  
		Size: 12.1 MB (12139368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e47a98f1c8069413476f85516b35354634f4daaa2e1d3f9e690b44c57dff2e`  
		Last Modified: Sat, 07 Sep 2024 00:53:51 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1909837a535c1bc4a0a425f2580c3b0da72f807ccc6a0d7451f448b4cb553fac`  
		Last Modified: Sat, 07 Sep 2024 00:54:08 GMT  
		Size: 11.7 MB (11704474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8081fbfaa65735b325964ecc9645221aba908df43847ae33d0701e0748991b0`  
		Last Modified: Sat, 07 Sep 2024 00:54:05 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f62fbfdb01a22b448cd41fd53a8e53bd430b572490ddcc3b6d1935f2ce3cf3`  
		Last Modified: Sat, 07 Sep 2024 00:54:05 GMT  
		Size: 19.4 KB (19398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063c22b8ab1f2f09c08a93863c5c95338c617cbd29d624e90ed3f9b26a32b55a`  
		Last Modified: Sat, 07 Sep 2024 00:54:05 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b359a82405185586e7ad35c071a689f1f234364048110e0422b3ddaccbe8d18d`  
		Last Modified: Sat, 07 Sep 2024 12:59:45 GMT  
		Size: 1.7 MB (1740063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6767d59b79bd92fafe6892cf4cc8addd1aeae991ce646a799323f8d963ef9f`  
		Last Modified: Sat, 07 Sep 2024 12:59:45 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a1e670219096ec33850d6e741d2a7cdc21a4c2a9bc38105d1102621c351fa4`  
		Last Modified: Sat, 07 Sep 2024 12:59:45 GMT  
		Size: 3.4 MB (3427638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:b65a9f3e4864aaa61a93f5d2e39f020cf5e4d3a5f2ea465d477473db7da322b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 KB (21201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a866adf362730dc163ff513d44ad4926e3693bddee8df44295f206eacd60d9`

```dockerfile
```

-	Layers:
	-	`sha256:f37796eb461db5076a9114c99bc839d1d8f33f5a1fba47ec1ca0d0126ab393ee`  
		Last Modified: Sat, 07 Sep 2024 12:59:42 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:430bc5ee087371aae1b3d58919387f6b3838d14d7576ffd1fa8261ba6d6944f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34149563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2279b178f8d0351d75a222f5bbb6c1e6840403e993b9f38a6f354204f7186e48`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.23
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863aa9b51e5e1bbb394dd698dad31a25269c0ec73e5772d64f8377b4dd1345a5`  
		Last Modified: Tue, 23 Jul 2024 01:15:11 GMT  
		Size: 2.6 MB (2624619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08abe10421ea530a6bc3d6d4e3605c900736b36d5d0caf2437915e09a6472e51`  
		Last Modified: Tue, 23 Jul 2024 01:15:10 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0547dcde17bbff569bac562ee7e2af6598f418ebafe66e067c5e00d61194af`  
		Last Modified: Tue, 23 Jul 2024 01:15:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5aa976e0a572504d7f1ca684c12340d1ed2db2563fc161f7b7fbd175e80d1`  
		Last Modified: Fri, 30 Aug 2024 21:56:27 GMT  
		Size: 12.1 MB (12139356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d28411c5a909e0dfdbac5b2f655912aac61acfc32ac8c02685c0a8749fdb9f1`  
		Last Modified: Fri, 30 Aug 2024 21:56:26 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca13382246362483b4b5cc77cd1c51d43a2c435e221d6430503ed1d1e172c3ab`  
		Last Modified: Fri, 30 Aug 2024 21:56:44 GMT  
		Size: 11.4 MB (11392712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d40e9a877b9330f7cd331bb4e39a8fd335db5f68c4becfe7ca8187847cf097b`  
		Last Modified: Fri, 30 Aug 2024 21:56:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13ee690b68ff0402e53c34a2b19c99ed4b80aab51a0c1737b93e7a4742dc3ed`  
		Last Modified: Fri, 30 Aug 2024 21:56:42 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e188cfc3d7e1f70b5f844c205f1390c2de68d1cdcfef6a8a40de91b5bc0fa664`  
		Last Modified: Fri, 30 Aug 2024 21:56:42 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54ca8d31aa99a6644f804805eb23503f605b102fd2ad501864927389b8d39a9`  
		Last Modified: Sat, 31 Aug 2024 02:39:30 GMT  
		Size: 1.6 MB (1604877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d788e34030e491941143e3def37a52ea9767f1182cd56be979e5e4c4a986b36d`  
		Last Modified: Sat, 31 Aug 2024 02:39:30 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1d6f807f8113217b7bb788b0dc977cb38df60b8436c6e494712f5b627e68f6`  
		Last Modified: Sat, 31 Aug 2024 02:39:30 GMT  
		Size: 3.4 MB (3427637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:54e3fc9d61e3f1c00e8a4fc42306d7ce8770d452fa1f3af55eb4c7a47cd62889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 KB (298796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ca980b49157682d625dedb552349b652ff1222cbfd431e7976a6eb46fe3b62`

```dockerfile
```

-	Layers:
	-	`sha256:b12f89709cff4b9c4dfe8dd66c8ec2e7aee0595671449efac125bbb2ba2b413e`  
		Last Modified: Sat, 31 Aug 2024 02:39:28 GMT  
		Size: 277.4 KB (277376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4aa5d820564db8fd6cdd476c9a3e0e2b45f9b20fa134b4b65cdcd7fdf749bd8`  
		Last Modified: Sat, 31 Aug 2024 02:39:28 GMT  
		Size: 21.4 KB (21420 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:248c4c8506262f90c0ef40bbdf66d8a0644be4e2371f336ab62561e785e2370c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37290843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d685359ac7b15287f62724690cc337743db1bf9853d369d59278a0db2c166766`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.23
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcba0d3205eeb63702adadaad8d4c4acc15c7aa55aadd0394eba5e6aa96d810`  
		Last Modified: Sat, 07 Sep 2024 02:24:38 GMT  
		Size: 2.9 MB (2852359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d9bfada5ad27fc98699cf473054b7827a2c9eca3e3d1b114812b165543914e`  
		Last Modified: Sat, 07 Sep 2024 02:24:37 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b570e101846a542a573e6fa0bb6d500cf65aa7c65544c86040968f41d933a9ce`  
		Last Modified: Sat, 07 Sep 2024 02:24:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0425df8422aafb4836f784e240476e7721f9faa3dcf04fbad7d7d836897e576f`  
		Last Modified: Sat, 07 Sep 2024 02:28:18 GMT  
		Size: 12.1 MB (12139360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba17632d78c01e92158bcd171f080807a9cfcb92e0c8d47dbc8e24be0b5cf9c`  
		Last Modified: Sat, 07 Sep 2024 02:28:17 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c4a17b11e9f58bf868bc59dd3f92500a869ab0dffe9eb4b034819eee3713bb`  
		Last Modified: Sat, 07 Sep 2024 02:28:33 GMT  
		Size: 12.9 MB (12924043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecca43065918dbf61d86cf3bd0464ca2dfb0fe790b43d3c1da6b75647321ee3`  
		Last Modified: Sat, 07 Sep 2024 02:28:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5149e661a40011867f26c260eb489bb93b67cd66f346cbcf2215142071ce48e`  
		Last Modified: Sat, 07 Sep 2024 02:28:31 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ca5b9564c9bd5a729c295c260e9a2cae38d6dfcb23ed9d198dc4fac6f9aa0c`  
		Last Modified: Sat, 07 Sep 2024 02:28:31 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d03df622eb52c9cd23045e99ec6e45a1ccffa63718bdf965d2f793d30de494`  
		Last Modified: Sat, 07 Sep 2024 12:31:38 GMT  
		Size: 2.6 MB (2555069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84baad4b51da1c7a597caed9fa2bef1482c4d7ff20472900538749ae48283cc`  
		Last Modified: Sat, 07 Sep 2024 12:31:39 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086400a4ae404be7fb884bac4764cdd3f11165f5cbe0f979dda19a59786ec2a`  
		Last Modified: Sat, 07 Sep 2024 12:31:39 GMT  
		Size: 3.4 MB (3427634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:29847d165fcb00b34a5eca58409460684384d31daef0701023d34873c218e859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.0 KB (299015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f39d63864dcafd098c1c3d698bc66ce1c4f5ba35b1a0e97471cecdd53601e`

```dockerfile
```

-	Layers:
	-	`sha256:90baf159afd81ab5fc4fe31eebaea27aa42a7842576d6778c9e6545e61098b99`  
		Last Modified: Sat, 07 Sep 2024 12:31:36 GMT  
		Size: 277.4 KB (277388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:750aea9253d15751832311ffa674b1df0ae7b8df7edb41be6dbefb02c1fe8b2f`  
		Last Modified: Sat, 07 Sep 2024 12:31:36 GMT  
		Size: 21.6 KB (21627 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:ef5b57948d9bb36e5997896c923870e16a57b6c043f15ecb351a34eeb272afb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37234780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a54e6abbc5c67242afcfcb74db3080a7eec1711f972f7f521704c67454f3e3b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.23
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398c42517a47f2db3a1b8799c3d9d1b17ab5a75db26505b01757d2b29f4a8884`  
		Last Modified: Sat, 07 Sep 2024 01:50:43 GMT  
		Size: 2.9 MB (2860989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58223ab98625da463b4d940ab7ebbb4eac608a94b3da464a1cee42974f5d2b73`  
		Last Modified: Sat, 07 Sep 2024 01:50:42 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e403c72b367566d502e0e7e9550bf71d2ff66fd72e51dd3b8f4fbef11d14ed1b`  
		Last Modified: Sat, 07 Sep 2024 01:50:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d864be1f21fd028dc25ce906a602763b226efcc0f56110a48a2721821f1b4e`  
		Last Modified: Sat, 07 Sep 2024 01:54:59 GMT  
		Size: 12.1 MB (12139368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b84d5db728c8534da4ed99538352ecd7053d116bfa664d16147a5af81d6804f`  
		Last Modified: Sat, 07 Sep 2024 01:54:57 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ba70f4298b4b97f044adc886274f55ef7169ed82d775d9d14d0231e955cd0c`  
		Last Modified: Sat, 07 Sep 2024 01:55:16 GMT  
		Size: 13.2 MB (13202553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3cdd003e41af11918a6193217026da26100d2a5bc7e7ccfb8ab626eb1316ef`  
		Last Modified: Sat, 07 Sep 2024 01:55:13 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7f1f38bd1ec2fda23a46bb4f78bd5cd39659b1b883777f1bfe5f3659fe2098`  
		Last Modified: Sat, 07 Sep 2024 01:55:13 GMT  
		Size: 19.6 KB (19556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34100439dac059150b92147be2877792c80e9ac249d1e8da0f12d305708baa7`  
		Last Modified: Sat, 07 Sep 2024 01:55:13 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab374a41362a762ddbd5af032b1549492956b48139d112aac36d252462c2520`  
		Last Modified: Sat, 07 Sep 2024 02:58:03 GMT  
		Size: 2.3 MB (2317192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33612d66f3a1f0be45f9359b39de20d16c8504e2e1ece1f2c51eb4bc2e564dd`  
		Last Modified: Sat, 07 Sep 2024 02:58:03 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6274d93a649addeb7719dd03c0f75b91451878f25cc0e509ada02f0d87b12a17`  
		Last Modified: Sat, 07 Sep 2024 02:58:03 GMT  
		Size: 3.4 MB (3427633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:d57133d7c683843997d50d59ea180ff0beee13d7c71b22afe19568e4ea73fd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 KB (301522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55386adfd98a1f936cc0001b013f1caa74d577c8bdf719f8a736e0c8803f8b2b`

```dockerfile
```

-	Layers:
	-	`sha256:38f21878f68efc6eebd370e3396d5c067081174bfb0cc357a7a3737d5a3afd9a`  
		Last Modified: Sat, 07 Sep 2024 02:58:01 GMT  
		Size: 280.2 KB (280205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c56c63c15cd3027b0f5804bd8247f5959563f3ad2fe22a292a217a7949eb9dc`  
		Last Modified: Sat, 07 Sep 2024 02:58:01 GMT  
		Size: 21.3 KB (21317 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:a351a86718b9688b7b6a593a618bb0beb4dafd49c8267eb597870be4a4f42d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37304268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e34290828cc419ccdbbae3def18aba723d495547103a499b159c70dfe54565`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.23
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4514a75734a8a2c464727a1d2643b6ffc19526edfbc2100de62e45284ef3699a`  
		Last Modified: Sat, 07 Sep 2024 01:45:56 GMT  
		Size: 2.9 MB (2882579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946f8448bd3215cc0574597d31b6c547a6035486812c2fcbfc8e931d6279885`  
		Last Modified: Sat, 07 Sep 2024 01:45:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1903ff2eae36c9cf63d249425e3f7bd588d8fcd648ecf498db42a9c9c09ab6a2`  
		Last Modified: Sat, 07 Sep 2024 01:45:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d6d49f3bef688b7d3438113528517066d6a9354e29ffa35b721c0da994a013`  
		Last Modified: Sat, 07 Sep 2024 01:55:16 GMT  
		Size: 12.1 MB (12139356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e70b2ef583a9a05aea9dfe998c599345b05d68efbc5f215758d97614b68ef93`  
		Last Modified: Sat, 07 Sep 2024 01:55:15 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69506ab290702b858e26e2cd92662b6294c26df8a50782e1f3dadc90dfb743a`  
		Last Modified: Sat, 07 Sep 2024 01:55:32 GMT  
		Size: 13.4 MB (13351913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9effb4b0fcaebc881550f8eb56328996a1b659642bee46a838ab639802a277a`  
		Last Modified: Sat, 07 Sep 2024 01:55:30 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464351f402a71cd531747feaab9cc914f9f2ad9bdbd350b1931cbd0f96e42bf9`  
		Last Modified: Sat, 07 Sep 2024 01:55:29 GMT  
		Size: 19.4 KB (19383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f482e8f309149a3bfe20b70193caa59a3a8330828592dca6b597567fcf87fcc`  
		Last Modified: Sat, 07 Sep 2024 01:55:29 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c834f69fffe2ba4d7e7e7e832c51f15527bb9b6562dfbae88eb62216e327c6`  
		Last Modified: Sat, 07 Sep 2024 12:21:00 GMT  
		Size: 2.1 MB (2105033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d486eff64ab8eae71d24ba6589685a6f3b563a23c04c13a1ac8d04268fb4d48`  
		Last Modified: Sat, 07 Sep 2024 12:21:00 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355884ba3a028b60cdcd8999f780d305bb2a7f4f03227219d4a7a6674d75ae17`  
		Last Modified: Sat, 07 Sep 2024 12:21:00 GMT  
		Size: 3.4 MB (3427639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:88dfc24ddde05e6aa1015d229990d33c223bfd8d8f6481939a9e180a3682f166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 KB (296794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3503e516ffcb5bdd49d760c59d11551b3a87519fb3466bc3024784e98c807fb`

```dockerfile
```

-	Layers:
	-	`sha256:33f616aafcd90c3f58b22540a951791083c2107f8db1924de4ddad16471b1e61`  
		Last Modified: Sat, 07 Sep 2024 12:20:57 GMT  
		Size: 275.4 KB (275424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67fa979db39afe18ce6d08a6e4bf546fb7b86f1a6412d1009cd29f29f327546b`  
		Last Modified: Sat, 07 Sep 2024 12:20:57 GMT  
		Size: 21.4 KB (21370 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:6b6ccb581e7f547a5807c78c8bc4847e5bd0396b2b5f0914c2c2c3bbe0de9c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36652943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d837aade34cd96774c2be857080fa28bed40075a4f58848b6d1de81e58194d01`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 05 Jun 2024 22:17:43 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 05 Jun 2024 22:17:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Jun 2024 22:17:43 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_VERSION=8.2.23
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.23.tar.xz.asc
# Wed, 05 Jun 2024 22:17:43 GMT
ENV PHP_SHA256=81c5ae6ba44e262a076349ee54a2e468638a4571085d80bff37f6fd308e1d8d5
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 05 Jun 2024 22:17:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 05 Jun 2024 22:17:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 05 Jun 2024 22:17:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 05 Jun 2024 22:17:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Jun 2024 22:17:43 GMT
WORKDIR /var/www/html
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 05 Jun 2024 22:17:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 22:17:43 GMT
EXPOSE 9000
# Wed, 05 Jun 2024 22:17:43 GMT
CMD ["php-fpm"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252a16b4a3f1ff8b7342597a1478d555f90a9466c5c0b4390a680b41165487a5`  
		Last Modified: Sat, 07 Sep 2024 00:43:13 GMT  
		Size: 3.0 MB (2976667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f2ec96a13f97950cd572f6ba53cd2b32756a6b0fbbab2578461fca19ef5a`  
		Last Modified: Sat, 07 Sep 2024 00:43:12 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a33bb433d3ff1f94ee0dbb35f0d25b17087375b1397e429df7974ffd56abf9f`  
		Last Modified: Sat, 07 Sep 2024 00:43:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1816e2109fe52954c2e42860d3e23bcda78597a17b9fb45b20ad3c4263d464`  
		Last Modified: Sat, 07 Sep 2024 00:45:55 GMT  
		Size: 12.1 MB (12139355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b557cae790c7b7f4c4796ee4aea6f122b24a78bdf3c59a49f37d42e8d730e5`  
		Last Modified: Sat, 07 Sep 2024 00:45:55 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b326026ab779c95b264b389c3c30f6828fa6dfd7e3a79de1e925b8fe46d36135`  
		Last Modified: Sat, 07 Sep 2024 00:46:06 GMT  
		Size: 12.8 MB (12823907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7039ab252967cc72316743b6abf4b4244037500ae1b2a94e653d198fd0d8b2e`  
		Last Modified: Sat, 07 Sep 2024 00:46:04 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c982b5e7a3f063f1abe1c85c1f650f6042ddfa4a0d2bd23198cd80b7d0243230`  
		Last Modified: Sat, 07 Sep 2024 00:46:04 GMT  
		Size: 19.4 KB (19378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba6a6abd642fa337fd65ba95b4e287747199375315927cab5828584b49b987d`  
		Last Modified: Sat, 07 Sep 2024 00:46:04 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f93a28e7ec8fc6ca160d191e9b0566c2f2da19e6a72bd61a9c9f3f89c07f647`  
		Last Modified: Sat, 07 Sep 2024 11:06:47 GMT  
		Size: 2.0 MB (1998758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185bd693b182fc3bc14a041b4a20b7ffe28f3211ea7eedf1b0a5deadf15e436c`  
		Last Modified: Sat, 07 Sep 2024 11:06:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf220b9e84581437d20d415777ccd7a82625c8db8a72d031c001612de7ba9fd6`  
		Last Modified: Sat, 07 Sep 2024 11:06:47 GMT  
		Size: 3.4 MB (3427634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:9714d4c2caac5dadf1bbad9f818893451632f51383da07685a062b478910a67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 KB (296742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebfe45a148a6d3a6b7126ea9c2c9081baff84a79a1bfaac1383224ed426c835`

```dockerfile
```

-	Layers:
	-	`sha256:9e7efac988ee9a918cd9b1570678952fc1351c75495432772f2720c168da45bd`  
		Last Modified: Sat, 07 Sep 2024 11:06:45 GMT  
		Size: 275.4 KB (275402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b52ee64dcbd8367c39fc2a63be3b94f37918ace414a096b3bbd8096aededfa`  
		Last Modified: Sat, 07 Sep 2024 11:06:45 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
