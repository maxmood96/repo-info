## `wordpress:beta-6.9-RC4-php8.3-fpm`

```console
$ docker pull wordpress@sha256:47737f576057f240aac5f87aa4fedf9277506bf4cc5fef66e81586d4baa53535
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `wordpress:beta-6.9-RC4-php8.3-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:e1f265fe7f4f670aa49fa9a3ed419f7529b4077bfa07ef6b378677d2e1cc0566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259629328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755ea5273fa5565964dd67b74cb0ae80df0ea8609d3bba3199a095abf7d0f1a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 20:00:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 20:00:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 20:00:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 20:00:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:00:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:00:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:00:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:00:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:00:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:00:30 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:00:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:00:30 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:00:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 20:00:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:03:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:03:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:03:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:03:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:03:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:03:02 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:03:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:03:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:03:02 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:03:02 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:12:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:14:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:14:11 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:14:11 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:15:55 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:15:55 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:15:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:56 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:15:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47706e76e39c8c94dad95273f761f8e7071236bd46329fe692a30d0203c4d9a0`  
		Last Modified: Thu, 20 Nov 2025 20:03:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366713611e0ffc22f9fff716950ee2628cf9b430b0d7775ac46e01956b689bc8`  
		Last Modified: Thu, 20 Nov 2025 20:04:01 GMT  
		Size: 117.8 MB (117838061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d16d1f0a0630cc712ab560cd505e909924a426dd4d0300cd80d426cd7d0a61b`  
		Last Modified: Thu, 20 Nov 2025 20:03:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c09bcb3777d8cc7b69550e2ce888619de2fb5c85c4dc845169c96adf4cae3e`  
		Last Modified: Thu, 20 Nov 2025 20:03:50 GMT  
		Size: 12.8 MB (12751502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05e6fb0c35523d0c25bdd9baf7d5c14f0ec4d9be56cf68767ac0202e5f7589b`  
		Last Modified: Thu, 20 Nov 2025 20:03:49 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3c2c08cba475ab228ea58e07da8c9b77cc40f05e8de5bdd1f6e1ccf0dd3322`  
		Last Modified: Thu, 20 Nov 2025 20:03:51 GMT  
		Size: 11.9 MB (11896569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03026bb9f66e83f3b54a24a6be7c80b0ac943a515c69c0f3ac49e98a4810c9f`  
		Last Modified: Thu, 20 Nov 2025 20:03:49 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c1e6950820e677dfd9a8dd414f9eeff45b9bdd75ec03bfe0dc5e4ad8efb30c`  
		Last Modified: Thu, 20 Nov 2025 20:03:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb5c4f59cc36a7d934179cc11f6949a94dd94b660517ca388462045bf0a140`  
		Last Modified: Thu, 20 Nov 2025 20:03:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d5db169194f7e9d83cc0216578337242284a075a0b9d8811551f29263a4ed`  
		Last Modified: Thu, 20 Nov 2025 20:03:49 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c1e98ee6685ed85b0dd77e00546f44f98b298498f2dd288e1308a520a8e1a2`  
		Last Modified: Tue, 02 Dec 2025 01:14:56 GMT  
		Size: 26.4 MB (26414865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0faae0326e784eb8db9a1ecb532406c407d22696c9d60aadf9e63efe2507dfe5`  
		Last Modified: Tue, 02 Dec 2025 01:14:58 GMT  
		Size: 33.9 MB (33908993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d08d945cd4a9c03a187099c6400cd425eab4a95260764ce356d62290fc096`  
		Last Modified: Tue, 02 Dec 2025 01:14:54 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88b8314b2ff56ff8bc2ba4f9cf3a3d20ed989b89a3da3b60cd12e9be89076d`  
		Last Modified: Tue, 02 Dec 2025 01:14:55 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557e261985e0b81220e251463bfd2ca2a9d5963ed4a086fc84a4ce2bdd71395`  
		Last Modified: Tue, 02 Dec 2025 01:16:39 GMT  
		Size: 27.0 MB (27024642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccb9a388ef8583e10030b5c60e2d040d0bc58980caf02dd5657bb82d0f78188`  
		Last Modified: Tue, 02 Dec 2025 01:16:31 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c1a0b473114e0e302c6dff2b8aeda891ca8ccce0019e149fddcd3d5d984c23`  
		Last Modified: Tue, 02 Dec 2025 01:16:31 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace4b7776a5a28cff865e4f94085c050d4c5b0ecbf83fdde9a1261eed822dc6`  
		Last Modified: Tue, 02 Dec 2025 01:16:31 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:0ce5f478ef11096437dcf26c78506967970c473fc58eb5edde66100584deaf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8202915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d57879942cc1df6a3646a07ed67fb060bf926e780243852916feeff4e81b962`

```dockerfile
```

-	Layers:
	-	`sha256:bdf0dfc303f12ca7ae564599953db663eca01c0b5be1b59400577420d49eae53`  
		Last Modified: Tue, 02 Dec 2025 02:24:46 GMT  
		Size: 8.1 MB (8149609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c3e2ccfa83556283f8e297d4c9063d79514a13268299697f271aad086dd3ce`  
		Last Modified: Tue, 02 Dec 2025 02:24:47 GMT  
		Size: 53.3 KB (53306 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:c6e9f30774de40542756cb0c832b9cdcedfd5cc63198551d8a3344e71f1bf1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229168812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6171a96e987b209836f0aa30cb702999f5426f346374ad1959f364cbb6e09308`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 19:45:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 19:45:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 19:45:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 19:45:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:45:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:45:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:45:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:45:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:45:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:45:39 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:45:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:45:39 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:03:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 20:03:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:05:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:05:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:05:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:05:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:05:54 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:05:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:05:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:05:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:05:54 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:15:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:17:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:24 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:17:24 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:26 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:17:26 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:26 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:17:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:26 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:17:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f5dfa04175c1a79dec887ba469bf5abccb55128786394f215864622002661`  
		Last Modified: Thu, 20 Nov 2025 19:50:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696213cc4aa34828847dbe537e05c982c80e53783a26151abd9b6309a7a7e4c4`  
		Last Modified: Thu, 20 Nov 2025 19:50:20 GMT  
		Size: 94.9 MB (94874282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a055088953430a77e16c3c0d2fa58db0698987df6ad113dff27edee70550df`  
		Last Modified: Thu, 20 Nov 2025 19:49:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dec0247cea8417f906c5077b3a8c219c425148115d9fd6ab82e24fbbf09dad`  
		Last Modified: Thu, 20 Nov 2025 20:06:22 GMT  
		Size: 12.7 MB (12749075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c021300848fd726358d2f75fc1bcf4b94dc2f3b886c2b42ab89872fb38466c4e`  
		Last Modified: Thu, 20 Nov 2025 20:06:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2e4fd948e47a29414aa3db0277d1560bd1b2f417b6b5a04e8a99610cd4f4f7`  
		Last Modified: Thu, 20 Nov 2025 20:06:23 GMT  
		Size: 10.7 MB (10690086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e77b364d80b5536bfae32ac9209a7067acb5f677efec319cd1ebd5b5c20ffb`  
		Last Modified: Thu, 20 Nov 2025 20:06:22 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2dd371805ba8cffd3d2f57140ef5bee91eb5b6b91454b087b94dc8b374d310`  
		Last Modified: Thu, 20 Nov 2025 20:06:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bb4c7073e05f60f5311a0cc8552e93830c04bd5193bb484e5ed202ba3bb91b`  
		Last Modified: Thu, 20 Nov 2025 20:06:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dead7d8d5e9dbd2faf20e0d7240678e0a57cd85febf70920422cfc7305dc644`  
		Last Modified: Thu, 20 Nov 2025 20:06:23 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edce0d8a2e86fab01b65d1f4f9ea15190f1881094d40490f8bbfb89beeb88dd5`  
		Last Modified: Tue, 02 Dec 2025 01:18:04 GMT  
		Size: 25.8 MB (25836280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de4dfb13e080f02b4f1d58b41fa16c686e61e0879f65f1c56f83b47e6fd973`  
		Last Modified: Tue, 02 Dec 2025 01:18:04 GMT  
		Size: 30.0 MB (30032097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22674647f0131a03c8b05232bef2a95a075d262a973d0671783709df7e10ccec`  
		Last Modified: Tue, 02 Dec 2025 01:18:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d50ebc415a3bff74bf3f5eed21d645311e193ab07e4d81612c829ef31556f`  
		Last Modified: Tue, 02 Dec 2025 01:18:02 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb93de67b510dbaa8e18eca3126c9bff5dfcc4b52779bcb3d3f37a11200ca96`  
		Last Modified: Tue, 02 Dec 2025 01:18:05 GMT  
		Size: 27.0 MB (27024623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c9e94425d28a3632f6f2fd43b5df8daaf8ef46ff187da6961d2dea9982afb`  
		Last Modified: Tue, 02 Dec 2025 01:18:03 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f65bf9829c83f45cb606f10b2ecf76c0a3a5a72554dc655ca5d8f5cd59ea185`  
		Last Modified: Tue, 02 Dec 2025 01:18:03 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615760d95e40ecf773cc6078e5e9996729b70b26936106ec4f754af7e82f042f`  
		Last Modified: Tue, 02 Dec 2025 01:18:03 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:c97913405af96403b2164a4d8d489d72b1549f49c1d8cac4a1dd17956589ab6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8002102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e9f7a1cb3fdda630820d6a30c906066e012164ffc7e7846016594ae89306ed`

```dockerfile
```

-	Layers:
	-	`sha256:a26c582cecad586df49e8d9febecb7461cbd937b335afff24e79f51d12305fed`  
		Last Modified: Tue, 02 Dec 2025 02:24:53 GMT  
		Size: 7.9 MB (7948628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c039da3e1bc11f6b32972cd5c8d7ba945bb88a15f5c0e9eb60ea5709d723ec`  
		Last Modified: Tue, 02 Dec 2025 02:24:54 GMT  
		Size: 53.5 KB (53474 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:def696552ce2c9df18c14d55f6d527f0fd5776afbbfa349711991ec0669b4d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215659025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24965797931e4b006d16d84b156546e97e46d6cec815415846692e0d867b4dfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 20:14:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 20:14:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 20:14:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 20:14:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:14:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:14:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:14:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:14:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:14:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:14:52 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:14:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:14:52 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:15:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 20:15:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:17:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:17:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:17:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:17:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:17:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:17:38 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:17:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:17:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:17:38 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:17:38 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:19:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:21:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:21:27 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:21:27 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:21:28 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:21:28 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:21:28 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:21:28 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:21:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702d318691b1d05f56643ac48f4b0c5f136eea86c7b3d6079c0f08effff316c0`  
		Last Modified: Thu, 20 Nov 2025 21:04:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561e96aac34ee91dfa768455ceb63945b16277c87eab48665dd55a2dffbfdda5`  
		Last Modified: Thu, 20 Nov 2025 21:18:14 GMT  
		Size: 86.2 MB (86246300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce531f0d9809e2129eb61d0376214fb381014e6f6741f2eab74eab4fe455fbca`  
		Last Modified: Thu, 20 Nov 2025 21:04:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24331573eb3a0656e9abac2acd9b56bfb3b5ece70d0802bc9f8bbe62afc28e22`  
		Last Modified: Thu, 20 Nov 2025 21:17:53 GMT  
		Size: 12.7 MB (12749191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59f773e7a43cb7999f549096e38ac13b0bfbf0056f278c6ec70c043c0e207`  
		Last Modified: Thu, 20 Nov 2025 21:04:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1fbda1e379fa854a7ada51439c6a5559635ecf441d698e1c1fdc12a436a0b7`  
		Last Modified: Thu, 20 Nov 2025 21:17:53 GMT  
		Size: 10.1 MB (10077569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47917dec28cc08e0270738d6bad158ff5839909c7fc8e9b1fa8d52601d65bd86`  
		Last Modified: Thu, 20 Nov 2025 21:04:43 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966e6f1c46f43a9b455e5f8df16f6d7e70f62b12e90bd48ee13271f621960399`  
		Last Modified: Thu, 20 Nov 2025 21:04:43 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f337e462bdca88a356fdc1ef75fb6753a35f79fb31cb9c8d5601a4f437616f4`  
		Last Modified: Thu, 20 Nov 2025 21:04:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e3fa26df6766db67b64d5949b762576498b789fbd9d56f973ce7295bd512ea`  
		Last Modified: Thu, 20 Nov 2025 21:04:44 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa2ded6023d13adc682cc28cf7b01eaed94ef1e5433f8bff5dcbcd00b991d61`  
		Last Modified: Tue, 02 Dec 2025 01:22:08 GMT  
		Size: 25.2 MB (25159104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0808e7bb513814898a0f161455f8630d69d9ba9544bff429b469916769d5c1`  
		Last Modified: Tue, 02 Dec 2025 01:22:16 GMT  
		Size: 28.2 MB (28174028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c2a7ad9fa5bc4bc1067a7aacd79667a555b01be5419156c32455252bf056a0`  
		Last Modified: Tue, 02 Dec 2025 01:22:06 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec38285244276fff8b151125092159ad895f2e862f80a8fdb12c57d563e0a55`  
		Last Modified: Tue, 02 Dec 2025 01:22:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bd8c47150f6fe7388e30d761228b2d37a595423e776952e892887554a3f3bf`  
		Last Modified: Tue, 02 Dec 2025 01:22:10 GMT  
		Size: 27.0 MB (27024637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336e20f978075c117c19573292e97492c05131f8e15636dcc0e8464bb6f94cda`  
		Last Modified: Tue, 02 Dec 2025 01:22:07 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5a33e3dcf4b4811a05e0960fc540ab03d100a2e1bf91258d857a162dc10f1c`  
		Last Modified: Tue, 02 Dec 2025 01:22:07 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfcdb646bcc3fa601fae6b85be72934cba0764f4beb25c811141eac038a347c`  
		Last Modified: Tue, 02 Dec 2025 01:22:07 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:4bdaf75949e8f0ca4c66b564ffd5742285b253e43b62c48f51564a80d755fffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8006902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6ab4ccc15ecbbd58caa7757281447a1968f1568deed23ec81c70979c564277`

```dockerfile
```

-	Layers:
	-	`sha256:22bcab00ea3c57c5c45d911af909fef37de5d728c014f296285357c0ab8a7353`  
		Last Modified: Tue, 02 Dec 2025 02:25:01 GMT  
		Size: 8.0 MB (7953428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9358e716b957f0c6b74c93d7cdd473ff4d5f8cec5105759d30b4ca4441f287`  
		Last Modified: Tue, 02 Dec 2025 02:25:03 GMT  
		Size: 53.5 KB (53474 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:83c3a24466d9c04aa3c1c8a5ba7777adc76e12e3d385c5c663d1ca5fd0d6b783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258004708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d41cbbb6da1b165b83a35f8176ef6cdaa790e1b850c61f162b7b53a177d4d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 20:01:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 20:01:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 20:01:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 20:01:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:01:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:01:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:01:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:01:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:01:37 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:01:37 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:01:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:01:37 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:01:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 20:01:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:04:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:04:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:04:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:04:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:04:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:04:46 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:04:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:04:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:04:46 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:04:46 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:11:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:13:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:13:19 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:13:20 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:13:21 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:13:21 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:13:21 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:13:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:13:21 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:13:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29b1e871294ed257f00913f03dde53520c4d901bda4ae587318fd83b86bcd25`  
		Last Modified: Thu, 20 Nov 2025 20:05:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec3285e7ac800adb8bed751006a5d5d01d8c35d41e5c9b74ee75f40b383cc0`  
		Last Modified: Thu, 20 Nov 2025 20:05:59 GMT  
		Size: 116.1 MB (116138692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff692ae3944caeb0a92f929e2de47d04c1b8e8fc4f5447003ce92fddfacda427`  
		Last Modified: Thu, 20 Nov 2025 20:05:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eaae2587121480fab8242d4c660e986a8b511f187044f31c16d0cf5088b70e`  
		Last Modified: Thu, 20 Nov 2025 20:05:37 GMT  
		Size: 12.8 MB (12750458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc3efce988d1f79e015269e95d02b08d5a5df705bf2dffef02a34ae9a1a3f2`  
		Last Modified: Thu, 20 Nov 2025 20:05:35 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d68c11e538cba7c9540e49185c78f80923e9a4d0db7e8f46f581d1f1603a9d`  
		Last Modified: Thu, 20 Nov 2025 20:05:36 GMT  
		Size: 12.1 MB (12104229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6183f19fca3ad0a6afedefdb6da5f47fd01e724330f1e2361311d4b4da02e4`  
		Last Modified: Thu, 20 Nov 2025 20:05:35 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bced39d658e1dee298b69f318d5c74d568603bc1e574edaa871577ced3513`  
		Last Modified: Thu, 20 Nov 2025 20:05:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2f50cb33ae145b9a937bb71c2a735f93ab40d40ecbaaee992c5ee65410c731`  
		Last Modified: Thu, 20 Nov 2025 20:05:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c2771839b1449022a3ab4ffeac81540eece8135d43db211af1518c2f507b6`  
		Last Modified: Thu, 20 Nov 2025 20:05:35 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01e30cdb302e110273b4ae6788b9cd137a776a689161282d781d6a6e153ab27`  
		Last Modified: Tue, 02 Dec 2025 01:13:36 GMT  
		Size: 26.9 MB (26871154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b443acd78f2cdb1261f1a24d1b8e73d694cd4093c6a04f20500ec1d132da787`  
		Last Modified: Tue, 02 Dec 2025 01:13:37 GMT  
		Size: 31.8 MB (31804244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b4b35375df1eb0d0daa20bac7a26bbb4bcc82d068f2827017f8e705d5cd4c9`  
		Last Modified: Tue, 02 Dec 2025 02:07:42 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a94c4c29a014091848162d0c2a589f2a672a9de0ecfe446e91e07cdce79223`  
		Last Modified: Tue, 02 Dec 2025 02:07:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c3f34d830ef4b282ca7b192ae3372218cdf2b2df403bdda6de9da396c34d57`  
		Last Modified: Tue, 02 Dec 2025 01:13:37 GMT  
		Size: 27.0 MB (27024627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3074713c316ba1726d524253fc63502d8cc126c53362c7cd7db775b4ea3ed97`  
		Last Modified: Tue, 02 Dec 2025 02:07:45 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5411b63d0e60fc3927f8811613c81e61676d4a647929314ca6d438d8ebff0b1e`  
		Last Modified: Tue, 02 Dec 2025 02:07:42 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036461ce95eefa6541f39633333df6b942132d29d24703a29c39158fbb014a8b`  
		Last Modified: Tue, 02 Dec 2025 02:07:42 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:60e85ab16896cb143f562b91fa057502e4699b7c21c9b26b0d5faccd266d3254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4f53b0cbba182bdee043e39f29d32b9ca1b5a7db4f14c0088e9d888c2411f8`

```dockerfile
```

-	Layers:
	-	`sha256:836d9663030ee22d35ec1b6da2229d1b16c99cac9da906d338da1c4ab6d5b382`  
		Last Modified: Tue, 02 Dec 2025 02:25:16 GMT  
		Size: 8.1 MB (8122649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870d8ddf5ca5218f2c9594de30f35c03cb93d828a0c5884f1b8c02df9da7d2fc`  
		Last Modified: Tue, 02 Dec 2025 02:25:17 GMT  
		Size: 53.2 KB (53243 bytes)  
		MIME: application/vnd.in-toto+json
