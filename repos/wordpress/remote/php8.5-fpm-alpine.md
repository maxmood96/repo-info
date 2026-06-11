## `wordpress:php8.5-fpm-alpine`

```console
$ docker pull wordpress@sha256:f83b4535729f95b0adfbc6ae116f6057121595d97007214386ac61a0319f7227
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

### `wordpress:php8.5-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:ecc5f606f7c7de3a993284db7c4d960e892d6550a2aff2ae8b5ce9a6b39c0381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113126829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8936f80d86c6efa1a9d0c8a24e2d95cb3e6fccb86b8821feaa96c87f584edec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:53:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:53:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:53:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:53:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:53:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:53:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:53:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:53:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:53:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:53:41 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:53:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:53:41 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:53:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:53:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:57:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:57:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:57:06 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 20:57:06 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 20:57:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 20:57:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 20:57:06 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:15:34 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 21:16:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:16:30 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 21:16:30 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:16:32 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 21:16:32 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:16:32 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 21:16:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:16:32 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 21:16:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:16:32 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73885a30b4594dc1ba7816c8b567c0b6aab970cdea2eb34fd27efc9e418e49c4`  
		Last Modified: Wed, 10 Jun 2026 20:57:13 GMT  
		Size: 6.0 MB (5975990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67158ac2f4aff7ad0d3057b6dae59595e7a2e499ebc2ac7e0be7faade0ecb1c`  
		Last Modified: Wed, 10 Jun 2026 20:57:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92e2b2d3524bc199f393ae6329c80b7d27a7c6e97369e41176dd125d4f56eef`  
		Last Modified: Wed, 10 Jun 2026 20:57:13 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcba1b0f5d784770da86dc38778fc43a200e9bf1d02a9e0d930483531b89b147`  
		Last Modified: Wed, 10 Jun 2026 20:57:13 GMT  
		Size: 14.4 MB (14421884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735b98b1e947401bce67f01439356149c5a23ebc532601180f9b4af6c6de1f8`  
		Last Modified: Wed, 10 Jun 2026 20:57:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7631a4140ff83ff175a1330b7aa51ba499326bbd746ccbdeed362bf6c1afc3e4`  
		Last Modified: Wed, 10 Jun 2026 20:57:15 GMT  
		Size: 16.8 MB (16845764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325d6647dba8b6f0658c765bf3f9ad07dadaa53dc2ba411bb2e49bbb4b6dfde4`  
		Last Modified: Wed, 10 Jun 2026 20:57:14 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0313b5800061fd701fd710b5a66cfcb45cb3f57a43b9f70c74ad8ea2cff94e73`  
		Last Modified: Wed, 10 Jun 2026 20:57:15 GMT  
		Size: 23.2 KB (23241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c95551467e004e1f87340189580f55353bd5ec456e2e6ef60beae5b4c38ee8`  
		Last Modified: Wed, 10 Jun 2026 20:57:15 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6494a45c0ba3f93826875a796c785db9037be30ba5d043475e7009642a4293d`  
		Last Modified: Wed, 10 Jun 2026 21:16:44 GMT  
		Size: 32.8 MB (32808641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a53348e4665f05cec1c02d164ccc65374c7fc6ae714804daee4cb2cabf12a8`  
		Last Modified: Wed, 10 Jun 2026 21:16:43 GMT  
		Size: 9.5 MB (9516784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4c566d9383c969224e22321e69791e313506b325c9beace05444e025322d8c`  
		Last Modified: Wed, 10 Jun 2026 21:16:43 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad64607432db0d4997fb72faec2ebb0e2866a9befd108a42a972bc30094bb42`  
		Last Modified: Wed, 10 Jun 2026 21:16:43 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98dcf8474d568bfd7f6065f4c49fabaf22e059a04bc384542747cecf8103be8`  
		Last Modified: Wed, 10 Jun 2026 21:16:45 GMT  
		Size: 29.6 MB (29649304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1068bd8b2a10a380be3d3b5eba62f1083255b95ff872de7eead3b78c106345e`  
		Last Modified: Wed, 10 Jun 2026 21:16:44 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc457ab3b77c1a3d611275d0336c691e4f4651c769954ff753349c71f6768ae8`  
		Last Modified: Wed, 10 Jun 2026 21:16:45 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc5b8ac0e1da93f3ac81c805326c01bf233e4224eb8053d98da05197f6592e8`  
		Last Modified: Wed, 10 Jun 2026 21:16:45 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:dc9e8af7d351a34e63af2c80ad3f528a229b0eca8ead911cb38460dec718b2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b817b74daf0e83e214a77c63d237f3d2c66511b2c5618df5217ab4bd1478c53b`

```dockerfile
```

-	Layers:
	-	`sha256:2bb9c89204cf84d0ae0f9259263df4488ee9dddb3e674eb184931e03cf24945b`  
		Last Modified: Wed, 10 Jun 2026 21:16:43 GMT  
		Size: 1.1 MB (1118370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86bea4d31694927492ea07631f2d41058cfebefbe52179256da5537b6cfeb4ee`  
		Last Modified: Wed, 10 Jun 2026 21:16:42 GMT  
		Size: 50.3 KB (50300 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:0d17c40f24f5bcb79e92f509d3060e72d3285ce2e80458bf0cd7a53ea71c895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104655319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b6f098ff5455d7a8a983a574d1b0d2addc491774e32583955f26babab67b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:41:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:41:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:41:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:41:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:41:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:41:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:44:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:44:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:44:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:44:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:44:55 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 20:44:55 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 20:44:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 20:44:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 20:44:55 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:26:21 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 21:28:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:28:02 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 21:28:02 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:28:04 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 21:28:05 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:28:05 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 21:28:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:28:05 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 21:28:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:28:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63958e40f8fe47265f80138ae6d5289666a596a8c5006829db8dc972fd2c50f2`  
		Last Modified: Wed, 10 Jun 2026 20:45:01 GMT  
		Size: 5.6 MB (5569135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820b083e64a778e1fe1b4837260b4689f2e2c6430787238b50f70c8419f6303b`  
		Last Modified: Wed, 10 Jun 2026 20:45:01 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20067b58aaf1e0a1e54d51a8526f71ee55103512ee1714518f48dd59c256c140`  
		Last Modified: Wed, 10 Jun 2026 20:45:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e46dea1829fc8bcb88b3e6e6412795e999ade347b7cf6101ec676a3be11f25b`  
		Last Modified: Wed, 10 Jun 2026 20:45:01 GMT  
		Size: 14.4 MB (14421907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b70ebcd554b960a9af0f2e64bd50a0dff7516c4c7907c191db225418117c89`  
		Last Modified: Wed, 10 Jun 2026 20:45:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61840a6d6702c8ae23f8c7f5dd7fb94986881ea609d4d3f064523050d3adaf2c`  
		Last Modified: Wed, 10 Jun 2026 20:45:02 GMT  
		Size: 14.7 MB (14740593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5fd93c77e83b93a1435844703e06a64949734dd649930c899789c95beabc1b`  
		Last Modified: Wed, 10 Jun 2026 20:45:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63447f214e124471bae4eea45a8d415c56ce0bee41bcbcd009adfac54a78450a`  
		Last Modified: Wed, 10 Jun 2026 20:45:03 GMT  
		Size: 23.1 KB (23052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a222e4fddb693bb8391697ed8640fab0fef0ef4dc4e5106b035200ba99d7d36`  
		Last Modified: Wed, 10 Jun 2026 20:45:03 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7650e6e7475cc9558d62886ddb916a354bed2ed1822236433cf1ca895056107`  
		Last Modified: Wed, 10 Jun 2026 21:28:12 GMT  
		Size: 28.8 MB (28768834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0d6ef8b87cca80eddfd1301b84fda394c6c5d22768ca42cc5587631db2888f`  
		Last Modified: Wed, 10 Jun 2026 21:28:12 GMT  
		Size: 7.9 MB (7888704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4ceffc48e35a66fa800ea2bce1abee3163c677d85e32094ae3373eba21eccb`  
		Last Modified: Wed, 10 Jun 2026 21:28:12 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6516569f44521c199e6edbd3dd6a0beee440aca39ef1d783ec5160658b160a`  
		Last Modified: Wed, 10 Jun 2026 21:28:12 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c21f754de8490438ad9ba4a2286ede2d602b48683e98fc93b0ee943066b450`  
		Last Modified: Wed, 10 Jun 2026 21:28:14 GMT  
		Size: 29.6 MB (29649305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a845c04a6b3f8a4e6d73710f6bb34275fbd2ca0345a9fac324f6780e045d9721`  
		Last Modified: Wed, 10 Jun 2026 21:28:13 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b2ab8399ccf6512f1610d684945710a3e07406580aa2faab15f88d69c0f2e0`  
		Last Modified: Wed, 10 Jun 2026 21:28:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14472a8a362d327bb1f02e6f4da1fc6edd215c47a76db8b90676b1323487714a`  
		Last Modified: Wed, 10 Jun 2026 21:28:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:540ab0cebe30cb1adcedb3039fe89dbea59247076ee51871252cfd3f514c93e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a198c34075e743c4f902d4224288476db7e8dfbc487982579a420cab2dd9ab03`

```dockerfile
```

-	Layers:
	-	`sha256:e93e345f5848056c3086e826a7bf9f37164dd9d485bf43f9d782665def514a49`  
		Last Modified: Wed, 10 Jun 2026 21:28:11 GMT  
		Size: 50.2 KB (50231 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:91dcba73b4a6d51f89ac0bef79c2b5ecccf164493623605a81926a432f31f062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102537599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f27f6720912e5c3225e513bdac1d57b418032ddf70d63fe2ed05220d9c99dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:55:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:55:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:55:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:55:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:55:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:55:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:55:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:55:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:55:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:55:09 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:55:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:55:09 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:55:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:55:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:58:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:58:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:58:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:58:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:58:17 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 20:58:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 20:58:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 20:58:17 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 20:58:17 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:32:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 21:34:38 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:34:38 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 21:34:38 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:34:41 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 21:34:41 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:34:41 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 21:34:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:34:41 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 21:34:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:34:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6211b14b95a58de8b30d4f32c4285efe32eef724740d063ed3092cbd7085683f`  
		Last Modified: Wed, 10 Jun 2026 20:58:24 GMT  
		Size: 5.2 MB (5223410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41bf705d2d67db6b5e79327a872fbadf2e64675eebc540b379e44cd8ea0a75ec`  
		Last Modified: Wed, 10 Jun 2026 20:58:23 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad3d09d66cc966d97fdbb8a1ae7ffd7a3f01c3ea743e1b8a8be91f6650471d2`  
		Last Modified: Wed, 10 Jun 2026 20:58:23 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce093e62dd83f6de07dc712a468a71c1a8df3c7c5a308043652ec80cc93d5952`  
		Last Modified: Wed, 10 Jun 2026 20:58:24 GMT  
		Size: 14.4 MB (14421913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5681dc69858ffabeab01e02fd79cdb7eb2b8cc3617b597d2cd8629b504168aa`  
		Last Modified: Wed, 10 Jun 2026 20:58:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50dbfbf9f12e70c3e3c83f27143fe084f522d59a494c4bd92eab5b9b411dd6b`  
		Last Modified: Wed, 10 Jun 2026 20:58:25 GMT  
		Size: 13.9 MB (13929111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e16d81564d64e24baa4e92c90d4a091ff3f997594fea3599e552dacf5c8d0a`  
		Last Modified: Wed, 10 Jun 2026 20:58:25 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4b5dd16a7830de8ce692b4a7b933d85e26a66390ea343927615625bf75315a`  
		Last Modified: Wed, 10 Jun 2026 20:58:25 GMT  
		Size: 23.1 KB (23062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7baec03c03bf4f5236463dc7cae9fccf5bbb6e467f85c3b13748cbc9350f70`  
		Last Modified: Wed, 10 Jun 2026 20:58:26 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8be691c2b50e4a2f5c273d3117e3b8a89c511d28d10c021b9d396579aa817bb`  
		Last Modified: Wed, 10 Jun 2026 21:34:51 GMT  
		Size: 27.1 MB (27090926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6c978af2645b9b8f909cb4f667ddaccb1fb36e4a2f7fa44976139ee127921e`  
		Last Modified: Wed, 10 Jun 2026 21:34:50 GMT  
		Size: 8.9 MB (8895231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6449bff2aac24f3734e257d0f4c865a5e4af372f74e3dbc1d4eebd5eab0b8f15`  
		Last Modified: Wed, 10 Jun 2026 21:34:50 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f37a7a27a4ea7a9531a6fad88520129b0ff7ea0757645588283c84a16e88b6`  
		Last Modified: Wed, 10 Jun 2026 21:34:50 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286f2fe017d4ff29b68e7f6562035b577491d22dfb764895958c38759132f263`  
		Last Modified: Wed, 10 Jun 2026 21:34:52 GMT  
		Size: 29.6 MB (29649308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fad5b71e142a947149638a420859660e46b3237b3c4d4cb01d31099e4a55f2a`  
		Last Modified: Wed, 10 Jun 2026 21:34:51 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43d1455b1ef26426307252878b99ef723fdcceb01f78786df51d6c00469b311`  
		Last Modified: Wed, 10 Jun 2026 21:34:52 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a71424407bc30f6dfb1ff56dc5188fb7bae522e5f4ea408cf3b96299f99ee34`  
		Last Modified: Wed, 10 Jun 2026 21:34:52 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:67eb6631649e8e275c00003cdb125038cc75c1f7e6febcbf4226d38fe2a9b36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1166960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6d440a40cc8cb888d601cdbe66d3a709c60c1bf55f0d3f9b3ee7b5fb1f20a0`

```dockerfile
```

-	Layers:
	-	`sha256:aef6e92cf1eeb3cf266dfd179015847d16076f29fb99b92fdb0ec8451f6c03b9`  
		Last Modified: Wed, 10 Jun 2026 21:34:50 GMT  
		Size: 1.1 MB (1116514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dbab60fcbcc0d4f75fee26d55aeb7c16334d9eb313b2270eef54425e88ae4a1`  
		Last Modified: Wed, 10 Jun 2026 21:34:49 GMT  
		Size: 50.4 KB (50446 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:71b6d24f2d90dc98fa056ad918fd508742752d87c21ec2d795ad0ae79350d75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112590689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86709d6bcdff6011fc9f93742678355173d30c614005471f76c395dcfa84612`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:56:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:56:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:56:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:56:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:56:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:56:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:56:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:56:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:56:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:56:49 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:56:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:56:49 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:56:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:56:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:00:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:00:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:00:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:00:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:00:22 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:00:22 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:00:22 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:00:22 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:00:22 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:10:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 21:11:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:11:33 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 21:11:33 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:11:35 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 21:11:35 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:11:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 21:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:11:35 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 21:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:11:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1dafb80d687b148a5238b80683ee38e1c33d61307d71e267184b92683c3961`  
		Last Modified: Wed, 10 Jun 2026 21:00:30 GMT  
		Size: 6.3 MB (6287197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710dbb35e8ae9d6237329c367c66cc0f2a31ab971d3967ec02f1864a990e6088`  
		Last Modified: Wed, 10 Jun 2026 21:00:30 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f7f580bce05499d4a787842db5745563db98d09de1a0cb224623d4a52a9c0`  
		Last Modified: Wed, 10 Jun 2026 21:00:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba8322850327b2e058322b1b911cd940aa623ce73483230818595ffdb3584c4`  
		Last Modified: Wed, 10 Jun 2026 21:00:29 GMT  
		Size: 14.4 MB (14421871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5716a5ceba66af20e0666b36655e0bfb219f84b3a639d6e47db1ab1d15f9164`  
		Last Modified: Wed, 10 Jun 2026 21:00:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4b37dfb30d0c10d0b21d5b6c8b67f798f10927d823498ce267718f47bb2e53`  
		Last Modified: Wed, 10 Jun 2026 21:00:32 GMT  
		Size: 16.3 MB (16253970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4531009cb61e5161728691de5e28fe3b285baf8699c56da92a03371fee9ad3b`  
		Last Modified: Wed, 10 Jun 2026 21:00:32 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a528b7b338d63f983cc56fb9f196d85169c40358c92c135c7ba2971f8c323b85`  
		Last Modified: Wed, 10 Jun 2026 21:00:32 GMT  
		Size: 23.1 KB (23050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ae5b559dce2cde2c650cc6dcd9684cf0ef2191dbc3de5fb82a71567fbd429`  
		Last Modified: Wed, 10 Jun 2026 21:00:32 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0d3b2532cacd0bdd38204ec3e8be9af5aa0fd212232f0416eb815e1b3699da`  
		Last Modified: Wed, 10 Jun 2026 21:11:46 GMT  
		Size: 32.4 MB (32429060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0d23835bac96f7e7580b4303f189118e46fb22747e7565863011d08f1e35d1`  
		Last Modified: Wed, 10 Jun 2026 21:11:46 GMT  
		Size: 9.3 MB (9305431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb488376ef6daf862d0017afddd79b028366ddfaa9ab80fd12366eb7cb9d377`  
		Last Modified: Wed, 10 Jun 2026 21:11:45 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d82f016bdfa5557e3a8f4ddf700948d2e1830f6b22dbcb569af019360fbf85`  
		Last Modified: Wed, 10 Jun 2026 21:11:45 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d5bb18c5aa512bdc42fd7a2b8ba3bdd37aa15335956b91c6c2c9b5f169a9be`  
		Last Modified: Wed, 10 Jun 2026 21:11:47 GMT  
		Size: 29.6 MB (29649308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f58b2d07b156810a68bab0dde800256b1c99222e762e62404db27df549d4eb`  
		Last Modified: Wed, 10 Jun 2026 21:11:47 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e829cf4eab6fa87164890322f3b1bf155c39bd3637e29d6a0d50510541b364`  
		Last Modified: Wed, 10 Jun 2026 21:11:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c0842cddad8a7480cdc8344a26f54f4db99cce120ff233017da7c69a3dfa24`  
		Last Modified: Wed, 10 Jun 2026 21:11:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:92e03496d5f0ac5cfc05a74e3e497ba12776646a3292126ffa07d0558fb9e04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7617f23223221cd007c383ec9519c44b573a13b20d42c46aefa6ffe7df0bc83a`

```dockerfile
```

-	Layers:
	-	`sha256:ffeada2c81534facfa9f58952fd58c12b593d353d5fdd5b5f8942145e60f8612`  
		Last Modified: Wed, 10 Jun 2026 21:11:45 GMT  
		Size: 1.1 MB (1116534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b39e722f8cbb9a9d68ea31c243417179ccdefc7990a4124c065104805de9a7`  
		Last Modified: Wed, 10 Jun 2026 21:11:45 GMT  
		Size: 50.5 KB (50480 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:8ae2d3265d09d9f898c93bf97e67e6b54aea400a54cc023ee8b772d1a3a30e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112419189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263b5b6d885405c4bcb884eb7d6d27b50f346d07dd2e8b3e2bffbf13107eedf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:32:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 21:32:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 21:32:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 21:32:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 21:32:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 21:32:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:32:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:35:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:35:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:35:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:35:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:35:25 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:35:26 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:35:26 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:35:26 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:35:26 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 23:10:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 23:11:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 23:11:53 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 23:11:53 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 23:11:55 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 23:11:55 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 23:11:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 23:11:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:11:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 23:11:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 23:11:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58ddfeb4bb4e13afa132216ca3d4e09b5774bd6144f850dade79d28eb6c1980`  
		Last Modified: Wed, 10 Jun 2026 21:35:32 GMT  
		Size: 5.8 MB (5823661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e50921cdc8a590528dbacfa0a674d05f298897b0622bbeafe2291337236aa`  
		Last Modified: Wed, 10 Jun 2026 21:35:32 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f33450dfd09801a409b585c2e2b4b24f79cfaee89ebcbd4b9fbccdcc9da72`  
		Last Modified: Wed, 10 Jun 2026 21:35:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8593829f3b05b7c6fcbe094cd45462a1123a434e7e68e6ad2f38a05ddfc9496`  
		Last Modified: Wed, 10 Jun 2026 21:35:33 GMT  
		Size: 14.4 MB (14421868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bfe88020a2884916c9a8b9a75b00b4e41fdab771729e7dfa8a1977b46e6c4a`  
		Last Modified: Wed, 10 Jun 2026 21:35:33 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f06afc47b4d2513b376bfb89c332f309d9e0709c83bc165d8532366e6d396f`  
		Last Modified: Wed, 10 Jun 2026 21:35:34 GMT  
		Size: 17.2 MB (17192208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40545fa7cc32666cb8b93a8b83310c8836d97d472287cb28fffd2cf24adaa357`  
		Last Modified: Wed, 10 Jun 2026 21:35:34 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fef2e28ad937940c0349f12c07806896171144968607c68f27de38ec1de6c0`  
		Last Modified: Wed, 10 Jun 2026 21:35:34 GMT  
		Size: 23.2 KB (23227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabd920a88747953ec19070e8fadcf74eaa51e2e7f51635f7a7ef412fed4629`  
		Last Modified: Wed, 10 Jun 2026 21:35:34 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4d3b47a8f44789fb48351f204992a67dd79de09a07c0c7a66a0c280cb4bc2d`  
		Last Modified: Wed, 10 Jun 2026 23:12:06 GMT  
		Size: 33.2 MB (33220882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa32efe99013d1279d397745fd9a27e578bd757cd9dffd1b93e5d32735593557`  
		Last Modified: Wed, 10 Jun 2026 23:12:06 GMT  
		Size: 8.4 MB (8377807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282d085d9fa0d9508c6f27acb7022898c3e160c3d955c36c77721e0a741970a3`  
		Last Modified: Wed, 10 Jun 2026 23:12:05 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ae020b9f091f9dbcca67c23d090a4292ffdc69dad5907d2e1a61d34ebf8b38`  
		Last Modified: Wed, 10 Jun 2026 23:12:05 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa36751d24a506d856320c0aafc1faf80452afc8eefaa6f4e2887e760f7e003`  
		Last Modified: Wed, 10 Jun 2026 23:12:07 GMT  
		Size: 29.6 MB (29649303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00263cd63157bafa125f2ddc5563e73491bbdeb886d5df522a0a44eeec949afb`  
		Last Modified: Wed, 10 Jun 2026 23:12:07 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1737ee4921bed4fae2c4f41bc4628f21dc00ed345f912a75e3099df1e8efb441`  
		Last Modified: Wed, 10 Jun 2026 23:12:07 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497b4b3079181fbb7612a0ec943e99f6fde82b12731b943753cc5c5af5da33e8`  
		Last Modified: Wed, 10 Jun 2026 23:12:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:b05121f5a3270e1280173c34d8fefee2e3a9f632db6c960b897b443af1912176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7411c48bb25791ae61f9ab019051c5cc1548a5119e32c37b953be7ed4ba4dd1`

```dockerfile
```

-	Layers:
	-	`sha256:63d83e06d3d793cf1c3cc47c1f83df4747214ae1829edf28b53c8113a2e2eb4e`  
		Last Modified: Wed, 10 Jun 2026 23:12:05 GMT  
		Size: 1.1 MB (1118345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50fcda135cd995a764e3e1b820a45b257ccdce0794363cc2ff6f348b7ecabf50`  
		Last Modified: Wed, 10 Jun 2026 23:12:05 GMT  
		Size: 50.3 KB (50258 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:6856bf68e172522ebd7307dd7fcfb7e8ab776a0750b7ed528c7e4df4e6c53a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112615235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b644d4c3443449ed698cf662f771413283abc9ee656343205ad51437e2aba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.5.7
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 01:34:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 01:34:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:41:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 01:41:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 01:41:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 01:41:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 01:41:55 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 01:41:57 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 01:41:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 01:41:57 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 01:41:57 GMT
CMD ["php-fpm"]
# Fri, 05 Jun 2026 02:09:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 05 Jun 2026 02:11:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Jun 2026 02:11:47 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 05 Jun 2026 02:11:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 05 Jun 2026 02:11:52 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Jun 2026 02:11:52 GMT
VOLUME [/var/www/html]
# Fri, 05 Jun 2026 02:11:52 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Jun 2026 02:11:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 02:11:53 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 05 Jun 2026 02:11:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jun 2026 02:11:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a446573689f8d3cbef54f6c649ba454330116f9d75b4f418c595229567eb07`  
		Last Modified: Fri, 05 Jun 2026 01:42:07 GMT  
		Size: 14.4 MB (14422026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90449a89084b470b4d104decde8a8b7ad5984470fec6f94ef7574b58dc3b20b7`  
		Last Modified: Fri, 05 Jun 2026 01:42:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00f0927af2e218a1351e002baa2d5189a310e2f724ea3e49e2dfc8b3cf0b0d4`  
		Last Modified: Fri, 05 Jun 2026 01:42:24 GMT  
		Size: 17.7 MB (17736794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7993df5777f2c4af30dfab92fd47a6388b6abe3ea11af857083dd959026d3839`  
		Last Modified: Fri, 05 Jun 2026 01:42:23 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b3e15ec901da1ff9d6fce54ad3319e573f1a8cbc5d4b7c5e6c03311ee15a20`  
		Last Modified: Fri, 05 Jun 2026 01:42:24 GMT  
		Size: 23.1 KB (23070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451ebae85bf436bd91b19d947f5b031d7c8269e8802c19f071f464b6c91f7c3a`  
		Last Modified: Fri, 05 Jun 2026 01:42:24 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e4e4274cf3bf5b36761428a93af3a960da0ca03a9e9557a2e19f1506d3f69b`  
		Last Modified: Fri, 05 Jun 2026 02:12:19 GMT  
		Size: 34.1 MB (34107341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c65cb69b3fab2110b802be0e690e480296d28ee4d0ec912f17e365185d83f5d`  
		Last Modified: Fri, 05 Jun 2026 02:12:19 GMT  
		Size: 9.1 MB (9060181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b16f2234c7eeb824d44f6c2e3adeef890a631289f21e4298a5d3781128d25ac`  
		Last Modified: Fri, 05 Jun 2026 02:12:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43818da77f26c912f61ef0555598a95aa7504cacb584c1c10a2f50951dabe26f`  
		Last Modified: Fri, 05 Jun 2026 02:12:18 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e981096805724cfd231fc500de8f1085892d14da62b2cd4b82f9716a82caac0`  
		Last Modified: Fri, 05 Jun 2026 02:12:20 GMT  
		Size: 29.6 MB (29649308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcd5871449cdf4130acb9a31796db6994f610cfda7050248e77a71759a31939`  
		Last Modified: Fri, 05 Jun 2026 02:12:20 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ce4b42ec3eef80b81ba5d1cde10ae87b868118a0b83fae8c0f723e4cc1edf7`  
		Last Modified: Fri, 05 Jun 2026 02:12:20 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb8993107aae3b39c548eb20256b6ea0a50a21d769602b09a2db52ffe54ab5e`  
		Last Modified: Fri, 05 Jun 2026 02:12:21 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9795d5dbd437e67bc1a7499b3c534c1c7d9b4a83622c562d6de0e5ca615e0980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1165721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f11fa27fc4bbe6deab7af36dc0357ee000015549f3595e80031c1927605d978`

```dockerfile
```

-	Layers:
	-	`sha256:c9b48aef19a180d5583d823c52f555ebbc21410a5fa307b45d9e049e90cac78b`  
		Last Modified: Fri, 05 Jun 2026 02:12:18 GMT  
		Size: 1.1 MB (1115366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d37cc427e5ef16ebc2b4124757ed911ebe699999eadddd4c96683cf92ff154`  
		Last Modified: Fri, 05 Jun 2026 02:12:18 GMT  
		Size: 50.4 KB (50355 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:4a7245110ed4a5c04c68ff787f136da866115dd4547842db0d459fe5c34639da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107604151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7fd1fa586abed849098b89a250b5deb308e5be9d19799bd3d68013b578583e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.5.7
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Fri, 05 Jun 2026 05:18:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 05:18:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 06:37:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 06:37:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 06:37:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 06:37:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 06:37:28 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 06:37:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 06:37:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 06:37:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 06:37:28 GMT
CMD ["php-fpm"]
# Fri, 05 Jun 2026 11:50:58 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 05 Jun 2026 12:14:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Jun 2026 12:14:30 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 05 Jun 2026 12:14:31 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 05 Jun 2026 12:14:41 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Jun 2026 12:14:42 GMT
VOLUME [/var/www/html]
# Fri, 05 Jun 2026 12:14:42 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Jun 2026 12:14:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 12:14:42 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 05 Jun 2026 12:14:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Jun 2026 12:14:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83c25d050b633c94fba50d279b2d7b6c29826b999bd81a90516a78c942ae19d`  
		Last Modified: Fri, 05 Jun 2026 06:38:29 GMT  
		Size: 14.4 MB (14422060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabf9ca2a5430c85237d5dcabacf556b0831ae8c97d72577a9fab19b67f2b0de`  
		Last Modified: Fri, 05 Jun 2026 06:38:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b17984f96ce300d5d559ebd5eff0d1ffecf34ba24118e9c0dab8d1372ddabc`  
		Last Modified: Fri, 05 Jun 2026 06:38:29 GMT  
		Size: 16.3 MB (16320858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0515574d6f9f35002185e4a1d4324ee9a5d4733437e00b4ffbe351f6b72c6ebb`  
		Last Modified: Fri, 05 Jun 2026 06:38:25 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee443b74e6c7f5b3a69e45e291e5215cba2091c3fbed99d95959b24ddf6881f`  
		Last Modified: Fri, 05 Jun 2026 06:38:27 GMT  
		Size: 23.1 KB (23070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7016d10afafe89fe85017e6089ca4f9ed1c16b9a7b072020e95c68de8bd3da6`  
		Last Modified: Fri, 05 Jun 2026 06:38:27 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48a4e613a2d659b94ed595d4ae6dc1db36f5baa97118ed6e108b5cc3371ad91`  
		Last Modified: Fri, 05 Jun 2026 12:16:45 GMT  
		Size: 32.7 MB (32684450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4afac2821c0998e594e594f4eff07f191400ddc35992386c7e9bbdec953e9d6`  
		Last Modified: Fri, 05 Jun 2026 12:16:38 GMT  
		Size: 7.2 MB (7163986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21856fb747edfdbd71cb764c07d7eec802052407b81cb2a179234836d139d28c`  
		Last Modified: Fri, 05 Jun 2026 12:16:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b44ab925cae367286b2b09f5fb173ad1b7c5e52fd9a0c8429cc90850623928`  
		Last Modified: Fri, 05 Jun 2026 12:16:36 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033bdd5529148add8df56715fb665d3e2753e9b6c9bf7c99bc87db34c4cb120c`  
		Last Modified: Fri, 05 Jun 2026 12:16:46 GMT  
		Size: 29.6 MB (29649320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d4595fe71ffcc7300e33a3b8a97f63b50f39448884ef7d1d66674fa553db4`  
		Last Modified: Fri, 05 Jun 2026 12:16:38 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3011b1817a5385348b3112c8eaac56a4bce9b9ff9477073db668fc94e63eff24`  
		Last Modified: Fri, 05 Jun 2026 12:16:40 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b12f34ad6b94705500fea00781fbd4a0874ebc25869b62aa5be8911c3f5d59`  
		Last Modified: Fri, 05 Jun 2026 12:16:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d2d52c28e2a430533b67de5c06dd56c0c6fea89df059661abb69e28308fd0916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1165717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e811390ddf4d86c6d06df9ff15122e9e4127bb1da649e6bd94d571402ea00dc8`

```dockerfile
```

-	Layers:
	-	`sha256:1ccd5670f73675d40adb2a39f372dbb495b0084bd7848e1380c063d046b8e656`  
		Last Modified: Fri, 05 Jun 2026 12:16:35 GMT  
		Size: 1.1 MB (1115362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5f9c860e2e96f3c006f88e7215aff365fb5d568e39f0b62f7ec3ebfdc4f889`  
		Last Modified: Fri, 05 Jun 2026 12:16:35 GMT  
		Size: 50.4 KB (50355 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:f7972ab6bc98b90ddc1c56c0d7e6fb7dd3646ea7a5e050720094b9a6e8e03905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112593625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a94f987410ac3f3040213eda62d1a73e14ff1870c27ef77660873273b2c7bf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:59:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:59:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:59:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:59:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:59:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:59:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_VERSION=8.5.7
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 10 Jun 2026 20:59:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:59:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:05:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:05:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:05:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:05:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:05:46 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:05:46 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:05:46 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:05:46 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:05:46 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:59:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 22:00:52 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 22:00:52 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 22:00:52 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 22:00:54 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 22:00:54 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 22:00:54 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 22:00:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 22:00:54 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 22:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 22:00:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3da918cbfec773715cb5c2ba09c98813438f50a50d3430a86242f9c3ace75`  
		Last Modified: Wed, 10 Jun 2026 21:06:04 GMT  
		Size: 5.9 MB (5943440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d360246fb66915c6b8442bb5acd4465ad8e9cb2f0adb4488237ce2913320143`  
		Last Modified: Wed, 10 Jun 2026 21:06:03 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed332689978f619c05676c7b3c891e5c4e1deced85ca5ffcbcf5b048210f92d8`  
		Last Modified: Wed, 10 Jun 2026 21:05:15 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c98d2e55df3a968d41bfe27ffed7542089da32070461cf6cd8a6c3f5465653e`  
		Last Modified: Wed, 10 Jun 2026 21:06:04 GMT  
		Size: 14.4 MB (14421886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bfe5d067775dcf75677b829c39bfdd990c8aa2537353e8ba2ed660991a4c66`  
		Last Modified: Wed, 10 Jun 2026 21:06:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad334b3fe2c53e8ae3ca64a3f4dae3eb9b9a297dfa8538d28af5e0e9bf3fa1f1`  
		Last Modified: Wed, 10 Jun 2026 21:06:05 GMT  
		Size: 16.1 MB (16093841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11641c12edc3dd2fc3558251571a793cc0ac872bb7d2ccdd5ddc36444e69e91`  
		Last Modified: Wed, 10 Jun 2026 21:06:05 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753b88f5462db2eed222ff7d63733f8530bababf89789b5b616bea777c17101d`  
		Last Modified: Wed, 10 Jun 2026 21:06:05 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8366a0ed19732cd82384444dd9dc7c462919d0a214b64ccb8b0993c78540fab`  
		Last Modified: Wed, 10 Jun 2026 21:06:05 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482fa0b6102063e57675ebbf3850fc7fdfb17e11e28f770e0eaa5f99f54baa89`  
		Last Modified: Wed, 10 Jun 2026 22:01:10 GMT  
		Size: 33.9 MB (33949629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70997359cc7266d4d075c3a9c979cb5a92a0d86bbea5bb69f987916acd87d74a`  
		Last Modified: Wed, 10 Jun 2026 22:01:11 GMT  
		Size: 8.8 MB (8763775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512f24a02d82c027538cc821241e552f8ac69351d60743212d25e6d104d46657`  
		Last Modified: Wed, 10 Jun 2026 22:01:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d8406b13de00328c78d639335a27c284245adc6e9d00df9f6af46aa88a826`  
		Last Modified: Wed, 10 Jun 2026 22:01:09 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d0e995eeeadb479efa8cac3159b610cecb56ae84e72047d2ff581308cac070`  
		Last Modified: Wed, 10 Jun 2026 22:01:11 GMT  
		Size: 29.6 MB (29649309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f5fe235407ad14d754ba81ae6c8f520d2825ee9160b46ee19e2436dded5b81`  
		Last Modified: Wed, 10 Jun 2026 22:01:11 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d01e6ef32bd179e3f6bab008a225cd5e5780a5e9715e887b38c998ddbf98d2`  
		Last Modified: Wed, 10 Jun 2026 22:01:12 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e397d93846a31c75dec3578ef811a90bdb3d4fde1cd7c7b0b63ac925970cdb28`  
		Last Modified: Wed, 10 Jun 2026 22:01:12 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4346aaa274818ebda3eec0831c4c8aecd874ae91305220cbde7186f5aaa65074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1166778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce65953cab6462a9a789a202528b30de81bfe5480e1c751b63059505f150a05`

```dockerfile
```

-	Layers:
	-	`sha256:922b8f15d9751bc0713cb2d4cdd1602ed10d2767317d4741bccb6f7711be8354`  
		Last Modified: Wed, 10 Jun 2026 22:01:10 GMT  
		Size: 1.1 MB (1116477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95b613e052645c342b063f0e97d0d2ce08a4e9b92cdce65ce492c0e74e222318`  
		Last Modified: Wed, 10 Jun 2026 22:01:10 GMT  
		Size: 50.3 KB (50301 bytes)  
		MIME: application/vnd.in-toto+json
