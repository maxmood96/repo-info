## `wordpress:beta-6.9-RC4-php8.3-fpm-alpine`

```console
$ docker pull wordpress@sha256:ca202de936e5534c44ac343c204689b7021fc4797d2c50ef3c1230ff95002e3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `wordpress:beta-6.9-RC4-php8.3-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:8cce35561533cb4d629089cd9f97b3824ea2c5ee8363e66a703a9e44a7d83a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97757775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b3f11d4a360d977e7865ff195ed5e7de0fc5203e2a66a033415fa2cd430700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:03:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:03:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:03:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:03:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:03:56 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:04:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:04:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:07:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:07:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:07:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:07:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:07:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:07:06 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:07:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:07:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:07:06 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:07:06 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:16:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:17:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:10 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:17:11 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581d36e768dbacf5bdd194bbf9fe2fa06835e31f9daf22b51a674081d71bdbb7`  
		Last Modified: Thu, 20 Nov 2025 20:07:27 GMT  
		Size: 3.5 MB (3463770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd5a3fcc2dd6a8286922bfaeb41e4f6c3e903acbb27688538cc48d05ce1b8ed`  
		Last Modified: Thu, 20 Nov 2025 20:07:29 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6fa6edd4f26b32894cdaf1d71232133c5544f3071fae5df8ea7229d35630ea`  
		Last Modified: Thu, 20 Nov 2025 20:07:26 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6421ac3f83f664829c691279f8ee8a38a08a6b57633bf3322e0e06cfbb53ad6d`  
		Last Modified: Thu, 20 Nov 2025 20:07:28 GMT  
		Size: 12.6 MB (12625125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8994e0a506927e4635bd453fd1807827d89aed4075e656c4dd05c2a3d026c5d9`  
		Last Modified: Thu, 20 Nov 2025 20:07:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46564e0a987d7ad2cf420f22c1ebaeaa705ed03d3611efe60d1aea7040709b12`  
		Last Modified: Thu, 20 Nov 2025 20:07:29 GMT  
		Size: 13.3 MB (13273057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5c27422ace307c473400f5e670e512119f50c8c7ea3abe0e073a1daf3e0481`  
		Last Modified: Thu, 20 Nov 2025 20:07:28 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90831669701bd29cf5ba9bd319e9c47ae19be5ed86fa0b99c7218630b2c343de`  
		Last Modified: Thu, 20 Nov 2025 20:07:28 GMT  
		Size: 20.1 KB (20081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0758fb508b003ef455a3cd0b29fb2e33b314b4b646e3949a249e1a02376ed6a`  
		Last Modified: Thu, 20 Nov 2025 20:07:29 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcccce939e3c6ca05cdbdaafc21e2e4ee2923a75242bc8c5b289ca40a93955cc`  
		Last Modified: Thu, 20 Nov 2025 20:07:29 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a2e7299439d07e4a5150bc3e851922b0d9e1682fe170281420506b1e12c1e2`  
		Last Modified: Tue, 02 Dec 2025 01:17:40 GMT  
		Size: 28.3 MB (28282738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2a7189d58c4707a4ad9de6f0daf66b992b165b4b4df9d9751f77acfe455f06`  
		Last Modified: Tue, 02 Dec 2025 01:17:38 GMT  
		Size: 9.2 MB (9226872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a8d7c2c68be9c8f664ac3d7975c2f8389a295cc01646d90bc8488d8c114ab2`  
		Last Modified: Tue, 02 Dec 2025 01:17:36 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c735eda1edf5bf7dfe17067fe8081194a3eff55cd7e14ab13685088f0a667c`  
		Last Modified: Tue, 02 Dec 2025 01:17:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f705a735acc8bbc7c86e0b7110cc03a56ec3889e5ab4180cc6c3ba06dc90a5d8`  
		Last Modified: Tue, 02 Dec 2025 01:17:39 GMT  
		Size: 27.0 MB (27025200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5c3aaf3463efed163b3a07671a3fc6315851bc1aaaa2e03aa5f9f550239f9b`  
		Last Modified: Tue, 02 Dec 2025 01:17:37 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8eea785ae2eb5f968382621c32045beeffb527b1822091945e4101fb1f6d2e`  
		Last Modified: Tue, 02 Dec 2025 01:17:37 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e181fe8deb621a28e4c5c564597997ce97caec6279a76271a23cbe90183493`  
		Last Modified: Tue, 02 Dec 2025 01:17:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:55fc364d2ae51246acd09066d4654a36430d1994ce661537b9740e11bbe85f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1136172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912192e91171c9eb259fe23543ad0c0d8fc309a1628ef02a0daca89ef840563a`

```dockerfile
```

-	Layers:
	-	`sha256:cae11cd4adfb22416917774eed1e8a8a1a465e9a705456df4b14213f8f886cba`  
		Last Modified: Tue, 02 Dec 2025 02:25:05 GMT  
		Size: 1.1 MB (1083087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcef4251127e0324c34938022583111f39a6fbe6bcf60167d07e374a1929f2b1`  
		Last Modified: Tue, 02 Dec 2025 02:25:06 GMT  
		Size: 53.1 KB (53085 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:d17fbfe3e73d7c73371b211703283f18819962314536881117bc164476c9a3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90664689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4412638c41e37c36fb32b3a83a668b52518e572878b80b5e284bd072ee68e4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:58:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:58:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:58:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:58:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:58:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:58:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:58:11 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 19:58:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:58:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:01:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:01:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:01:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:01:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:01:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:01:06 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:01:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:01:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:01:06 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:01:06 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:15:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:16:28 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:16:28 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:16:28 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:16:30 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:16:30 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:16:30 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:16:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:16:30 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:16:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:16:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc37df1221ed237d17e665fdd71dad79d915044e97eb493b116f73f9d73ac987`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 3.4 MB (3428341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db45bdb2468e503765c9317a985379e7dff83ad0c811221c15db1bbf8e018cf`  
		Last Modified: Thu, 20 Nov 2025 20:01:40 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc60ea8fc0e4b64ead950b75712383229d8fe7e62194157598a5a62b1edf736`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e2ac2e870149c9aa7689a095a9afe28608aefa5adf7dc4549e133b7bea3f0b`  
		Last Modified: Thu, 20 Nov 2025 20:01:44 GMT  
		Size: 12.6 MB (12625122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9290b68559d797a7a15ef80386abd14df48533137849e3540c0463ebb60600d9`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788110136de653a7035c8d38ccf47351a212fcaf96ad048ca936870c2e6ba284`  
		Last Modified: Thu, 20 Nov 2025 20:01:44 GMT  
		Size: 12.0 MB (11986225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e817bb5d5aa1d8c1a6e709834ea5d640ee9b80c74991f3e2a375ab63b620d7a2`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ed9ba8eaf79cc949ba58cd00db64c604868388cb83eeeccbef5095e1c3dab`  
		Last Modified: Thu, 20 Nov 2025 20:01:41 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d59c6a492ca9530b3b1c03faca08b2c4b3c84e7d98ca25ba9e20e13140a8a5c`  
		Last Modified: Thu, 20 Nov 2025 20:01:42 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cabc0a8d2fc2e5fa2dc11f76250be56ae288e30ae342d64e79d4ca993ca6979`  
		Last Modified: Thu, 20 Nov 2025 20:01:42 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559ae6e7370eecdfacb8df33b9e4c9e47b8a3af3b8b99dcce73f70a30d2869b9`  
		Last Modified: Tue, 02 Dec 2025 01:17:01 GMT  
		Size: 24.4 MB (24377239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db88e3b9ad3768e708f652c6067403550293840da50dd211993dcc04efe41192`  
		Last Modified: Tue, 02 Dec 2025 01:17:01 GMT  
		Size: 7.7 MB (7660338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ff2e6a164668e8df3e5a4c2a2f6678803011201bfff19d8bb073624c9ada37`  
		Last Modified: Tue, 02 Dec 2025 01:16:58 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5100566b63bb4837ee8cb12e64ebabe373122d6ced5917b18ab892f84696bacd`  
		Last Modified: Tue, 02 Dec 2025 01:16:59 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a64e1f798904db32a547776dc9f7d51c5dc0f21a3660f480fbef24e3db8e16`  
		Last Modified: Tue, 02 Dec 2025 01:17:02 GMT  
		Size: 27.0 MB (27025201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9f55905a6a5877dff2f00dfb85a78cda48bf30a33fd4c816521c5abe15a8bc`  
		Last Modified: Tue, 02 Dec 2025 01:16:59 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69380d9d109ebe3ce72413e20acc222a6eb39af577a2742ea06eb0b06c2e859`  
		Last Modified: Tue, 02 Dec 2025 01:16:59 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252ff6d8922a95f3155535fad4cb411f183bce0bb0e1b9422a3a6cfa275c458d`  
		Last Modified: Tue, 02 Dec 2025 01:16:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:02dc55d84b7fea19449cb4f2aa59150c39d8846c15b8ad72377a56f2d0cba44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 KB (53047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b142c43cc1b098a587716f3ae7b61147a2b3431c05ac0e842fba5d0ebe6dde3`

```dockerfile
```

-	Layers:
	-	`sha256:9efdd856269b9f53aae491b608d3564b9798d2a030d271e3f9bf07ce2d0fc21a`  
		Last Modified: Tue, 02 Dec 2025 02:25:10 GMT  
		Size: 53.0 KB (53047 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:f0887487ff8b4bee144ac8b09e71b84afd5dc982a6a20b28250e1625960ff68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89380008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538bb1cd27bdf59d745535b9ebef4d281efcc5a824130a89fbe417138812602`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:16:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:16:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:16:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:16:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:16:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:16:34 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:16:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:16:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:19:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:19:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:19:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:19:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:19:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:19:23 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:19:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:19:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:19:23 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:19:23 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:09:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:11:00 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:11:00 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:11:00 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:19:29 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:19:29 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:19:29 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:19:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:19:29 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:19:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24006ca79b19813864910cc813946667a37fa2dcb1c183d771668a38685e9d79`  
		Last Modified: Thu, 20 Nov 2025 21:05:22 GMT  
		Size: 3.2 MB (3244419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492c64266c1e3e312d13a40ecbcfafa94e2856d0cfbe2789657eb0421c9dbd12`  
		Last Modified: Thu, 20 Nov 2025 21:05:01 GMT  
		Size: 938.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31c8a839b8e35d22d94761b3db7bf49c0d267e62f5c28d5acb586fa0e964518`  
		Last Modified: Thu, 20 Nov 2025 21:05:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f36284021159973665a155a90723b258caa120bb0f52604c8abf0157506c5c`  
		Last Modified: Thu, 20 Nov 2025 21:17:52 GMT  
		Size: 12.6 MB (12625110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524751bc1919023503d64e914b985b2ea6bed64c7b0690639a64b30324044ea0`  
		Last Modified: Thu, 20 Nov 2025 21:05:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e716dbcfaf71c1469c2a91f9b7873c7e22062af70a0fad98bedb6f88d383b56d`  
		Last Modified: Thu, 20 Nov 2025 21:17:51 GMT  
		Size: 11.3 MB (11293429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c518c819621305d7106c117fc83d873fcc37ac427a439a57f01fe102eff1ea`  
		Last Modified: Thu, 20 Nov 2025 21:05:00 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25612b4c22efa0e60f64fc7ed4064474319a43d6b8d1a82ba8a25d14211d62a6`  
		Last Modified: Thu, 20 Nov 2025 21:05:01 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549d2d41bad136320446b1215475da892aa80d9f080685949d870d7d15031e4b`  
		Last Modified: Thu, 20 Nov 2025 21:05:21 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd8f42946365810d9e87af4f15833e2dce6cd5b847610ebd6819a5399d564f4`  
		Last Modified: Thu, 20 Nov 2025 21:05:00 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee613f7e56f9272809e5f2f43593f3c5d0aff2682d8fabbf8b54f0a9830186ee`  
		Last Modified: Tue, 02 Dec 2025 01:11:25 GMT  
		Size: 23.2 MB (23152247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7166000f496e2c97741f8ae9d29bb4b95b0d630afc5f8c222716aaa1d0dabff`  
		Last Modified: Tue, 02 Dec 2025 01:11:24 GMT  
		Size: 8.8 MB (8759929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bad3161336f2c804fa592a7b065c3c0ab0848703c8097547d52caade42edaf`  
		Last Modified: Tue, 02 Dec 2025 01:11:23 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f9528dfc84687d719d5de980fc3babd55743db0693362092e397249d8f5a43`  
		Last Modified: Tue, 02 Dec 2025 01:11:23 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d44083a8e8a037995be17062a9ad5eec934279d88e0a97edb554101c129000b`  
		Last Modified: Tue, 02 Dec 2025 01:19:51 GMT  
		Size: 27.0 MB (27025196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4bb52f3d8ecd7ef9e4f1f2faa6ce3a4944173d0f69fc9e1cda6ce791fd1e0`  
		Last Modified: Tue, 02 Dec 2025 01:19:46 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30e527ab2506dba21ce885f7b3a0cb3caddb52607dc53102a673a3edb7221e9`  
		Last Modified: Tue, 02 Dec 2025 01:19:46 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5264f5b980b7e55c97274747e8f870d7d89aad256b984e3e9531b6081a432776`  
		Last Modified: Tue, 02 Dec 2025 01:19:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:2895e3de828a446917705d4841270e04ba21203faacdfdcf44ba0dcf397201b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1135173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d814da0b995bc2038a8b44c11b0d65d977a6ecfb94492c963eede96792bc03e3`

```dockerfile
```

-	Layers:
	-	`sha256:a2729654f750040152430cb8595bfdf497ee2db57532d7295d8c385dc7530d3e`  
		Last Modified: Tue, 02 Dec 2025 02:25:13 GMT  
		Size: 1.1 MB (1081911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56198f5b0784ea34e3f8fd3930ab1971e3c7104922a4b02f1962eb4caf7d34ca`  
		Last Modified: Tue, 02 Dec 2025 02:25:14 GMT  
		Size: 53.3 KB (53262 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:e44b9bc82f676aefbed87940d1b30fb3df4fed0a8428639beed39d73e9a57844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96989799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2df77aa05919e48368b4a792b16076fefcacab54c7156ab838b85b611d4b9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:59:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:59:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:59:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:03:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:03:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:06:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:06:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:06:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:06:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:06:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:06:39 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:06:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:06:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:06:39 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:06:39 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:11:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:12:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:12:36 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:12:36 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:12:37 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:12:37 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:12:37 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:12:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:12:37 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:12:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:12:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6509e3b357df36f52696dfbe328393531f7e3356e402d07e199f3d973331203f`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 3.5 MB (3522951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e039386f4b37dbfcbea789b4f5f316f5d4dd9d0e451b31a1f50c6386261e42`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39301bd5b5ff1a20465358c20a4027ac1a97efc27ed5ae1eac1a398cd9fbfbd3`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9b8b22c3cc05570c3e5f1b2db3e48b23575af4641a32dafe5be18ab76f2293`  
		Last Modified: Thu, 20 Nov 2025 20:07:06 GMT  
		Size: 12.6 MB (12625079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c291b968b60244e3558f345bfa1bc727d6f2d5da4a5c027a4aea79dfa32eb`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96cab2c2542154024f59b595ed51c6b720c5bbae58d98cf3c8a27f18cf71d0a`  
		Last Modified: Thu, 20 Nov 2025 20:07:04 GMT  
		Size: 13.6 MB (13583064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159b936d878ae45e15824dbc02adcd3e400e8c701b2188391638a842dc807f0`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c789ef3d045e4f68762afb1fb5f7381d73738745e97ac4379b88c6ca4da8f4e`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4cc9837f008b85ef99be633e259a312c1a3f68e82a88cd81bc14372daa7a2a`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df52ce8f9e5e399e732090e679cbd16c8b262bf513c841543acb861d3e3052bd`  
		Last Modified: Thu, 20 Nov 2025 20:07:03 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd3e1a264a475807f1888403e469a87b6d1ddc4c68863b098012613a55bce5b`  
		Last Modified: Tue, 02 Dec 2025 01:12:48 GMT  
		Size: 28.5 MB (28494186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a98c30bd6832ed678e1d8f68b2bf34e1aae1f312294edbd2b664c065a52340c`  
		Last Modified: Tue, 02 Dec 2025 01:12:47 GMT  
		Size: 8.1 MB (8061901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c31f39113e7035737fb92878dcd39e27a91db42308daba82de8783a2f321f0`  
		Last Modified: Tue, 02 Dec 2025 01:12:47 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ff0444f807a6b2527183352f9f95277bfa0d207829b4030b57f3ef8349d5a`  
		Last Modified: Tue, 02 Dec 2025 01:12:47 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8543794e2bc5ca2b683de60ebd405574e8977594576f62cba6d2624fd2fc75`  
		Last Modified: Tue, 02 Dec 2025 01:12:49 GMT  
		Size: 27.0 MB (27025187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a490887f5f63d61ad8a96e2191707b843ba59a609a31422353fa6f4cc65750`  
		Last Modified: Tue, 02 Dec 2025 01:12:48 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908eed51e79c8315683563f7d4f72fd65230fbeb2bca379955bd9be4a116bfc1`  
		Last Modified: Tue, 02 Dec 2025 01:12:48 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9446cdbf50d704eba874df7324f427c8b67acbc88a21c0998c31d872e5e4ca3`  
		Last Modified: Tue, 02 Dec 2025 01:12:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d0314b30055d8e6f7670832e1142aff43896ca420a318ef24e37b5e90af41d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1136064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96106c31dc6f2046864cc330d4b7414f2f490f3e5d20750ab56e026f8b3f4c5a`

```dockerfile
```

-	Layers:
	-	`sha256:a7317505da8cb676dda14db38b0ef4634ac4a5c670b37fc8cac35a51d6aa7807`  
		Last Modified: Tue, 02 Dec 2025 02:25:22 GMT  
		Size: 1.1 MB (1083042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c73051fd885c4f0a3fec05eadf81b5981decdb3dfa0eb0718fc757779fcc095`  
		Last Modified: Tue, 02 Dec 2025 02:25:23 GMT  
		Size: 53.0 KB (53022 bytes)  
		MIME: application/vnd.in-toto+json
