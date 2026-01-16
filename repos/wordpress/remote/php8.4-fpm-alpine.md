## `wordpress:php8.4-fpm-alpine`

```console
$ docker pull wordpress@sha256:a8fdb79be0839683fa9963f997d1505d781880dff0000225ef897638f46ac575
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `wordpress:php8.4-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:5a62db51934316d2054876aee0718bcea6b520e8152aa279ca820ca4152bc38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105653820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd021eec73883e3c0c144448766d12a78e187e8f4a3fbcf43f71574a76a58d4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 23:04:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 23:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 23:04:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 23:04:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 23:04:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 23:04:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:04:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 23:04:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 23:04:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 23:04:14 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 23:04:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 23:04:14 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 23:04:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 23:04:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:07:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 23:07:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:07:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 23:07:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 23:07:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 23:07:28 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 23:07:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 23:07:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 23:07:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 23:07:28 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:53:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 15 Jan 2026 23:54:03 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 15 Jan 2026 23:54:03 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 15 Jan 2026 23:54:04 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 15 Jan 2026 23:54:05 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 15 Jan 2026 23:54:05 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:54:05 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 15 Jan 2026 23:54:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:54:05 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 15 Jan 2026 23:54:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:54:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a33dfe9a56d3896d919b47fbc71ca0b3b508cf2280a80c2e8654b202036410`  
		Last Modified: Thu, 15 Jan 2026 23:07:43 GMT  
		Size: 3.6 MB (3591425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173e3992a8b80df213564732cdf246153cab1d2754a419fc972eec1d54993e8`  
		Last Modified: Thu, 15 Jan 2026 23:07:43 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148cfba25122be912dbbd01103b899c186bb9dfe232d3d2e216291e9be2a41ee`  
		Last Modified: Thu, 15 Jan 2026 23:07:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d99bb2a0ae5a5b99582a8ad9960180844d066f5e0b72d9d4c54ec2a625c8c`  
		Last Modified: Thu, 15 Jan 2026 23:07:44 GMT  
		Size: 13.7 MB (13694306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60472fd5955f4b78b89cb2bba65e6418d312c89dc1b6c56725b025851299e70d`  
		Last Modified: Thu, 15 Jan 2026 23:07:43 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c6404755401240e3b80a7239964607fd531ead459e6b39c52e46f3a0fdd7e`  
		Last Modified: Thu, 15 Jan 2026 23:07:44 GMT  
		Size: 15.2 MB (15183309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426e222c4335700f5e5e639860ed2c3dd9cf712ac198afcd6df5bef2161b2a17`  
		Last Modified: Thu, 15 Jan 2026 23:07:43 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52297a8471e57df4a9550e021b44ae32b4db4b20604329d202343d463d70990c`  
		Last Modified: Thu, 15 Jan 2026 23:07:43 GMT  
		Size: 23.5 KB (23482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a932be1f41f47f89c1cd3906887b15b396e0a925d3e3f6ef0eaaca87506678`  
		Last Modified: Thu, 15 Jan 2026 23:07:43 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d441ef4837e89f727d1c3070027804708c776302f4df18a76dc0befe8cb8e3`  
		Last Modified: Thu, 15 Jan 2026 23:07:43 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d0a83319d0e0a69a631524374a0e78195298fe6c28f5e44066ff1707ceeb80`  
		Last Modified: Thu, 15 Jan 2026 23:54:27 GMT  
		Size: 32.8 MB (32820026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd22befa4149d2c8b6576eb84d3094e098b3adba2332b2ca8cf398f090d56e59`  
		Last Modified: Thu, 15 Jan 2026 23:54:25 GMT  
		Size: 9.4 MB (9414014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b20180f2b14eb95ff2f8b1625f1f7de0991e28368c46e01615c4791f45babd`  
		Last Modified: Thu, 15 Jan 2026 23:54:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73de4de666c4cbe5023d62a5c4425ed9d3803aac203f4cf5fcb4300fdf5d5669`  
		Last Modified: Thu, 15 Jan 2026 23:54:25 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643b44521d889f2f2045b93250f49748c08b519bbff23244c0251ca6fc322cf5`  
		Last Modified: Thu, 15 Jan 2026 23:54:26 GMT  
		Size: 27.0 MB (27025226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad116e78d0cce87cd316e70e445d5f35b388ca04207a24eba3f766a13054613`  
		Last Modified: Thu, 15 Jan 2026 23:54:25 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd3e657c318f393e09368860df043f640679fad464f33f10e072224a98e9f4f`  
		Last Modified: Thu, 15 Jan 2026 23:54:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0306f7b29710451a30c0b923f1c6adc38d8c168507fe3c11a4c74a76a9c546`  
		Last Modified: Thu, 15 Jan 2026 23:54:27 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c971ae4374e7f335f12d712983423056be99c0882a309ef6dcbdd637516d8574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664ea388f31bbf079993d7d5a68cc085bd9795737c2c42f35c0f1c8403e0881`

```dockerfile
```

-	Layers:
	-	`sha256:40af81baf5208e8dc8a396b92c00bc058e0031db950b4cda2edcf23015813aa6`  
		Last Modified: Fri, 16 Jan 2026 02:16:30 GMT  
		Size: 1.1 MB (1122037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e7e41e6e0e8bb9aec19563a336e0a7b55e6db2418ccee8abae182380b6e59b`  
		Last Modified: Fri, 16 Jan 2026 02:16:31 GMT  
		Size: 51.7 KB (51723 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:173e1f9959e522f59b968fa5f5d4299ba7bed47aa056265e4be0016e60b3eb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97830220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f74945393754bcb7d4dbb9818a3e7f4c97b0b5f862c4214828f8e3e526501d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:19:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:19:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:19:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:19:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:19:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:19:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:19:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:19:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:19:42 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:19:42 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:19:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:19:42 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:19:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:19:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:22:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:22:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:22:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:22:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:22:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:22:51 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 22:22:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 22:22:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:22:51 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 22:22:51 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:15:01 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 15 Jan 2026 23:16:25 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 15 Jan 2026 23:16:27 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 15 Jan 2026 23:16:27 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:16:27 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 15 Jan 2026 23:16:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:16:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 15 Jan 2026 23:16:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151f11231e4ef57a8e61844b471b3f583ece4e22c2ebf88966aabb7b63a547ed`  
		Last Modified: Thu, 15 Jan 2026 22:23:06 GMT  
		Size: 3.5 MB (3548058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29203c65e44a2091d357225d87a310c9ae0b01a2e615256787c9aa8516ee6108`  
		Last Modified: Thu, 15 Jan 2026 22:23:03 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3f7132ba04b7ed876138a29266f5c19a9c6f078faf4c093884ce8acb9740d4`  
		Last Modified: Thu, 15 Jan 2026 22:23:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31cd91d2fbef831e424116db3d01c6005b4d88d933e92f8e7df66e60e32691`  
		Last Modified: Thu, 15 Jan 2026 22:23:04 GMT  
		Size: 13.7 MB (13694317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dcdaa343620c0f1d341dd62bc88f5b489b28cb936c8fd71b7e4be8ce22bce9`  
		Last Modified: Thu, 15 Jan 2026 22:23:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07146652e28fe7a5d862c82d64bd5b602fd85d685ca3dd391df0a414e76d492`  
		Last Modified: Thu, 15 Jan 2026 22:23:04 GMT  
		Size: 13.7 MB (13667948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3b26911433cfc5fa5b52a0cefc9de824ad7edcbd1442ebc458319a728549`  
		Last Modified: Thu, 15 Jan 2026 22:23:03 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb60c501509bc3a151e57436a422ed0843a36dc5af4bedff043d426367ac5f8f`  
		Last Modified: Thu, 15 Jan 2026 22:23:03 GMT  
		Size: 23.3 KB (23319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e99a9a96e0cac1251202ee13c468f7d68e88503c382147d18168881693c152`  
		Last Modified: Thu, 15 Jan 2026 22:23:03 GMT  
		Size: 23.3 KB (23339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a638d16e2f55818b6cc48c66c980b6dbd4ef2e464b5ca4eea794beaed65fbf0`  
		Last Modified: Thu, 15 Jan 2026 22:23:03 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff477deb4dc847d93baa34ea75e292b11cc62fbd4647b3db7d78932cdba033d`  
		Last Modified: Thu, 15 Jan 2026 23:16:59 GMT  
		Size: 28.5 MB (28536526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244573c5f5f74ca9537bfd22169a5ac1eaf33bc3cdeeff34eb52dfc32da7c314`  
		Last Modified: Thu, 15 Jan 2026 23:16:57 GMT  
		Size: 7.7 MB (7724623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d99b91d1223707856139f9b2831f4b20a0ec6e78f11ebb4f0da9993f46bdce1`  
		Last Modified: Thu, 15 Jan 2026 23:16:52 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430878698943940bd58aa05360e4bb75a647bed3da6b4ceb0af433e8d5485642`  
		Last Modified: Thu, 15 Jan 2026 23:16:52 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db6380d5eb6f1b4f41f3b5a1c8cd73e847dd99b9dae98eb8ca74dc5d852a222`  
		Last Modified: Thu, 15 Jan 2026 23:16:55 GMT  
		Size: 27.0 MB (27025225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f921212db9e39b30dbf0b8f72b7a3cb421342ddbc8c0cbc6257e685cc8099a`  
		Last Modified: Thu, 15 Jan 2026 23:16:52 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a860d67028bb046ae9913e15c52fdc865ad5a3e9fdf1b6e6639112970d7466`  
		Last Modified: Thu, 15 Jan 2026 23:16:52 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed56fa2d9e186a23bb2bede8c8e17010e4c3c46275d70d6187b047af8531d31`  
		Last Modified: Thu, 15 Jan 2026 23:16:52 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:62c6615d1e3437998500ed6fb66025cc426c374d23e4ef41a097e4308a2ede86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0a5ddfb2d8b8516d05e2b8baa75f5dfd3702c9cf4cd89b3268584ace5de806`

```dockerfile
```

-	Layers:
	-	`sha256:f8f1fbdfb827df035130543bc228bd232ecef6f8aa46617662f390891a302128`  
		Last Modified: Fri, 16 Jan 2026 02:16:34 GMT  
		Size: 51.7 KB (51653 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:7ac95365e0503918c335de956d15b9bc308bafefc38e9d28f56de4afec9afaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95931565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a68899b8c9826636e121447cfbac4d70db37e0d66008c8337a6654f68a56e55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:31:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:31:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:31:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:31:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:31:39 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:31:39 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:31:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:31:39 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:31:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:31:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:34:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:34:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:34:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:34:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:34:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:34:49 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 22:34:49 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 22:34:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:34:49 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 22:34:49 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:24:45 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 15 Jan 2026 23:26:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 15 Jan 2026 23:26:12 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 15 Jan 2026 23:26:12 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 15 Jan 2026 23:26:14 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 15 Jan 2026 23:26:14 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:26:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 15 Jan 2026 23:26:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:26:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 15 Jan 2026 23:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:26:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a2190c65fa86394f00ed8e0f769b6c8830d84b74065a2fc9e569d0ec2612c7`  
		Last Modified: Thu, 15 Jan 2026 22:35:06 GMT  
		Size: 3.3 MB (3346829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c74993b23dc24914499561a6c094ecfe8e051a670f52138b74a3f0c837ad236`  
		Last Modified: Thu, 15 Jan 2026 22:35:05 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c897cf1f4bea64028df8476e11aebf8a95ac90fe67bbc4b9d7195bd15186d37b`  
		Last Modified: Thu, 15 Jan 2026 22:35:05 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212bb71d7fe95bd195c3048f324fcd00c35041d197d8bfa6a6a791e98de9d2c2`  
		Last Modified: Thu, 15 Jan 2026 22:35:08 GMT  
		Size: 13.7 MB (13694314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a713219758e04e311ca4bf72308ff0dc789e543f12a937c85dd823575acde62`  
		Last Modified: Thu, 15 Jan 2026 22:35:05 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2411319c9656494c3bd25d87b02aebc55b5dbf47910a12887fe1f94e12b195a`  
		Last Modified: Thu, 15 Jan 2026 22:35:07 GMT  
		Size: 12.9 MB (12906821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45e0c695e1790c063edceb8d439e29bd5f39bfab858d740f2e33fe5c8831822`  
		Last Modified: Thu, 15 Jan 2026 22:35:05 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b594126cf144adbed774eb7e5b0c90850a0964c0581522c1639ef754398b6154`  
		Last Modified: Thu, 15 Jan 2026 22:35:06 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa6f2c73dd1b77200b99ff6448b515afcf2cbbbafbbe1f59d7d472ba3acd85`  
		Last Modified: Thu, 15 Jan 2026 22:35:05 GMT  
		Size: 23.3 KB (23343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f95627066e2086146e28686b67c0991ab733fd48332bbd0702d10f10e08202`  
		Last Modified: Thu, 15 Jan 2026 22:35:05 GMT  
		Size: 9.2 KB (9219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa9a5739b3043f41601ed68c5b8d8d8ea6f3b3ad4a0b0e086b367d4dc8f172`  
		Last Modified: Thu, 15 Jan 2026 23:26:42 GMT  
		Size: 26.9 MB (26886285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba735dc596dc9c9b62bb3b360715814a944e43bf57ffe6adf84d1aa23053383`  
		Last Modified: Thu, 15 Jan 2026 23:26:40 GMT  
		Size: 8.7 MB (8727608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05f429158b76463d02e631c43fa9294ce60f1b4c1712ebc2bd48c03d3e6f548`  
		Last Modified: Thu, 15 Jan 2026 23:26:39 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027beb3bf67a26fa7fbe9be5e3d9ad3ca6b15faa3cbfe5148c44c4d3f9ccf5d9`  
		Last Modified: Thu, 15 Jan 2026 23:26:39 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ab23c6b9e5cf9d61820136c731c9200d8c4be441f73c1ce36a801dcaad8f6e`  
		Last Modified: Thu, 15 Jan 2026 23:26:51 GMT  
		Size: 27.0 MB (27025226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b5c82304065957b0a1edfd4bf7a8bf482a7ad60910c98e084f9d5fb7f7505c`  
		Last Modified: Thu, 15 Jan 2026 23:26:39 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be67890838a3868ee7543cc07a3f8082ed21f6af5de6910ba0cf7139c21a59`  
		Last Modified: Thu, 15 Jan 2026 23:26:39 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1c718cc44252d2e0a9f86064dd835c6f5aa1a7b64d5afe37faf2a4b2261ca6`  
		Last Modified: Thu, 15 Jan 2026 23:26:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7b004836c790a9ae53cfb81cf2290b3178c7f73a2524d5df6ff138292fe91d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8040a73903779e7f5ef00845668e597c4638ffd78d7ae0aca62361e62474eb43`

```dockerfile
```

-	Layers:
	-	`sha256:5dd159acd5667ed82a5247514c281dfeb9902828faec77fffe7180755862129e`  
		Last Modified: Fri, 16 Jan 2026 02:16:38 GMT  
		Size: 1.1 MB (1120179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38e38e88cf783691655f596b2b6607b32ae3011ce630b60aca37d7ac90b55a7`  
		Last Modified: Fri, 16 Jan 2026 02:16:39 GMT  
		Size: 51.9 KB (51868 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:f283386c7509f6bf8602f5d2b734153c5effe1386a9bd9a3959cdffa1967abca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104826453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4a5bfd5a98e3b388fee563d3aa257bf1a6efdc9788c0c373630aac81a750f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 09 Jan 2026 22:47:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 09 Jan 2026 22:47:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 09 Jan 2026 22:47:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 09 Jan 2026 22:47:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:47:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:47:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_VERSION=8.4.16
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 09 Jan 2026 22:47:13 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 09 Jan 2026 22:47:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 09 Jan 2026 22:47:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:50:42 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:50:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:50:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 09 Jan 2026 22:50:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:50:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:50:44 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:50:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 09 Jan 2026 22:50:45 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 22:50:45 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 09 Jan 2026 22:50:45 GMT
CMD ["php-fpm"]
# Fri, 09 Jan 2026 23:29:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 09 Jan 2026 23:30:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 09 Jan 2026 23:30:18 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 09 Jan 2026 23:30:19 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 09 Jan 2026 23:30:20 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 09 Jan 2026 23:30:20 GMT
VOLUME [/var/www/html]
# Fri, 09 Jan 2026 23:30:20 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 09 Jan 2026 23:30:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:30:20 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 09 Jan 2026 23:30:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 23:30:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081121271225baa92f1d3bee236b13f2fa023fb6a911fd7165e9e9d966d92442`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 3.6 MB (3600957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9623b68389765eee841dc588c562b05e8b8da3660eb6fb0af89ffeba4e0e8eef`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e21a42b344c900deae9f11fefc7142435bf3add3e0cc2af1225971a99f7097`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b132d7fe4bf49928fb371b95ef655dd0b5700ff29403aef297c75d02275534e9`  
		Last Modified: Fri, 09 Jan 2026 22:51:01 GMT  
		Size: 13.7 MB (13685132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89ae1c9f1ca140b1e576380beb09b4c9acc3bc29564b3bf89803353c304f874`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40eda0a31b8009bffcd5f677bed3d6e28696b8ffffac98cf7de859ddc4e0072f`  
		Last Modified: Fri, 09 Jan 2026 22:51:04 GMT  
		Size: 14.7 MB (14684753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa20cb7b2efc796edbe85bc2ad56a382981d4b03196f06569752d30a999a3c`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8c7524a9880a8e4de9e2189e2f96ecc29b9b11b2b601139a3271052507ccdf`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 23.3 KB (23347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526828f7a78402c01e32b56651979e0149456170dca5bcb2cb9e00ee3ce076d`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 23.4 KB (23359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0927879323835f9f4c50a8ecb4c5bcc57aff54f5e33a3d257e01b9144d94809b`  
		Last Modified: Fri, 09 Jan 2026 22:51:00 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe984765f92afa0a3b84a1fc0912d23c406c3c173fa66145881dcea7dd340681`  
		Last Modified: Fri, 09 Jan 2026 23:30:40 GMT  
		Size: 32.5 MB (32455148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9c5c2d5fac72afe2181d5a9f8b184ab32c5912e5cebda9b318c33d6ca7e576`  
		Last Modified: Fri, 09 Jan 2026 23:30:39 GMT  
		Size: 9.1 MB (9114386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44074cb6507005d040b3c05ffd1851e46cee3db25a3947d52e2d4f642103e4ea`  
		Last Modified: Fri, 09 Jan 2026 23:30:38 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88401fb335aa628ed7bdadb718e5ccb0ba7abc5519f33f59094790f5712056a`  
		Last Modified: Fri, 09 Jan 2026 23:30:38 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86a34a1da555fd42a306ea176f08186b0ee706eb7dc53d24d8052d9e812afe5`  
		Last Modified: Fri, 09 Jan 2026 23:30:39 GMT  
		Size: 27.0 MB (27025234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46493b1ff7deac39d2819a215d5dbf6153c3306b67d7044c307f16f9c50b7c73`  
		Last Modified: Fri, 09 Jan 2026 23:30:38 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09868dc40e4314f4c9e702dd0ecebdd141b0f9b42addcfe594a1a9f3089c86c1`  
		Last Modified: Fri, 09 Jan 2026 23:30:38 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256c6d6e49cbefd1090bb245a60748992cd519c298fcc47ab4807b6b56310d73`  
		Last Modified: Fri, 09 Jan 2026 23:30:38 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:71fccc9a7de159a4246f500c9e8c180811a454151433ef5a99a7d9eea52beb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dbd9a9491e3fa7c8c812d5de4342fef6670897b43c07b5813324b20985d480`

```dockerfile
```

-	Layers:
	-	`sha256:cb12a2a01d5b3834ececdc56f5c4312b40bbd9bd515c3aae736efe383334d692`  
		Last Modified: Sat, 10 Jan 2026 02:16:39 GMT  
		Size: 1.1 MB (1120185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46af3c7084a08f59d3f726b186ce04a3812c0d383456b9ece587763ace3893cf`  
		Last Modified: Sat, 10 Jan 2026 02:16:40 GMT  
		Size: 51.9 KB (51902 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:4b0d07cef549bde467b061251cc8e1ca48d3848ec9bfc18160e73c48abbdc0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105142909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a51b68e67d3d213f195cebb0199bc46275a60bd32d85cdbe61be87c15a6e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 22:24:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jan 2026 22:24:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 15 Jan 2026 22:24:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 15 Jan 2026 22:24:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jan 2026 22:24:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 15 Jan 2026 22:24:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:24:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jan 2026 22:24:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jan 2026 22:24:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 15 Jan 2026 22:24:22 GMT
ENV PHP_VERSION=8.4.17
# Thu, 15 Jan 2026 22:24:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 15 Jan 2026 22:24:22 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:24:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:24:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:27:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:27:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:27:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:27:31 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 22:27:31 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 22:27:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 22:27:31 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:18:09 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 15 Jan 2026 23:19:07 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 15 Jan 2026 23:19:07 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 15 Jan 2026 23:19:07 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 15 Jan 2026 23:19:09 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 15 Jan 2026 23:19:09 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:19:09 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 15 Jan 2026 23:19:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:19:09 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 15 Jan 2026 23:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:19:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c6c93f6fdd5c34e1dc9199c5b8a3e73dbdfdb418a54332fd0427a1ad9ba2e0`  
		Last Modified: Thu, 15 Jan 2026 22:27:46 GMT  
		Size: 3.6 MB (3628736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bb681187740c55b3ccfb227e8bada2cdd6d46822229871a99d8bc2adaf79e8`  
		Last Modified: Thu, 15 Jan 2026 22:27:45 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07524346dd56742518997eaa24082432ee604f802e121b2175638a94f009d7e5`  
		Last Modified: Thu, 15 Jan 2026 22:27:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d5d31806a76df81f1d84da23fd734ae56d5fc2672d3a2d0e63cfc8ec6e20a4`  
		Last Modified: Thu, 15 Jan 2026 22:27:46 GMT  
		Size: 13.7 MB (13694298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4826b61bf32037af3036ead7a8bc3191c722dd3902f4f44302c6f20601c67`  
		Last Modified: Thu, 15 Jan 2026 22:27:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc26e3ed1f06a7add0100eed1abda0bd3de95b72db606cd4c9ad59b9c713e80`  
		Last Modified: Thu, 15 Jan 2026 22:27:58 GMT  
		Size: 15.5 MB (15494529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f82fc3e008afdff657ee52e05c6b528d5fa106ea11dbaba58fb7cf3238fd007`  
		Last Modified: Thu, 15 Jan 2026 22:27:46 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb55456f4ce6336d4fab28e2406d2f538be68ff210a123ba8d56b6133ddc6acd`  
		Last Modified: Thu, 15 Jan 2026 22:27:46 GMT  
		Size: 23.5 KB (23502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664380bf57b354c6383e8234c33409f063a7a3d22d820a5de18ec22a8e2acecc`  
		Last Modified: Thu, 15 Jan 2026 22:27:45 GMT  
		Size: 23.5 KB (23528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c34ef8b71e705178f381d802c1e1d90d04dfebb48c608d5eeea5fb2613653f`  
		Last Modified: Thu, 15 Jan 2026 22:27:46 GMT  
		Size: 9.2 KB (9222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ad0a9b4dd1fa1f8768daa6170051819e00288be280cd8baa1e25e99dd7b9e6`  
		Last Modified: Thu, 15 Jan 2026 23:19:30 GMT  
		Size: 33.3 MB (33293488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b61c45a2009e91414294d19842dfe57d7882b117f1a10393cdbbdc63993883`  
		Last Modified: Thu, 15 Jan 2026 23:19:29 GMT  
		Size: 8.3 MB (8255070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36474b2fc184c825889ea3b6ebb7b09ff9316671091fc22d115b84debb240a12`  
		Last Modified: Thu, 15 Jan 2026 23:19:28 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c92d3c002a2fdd1b46bd51e9cbe7a8638b7a6327bc547d57e3be937ce687ea`  
		Last Modified: Thu, 15 Jan 2026 23:19:28 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdc62fdb03c77235e502c67a9302d1c15662ba3bcd9f52c89863429fef5ae22`  
		Last Modified: Thu, 15 Jan 2026 23:19:34 GMT  
		Size: 27.0 MB (27025225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1e7ed05959efd385ac7c6827c84f7d0114414426627120731a1b363ea654f4`  
		Last Modified: Thu, 15 Jan 2026 23:19:28 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39186a3db231ea7e757e0a131f09aec088a4e21e8479415fc96d887d232cc69`  
		Last Modified: Thu, 15 Jan 2026 23:19:28 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b055595ab8acf0311a5e3f45618dc550d4d886ab05801e82169606c019ec76`  
		Last Modified: Thu, 15 Jan 2026 23:19:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d018dee758b18213cb13b999c24f2457f53b492759d6581d2fec5fbb061e54cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ce22f8b18e5ca4db1cbc7fc29bf5d6d2d3149e19809c8daa2e703785bb2f6a`

```dockerfile
```

-	Layers:
	-	`sha256:87e885491192141eae9911aeb6514f9da1fd95459d54db0d574d0274383e7252`  
		Last Modified: Fri, 16 Jan 2026 02:16:45 GMT  
		Size: 1.1 MB (1122012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf24c3bfc85d883b5f9e890a7059e70c9e54d5910af8477c2532558fbc23f6a`  
		Last Modified: Fri, 16 Jan 2026 02:16:46 GMT  
		Size: 51.7 KB (51681 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:271583a0a98bf4c3637a3debc4ecd3a90881e66b8978f641b215bc7adf312e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107142098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427e492f9318ec0363c713cdbf19a7a9852f3eafe8c59ec03f6d5a745db3fd7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Sat, 03 Jan 2026 02:13:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 03 Jan 2026 02:13:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 03 Jan 2026 02:13:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 03 Jan 2026 02:13:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 03 Jan 2026 02:13:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 03 Jan 2026 02:13:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_VERSION=8.4.16
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Sat, 10 Jan 2026 00:33:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 10 Jan 2026 00:33:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:38:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 00:38:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:38:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 10 Jan 2026 00:38:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 00:38:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 00:38:58 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 00:38:58 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 10 Jan 2026 00:38:58 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 00:38:58 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 10 Jan 2026 00:38:58 GMT
CMD ["php-fpm"]
# Sat, 10 Jan 2026 02:46:44 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 10 Jan 2026 02:48:23 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 10 Jan 2026 02:48:23 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 10 Jan 2026 02:48:24 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 10 Jan 2026 02:48:28 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 10 Jan 2026 02:48:30 GMT
VOLUME [/var/www/html]
# Sat, 10 Jan 2026 02:48:30 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 10 Jan 2026 02:48:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 02:48:32 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 10 Jan 2026 02:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 10 Jan 2026 02:48:32 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e772e0a90d4aa4f209aab27b75a49043c6df83f144ec29ba8e6c8e964a8a165a`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 3.8 MB (3768859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb9c8b89ecca8688bdf852690f34dbf7da2dc90d2e06d7221c85ff1070c08b`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce8460d16487c23dd44b0afef57a49c4aeca53309e968b330dc8c9044d5e51`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75e031f50889f8c3deb6050e8bb962496587378f77c4493db396be3ae7c21ca`  
		Last Modified: Sat, 10 Jan 2026 00:37:29 GMT  
		Size: 13.7 MB (13685174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8670d98f01b06fbcc366c33c3b4810823e289b968e763b2a9aa27784fa64c403`  
		Last Modified: Sat, 10 Jan 2026 00:37:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c93286e9ae5ea79838bb595530293030b710f5ecdf28a35cc980302ce2c84a`  
		Last Modified: Sat, 10 Jan 2026 00:39:24 GMT  
		Size: 15.7 MB (15718707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf48b12d4078974543d49490edb5e0de80d2e9a04402cebe18bacd969286c34`  
		Last Modified: Sat, 10 Jan 2026 00:39:23 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e663300f1e41eedbc6853fc705e49b6fbf8034583f9dc28fe19f51075d1894a`  
		Last Modified: Sat, 10 Jan 2026 00:39:23 GMT  
		Size: 23.4 KB (23364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da597c676df0a14dc7f6c3eb6384c1ce80b1ea89b1f5ae96f087677a7bb499e`  
		Last Modified: Sat, 10 Jan 2026 00:39:24 GMT  
		Size: 23.4 KB (23378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef243b65b7f5d7600779702b32126e0ca9127085cd3a6aefa635e3379b4871c`  
		Last Modified: Sat, 10 Jan 2026 00:39:23 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd634eeda07a54815b828cbdd02afba811bdbee13376653b31f8b2ec31d8eb88`  
		Last Modified: Sat, 10 Jan 2026 02:49:10 GMT  
		Size: 34.1 MB (34051074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0f33336de3b2f0c26a72fb65505c808a5b1d5955e3a94e38153017ee07ef93`  
		Last Modified: Sat, 10 Jan 2026 02:49:08 GMT  
		Size: 9.0 MB (9000131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d5f067aceeeeea739db95aadd6cd58aa701dcc00552bf24c4623c3a64dc06`  
		Last Modified: Sat, 10 Jan 2026 02:49:08 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859d96d752e53ca9b3470760505d9ef4ba4781d40253685a60fc788783501a7`  
		Last Modified: Sat, 10 Jan 2026 02:49:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521629d869a9613719b2ada790c3cc398a8acbc53397e8bfdea9b04e5a7817b`  
		Last Modified: Sat, 10 Jan 2026 02:49:10 GMT  
		Size: 27.0 MB (27025230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6ffac9e579285d9d3d85bdc45499f15bd88a6a1b07a2212c40c8d350aafc50`  
		Last Modified: Sat, 10 Jan 2026 02:49:08 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b40adefc8cb3dcbb1d66afb27cb74b256ce28396db6cb951ba126de5d96b24`  
		Last Modified: Sat, 10 Jan 2026 02:49:08 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f849f329f2598b5085a29ef6b6a65c6618b88b484daee7cbb0932f29356bd6`  
		Last Modified: Sat, 10 Jan 2026 02:49:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c702bca859d16b6df539c4d420ed70d0b8ae92b3d1757c6097f3c290e60c4b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad39efca2e699b0ec8cdcadac6eb46e38227a7315a1f2cae40e4dcb535c9c27e`

```dockerfile
```

-	Layers:
	-	`sha256:665e27df78b34eeba30d56ff0bbda59f0852433ae2092ef4a4bafeacc14ef0d6`  
		Last Modified: Sat, 10 Jan 2026 05:14:41 GMT  
		Size: 1.1 MB (1120162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e134468334196e5e1fad7b316c4d79d425a342f56f0e5c8c9d7c46a035dc98fc`  
		Last Modified: Sat, 10 Jan 2026 05:14:41 GMT  
		Size: 51.8 KB (51777 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:ed868348403fd650ecee78784bf9c8a8c4b137cfee2066df3e802cd3ec794593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102289086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e2caaac9ea37214c2707e459ea1387ee6723cdedc144b12e8156f0acdd573f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 07:08:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 07:08:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 07:08:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 07:08:05 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_VERSION=8.4.16
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Sat, 20 Dec 2025 12:32:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 20 Dec 2025 12:32:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 14:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 20 Dec 2025 14:49:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 14:49:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 20 Dec 2025 14:50:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 20 Dec 2025 14:50:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Dec 2025 14:50:02 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 14:50:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 20 Dec 2025 14:50:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 20 Dec 2025 14:50:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 20 Dec 2025 14:50:03 GMT
CMD ["php-fpm"]
# Mon, 22 Dec 2025 16:30:53 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 22 Dec 2025 16:47:05 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 22 Dec 2025 16:47:05 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 22 Dec 2025 16:47:06 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 22 Dec 2025 16:47:15 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 22 Dec 2025 16:47:16 GMT
VOLUME [/var/www/html]
# Mon, 22 Dec 2025 16:47:16 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 22 Dec 2025 16:47:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Dec 2025 16:47:16 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 22 Dec 2025 16:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Dec 2025 16:47:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b530e2aa9b2657de1d52e221d1841cf1970adc8a19d28df2a836438ca82d59`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 3.7 MB (3740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f161979011df79f0935c37e8044239316a16a481a51548ff3d1420fa2b71d7b`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8e47306a76921db05f6fca6bbff42051f7da8662b35dfc0b3cc197f7cc2ee`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f07de48b98d9df76c597f487e25e8737651d83a949ff05705b978942f53584`  
		Last Modified: Sat, 20 Dec 2025 13:41:05 GMT  
		Size: 13.7 MB (13685150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9cbd39e4b1aeb020d9085575e36f25487465f2d547538f6eb8e72b9c24b73a`  
		Last Modified: Sat, 20 Dec 2025 13:41:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1366849919efac8c73460f931838e5f6866ef65b46101e18ce4a5b3d78577f06`  
		Last Modified: Sat, 20 Dec 2025 14:51:05 GMT  
		Size: 14.5 MB (14455154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d3f79a2e1f3ee9e68e13c2dd4b6b679b730a667bbca7a7e0ffe6004f6ccd9d`  
		Last Modified: Sat, 20 Dec 2025 14:51:04 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5103ad93a9b5d725810109621e7f9f3f96fe4d02599fa1e5dd3fd89c8dd8d143`  
		Last Modified: Sat, 20 Dec 2025 14:51:04 GMT  
		Size: 23.3 KB (23326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5545fcf0afb271650a0465d9e688304a0fd5e6b795dad6d6c74297f3be749201`  
		Last Modified: Sat, 20 Dec 2025 14:51:04 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e157f6f72a2cb2f8221607f51cc2a26715fea7a21f321d9061014c42798b197`  
		Last Modified: Sat, 20 Dec 2025 14:51:04 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ff6e0ea9de29390dee98dce710501b8c097f6629a7d5564553043949ff600`  
		Last Modified: Mon, 22 Dec 2025 16:49:27 GMT  
		Size: 32.6 MB (32639984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a8c81d7e67fdf22e61a4cc104d155c9bfbacad400c97e32f04e5b507cd35fa`  
		Last Modified: Mon, 22 Dec 2025 16:49:24 GMT  
		Size: 7.1 MB (7094314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da0d8a3713ce9ed92ee221ff8ceff3c003bcef43bb0beda45d5c98a9a87eb33`  
		Last Modified: Mon, 22 Dec 2025 16:49:23 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee8316760306e9f09ad4b036a8ca0caae34b4220ffa37f864f7e4848a0160be`  
		Last Modified: Mon, 22 Dec 2025 16:49:23 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36da0c72227d6cf7e266b18d3c58beaf50a310ffb7757a8af1cb088390c2e93c`  
		Last Modified: Mon, 22 Dec 2025 16:49:26 GMT  
		Size: 27.0 MB (27025236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1078a9ded626bee64d46ef80bd06b2925510f52a90aa4dea2aacde83a632e76b`  
		Last Modified: Mon, 22 Dec 2025 16:49:23 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c93dda8196109713e558075fd5511142b172244140a974247723e865979485`  
		Last Modified: Mon, 22 Dec 2025 16:49:23 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b442e687e96f19a458327f01174dddf442dae310411292e9b6ac146ca11f461`  
		Last Modified: Mon, 22 Dec 2025 16:49:23 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:b0b959109de7b512df27334f600f048735a079b7bc0afeeee2b734b09b1de28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064bac12ae98ae6a28f2889cdfa471134eeefaaf22fdf901b681843789950fd4`

```dockerfile
```

-	Layers:
	-	`sha256:3ebff2c0522cc8faf6f83bbe4dcd934df52d4acb8a0d68d53ab079a1c9a06ac0`  
		Last Modified: Mon, 22 Dec 2025 17:14:02 GMT  
		Size: 1.1 MB (1120158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e57126777fef10cbc895e75a652dda277c172907d4b5b357f5d5056c183186e`  
		Last Modified: Mon, 22 Dec 2025 17:14:03 GMT  
		Size: 51.8 KB (51777 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:07b969b85e72c3760f6dff475d342d98a37a1e6998d96e39a08c63367c179700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105906786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eabe43bfc857fabd56ae20587325cf70892f93d81d445754304ba7a8052c4ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:30:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:30:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:30:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:30:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:30:50 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_VERSION=8.4.17
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:38:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:38:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:43:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:43:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:43:18 GMT
WORKDIR /var/www/html
# Thu, 15 Jan 2026 22:43:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Jan 2026 22:43:18 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 15 Jan 2026 22:43:18 GMT
CMD ["php-fpm"]
# Thu, 15 Jan 2026 23:29:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 15 Jan 2026 23:30:41 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 15 Jan 2026 23:30:41 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 15 Jan 2026 23:30:42 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 15 Jan 2026 23:30:43 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 15 Jan 2026 23:30:43 GMT
VOLUME [/var/www/html]
# Thu, 15 Jan 2026 23:30:43 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 15 Jan 2026 23:30:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 23:30:43 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 15 Jan 2026 23:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 23:30:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9af672712b2dab3c8a68ddbd40990098668c349a31bf4fe54360519012d2e9`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 3.8 MB (3794529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e82f0b184abfa92d79d92b03514acd8b9f92c2ca083f9fa2e62587fde8871a2`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b827f069b40835efda3a88ba34853291bec4baedd59564b9d33abc39667950f2`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9915ee6e7bc986c6bc00ae2c7377c4d1c1da6dbf61e114f2c04afb7dc64a0bce`  
		Last Modified: Thu, 15 Jan 2026 22:42:52 GMT  
		Size: 13.7 MB (13694323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f9ccec429d4e1a40b769a08c6f8d17f5bff7a5d62fd841f4289153c436a1ec`  
		Last Modified: Thu, 15 Jan 2026 22:42:50 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a407f2c328e5a18805d337d681f17b642de3d8c9212011c3ff2429a6a60c0bb4`  
		Last Modified: Thu, 15 Jan 2026 22:43:38 GMT  
		Size: 14.9 MB (14937420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c362a94da127124552fae11ffa50cb8d55fad52ab275beae95b230e31b2f8ac8`  
		Last Modified: Thu, 15 Jan 2026 22:43:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f1f65cd6a194f15031fda4d062aee532f193b26a35b25d2497bc4303580e62`  
		Last Modified: Thu, 15 Jan 2026 22:43:37 GMT  
		Size: 23.3 KB (23345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f7c47560b39f708a2870f22295445625d58b38c19d51f4f3393fc135d2863d`  
		Last Modified: Thu, 15 Jan 2026 22:43:37 GMT  
		Size: 23.4 KB (23358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cd6b5f7289941b9401b5abb1b81419dec7f5d515d1b45a3ed72c1e14959ba7`  
		Last Modified: Thu, 15 Jan 2026 22:43:37 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb5402b2943b7ae8ad68e0a146a18363b9a61079863da8c39fec783ea3757ce`  
		Last Modified: Thu, 15 Jan 2026 23:31:09 GMT  
		Size: 34.0 MB (33987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d81fdd41da0d472c9846963c1de6b5a51df5efa17a65e3ba2205def4f504d0`  
		Last Modified: Thu, 15 Jan 2026 23:31:07 GMT  
		Size: 8.7 MB (8678564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc13623c6f1391d76b24508d63010db4d7835dbcbc11206f36bc763e16679cb`  
		Last Modified: Thu, 15 Jan 2026 23:31:06 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3de6a4c4346783d29cf89af4d897397adb40aeda36b4129589c792b675a64`  
		Last Modified: Thu, 15 Jan 2026 23:31:06 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91a0a92f8c904a9cfcf3decaca45fcf526942a9ecd3959041fcbd5571f859da`  
		Last Modified: Thu, 15 Jan 2026 23:31:09 GMT  
		Size: 27.0 MB (27025229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad291dd74feb5ee34dac62de7165996bcb1ced290ad554653d9783973cf46db`  
		Last Modified: Thu, 15 Jan 2026 23:31:06 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac44b21a6f5b0bbe8162f847fe633d7877aafae96727480558375ebd56f68428`  
		Last Modified: Thu, 15 Jan 2026 23:31:06 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd2d65ea651971d2c5f97a4083bb58badcacda016dacfe65128a04a6f5403`  
		Last Modified: Thu, 15 Jan 2026 23:31:06 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:896bda16dbd8eb452d7ce9b428acdc635526eddfa9af5e3538e449be12dec9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5051f8ecefeec6ee51cd2eb7934534f7d3609cb12b307944d609cec5a8d1b8`

```dockerfile
```

-	Layers:
	-	`sha256:ffdfa92b2d89f5f678d920eb9a513c8c0327b8b759a29d8cd580c50f6a53ec7c`  
		Last Modified: Fri, 16 Jan 2026 02:16:59 GMT  
		Size: 1.1 MB (1120142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac9641e59ed2badd0e1d92dcb8f38c6c6c0adb37d9e35c16f531c59d7d006099`  
		Last Modified: Fri, 16 Jan 2026 02:16:59 GMT  
		Size: 51.7 KB (51723 bytes)  
		MIME: application/vnd.in-toto+json
