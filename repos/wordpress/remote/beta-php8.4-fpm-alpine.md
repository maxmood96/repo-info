## `wordpress:beta-php8.4-fpm-alpine`

```console
$ docker pull wordpress@sha256:93ae7847fa14ff3eeaef924c11a245986bfbf56be5e9636f5f83a7cf15b273b0
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

### `wordpress:beta-php8.4-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:420753735c34d4e04db9cf54846e0f81faefa0c9defc452c405034b1d567dafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (108005646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46a3e40e5561744ad4ffe617915ce01abb3c5ef1b2834ffccd415e08a46fd86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:27 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:21:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:21:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:21:27 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:19:31 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:20:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:20:17 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:20:17 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:21:47 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:21:47 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:21:47 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:21:47 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ef6327a484adad40c70cc6260e6c05b6496a95d7f17bc657f1608ef1d98c65`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 3.6 MB (3587421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34a3b26ad831d1b88e28205d0697d293a6b9bd48bba6c0618d2a962f6b7ab5`  
		Last Modified: Wed, 15 Apr 2026 20:21:17 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd24741e080b2f5812c84cec27dcacc6faa6834e57a410d0498f39e3f589d63e`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eae9fc1b3d2fd71e5fe569524101eda391f21af0725aee92bb039cd3e3e2ec9`  
		Last Modified: Wed, 15 Apr 2026 20:21:35 GMT  
		Size: 13.7 MB (13709881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cfb46d077b27f03899c4f08b5ebd738a21e79448dda30c53e084e4d1ee1b0`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6b4452123be6c2fb9a132b567d46df619e884ca6553bb2e96c5073a44ac072`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 15.2 MB (15201457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5ec8e36b924dcf98696ef1cf37b7f68a7521e815288899c6939d7bcddb5012`  
		Last Modified: Wed, 15 Apr 2026 20:21:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbd3ef9745bc4e4b2d2170cdc2beda14f18aba440b3973124628fe77aeb08b0`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 23.4 KB (23403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80181fe3ced17e0662a1f6639130ad39f9d44b208813f75cb2e77e3597e4da87`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 23.4 KB (23414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9440a7ee03ff048797e0bc98dadb4bca879b081ddaf7f005cad80dbb7c779`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42a6b484ce216bffc277877c1cb798eb64949f0e536b3186be38defc861aee3`  
		Last Modified: Wed, 15 Apr 2026 21:20:30 GMT  
		Size: 32.8 MB (32839371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929d0a1c4b7bc021ec4de8840453bed63bdeeb52a3f3ead3557220b26dc4c1bd`  
		Last Modified: Wed, 15 Apr 2026 21:20:29 GMT  
		Size: 9.4 MB (9414183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15aff24ce473e07d069b711d12d2c52322c2c51cd7674e8b0bb36d222823d1f4`  
		Last Modified: Wed, 15 Apr 2026 21:20:29 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc0f055084d23e7ca30bcb6e09408f9dea0a4363bf662bfa2cf34f03b7b578e`  
		Last Modified: Wed, 15 Apr 2026 21:20:29 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ae2cd613b205bdad5ea827838bfb58e81efaaaf43f3ba2e31f7e5e5931405a`  
		Last Modified: Wed, 15 Apr 2026 21:21:57 GMT  
		Size: 29.3 MB (29323858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4955c601b1c0c25b51deb0f7f3d8f144ecbdc2fbb700a60e017143260fa7bc`  
		Last Modified: Wed, 15 Apr 2026 21:21:56 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7f8baa1d1cdbdb7fb4429361356ccd4df53bd36825288790c12881c28594fd`  
		Last Modified: Wed, 15 Apr 2026 21:21:56 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cc8dbd1ba616f209fbf8aaa23ab28867590133a14778901270b5c586bf3606`  
		Last Modified: Wed, 15 Apr 2026 21:21:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:36134dd257aa828801dc109c104fff251b53853c278dba93125e2de70fb22410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e760052a3d5e6795be0e14851ecfccf1442b95bb53ae70f1623031f38caefd7`

```dockerfile
```

-	Layers:
	-	`sha256:a4f2b12d26314e921cacd2854a7ad5a240e25ded24d111fa290886835a7d1abd`  
		Last Modified: Wed, 15 Apr 2026 21:21:55 GMT  
		Size: 1.1 MB (1120126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d956e63f039dc78db83376ee828ea416e5ff962dee41bcfec1646fb399af1f`  
		Last Modified: Wed, 15 Apr 2026 21:21:55 GMT  
		Size: 51.8 KB (51769 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:4bcecd77ec33a117fa6059b6c0d6b70408e6462a8200bc54583b9893780db2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100163264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320d577e61a96030a4fa5d81af7eddd8d8de63613d9f1ff547d0823ba0ec78f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:21:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:21:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:21:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:21:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:21:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:24:56 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:24:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:24:56 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:24:56 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:20:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:22:16 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:22:16 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:22:16 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:22:18 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:22:18 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:22:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:22:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:22:18 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:22:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a7c0fd01aa85d53a5cc462735eb1cd908410a74091bb824d85314c572a2e98`  
		Last Modified: Wed, 15 Apr 2026 20:25:02 GMT  
		Size: 3.5 MB (3543068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0990a4f4213cfb6f619b810861edf0e55ff77432a3a9995933d5e5e0f25b962`  
		Last Modified: Wed, 15 Apr 2026 20:25:01 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c4bf762147116095a30f26ea107900f28361d1ed6bcae3c7312e6e16503d86`  
		Last Modified: Wed, 15 Apr 2026 20:25:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611c551c89d0a52d0c1fc742df48242b4822774aeb29969a04de89b831b84d2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:02 GMT  
		Size: 13.7 MB (13709885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5ade602d1f9497bdb9f1408e2550053a861b3b97d3825ec1db2a3d0455503`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56588352628b072b8435ef48b6525542156117d05dc3638e928af0056385309`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 13.7 MB (13674677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268fbbb176b6d34f57da556ff71567e0c3b3c8a511e1cf4ed34733eaba6187ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e012c1772b42d6b1fba0c2455214494ec06551fd4a67e2fcef1658f848615`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc79448a1b097592a03822eba5c5d849e0e0adbd86a3409607fbc6466cf075`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 23.2 KB (23224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e05eec180821df7fd20ebc57b940908cae6bb1d78f21f26ea0f3ff23119e46`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca8607c227d6c63a53d0dd5417e17acd554bf46a2083454f17f94b5553b656b`  
		Last Modified: Wed, 15 Apr 2026 21:22:26 GMT  
		Size: 28.6 MB (28550516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743b2ae8d756b875a6e7596a200fc5972b5f904ff0f3c63cc28278bd2a20217a`  
		Last Modified: Wed, 15 Apr 2026 21:22:25 GMT  
		Size: 7.7 MB (7724507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ba7113a870206cf21d79c129887afb4e4cf096a9755ffa9277f7155f36bdc3`  
		Last Modified: Wed, 15 Apr 2026 21:22:25 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6a86f85cd1a7a74c657f800f77f81667fc9a827013ec67c6f71d7f13eea26d`  
		Last Modified: Wed, 15 Apr 2026 21:22:25 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300e1c1c74d099e7c01c442de8b131dfd8e5ddf26aa9103b0da4d0ae756a60f2`  
		Last Modified: Wed, 15 Apr 2026 21:22:27 GMT  
		Size: 29.3 MB (29323842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806c6d3d14bb78684102beeecf172596ceac700c345ced027498970561e3fc92`  
		Last Modified: Wed, 15 Apr 2026 21:22:26 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefafcee4b1134c59a2ebd335aa8ec049a6fb985124de7ad109c5d82fef445f`  
		Last Modified: Wed, 15 Apr 2026 21:22:27 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1ad0d765108f267e422b1cac67ea5c7a1052b4c35ba04afe47fe0c80c283aa`  
		Last Modified: Wed, 15 Apr 2026 21:22:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:279f9ff91971b1b52f73d1f1b6854ca5a849c182af40fc233749826e2123eea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0048ae1c996a53341975b76afee97999044d5435a8fe35e4c4215a7e64e4addb`

```dockerfile
```

-	Layers:
	-	`sha256:c54b1f1937202123f6d8c691aa97542ef1327815a588139f035f21e39ddeb280`  
		Last Modified: Wed, 15 Apr 2026 21:22:24 GMT  
		Size: 51.7 KB (51699 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:dc2611300290c9012c849a9f847e9ab795308878bad345ab407424a36719cb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98258818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d15fee89fcff222c68faa384a03eec3679ce5ab1da75fca5b0afbc84d89e6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:21:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:21:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:21:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:21:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:21:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:24:24 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:24:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:24:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:24:24 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:30:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:32:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:32:10 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:32:10 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:32:12 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:32:12 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:32:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:32:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:32:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:32:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:32:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b303a0989ba45e4f7b30cb9937c77a13a6d2c7ecd4eb8917f1512079f9f97`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 3.3 MB (3343367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfb6dec2dbf14603e2027ed5b971b0cded429fa6c207d9d90b199acc9cb3f9f`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae7b5f922f713096ada0c57083da1371a86516392d3d545429f9e6f086cfc1`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd82f5c870f06ad0977d75bfd5f221698844492f83e81d648b6df4d92191d57`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 13.7 MB (13709890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319ee333590a57384eec8d838e3097a7bbbaf98511fa5f754866f9c060f4ee53`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6db70784fe0b64129cd81fcc768162b61cfcfc6046390d05cccaf7bc7b34a4`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 12.9 MB (12905191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a2b25dcc6fc43cce4d7cb7527e44400765b559a9be6f70a9f0b870f5431a16`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc4e71b3774288941b5f1bfc7d26b51a56816bc620b4dc0adda2a995fe29d10`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 23.2 KB (23213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5dbac3789d20b6f7fdf3f3626bf3319aed3094a4b8438530220ba321dbfbf`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 23.2 KB (23225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c39b81bd3ed013ae106fd28f7de2a7f5a334afda4037ae7ad637f3deab270`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb55f85606be30eed6af76a1b2c9bbc7780863962b34355349e2416c8f167c5`  
		Last Modified: Wed, 15 Apr 2026 21:32:22 GMT  
		Size: 26.9 MB (26900910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e349d31cffe8a115b26e2a742f3453d5a7c8ceaec9a87b54c3d10304cc579b`  
		Last Modified: Wed, 15 Apr 2026 21:32:22 GMT  
		Size: 8.7 MB (8727550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df87049c2bcd07f24f47b33d51e3c1e7b8815743f62256d1a414aed92ec3bb3`  
		Last Modified: Wed, 15 Apr 2026 21:32:21 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef3f5f6ed4acd385b18046c9978c92c08b2f297be8c1a44321cd57d2225fd0`  
		Last Modified: Wed, 15 Apr 2026 21:32:21 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e9be2fb9533f5d656a6a2c4880a73265e64d41f0e252842dcc76d03e34352d`  
		Last Modified: Wed, 15 Apr 2026 21:32:23 GMT  
		Size: 29.3 MB (29323871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d211fef5a1b1fdb77c9389a235d34d551c6348e3e9d64cb446e5abdc873ea7`  
		Last Modified: Wed, 15 Apr 2026 21:32:23 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3488dde38c55546811f2df2f9dbafb9e514689354a97c94b99c609107218f9`  
		Last Modified: Wed, 15 Apr 2026 21:32:23 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81220c29d727aad216e2e31759bebfeab48ac148a450e5ce45a68779390800a1`  
		Last Modified: Wed, 15 Apr 2026 21:32:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:b71f0d5177e7d53c07c81bd0cba7f264de339a265a734c13b80cf71e465914c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1170182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e970693d5ed6caaf627c5caa1d1eb62a2b4b04caa5685015cd297a982084c8d9`

```dockerfile
```

-	Layers:
	-	`sha256:5f3f32480356818038d574675f73f2d0fca0b2cd015ceb0e05ca311d44317904`  
		Last Modified: Wed, 15 Apr 2026 21:32:21 GMT  
		Size: 1.1 MB (1118268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23135b73c9ef17a9b0ca892a2bdda7df5e21ed8b679f2d11411977f0114c404`  
		Last Modified: Wed, 15 Apr 2026 21:32:21 GMT  
		Size: 51.9 KB (51914 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:2cf8180ad884fdc7c4c7d46fd830679f9e410f01871fc95b1dc5502f0f485810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107192013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf753bc31585c21800f82982a405ced1fcbe62aaa537f423dbf2d75e109ca6ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:16:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:52 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:19:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:19:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:19:52 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:19:52 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:37:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:38:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:38:02 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:38:03 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:38:04 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:38:05 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:38:05 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:38:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:38:05 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:38:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:38:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f88c471740fcb5875464e516549da32c6c706f6987bc05fbbb6fd513a5802d`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 3.6 MB (3596129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992eab76c94334ac507bd24480ab30256763b2b3d9cbee2101f931af7891065`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e2ccbab69dff79d74edc28fd92dc771024392d7f27df7019a0996222edb8f`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b53c8276cf1764bdbc2a8cc4bd82d17c9abcec1caa79e755d4bb8f6cd08689`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 13.7 MB (13709885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c9424747f4f86a2634299b5c26a2827b3fee39c8784a2cffe3db0dcccfbf2`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72a7eb2230420c7fcbaa60c52674a748d09f2ceec7a1d09bb2384d3e9e4dfb9`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 14.7 MB (14702729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f864aebee5b8c62db6cc183f3cd9b7cda0fec6d388db0af242bb2496252e6b`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de20756a108dd2bb386335748415a405d248e1ab311f95e986cf3b417ed4163`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 23.2 KB (23213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84abee5e477c51afcf6df1e875a6d0c7b98a1ceed1df6f1b371d717edad39b06`  
		Last Modified: Wed, 15 Apr 2026 20:20:01 GMT  
		Size: 23.2 KB (23224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce22a0940badf7da9b32f48d60afebdc96dc96c225a972f67e8092b3457344e6`  
		Last Modified: Wed, 15 Apr 2026 20:20:01 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59981e6a412d93bdb57fb4bc56c65fe4c870465e524945cf0a88ae31518f55f`  
		Last Modified: Wed, 15 Apr 2026 21:38:16 GMT  
		Size: 32.5 MB (32479995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26990f31b69e597699b00077844fb9f18943278194dfcc181790ef555b5403a8`  
		Last Modified: Wed, 15 Apr 2026 21:38:15 GMT  
		Size: 9.1 MB (9114633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ba85cc36d08e2abc37eb550a465f85611254adc929f866a85b24ca86d156d`  
		Last Modified: Wed, 15 Apr 2026 21:38:15 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d880e60f798e78e143c8dad1f4734248cf6a9228ec232a975618dfd1a44daf`  
		Last Modified: Wed, 15 Apr 2026 21:38:15 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb66058deeb676a2b48ea049dd6de0d705c97c7a2b76929bacf78ca8dfe0d7`  
		Last Modified: Wed, 15 Apr 2026 21:38:17 GMT  
		Size: 29.3 MB (29323859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44838df35c47cdd4429763685c7e4c5703c15edf4e17386a2aa1b7e9a9c6d04c`  
		Last Modified: Wed, 15 Apr 2026 21:38:16 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a9ab6ea55a236b1f79ce67716c1e03f13c73b92e739cba090bb75c339e695e`  
		Last Modified: Wed, 15 Apr 2026 21:38:17 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfd3316feb5c09b6fbd6331032cb3ae4544016eb39799bc78f009ac7328db08`  
		Last Modified: Wed, 15 Apr 2026 21:38:18 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:0e5180b7a041bc0cc13d6c85d786599a9c889b478f7040d6808b68b413ff9566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1170236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d9d6e871c181cb3660bae3cb44e63559effe3b8255309c39294d787758dce0`

```dockerfile
```

-	Layers:
	-	`sha256:39b949d6b453829519fa1ec9fd4e8762e2735aab002f684104f576106535a4e3`  
		Last Modified: Wed, 15 Apr 2026 21:38:15 GMT  
		Size: 1.1 MB (1118288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c92ab9c9db31f7150a1dc557b524362a0378e957717436e880d5911ea0d28ec8`  
		Last Modified: Wed, 15 Apr 2026 21:38:15 GMT  
		Size: 51.9 KB (51948 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:db2e629b968f57f7764807a2509a0aebdc674dd68fefe2f4c208fba6c8705523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107482884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cada7da872dee0648c04caed038c0ad16684957dae7a65cf6ebef84be8b973d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 22:21:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 22:21:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 22:21:20 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 22:21:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 22:21:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 22:24:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 22:24:54 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 22:24:54 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 22:24:54 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 22:24:54 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 23:16:03 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 23:16:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 23:16:54 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 23:16:54 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 23:16:56 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 23:16:56 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 23:16:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 23:16:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 23:16:56 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 23:16:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:16:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c62319c64ecbc8864f653b3190fe2930cd0d7d729dd495e4f110d82beb5a8cf`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 3.6 MB (3625741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b237d5e55c87544bf498ed4aa2213ff7f3202b6e8ac11c0feb4eef6dc60561b`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ce09e8975bb1abc7c27969ab796d05155e31bf9607dbc4d8d6b9869d6f42f2`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba374fe7ae564b24b876c0e37c0e24ae10295833b103ec997c6f4d51b33a2618`  
		Last Modified: Wed, 15 Apr 2026 22:25:02 GMT  
		Size: 13.7 MB (13709870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1068ef912fbd9b5cd23278793990a073d89428d5fffb6721e01c234f10214b9a`  
		Last Modified: Wed, 15 Apr 2026 22:25:02 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e808d6508c20e9c7b0fb968a894ef6f3a08518435e4e95508d14a683736b4`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 15.5 MB (15507087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e4133cfa5665ce34eef08043c23f2f0dba6eef44cfdd177b97398f5bba9523`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536bae25de12f93460507a4870f8205b06a2eef459609bb23b73e1bd928c055`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 23.4 KB (23399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada671ef1cb78b082bc30975712e67aa71c719e0155289b05390c82eeca47ee7`  
		Last Modified: Wed, 15 Apr 2026 22:25:04 GMT  
		Size: 23.4 KB (23417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad1be0d762f8603f63ac3e25a8914ead38c4303e1cdf95c608adcbae90b5d06`  
		Last Modified: Wed, 15 Apr 2026 22:25:04 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f059ded67844e92d1e917c35976f4fec07432f97f9bbffaec6c7adfb10708`  
		Last Modified: Wed, 15 Apr 2026 23:17:07 GMT  
		Size: 33.3 MB (33305525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3270cf9c29d3e95ee07001e3389069b6af9f6e65e38fb476fde0d12fb002826`  
		Last Modified: Wed, 15 Apr 2026 23:17:07 GMT  
		Size: 8.3 MB (8255084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b188ddbb8230b90b14bdabd84ca1f496745eced5004acfdc99cacf8fa2c053`  
		Last Modified: Wed, 15 Apr 2026 23:17:06 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51452bf21ebcf107421d97617d5575cd211a710755b286d6836e8810a5683500`  
		Last Modified: Wed, 15 Apr 2026 23:17:06 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339526b8a75a0ed2a98fb4164b7977fd0837068bbea857aabf620e2621d72d02`  
		Last Modified: Wed, 15 Apr 2026 23:17:08 GMT  
		Size: 29.3 MB (29323855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3564d6ede0d5a4e9015656e53ac47c486b12a3103bc91811e8ea43eb0b0be2`  
		Last Modified: Wed, 15 Apr 2026 23:17:08 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b051b43e6f21fc33db9364513c9cd73a99f5b0c25cdec60bef7a7a850ef6ec0e`  
		Last Modified: Wed, 15 Apr 2026 23:17:08 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2561ed0828cee575eb03e649e5960c0b7452047146b524228c485b4c15edac71`  
		Last Modified: Wed, 15 Apr 2026 23:17:09 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:523fed73b369b7bb9585932f5b7a5457fa6244a20514ccaa381a4df19cc1d132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb452645ebfed13d1c8c5e286d812df50780e184406af358b7fc96b371c1391`

```dockerfile
```

-	Layers:
	-	`sha256:5b78ad80685cc4cf250188505306658b5a9d6a68aa8db2e096d9eb5d290024c8`  
		Last Modified: Wed, 15 Apr 2026 23:17:06 GMT  
		Size: 1.1 MB (1120101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308d78273f45355c536baec9c54d45ef81c4803c8e84f1028b93134c8347f8ea`  
		Last Modified: Wed, 15 Apr 2026 23:17:06 GMT  
		Size: 51.7 KB (51726 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:fa3e88486e1462dfb3bbd1d4a076cf572eb7ac59cf71b8394c1339116c8520ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109497806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253cd55a1cd04a3192a87a10e9370c3f31321cfac55d440495f0b575e9d45c86`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:26:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:27:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:37:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:37:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:37:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:38:00 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:38:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:38:00 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:38:00 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 23:57:08 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 23:58:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 23:58:53 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 23:58:53 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 16 Apr 2026 00:05:52 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 16 Apr 2026 00:05:52 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2026 00:05:52 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 16 Apr 2026 00:05:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:05:53 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 16 Apr 2026 00:05:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:05:53 GMT
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
	-	`sha256:0370fd1370a54392f3444f77669b0c6655267b3ae193cf4de50a9871836636e7`  
		Last Modified: Wed, 15 Apr 2026 20:32:23 GMT  
		Size: 13.7 MB (13709879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5dbe897696d0b00e89cb8cca0978c45cfac755af8488d2743b4d1d0e8349b9`  
		Last Modified: Wed, 15 Apr 2026 20:32:22 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed748167a4ba110e55bf836859404ed0d07c8012c0a38120a6a71eb553916df`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 15.7 MB (15732363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e837ab2c17d3b0ba367d2b928038674b2b671b658d5d1a8d2c7c6887717a6b7`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281189f4b70a3abcf43f4fbb010b7a91d30476a4f755d51d6b0dca53f4c4c6ba`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 23.2 KB (23227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0d3b6b2ac74c55e87998f3778dd5acb7b98b2ad5d5cda294b7423d2989ac16`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 23.3 KB (23253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f01cc8a62ac057a37f08692e3d3ca7a19a514bc8c37ba1f784049e37952d7f6`  
		Last Modified: Wed, 15 Apr 2026 20:38:18 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fa1c5dd0ce41c5a622e921720f33cd0dc9d6d6ccb5d619c3e748e6ea1b637d`  
		Last Modified: Wed, 15 Apr 2026 23:59:20 GMT  
		Size: 34.1 MB (34068735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f8feb7f632883203695e257ab16f759e559cab140dff687d3d7eae521a872d`  
		Last Modified: Wed, 15 Apr 2026 23:59:19 GMT  
		Size: 9.0 MB (8999953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354bef75c07f5b91cce358673fbe591ddc3d593c85cd19147e2c7fd6290ed895`  
		Last Modified: Wed, 15 Apr 2026 23:59:19 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c2d70b5fae249bd8c7346cdf2dc45985f72ad57ab01e28f34f7fa2c056c69`  
		Last Modified: Wed, 15 Apr 2026 23:59:19 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ff805eeff95539a7fcc801a6aea0cdfcee66d9d20473b408a1096485a69a28`  
		Last Modified: Thu, 16 Apr 2026 00:06:12 GMT  
		Size: 29.3 MB (29323883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0a516e74a7c73210e36d51e03dce3f255797755a476c04b63693235f990dc`  
		Last Modified: Thu, 16 Apr 2026 00:06:11 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0fcb0f59f1eb2006fb42ce6adc4b8930b6b33f0916da58ab684c17789e5936`  
		Last Modified: Thu, 16 Apr 2026 00:06:11 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1d79af19922cd6ba4c15baa0d4f98543b1deac190db33fe37bcd2e02f142d`  
		Last Modified: Thu, 16 Apr 2026 00:06:11 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c9ddfcac8f59df8f1fe03eab6e1bc0bae7c2ab18e8b93f7a54da83c9486c6d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1170088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a91c5c144705f395b82463ec70446cf120a84c2ecadca8c9bf0052af1fefc0`

```dockerfile
```

-	Layers:
	-	`sha256:7425021564a190e73c20df5d36e7fd73b489642d7c3863872a45a7c53e143fb1`  
		Last Modified: Thu, 16 Apr 2026 00:06:11 GMT  
		Size: 1.1 MB (1118265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:252781176e5d4c1b76f77b95e891c5197c65306118ab4464f9700c1b1149273d`  
		Last Modified: Thu, 16 Apr 2026 00:06:10 GMT  
		Size: 51.8 KB (51823 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:9b3a1ee1e5796c98ec0d02713e26fdbd8502aaa4dd0d2a42aa0817f8076ee584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107738404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a809e8436e97a2736dc1c4d1af2229480cefd94bff7bc61884eea3163425e8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.4.20
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 18:58:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 18:58:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 20:57:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 20:57:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 20:57:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 20:57:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 20:57:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 20:57:18 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 20:57:19 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 20:57:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 20:57:19 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 20:57:19 GMT
CMD ["php-fpm"]
# Sun, 12 Apr 2026 04:52:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sun, 12 Apr 2026 05:08:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sun, 12 Apr 2026 05:08:30 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sun, 12 Apr 2026 05:08:31 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sun, 12 Apr 2026 07:38:38 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sun, 12 Apr 2026 07:38:38 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 07:38:38 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sun, 12 Apr 2026 07:38:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 12 Apr 2026 07:38:39 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sun, 12 Apr 2026 07:38:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 12 Apr 2026 07:38:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfdae87dce600eeda7208c98ae006cd061e7aa5aea7598748846f26db985a32`  
		Last Modified: Fri, 10 Apr 2026 19:58:24 GMT  
		Size: 13.7 MB (13709976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f61ec46e0eb851487ff35e9478305799f2d18216836fbf785f14606af80786`  
		Last Modified: Fri, 10 Apr 2026 19:58:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0554c2a3f9c4773d09414e5964b9f079b8ed871825fffd50b2d5d2f74b9c37`  
		Last Modified: Fri, 10 Apr 2026 20:58:15 GMT  
		Size: 17.6 MB (17565234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f749be7fecf1881975ae74fbe4eb0c1761d28cb6d1eb748886e1748966180684`  
		Last Modified: Fri, 10 Apr 2026 20:58:12 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc6b4a21964d6de35dfc306a93dfd2196704ecfe76b3eaa7d690f34f54f4f0a`  
		Last Modified: Fri, 10 Apr 2026 20:58:12 GMT  
		Size: 23.5 KB (23475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc825a1a3fc09e439ef71f666bbe31e16c16dd31167fbc581ac9eb0767c7786`  
		Last Modified: Fri, 10 Apr 2026 20:58:12 GMT  
		Size: 23.5 KB (23496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5898aaa3d19863302617c584d9db02c6be5430be0be6e0cdd8b0bb4f47c70f95`  
		Last Modified: Fri, 10 Apr 2026 20:58:14 GMT  
		Size: 9.3 KB (9273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd042565350f787960c45f6eed965362418f06dd7d0bbb8bed20c02bcd240456`  
		Last Modified: Sun, 12 Apr 2026 05:10:43 GMT  
		Size: 32.7 MB (32653004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8772629ed343b739e415695d026001d8b4aea66747f023e6b56187151a15b1a7`  
		Last Modified: Sun, 12 Apr 2026 05:10:35 GMT  
		Size: 7.1 MB (7094532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b53bea384d11ba44e8947cadd38707dac9da149c16b117988b78987920013f`  
		Last Modified: Sun, 12 Apr 2026 05:10:33 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e4bf373e8c6a4e97840725d6757a3b06930d99b3f4dbe30a14157cb5b2ed1b`  
		Last Modified: Sun, 12 Apr 2026 05:10:33 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017df5773ba79977e0049150bf5c3da9058bbb0d3a6b110cea5c4fec97fe6676`  
		Last Modified: Sun, 12 Apr 2026 07:40:31 GMT  
		Size: 29.3 MB (29323883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd600ccf42eb806c8f42dc653fd199791c203f187aed4e799c51392d6bee302d`  
		Last Modified: Sun, 12 Apr 2026 07:40:26 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81967aebfa8d24dd4bea936a53276cf072a758dd917acc1c07abe55659c74824`  
		Last Modified: Sun, 12 Apr 2026 07:40:26 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b395b1de3718ac6862b8af41914fa4b295494b0198c78e5e0f8346f2cb8179e`  
		Last Modified: Sun, 12 Apr 2026 07:40:26 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:113b5f1e4760d15282c529e0c8c5ee9230e91e5d169d494bd975f286de186d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196d11db6330dde9593b4987c7ddf42822747f6b8ca826a813e2f337fa94f4d1`

```dockerfile
```

-	Layers:
	-	`sha256:8c3942466d329bb7318b5290220943e9410f93128c9311ba0745b6690b8058be`  
		Last Modified: Sun, 12 Apr 2026 07:40:26 GMT  
		Size: 1.1 MB (1121239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb40ee3fef9e6ff3b9844c95f5509582ed36c19f609eed799a3cdff362805b5c`  
		Last Modified: Sun, 12 Apr 2026 07:40:26 GMT  
		Size: 51.8 KB (51823 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:61df79afdc14cfde5e5bf19678eb1993478408e260491d4cc32007c697e88772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111529568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5646f3644638e9d977a0ddb100c8548cd061a23d1ecee8a044f320cea225781`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:37:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.4.20
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:38:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:38:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:44:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:44:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:44:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:44:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:44:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:44:15 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:44:16 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:44:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:44:16 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:44:16 GMT
CMD ["php-fpm"]
# Thu, 09 Apr 2026 23:10:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 09 Apr 2026 23:11:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 09 Apr 2026 23:11:22 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:11:22 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 09 Apr 2026 23:15:10 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 09 Apr 2026 23:15:10 GMT
VOLUME [/var/www/html]
# Thu, 09 Apr 2026 23:15:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 09 Apr 2026 23:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:15:10 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 09 Apr 2026 23:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:15:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348d21358ef752a357c33976b85357317bfb623a79cb91ec462b4e5128b82d5`  
		Last Modified: Thu, 12 Mar 2026 23:43:03 GMT  
		Size: 3.8 MB (3795119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a169c2de4deea9b877eb224ec8f2d4f4502dd0bb4e22037516ea41c23c8c1e6`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a80dfabed7faa02e1bbe28dd4e26c817c26d54bb3411b27cc398ea997ef8`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f98d65964168e54526ab553e0dc43c974776da7405cbb110d8b1285f2d8b87`  
		Last Modified: Thu, 09 Apr 2026 22:44:25 GMT  
		Size: 13.7 MB (13709975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f83e1d7974378e5b8b648e0a12335f23f71d81cff434d4ba577e4bc3e8263b`  
		Last Modified: Thu, 09 Apr 2026 22:44:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd8761553186dc155f4f3fccad908fc4e3ea25912933894b073d5c5ab338dd`  
		Last Modified: Thu, 09 Apr 2026 22:44:28 GMT  
		Size: 18.2 MB (18220326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59e1dcb28068d8d63751c38483e856f7daae276798259425f33f18ff549940e`  
		Last Modified: Thu, 09 Apr 2026 22:44:28 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6276f7f0400c60525e226b51c3ae8be6c9201ea13f121a0b052f3bf45a8aa2`  
		Last Modified: Thu, 09 Apr 2026 22:44:28 GMT  
		Size: 23.5 KB (23473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5011be93c589e26d5c5b274855498a678d24624d05f66fc8e22d9fc2483a7e56`  
		Last Modified: Thu, 09 Apr 2026 22:44:28 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623287c007d74155b8bccaef654ca7b07a5078bea7f3fc758a6aa54101270d1d`  
		Last Modified: Thu, 09 Apr 2026 22:44:29 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf452efa2afcfdda5cf8bf9cdaa86349eb62c7c5fb0cc225f533973826623fb`  
		Last Modified: Thu, 09 Apr 2026 23:11:42 GMT  
		Size: 34.0 MB (34010705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b44ccc042172cfa4faf203643f9076c83d2594853ae5fcbd2f43a5fcc4928b8`  
		Last Modified: Thu, 09 Apr 2026 23:11:42 GMT  
		Size: 8.7 MB (8678804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c26bb747ae8f375954cf88089c16ab54816e1c7f519829a1243079672f3ac0`  
		Last Modified: Thu, 09 Apr 2026 23:11:42 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cb2caa078b044034ef3acf218df2604d811f1f110ea8df5bd1017953e93413`  
		Last Modified: Thu, 09 Apr 2026 23:11:42 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8163e2f05f1c18003e7f26f41993f13a51d7290eae827c618ae2e9a77a6d6139`  
		Last Modified: Thu, 09 Apr 2026 23:15:24 GMT  
		Size: 29.3 MB (29323858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c383fd90f376f6604efabac44c76f81ae1dec2c05cbebff37284ee86b22292`  
		Last Modified: Thu, 09 Apr 2026 23:15:24 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af565f84894811ef7c86b7984f943e3a4b05393dead1351862a1f4742e86c750`  
		Last Modified: Thu, 09 Apr 2026 23:15:24 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f54513b557db344346d4d5d983811c2f18382147d606ba45c7cb8442fe7077`  
		Last Modified: Thu, 09 Apr 2026 23:15:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:3f814355ac422a1e1fe60c000b3e6459f1be16e85bde002f5a5e703a065e37d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857c1091398f9479b85170a3721f66145691f0364287952367d37e1258a2aeb`

```dockerfile
```

-	Layers:
	-	`sha256:eafd3a0c4aba28bc7f49d187a6a05f0f731d216531649820ef2fc36100898f35`  
		Last Modified: Thu, 09 Apr 2026 23:15:24 GMT  
		Size: 1.1 MB (1121209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d931f6ec0d9633d536aeb44271616b57209ffde1ca0973614195d8c9edcbcc0`  
		Last Modified: Thu, 09 Apr 2026 23:15:24 GMT  
		Size: 51.8 KB (51767 bytes)  
		MIME: application/vnd.in-toto+json
