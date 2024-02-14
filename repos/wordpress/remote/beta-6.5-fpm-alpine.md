## `wordpress:beta-6.5-fpm-alpine`

```console
$ docker pull wordpress@sha256:f4060eec88ff0f6155d0828e88fba7b38725cdda567588034be9d6b564f16b4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `wordpress:beta-6.5-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:8efa02f30626005e7504ca1f67a314446bdff99570940fb431dcc099fd0db9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89267666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c2805e71f75bd793b71bbfeaa2826c0fa6749be231b6ede4ced495a554bbf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:42:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 04:42:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 04:42:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 04:42:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 04:42:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 05:24:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 05:24:12 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 05:24:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 05:24:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 05:24:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 05:24:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:37:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 05:37:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:37:40 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 05:37:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 05:37:40 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 05:37:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 05:37:41 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 05:37:41 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 05:37:41 GMT
CMD ["php-fpm"]
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta1'; 	sha1='872eb3105b7c1c3d365a7df183b4748f6822c267'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 13 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 20:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91a7316d2e2098b1a91882947964b19bab201421576e249c440063e956bcab`  
		Last Modified: Sat, 27 Jan 2024 06:46:12 GMT  
		Size: 2.8 MB (2825332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a5caaf92a60154c94967702a2fdee5954dec8352f776f8abc87659c4de67f6`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d170158e1d1cffac62a145eb90dbbfd417840d1e2a9a4ae707cafa0bcc2781`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b705d96a822720c651828184408f1a6c9eea23d8197c63f104bccb6e1d73ba73`  
		Last Modified: Sat, 27 Jan 2024 06:49:03 GMT  
		Size: 12.1 MB (12096383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bce88821860841ad9fb8f2aa35e55484bf761143949eab88642252b79cad41`  
		Last Modified: Sat, 27 Jan 2024 06:49:02 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed75cac09ec5f9766a622ae1979291bcfa3db20e87749b8b96bdf1ce9fa7344`  
		Last Modified: Sat, 27 Jan 2024 06:49:31 GMT  
		Size: 13.2 MB (13195968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9ed1af92f7cd9d4833f43b5ec3fda659b5fcda099579bd9b1157f8fb3d7593`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ec9b7459eb3fb9025e10bfa088ab0bd24e214c524d477abddd714fe74a22da`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 19.3 KB (19292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd34332b4b5e6c9f8687d99b6d843b070f7aa9e20d70d6cf3b3dd2fe11b6964`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd1635b476ed62b3e8d05b91b85d433f70c7d416fd9c050c479756da4ae5c2c`  
		Last Modified: Wed, 14 Feb 2024 19:54:50 GMT  
		Size: 28.9 MB (28877528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f8b1a5698ad9f267d85ad9e6cc77d907bf8f23f3f945433b7b464703dd850`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 4.4 MB (4433161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c022f9a5e77f6f4ec9ad048839344a7bd38d0e978ed0af13f2c9ce3cc7c932`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 59.4 KB (59392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9100c3dca44d92820d35e5919882f016139bd09a0172a9ebcbe7f485c7cd37d1`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a9f118916a33ac7d0dfce1f49acf44bcc28d910901f0696aa37b6eed599a47`  
		Last Modified: Wed, 14 Feb 2024 19:54:51 GMT  
		Size: 24.5 MB (24498408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0c8dafe4bc476417175ed02bd02ace2f54db04fcd633bd4f8a9f4830ea5905`  
		Last Modified: Wed, 14 Feb 2024 19:54:50 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb72d4b8506a77212e04d759868203b51b720227bb24f6727ce75345f7bad3f2`  
		Last Modified: Wed, 14 Feb 2024 19:54:50 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7e8a952889bc9c46ff6c1eb349b38c5ca58088d9021c9c2b3f648b9f85077e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.8 KB (911776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f9bc4f809a10a147345ccc7f0d8b38ed362371147d576e337e4ee121c076f8`

```dockerfile
```

-	Layers:
	-	`sha256:abc3d2401e15922789005f820e350e5341a07f27876ea527072334342dbf6696`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 864.2 KB (864182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110403a2e6c712799f063d34da1ec1e074e183929a0868a237732b63c94ad46e`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 47.6 KB (47594 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:2eb3b4fa2996576857b1e964b019d1c1f13c5e3e094b6b6a20ac76b746e38d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90059955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff21612bc22a966f4254061432d70df5f758eb448f54b82ed37cef190f707ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:26:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 03:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 03:26:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 03:26:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 03:26:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 03:26:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:26:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:26:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 03:44:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 03:44:29 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 03:44:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 03:44:30 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 03:44:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:49:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 03:50:00 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:50:02 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 03:50:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 03:50:04 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 03:50:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 03:50:07 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:50:08 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 03:50:08 GMT
CMD ["php-fpm"]
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta1'; 	sha1='872eb3105b7c1c3d365a7df183b4748f6822c267'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 13 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 20:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8953adc2ed89719cf332d6841a33f5396f09790ebe287db3934fd2327d14b7`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 2.8 MB (2842838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a412c6f832e805dac7f8f5eb85b03e9340bde010929c469a7aa203611edf867d`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ad5c29bf6c410c283dc6e7c4619fb7570382a7860ef5d8b6a00e3228ea8a03`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dfc65a6989d02faf8ba64268e70055439b4184c1af31338fcc69df9aa4f4b4`  
		Last Modified: Sat, 27 Jan 2024 04:24:19 GMT  
		Size: 12.1 MB (12096378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc874be9fcdd85b468fdcd00a7ac26557a1dfa6ce3d214db4870df31d7669dd`  
		Last Modified: Sat, 27 Jan 2024 04:24:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee81264d77cbed5dd874c4a761f4e67f0318331456d87eddcfe8d4e300d3248`  
		Last Modified: Sat, 27 Jan 2024 04:24:48 GMT  
		Size: 13.3 MB (13338992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f291bcd4f88be6c7991d439cc1a391b19dac2294394a49112b4f5b107ee2b3d0`  
		Last Modified: Sat, 27 Jan 2024 04:24:46 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6b9d2ddd88902f6fb0a5c19a8b7ef7e3e5ba6782d74407d0345c3974feb779`  
		Last Modified: Sat, 27 Jan 2024 04:24:45 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce7c07f8ad7e826f226f530b811bd96fc32d55f47f15f89d99bb5a51c051e6`  
		Last Modified: Sat, 27 Jan 2024 04:24:45 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5ae5ac9534f96f0907b865b363f176137e21f41604eba47533c296c414be43`  
		Last Modified: Wed, 14 Feb 2024 20:25:58 GMT  
		Size: 29.4 MB (29379011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fb89b0344de3ee675712287fca52e1dd42684591f6e45c23e2edde10425eb1`  
		Last Modified: Wed, 14 Feb 2024 20:25:57 GMT  
		Size: 4.4 MB (4449361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195902de5b4a91f554ebecad4e5b1df04d6539cac008efd94052a734f0fb72dc`  
		Last Modified: Wed, 14 Feb 2024 20:25:56 GMT  
		Size: 59.4 KB (59410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217420d66c83b4b8b80dfd9862b4df96cfc50e7e958d30b0c4142073f809ce57`  
		Last Modified: Wed, 14 Feb 2024 20:25:56 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3752d0baf43a66f34ac9d42cbebb02123034d57ae0d952425d08b5af459efd32`  
		Last Modified: Wed, 14 Feb 2024 20:25:59 GMT  
		Size: 24.5 MB (24498396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71acc8b252facebbab55b71d2a770aa7e575ef1418880667e07b0e8a4d583788`  
		Last Modified: Wed, 14 Feb 2024 20:25:58 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd095623edf84ce158e20210e50514c9e6668696acfbe4bf8ee237a195d63b7a`  
		Last Modified: Wed, 14 Feb 2024 20:25:58 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:78d034d629fba7cfd2a819932ef9c12bdc2e8d438c20e5ab5e6341c08aa07b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **908.7 KB (908745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b63fb7c6c8ba1a962c0660117b8dc61a5896a24e5f5c8b55058f43effb761`

```dockerfile
```

-	Layers:
	-	`sha256:ae8c65f18341b27b056cbd676bb8df8898b32c579a8dbf4c50dabed78e8baeb3`  
		Last Modified: Wed, 14 Feb 2024 20:25:56 GMT  
		Size: 862.6 KB (862649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819d98cbdaf7eb14643f286390ad3b83a555d09c5881ab8f2cf958ace8b29cad`  
		Last Modified: Wed, 14 Feb 2024 20:25:56 GMT  
		Size: 46.1 KB (46096 bytes)  
		MIME: application/vnd.in-toto+json
