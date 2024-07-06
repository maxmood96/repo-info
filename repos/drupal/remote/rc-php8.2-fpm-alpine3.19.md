## `drupal:rc-php8.2-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:4504b2689a9f31a29b032757b0d2b11bb8e1f688e370ccc91d76df81d3990f81
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

### `drupal:rc-php8.2-fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:ee01d140a2db465d790037dd3a41212dbfadbd62e0f67edb799e45cc19e3469e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55685620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817bfc6faeacd55571b62de8cbe29115bbe861a728c325b35dd71595ff48a57a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.21
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523087b9c271ae77d92e944ca833899bac59254ff834ca6106f2b0008f864382`  
		Last Modified: Fri, 21 Jun 2024 02:21:54 GMT  
		Size: 2.8 MB (2775517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d060ecc216f23e008efa4494a28853d924be900e357c22e573c279a319af6a4`  
		Last Modified: Fri, 21 Jun 2024 02:21:53 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0597315652e0b3a62ece26492f0cc07086c503fddccf28f6b8cb0f3cf5632068`  
		Last Modified: Fri, 21 Jun 2024 02:21:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cf55575b77cb8cfe9d488d820bc8edea1f1a23c1ce548118f43fe309ba73ad`  
		Last Modified: Sat, 06 Jul 2024 02:32:36 GMT  
		Size: 12.1 MB (12128106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a09060bf37a118d1b7473012663ae0befdb26ee738e8a948ee1ebe85fa5f09`  
		Last Modified: Sat, 06 Jul 2024 02:32:35 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8760940fb00ec7d4794f9d268ceb4fad99c6da55e5ebbbad738a8c82fcae957d`  
		Last Modified: Sat, 06 Jul 2024 02:32:52 GMT  
		Size: 15.4 MB (15368899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7220a708423dca8263ffb3f3c1de83940763ad9423d8b0e1a8122f536f140`  
		Last Modified: Sat, 06 Jul 2024 02:32:50 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfd7673daa8e5237059d12a313133f65eb3a913bf77c345a6ec3c667477fb52`  
		Last Modified: Sat, 06 Jul 2024 02:32:50 GMT  
		Size: 19.6 KB (19556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9861f228f6e591089eff7192817b138cfb73d4ab8ce6f661859d101a3b88e68e`  
		Last Modified: Sat, 06 Jul 2024 02:32:50 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d532e177824d48b58cc5efce2cbe6d846038540996acdda875f088343a188d0a`  
		Last Modified: Sat, 06 Jul 2024 05:55:23 GMT  
		Size: 2.3 MB (2282638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2fb5f812aaeaf261a034a428a888a5a08b63ea0491d074cf0dd705a667db75`  
		Last Modified: Sat, 06 Jul 2024 05:55:23 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fb22aa902e95720508d31680d476845296eb94736ed7dc9ea9af5a6b38af2`  
		Last Modified: Sat, 06 Jul 2024 05:55:23 GMT  
		Size: 726.3 KB (726327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69805b91bb25330a163fb0b85d087f5ff4fa9566fbdc06518cc88733d153baec`  
		Last Modified: Sat, 06 Jul 2024 05:55:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6931e7a784f3dd38ec77c488344cff8ff4f31aa2407587500a57294f5e19b80e`  
		Last Modified: Sat, 06 Jul 2024 05:55:24 GMT  
		Size: 19.0 MB (18953237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:4418c9af2c7661940e9073dbac92e64baecf871fd9a877b37e2b19e9f17b135c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 KB (364537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bcc818fa6f02133487754e3e9aa75f66a244d17a1edc52034011f6272b449d`

```dockerfile
```

-	Layers:
	-	`sha256:7e3e762585252481c1ba9edd3a073a22bccfe9db46230dfb85479519618b60a4`  
		Last Modified: Sat, 06 Jul 2024 05:55:23 GMT  
		Size: 332.5 KB (332477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c87c014c9c6a51755f33d2b0618614353bea816c0ac9bac1eba8688b180a7a`  
		Last Modified: Sat, 06 Jul 2024 05:55:23 GMT  
		Size: 32.1 KB (32060 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:16e8384e21cdaf08cdb2abcb9942bf3fb5172a888cbbd65f024e9ed5c15205d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53452454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1967c8a4029a16bf6a7d7f8eadc4f5d94d7cd51e4f7cabd90b50411ebb4718e0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.21
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0fe3503923312700d0ad215db61ad54d143feac25bfc14ba0b4eb2cd554730`  
		Last Modified: Thu, 20 Jun 2024 23:11:30 GMT  
		Size: 2.8 MB (2782199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e727f9d3c5208e6085f44fcc1802704b726a7b2b884ee795f8ceeb3594b9e6`  
		Last Modified: Thu, 20 Jun 2024 23:11:29 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a49ddfbb89fe4110ef4b151edfe03948f99fe5bf8d637ef0657bd9bb46d10c9`  
		Last Modified: Thu, 20 Jun 2024 23:11:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2368e5ce245a66b896fdca2929871af7aea500be9686a338a63f5df6ec25a9`  
		Last Modified: Sat, 06 Jul 2024 01:50:35 GMT  
		Size: 12.1 MB (12128120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e5c686c402b03f8de8ea90c0332f36c642d3a80f2af6f929f82cab057f5f6a`  
		Last Modified: Sat, 06 Jul 2024 01:50:34 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964b4ee7ab28d81fe832aea7eb1e0c9c7bae22beb6f1185126c66b1c76d0b4df`  
		Last Modified: Sat, 06 Jul 2024 01:50:52 GMT  
		Size: 13.9 MB (13914969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f6b07a343e4756289bb0abde600492d458eb65b8cab249779c203ee46bd944`  
		Last Modified: Sat, 06 Jul 2024 01:50:49 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43145b115e3f355c0cbd6bd777a936eff9d2e1a5f7d7a30fbb84aab8245feb7`  
		Last Modified: Sat, 06 Jul 2024 01:50:49 GMT  
		Size: 19.4 KB (19407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f2c13b4cf2b71b2b85e3b525c0703a273cf920bab32bba19986152178e5`  
		Last Modified: Sat, 06 Jul 2024 01:50:49 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a233c8619da452e0af3215592a8048e51003ce0e3093b777dd127260bf4b17`  
		Last Modified: Sat, 06 Jul 2024 03:10:45 GMT  
		Size: 1.7 MB (1740113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081e363bccce11f18646d5b5884a6470b3948bd2e0ba3ceef932e6c834cb706f`  
		Last Modified: Sat, 06 Jul 2024 03:10:45 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f59f97f5f583e5c2db7663acdd8302f806e758fc7efbe3e7818c6f37089f5`  
		Last Modified: Sat, 06 Jul 2024 03:53:34 GMT  
		Size: 726.3 KB (726335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf5d374fb2035adba7616c4d4de5594a4bb8871b0f3f34012c44e4343138b1c`  
		Last Modified: Sat, 06 Jul 2024 03:53:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2017e4904cd2de8a8ee9147d43b7709773163be3b976ed8a61b4fe1f5343a1`  
		Last Modified: Sat, 06 Jul 2024 03:53:35 GMT  
		Size: 19.0 MB (18953398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:4e4a1792469f365193f67964711810b806fbd26f40cc22df6add5befa5bda630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 KB (32029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0fc0156565525debe52c37503b4dfabc27a154fb2d9ba4f80180f894f516f2`

```dockerfile
```

-	Layers:
	-	`sha256:bcfadb55d2485a0870b54c4a9ac78c46f6aa5049617461bcad16441c40efc4ea`  
		Last Modified: Sat, 06 Jul 2024 03:53:33 GMT  
		Size: 32.0 KB (32029 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:9d845edd22a605976b0b2bc977a31fa0127e4ada6105332dcd69bc997bc8c123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52032418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8faa1489777ca84bf40457d06ec474bb4ccd97d28d1740484679d5f194fc73`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.21
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fd2f7314fb5a1bddd9717973873845b50c0071affc1e794041d120c75898de`  
		Last Modified: Thu, 20 Jun 2024 20:09:38 GMT  
		Size: 2.6 MB (2624592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f23dd8be0ad44d730123eaa34961b21523892832d003182b0254c0a46ac650`  
		Last Modified: Thu, 20 Jun 2024 20:09:37 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd5cf20011ab84a0de7e85853e1003271ddd0a307016623fddf7d0a902750d5`  
		Last Modified: Thu, 20 Jun 2024 20:09:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3077ca3d521190f3f7a94174e2f924f518e43d9049ecc081774f4048adcfe74c`  
		Last Modified: Sat, 06 Jul 2024 02:52:22 GMT  
		Size: 12.1 MB (12128109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0298efb242bd0b948f75ffbe3a86f7af0f5c65e39808e38b26de6324084d096`  
		Last Modified: Sat, 06 Jul 2024 02:52:21 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001a86f23bc8b0c44fd51bd26d8a4cff4a566312cf68764f0dd77af5b05a3170`  
		Last Modified: Sat, 06 Jul 2024 02:52:38 GMT  
		Size: 13.0 MB (13035223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bbe0ea5db2c0c23f3bbcec66845754f2033888affde2530f5bbe8be2ed770e`  
		Last Modified: Sat, 06 Jul 2024 02:52:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3783404d469d5fa09aca9164a4eaaddd9bcf5800a690ef8aa025f48e9e190105`  
		Last Modified: Sat, 06 Jul 2024 02:52:36 GMT  
		Size: 19.4 KB (19378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3908eb7915b269be27d59fdec0c83a0c59672f76ad3411ff9e5c283cea47f29c`  
		Last Modified: Sat, 06 Jul 2024 02:52:36 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f9f38b080183b0003beda026b119253ce2e8a6a4c7096864805fb4a64b831c`  
		Last Modified: Sat, 06 Jul 2024 05:29:47 GMT  
		Size: 1.6 MB (1604849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1429d71e6e906e8b58e8936ad7387cc9c4c0948dfadbdb4611206251914b9a`  
		Last Modified: Sat, 06 Jul 2024 05:29:47 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0585463d436b63027a6445f240370fc6b4e47fbaa52f7aa0cc6ee17fb6c20a24`  
		Last Modified: Sat, 06 Jul 2024 06:06:55 GMT  
		Size: 726.3 KB (726338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2dedbfdf180812e3fc53804f05d9f98aa45c6ce0fe1c12dd741e66a9483a19`  
		Last Modified: Sat, 06 Jul 2024 06:06:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7abee780b58498793a5938331f764f727da360ae725c7e9fe0e6fa242f8f866`  
		Last Modified: Sat, 06 Jul 2024 06:06:56 GMT  
		Size: 19.0 MB (18953418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:c77ca468a46bb66ffdbf576c03b425502a9c56a168cdf8f8e1e3eb7a81bcf3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 KB (362199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99c497f40a46ca4f0f02667f41f91d76633ab46a3c2b936fcc515eb053b3222`

```dockerfile
```

-	Layers:
	-	`sha256:27be82eef46b8f85de71264bba13d74687f64ee5e2843d72172495b7aca82039`  
		Last Modified: Sat, 06 Jul 2024 06:06:55 GMT  
		Size: 330.0 KB (329951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ae34d64113e9b5dae05ada01e7c1741b8cc7adbc3b54c305145b5cc51713e9`  
		Last Modified: Sat, 06 Jul 2024 06:06:54 GMT  
		Size: 32.2 KB (32248 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:59ac983f9a87afe3922a704b1ae7843959cf1e55b9f133fb338e1f7be5c4fd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55921250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62670c060cd72a3a7295277c0511947563f1fe4bbbe57fce457a8c2b0050aefe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.21
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01446ea5918cdf1fe1b865bb8d7330b56410ce93061441cfcbd2f22e4a75c328`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 2.8 MB (2829133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121d7c7e80736da27a924b7bbc4c7d347f8de1e1e5d1227f2732342fd44df0a3`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7858568419b94cae9ac32ee0afc3ecfeb070d2bf79da8598e2e9e20e51a82578`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d71d56eb6f4c2ce28105392f6cf227d8a82996c669bd7bd86ab5866364faa`  
		Last Modified: Sat, 06 Jul 2024 02:36:40 GMT  
		Size: 12.1 MB (12128108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770369fbd5b29ca943ac0dbe894618b0b9333e51cb983fdb5e8c7db952b155ee`  
		Last Modified: Sat, 06 Jul 2024 02:36:40 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96085ecbe366fb5e86ce7dd6ce3d341a1dd64a2f9dc7a5366bc9afc31a20b6a`  
		Last Modified: Sat, 06 Jul 2024 02:36:55 GMT  
		Size: 15.3 MB (15338893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f209e65a29485ca2b9af2ba729c4e595bca9aee74bc446def577ecbd4ac64ae`  
		Last Modified: Sat, 06 Jul 2024 02:36:54 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127a6f40955a853109b0eaa87c0b3a9ef3f7cda68760a5be0e860b501f893cdf`  
		Last Modified: Sat, 06 Jul 2024 02:36:54 GMT  
		Size: 19.4 KB (19387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb89b7821a6c6c707248a4eb0054f2460771b2ad0fd107f07849712869edcf2`  
		Last Modified: Sat, 06 Jul 2024 02:36:53 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aa7b2bc17e66b5b5a1a107778cfbbc80321ab64b42db02545aad7beb14b5b6`  
		Last Modified: Sat, 06 Jul 2024 05:17:23 GMT  
		Size: 2.6 MB (2554982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24b989d72e912e8b4de0299c59ce86cc4e571e58068caef5d2e2cd64d5c0d55`  
		Last Modified: Sat, 06 Jul 2024 05:17:23 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d8a674a2a6683bc81eee0879f2195c854646b7b050bc8973382ae0c130153`  
		Last Modified: Sat, 06 Jul 2024 06:09:20 GMT  
		Size: 726.3 KB (726338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3091b5a38af2d56718d46f9d83c30f9251ca4610348e80ecd3778fb357bb8c2f`  
		Last Modified: Sat, 06 Jul 2024 06:09:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975df2f4231a7abb264ff50dc2c620272d3367f68bd555fa9f819be061089517`  
		Last Modified: Sat, 06 Jul 2024 06:09:21 GMT  
		Size: 19.0 MB (18953203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:ceb36b56941fd5a9c4fe3b12d09f02bd95e687027db1a6952310663b20564644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.8 KB (362750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfa31fe048d313a071de2dc82547a4d6e414888946c5c8b501a37368be9e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:82c6ef5ac2489297d4c40855cc35ddf4c46f8076ae078d4987a8d43278f50d75`  
		Last Modified: Sat, 06 Jul 2024 06:09:20 GMT  
		Size: 330.0 KB (329979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ae111da116d06744b8d9942f683a1481ca1eac6f53ccb0eee4c508b4f93c06`  
		Last Modified: Sat, 06 Jul 2024 06:09:19 GMT  
		Size: 32.8 KB (32771 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:19a1a130e9613e2ca1c2aab901b5861659410a570aa9d1b9b56170854ed0c300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53437176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17f7e764bf3dab04671acbcc8278af3208bf0343592dff0777a6aa7644c2403`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:fef5870f3bb90ed437c0331d7e65e52da6728b66d231aea95a605935fef056d7 in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.20
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e9c6bf0d8f3154c26ee87ffe9feb02c91666069b8cbe0668cfae10922ad80c49`  
		Last Modified: Thu, 20 Jun 2024 17:39:06 GMT  
		Size: 3.3 MB (3250890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee93461fb0affa26ec63de4968aec9b190a692f67387914ce5413631503cfc9`  
		Last Modified: Thu, 20 Jun 2024 23:00:58 GMT  
		Size: 2.8 MB (2839145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce563d818438283f6ad202048afaf917002b477ed8e9f7cf92f702cb6e107ec`  
		Last Modified: Thu, 20 Jun 2024 23:00:57 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bd536aafcd34aa58a5e1fbb549c18ea11942f80f21b693f10fb0b654c9cfeb`  
		Last Modified: Thu, 20 Jun 2024 23:00:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c7e95739d8f5c8d81755a873a59d74d2905411c06af77b2981de91c33122ca`  
		Last Modified: Thu, 20 Jun 2024 23:02:55 GMT  
		Size: 12.1 MB (12118923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44816f1dd08a0f66a6b875e917b58226828bb008cafdefc14b3282678abc2c6f`  
		Last Modified: Thu, 20 Jun 2024 23:02:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ab909de62441379d34b0415a0dd37e152c39a30d7dfac2f964c37a86ff92a4`  
		Last Modified: Thu, 20 Jun 2024 23:03:14 GMT  
		Size: 13.2 MB (13197972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb63279887715fab90f40fe719b0b96b93e046c178d4dfe837dd6f2b2c6b7ba`  
		Last Modified: Thu, 20 Jun 2024 23:03:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77f6da55977bb8c6b6ecbb9526a234fa1494d9d8cca528158154417b9d1d835`  
		Last Modified: Thu, 20 Jun 2024 23:03:10 GMT  
		Size: 19.6 KB (19558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4afed3e155dcfacf8c0734ff110722b493d217d7461a166247f5ec0fb90ca`  
		Last Modified: Thu, 20 Jun 2024 23:03:10 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da59c7a85727a3f439dfff98195a61d08881288f2cf589d4b4793bb2466a69ca`  
		Last Modified: Fri, 21 Jun 2024 02:00:59 GMT  
		Size: 2.3 MB (2317194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7a46354334844035bfe94fd72bfc68b73bb74abf584cb9029af52260360988`  
		Last Modified: Fri, 21 Jun 2024 02:00:58 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621977be19152d6f8618640fc58a863b5532cc15f75830c8bd8a3f7bb6babd79`  
		Last Modified: Fri, 21 Jun 2024 02:00:58 GMT  
		Size: 726.3 KB (726328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a0074a8111d27408a42492de8165cc1df44cd4a5a469225c3773a480224984`  
		Last Modified: Fri, 21 Jun 2024 02:00:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186fc773d724482acfcb67c9825284a605853deeca690c86ebd97561df0c2e55`  
		Last Modified: Fri, 21 Jun 2024 02:01:00 GMT  
		Size: 19.0 MB (18953164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:6f68951a756fe6cf554af827b889d644c0efc20d1a738b13d8d183b585dfc8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 KB (364451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65975657a5f878dea30f7946958cb57ac1f299d6ca1019a4755dd080b105663`

```dockerfile
```

-	Layers:
	-	`sha256:7dc256b18f175948fbada2f398a29c302e41e0b6a83e6a72f093014fc396b3fb`  
		Last Modified: Fri, 21 Jun 2024 02:00:58 GMT  
		Size: 332.4 KB (332442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7467538b82fcebb32da9777370d38fb63527bf0e5fdf47fa5f052a54d380917`  
		Last Modified: Fri, 21 Jun 2024 02:00:58 GMT  
		Size: 32.0 KB (32009 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:271b3d51c6c89ee4a75fa1d2e6a3925605398aa56159d07d8f34f3068f801d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53498487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc687c18cf20b5b3a47098021c9f4dcc81a8c7244e654086df55aefed83c8a72`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.20
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eb9ede040a8629a36c19a1019af3a33bdcab0e9b16dd4e50894df992e2bc57`  
		Last Modified: Thu, 20 Jun 2024 19:40:08 GMT  
		Size: 2.9 MB (2858706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1732b6eaedabe72854b318d620f62ca5985f9320a089bd90b6c760234d0c540`  
		Last Modified: Thu, 20 Jun 2024 19:40:07 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4078b4ab583744a8a16db200a1b0a44450c6b122867ead7a14b2a395921cd4`  
		Last Modified: Thu, 20 Jun 2024 19:40:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401f7ec3a545a393748afd413b96edc1d1a7d1a96a15d02f1ffaf1d652e4d686`  
		Last Modified: Thu, 20 Jun 2024 19:42:04 GMT  
		Size: 12.1 MB (12118918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5d8169172cbb51d4754bdfb510f495754ed53d9795cc0877906721d1bee64`  
		Last Modified: Thu, 20 Jun 2024 19:42:04 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24502c03f9ac65a961c293a00f80fac893912909f98471dddd1c27c0174139d3`  
		Last Modified: Thu, 20 Jun 2024 19:42:21 GMT  
		Size: 13.3 MB (13342070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff6274fe7275ae6cf86fe95c2dffb6db1f570bf5b7f3730264b5509dd834da`  
		Last Modified: Thu, 20 Jun 2024 19:42:19 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7bfe2f4b618a2635b70dd457dcc5ac235ac4fda212c48a6d49c3e129ebc81c`  
		Last Modified: Thu, 20 Jun 2024 19:42:19 GMT  
		Size: 19.4 KB (19380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb6b5ccc954a4b32ee891a9b0b8d6a1ed5585e580c8ff92ca21ec1d6be5a744`  
		Last Modified: Thu, 20 Jun 2024 19:42:19 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12ccae45e04dda068c03b20dd3654329bceeddeaa6c4ce516edb407a922e251`  
		Last Modified: Fri, 21 Jun 2024 03:29:59 GMT  
		Size: 2.1 MB (2105092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd52057e424ada2c8ef9b5a7a5d0f4c230a9c5ff250e7556e9beeeffd34b7798`  
		Last Modified: Fri, 21 Jun 2024 03:29:59 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c3e4b6363e1de83bc894bb44098a677c81607d7f2e372de51395e5e99b7b1f`  
		Last Modified: Fri, 21 Jun 2024 06:25:29 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366f3fe7fa87154a1e1ca78a004dc0244f78585a706458fca221bebf16a38b43`  
		Last Modified: Fri, 21 Jun 2024 06:25:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8367b23e2a3d1f9584132baa4568105a470059ae0e99e0efb324d45e2919a24`  
		Last Modified: Fri, 21 Jun 2024 06:25:30 GMT  
		Size: 19.0 MB (18953333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:f36e86c56a93051e13adb92ece32e66a4f9dc638cbc662342b965bf22dc0ea94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 KB (360169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107b13a66e294a8c6da21e532cad2e72e030d416ed5d6bc921373cdfbba21675`

```dockerfile
```

-	Layers:
	-	`sha256:171e978ac7ac174e2d8b4a67191f093c95d1b2b3a680a821cd2a16019646d40a`  
		Last Modified: Fri, 21 Jun 2024 06:25:29 GMT  
		Size: 328.0 KB (327991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:521ece96c17f0a8bf8fe4962c032056f276794da731f8bd96732616e8cea7aea`  
		Last Modified: Fri, 21 Jun 2024 06:25:28 GMT  
		Size: 32.2 KB (32178 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.2-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:463ba2f4fadd811636aef9d40b4b7bea0e36c5bc9aaeae221feba6f5ef18e0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55171012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1ae1fb54a06f8a64d528e609c97e073fce5f656e968c9a527ecac37800d226`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.21
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7206a1bfab077fd781ea2f1bff4245da6a985c14e5ac529be337f2a603bfe2`  
		Last Modified: Fri, 21 Jun 2024 02:03:40 GMT  
		Size: 3.0 MB (2956393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127507485549677fb9d01f808d1e93e9bd9c50738e97f7d5f24eb6c5c0177d39`  
		Last Modified: Fri, 21 Jun 2024 02:03:39 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d9ac49dc0992d0026684046dc69d1afde3acf6907aaf78e13654907905c8b7`  
		Last Modified: Fri, 21 Jun 2024 02:03:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6b26240051cb075d6cd566fba9974144bc239fa9494331cb750ea06d0a086a`  
		Last Modified: Sat, 06 Jul 2024 02:12:57 GMT  
		Size: 12.1 MB (12128107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c35ce0196eb7f7970b7a5aace64fc45d316c99012e6458a500a0cb038f886aa`  
		Last Modified: Sat, 06 Jul 2024 02:12:56 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af49b55935a663258837d86c7c79e62c88b5118378b767a2104eca7cdedb6e70`  
		Last Modified: Sat, 06 Jul 2024 02:13:09 GMT  
		Size: 15.1 MB (15122311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad75a227691311b10f98d104a1d99fe699846182c3c440b46747994d0da5f58`  
		Last Modified: Sat, 06 Jul 2024 02:13:07 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf273803a6e8761d4182808f91636c7ef245c6643be3c1cb2e99e5a859215e94`  
		Last Modified: Sat, 06 Jul 2024 02:13:07 GMT  
		Size: 19.4 KB (19372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295aa649f23a1813f18118fd39becd982caa78f641b1d358c03b3e8506d58416`  
		Last Modified: Sat, 06 Jul 2024 02:13:07 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c21577ba51ac5e5ff82dc61428614fcb3f8f8db643b1f55e7a1c63dca72fdb`  
		Last Modified: Sat, 06 Jul 2024 04:19:02 GMT  
		Size: 2.0 MB (1998725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901f9f7eb9e9e7f896eb9486364b3143d1d174055b70a9f1dfc8853bbe67160d`  
		Last Modified: Sat, 06 Jul 2024 04:19:02 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeb093a8e32bef309ab3fc51f402d6bd52a7a182778cc65144ebbbf423b206b`  
		Last Modified: Sat, 06 Jul 2024 06:05:52 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680c65776939655e172050e3c1c6d39fbb62ef0adc81a37eeea7850d7fd5d5e`  
		Last Modified: Sat, 06 Jul 2024 06:05:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45399c8b05747de7bc9a8fd54674ff42acb99c0323221590ae5f9af8c841e356`  
		Last Modified: Sat, 06 Jul 2024 06:05:53 GMT  
		Size: 19.0 MB (18953268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.2-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:d007a49f0c63b5f89bca4eec49f17cc9e37af2450c27c144fd9f5c54dae7b2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 KB (360059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27291436116aae8de45ea2585286c45833d594eb6589c4d577b037ee08d74d51`

```dockerfile
```

-	Layers:
	-	`sha256:2e94aeb2b2f5ac75efd11dede9823d6463a5b8c53aed9cc30e5f84cc66c75dd6`  
		Last Modified: Sat, 06 Jul 2024 06:05:52 GMT  
		Size: 327.9 KB (327945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3e8eaea4bf29db1b1df9b4aa3b6c71717d3abb8fe7b96dfb7d254afe8865ea`  
		Last Modified: Sat, 06 Jul 2024 06:05:51 GMT  
		Size: 32.1 KB (32114 bytes)  
		MIME: application/vnd.in-toto+json
