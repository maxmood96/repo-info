## `friendica:rc-fpm-alpine`

```console
$ docker pull friendica@sha256:35ba5f112183fabdadf711e8606478a8cfd05a3763514de752a9fceaf3f7ff2c
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

### `friendica:rc-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:5a279462c34253d7f152255499f9c840d6568dddc6c9079547764db81a03f92b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57178396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95e1b20b3161045ddbea381b3b31ecea43681765243642f75bf693bde386d1f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.24
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8676d1ae0063d638eac9c97e4ec86a026a3be413c032dd87aa5ec8d591f7d66c`  
		Last Modified: Mon, 04 Aug 2025 20:55:11 GMT  
		Size: 3.5 MB (3460958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7517a1f9f0ada357d3f27e82cc284be112d116c6c83c1db14e2b42a99f18f03`  
		Last Modified: Mon, 04 Aug 2025 20:55:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd9c59c6bca882d81c6983bccd63195240b6ab0925495efc06840568d8076fb`  
		Last Modified: Mon, 04 Aug 2025 20:55:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf171cbdd7e97e736bd36d0d12574b14a98e88c2d78f448fc12cfdecac8cd5`  
		Last Modified: Mon, 04 Aug 2025 20:55:12 GMT  
		Size: 12.6 MB (12599869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf5121770cd58b72b09b93340177ca2f2e4d9d25760085106e7a9aefb5d7cf8`  
		Last Modified: Mon, 04 Aug 2025 20:55:10 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730e0e13e9223ee1dc5c0ffae5cd7c82167cea26f2aba7147de13f8d3ac93f13`  
		Last Modified: Mon, 04 Aug 2025 20:55:20 GMT  
		Size: 13.3 MB (13263435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8b4dd1c10742e1996193f24e190324bc387ebdca258f40f50ad5c6dfa49dd8`  
		Last Modified: Mon, 04 Aug 2025 20:55:10 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aacccbab11eeab39d8464dd6b2d7806445cfc11629e02958ff411cadda6b626`  
		Last Modified: Mon, 04 Aug 2025 20:55:10 GMT  
		Size: 20.0 KB (19955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5dea65d152dd93fb497c00e9777494871b36153d4c0915a438d4c003b3402e`  
		Last Modified: Mon, 04 Aug 2025 20:55:10 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7e25200874ac7bc5db66f13e344ba615d59d1afbae78332a54fc29cd735e28`  
		Last Modified: Mon, 04 Aug 2025 20:55:10 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ef288056b542c933eb7f24ca30ccc4687222339eb6ea1b80738184c98e686`  
		Last Modified: Mon, 04 Aug 2025 21:07:26 GMT  
		Size: 8.8 MB (8754622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5c1a32509e77d58ba609bebbfc4b7342f3da5a48b88d5c1b6bbdd1eb228ce`  
		Last Modified: Mon, 04 Aug 2025 21:07:17 GMT  
		Size: 1.0 MB (1031301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113fa3608a91aa7d86ff6301387a24fa39442e2185a835f2939ba9e75b59ee1b`  
		Last Modified: Mon, 04 Aug 2025 21:07:18 GMT  
		Size: 9.8 MB (9822767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c09f0259024b96d1b9776864afc14e9efd0bba52777f712c8c68b9f13f583`  
		Last Modified: Mon, 04 Aug 2025 21:07:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256adc80de8474b67661e73b4b43ea06c3ff6a3c3a08996f43652955ac8da691`  
		Last Modified: Mon, 04 Aug 2025 21:07:17 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71494553b4bb4cd2fb14e661b63d2d4ca909f4e61b0d0526161071b2fc00e606`  
		Last Modified: Mon, 04 Aug 2025 21:07:17 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1093d10aa20eb88181911411142ec4f617cc6d3c39fb18fdbeb8fe3dd75574`  
		Last Modified: Mon, 04 Aug 2025 21:07:18 GMT  
		Size: 4.4 MB (4386528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfc3d4386b6bbed46a75b9f5c5fb983c8bc22fad958939f0c4cbd31ba1b6f13`  
		Last Modified: Mon, 04 Aug 2025 21:07:18 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdd786cd0363acca15cf90dcdc59d197e659cdcdecb3ce2e45348385f126215`  
		Last Modified: Mon, 04 Aug 2025 21:07:18 GMT  
		Size: 917.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:32297d215d9c9d5c04adef6d666b975ff1ad4e9b1bb88f2cd066dc248c4644f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b34212ebb11d808ce5ac64ef6970a44f2b2c6a59616dabade4a1be77ccd160`

```dockerfile
```

-	Layers:
	-	`sha256:f7f0aed595c27345170a3cd4b26c71fa7f2e302c7c49efd26a929227f8a7e9df`  
		Last Modified: Mon, 04 Aug 2025 23:29:11 GMT  
		Size: 55.6 KB (55554 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:519f2e8d3d2f0e7c0dd9a1d074a10421ed6598203d3098508a9be54cf37e4200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54162987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433b50ba1a599b357789526c7916fd6944704c41ba469af916e77e8fd47a6327`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.24
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412aab248b23001939c46b31a1bd44af1cabed7294fb2e28a2d617a380aeb622`  
		Last Modified: Mon, 04 Aug 2025 22:06:29 GMT  
		Size: 12.6 MB (12599867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46a8da570857cb3459270b7874c27c4bf86e6484af5228a4b6934143323e722`  
		Last Modified: Mon, 04 Aug 2025 22:06:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295337c6456a1d764b61b396d4080ade0d041de6dec37b3ec695ee41fae57584`  
		Last Modified: Mon, 04 Aug 2025 22:12:15 GMT  
		Size: 12.0 MB (11982091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01084443a99185615578eccfc5961886914790eb58f136137ee4e1352e9419`  
		Last Modified: Mon, 04 Aug 2025 22:12:12 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed776ca2836f12a914deea1513754c7bcb674d6f9a3477ddd91a62a93c99edbf`  
		Last Modified: Mon, 04 Aug 2025 22:12:12 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4003e2485f49b6410dc2e8cf1b7b76f508398546b836ecd30175ccff4cd672`  
		Last Modified: Mon, 04 Aug 2025 22:12:12 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fcaa21c9f581fe9397d5dd0dd156cb60831d6373f148ecf611d73254f56a9f`  
		Last Modified: Mon, 04 Aug 2025 22:12:13 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e73c0fba6901eb0e738486c3d24b59195e609c77fe2fdc77627edccf0f16be3`  
		Last Modified: Mon, 04 Aug 2025 23:57:25 GMT  
		Size: 8.2 MB (8247526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5a3a43de26631723df629aaf21610b8df283acff075e37834a3c936126919d`  
		Last Modified: Mon, 04 Aug 2025 23:57:25 GMT  
		Size: 997.6 KB (997561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191e53f3e28d17f06004316754b5e191903096c88214a0ebe4cc0fb00ccb64ea`  
		Last Modified: Mon, 04 Aug 2025 23:57:26 GMT  
		Size: 9.0 MB (9011990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6d966d872b53477076c5dc309b8dd2618a5896ef94dd3a146722b2fa2511ae`  
		Last Modified: Mon, 04 Aug 2025 23:57:24 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3e7b6c7f7632e6fc045558a6fbc1b51b3472f8d5a4b597d00ae663d9209e95`  
		Last Modified: Mon, 04 Aug 2025 23:57:24 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88023f14b87269c0c971f00a9da9b63af8896ed66f75eb1a12373b47ef7ac64e`  
		Last Modified: Mon, 04 Aug 2025 23:57:25 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ad24fcb576775b8a48ad90bb343b5f87242da016390ab8eb8b5ab6b04c6b7`  
		Last Modified: Tue, 05 Aug 2025 02:28:47 GMT  
		Size: 4.3 MB (4342255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4c217bfe9bc96996594536a9c2cf25d02ee766d240b620cf37f8878b4eb2bb`  
		Last Modified: Tue, 05 Aug 2025 00:23:54 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff62900f62067ecccb02ae0914c45f6797d5128e3d52a26d19e61011b236ada`  
		Last Modified: Mon, 04 Aug 2025 23:57:53 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:1ae49e99f58a4183e69adac12fa35d1a24dca0ea8d92577e4b276bc5f15b5996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1b31dc97352f5f00b6f9d6f79f8c5237f845dea2db1c36b54ff4a1a3aa3edb`

```dockerfile
```

-	Layers:
	-	`sha256:9753eb9169519b4096d12d22aa31e2328f65ae4d4ed8ec875c24c3e046fe1786`  
		Last Modified: Tue, 05 Aug 2025 02:28:28 GMT  
		Size: 55.7 KB (55684 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:0c4aa2859a279877501284a86ee4df3cdf826d56a5332e96c0a797d592f561a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51880755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f68cbf8dd73ca407e2baff28cf03524c8ab70f1a7ff87bf8a1ad657c79fcaa0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.24
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba00dd2d5d8f6a44bf0a20885871d1853fc7167d84fb6ec957e7ac660ed1f49`  
		Last Modified: Tue, 05 Aug 2025 00:07:34 GMT  
		Size: 12.6 MB (12599855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01db466338552dbc3e51fab25cfb4c0a29f8cba308945ce14c23b2f3cc32a569`  
		Last Modified: Tue, 05 Aug 2025 00:07:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5e1050777a14bb79aae042037d3142cdf0379a6fa13e1bbd464536acaab1c4`  
		Last Modified: Tue, 05 Aug 2025 00:11:30 GMT  
		Size: 11.3 MB (11287235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3533ff91d2cbf4b64276ed59a40895b09a8dcd8196b65d19578e2c5fb49878e1`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b0618cc8e7a0c9625469ed1f03151d3a30be85350383e190f2611267e11ce7`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 19.7 KB (19725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c93fa35098206749c593cfd31020dd3187b539cb278056d4b68f8a7abd3312`  
		Last Modified: Tue, 05 Aug 2025 00:11:29 GMT  
		Size: 19.7 KB (19717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c160173b8f73a178b3ac82cfd72acbd558dba08c5a7ed38426a8a9e6eb839f`  
		Last Modified: Tue, 05 Aug 2025 00:11:30 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffa9d63191b24247ab7a0db413ccb068c404ca08e5ccd6644a3b373f94ab080`  
		Last Modified: Tue, 05 Aug 2025 03:06:19 GMT  
		Size: 7.6 MB (7622070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99433156ca31ba342885d3ecf1f1cff66cd137895e3f19b1f7366c61ce9c429`  
		Last Modified: Tue, 05 Aug 2025 03:06:18 GMT  
		Size: 997.5 KB (997529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538185d10b33110b62a9583eb2ae6b76422ee9dafad24dd01f21665fe6e82b72`  
		Last Modified: Tue, 05 Aug 2025 03:06:21 GMT  
		Size: 8.9 MB (8907185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6acd1a2134a02f4013e82f8053ddd7874bdbfc8765238bd8854c32b8ef0006`  
		Last Modified: Tue, 05 Aug 2025 03:06:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc14a768da2d085e16754180a6bba20bafc8f3a6ad8af7f03eab04e8fc61657`  
		Last Modified: Tue, 05 Aug 2025 03:06:19 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c7cd2dd6281da646d752db779ca5937652d8895c74361fb98bc8b5ade0da2d`  
		Last Modified: Tue, 05 Aug 2025 03:06:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9f06c93faa4d8568b7407b4e379a50b578362cf9c43dbbaa703b948324988f`  
		Last Modified: Tue, 05 Aug 2025 03:08:14 GMT  
		Size: 3.9 MB (3948182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac6c115004be839d43879b18d0bada9eb8c617a2174b32e19cc285ad82b0eb`  
		Last Modified: Tue, 05 Aug 2025 03:08:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957cc197a70898f7b85371a3928c1d107a491efc0f677a0bc7aeba39568bba02`  
		Last Modified: Tue, 05 Aug 2025 03:08:14 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:0ad1a5a725b0d76a82b092116a2560918ee2f2dd438a2335434ffa3501c217f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a8d769abd8752bf15e91786ab590d7ea82ed3b8381adda683f7a7107d1a5e8`

```dockerfile
```

-	Layers:
	-	`sha256:506a5a5b039b76b7a9ff6118ba01a6c8a4149c751551f71d07e8179bcbe7cb3d`  
		Last Modified: Tue, 05 Aug 2025 05:29:34 GMT  
		Size: 55.7 KB (55683 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:d0b84dc7f2dcf24a6fd145b9c5a1410a70285e54b6a104906485fc635135dd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57436433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbc22ff5a860414ae1020fb06b8868aeaf904f50ec64e404d98851c31c42389`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.24
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c312f75964337f4db7770ce494c065e1775810a79a6ad25cc8846d1924eb8`  
		Last Modified: Tue, 05 Aug 2025 02:40:12 GMT  
		Size: 12.6 MB (12599871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3179efae18545d01b9663211a16a1cae37ca72749953364336d472c4e81e2f`  
		Last Modified: Tue, 05 Aug 2025 02:40:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e3af117145aa9db60dbdb547182b06888346793df58c20cf6ed3d58f79499`  
		Last Modified: Tue, 05 Aug 2025 02:45:31 GMT  
		Size: 13.2 MB (13249851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71127f1e5a0d78107b15f785398d341b771fdb0179d1132baacf28602dbaafd6`  
		Last Modified: Tue, 05 Aug 2025 02:45:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024bb4e36e07326dda259a05227cadf8e5e26b6fc8e6ff2c756423e75f55a5f2`  
		Last Modified: Tue, 05 Aug 2025 02:45:30 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110b4929c8b1443c6afd235ecbc59b4a2d6797414a06ba0cc2a541b0e7be8ba`  
		Last Modified: Tue, 05 Aug 2025 02:45:39 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaddacb01d48656b98dbc057e2387016c89d834cabaf74099ed0fdaa5ef89dc7`  
		Last Modified: Tue, 05 Aug 2025 02:45:29 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ff731ab8cb8d7a3d365a369d8cb7da11d1392a23fe74612619d0c08cb7afe`  
		Last Modified: Tue, 05 Aug 2025 08:53:11 GMT  
		Size: 8.6 MB (8625520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d5ecbc0c0cb6fb430aafa68a317da918e49064c6590b1d753b91d6884208f9`  
		Last Modified: Tue, 05 Aug 2025 08:53:11 GMT  
		Size: 960.8 KB (960821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1f24baea3d811c1f25a52ce5d56eb47f09e98e12da4c30d93c72d9a2781807`  
		Last Modified: Tue, 05 Aug 2025 08:53:12 GMT  
		Size: 10.0 MB (10025402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab8ae76772670db4ab721cab6593000ce5568c4924c7823e3075f0d6198005`  
		Last Modified: Tue, 05 Aug 2025 08:53:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b0f81a11b61b228b34fd7b07d9c4a8ebcf4658a3e0619b8ff5db1a9d6bd082`  
		Last Modified: Tue, 05 Aug 2025 08:53:12 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1455e8499394ef8075d51a620ebba25fa233dbc4a14d3ae0eac8ae16897eb541`  
		Last Modified: Tue, 05 Aug 2025 08:53:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466d336394427d1bce78349ea925c352c7b2e6702880fcb42953f0d15d0c2642`  
		Last Modified: Tue, 05 Aug 2025 08:53:12 GMT  
		Size: 4.3 MB (4330650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d82a559e1c2f8fbd321f6e12873aab22c88b7885276082bd24701529fea76`  
		Last Modified: Tue, 05 Aug 2025 08:53:12 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf6212497d5bb15b6943cf32f419fe91ac57f36e13a016f067f2d32187077cb`  
		Last Modified: Tue, 05 Aug 2025 08:53:12 GMT  
		Size: 918.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:e82a7b038f7dc1298015cca086f3851d0ad3e02b941fec6478cc728c1bea8ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 KB (55722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b696b794028cfe405d5134be0fa0d4c94fb73c1d7cc73525b70beeb6960e674`

```dockerfile
```

-	Layers:
	-	`sha256:febbf26610d396c13ecdaa5eddda3840a6f6f6ee93108611aef43d0d31714567`  
		Last Modified: Tue, 05 Aug 2025 11:28:41 GMT  
		Size: 55.7 KB (55722 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:284babd1b754664e258b8c418e8340a718ced80565c0b7c4096a187ec9b112f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57552679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb71df10423b36de35ea241ed7fbec87bdc3de972d45ec2eb55bd63d4f4929c4`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.24
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcbfc2a782133fe0f4c54292a79a01c7917399beeac35006d41667f1540a905`  
		Last Modified: Mon, 04 Aug 2025 20:55:37 GMT  
		Size: 3.5 MB (3516271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368a06896d30a81d370337cf5cf502f0dcf2f11ffa15dcf0644b81190a3ff19`  
		Last Modified: Mon, 04 Aug 2025 20:55:35 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772eb47d0120ba422d740c36a7d296af8496d516dbb682a97a6d34069a541e16`  
		Last Modified: Mon, 04 Aug 2025 20:55:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d9db780aa910616923ab27a4a731f68eff869a436a37b2773306c09f7c4801`  
		Last Modified: Mon, 04 Aug 2025 20:55:39 GMT  
		Size: 12.6 MB (12599872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd01eb99bfb7bf951d7fb852783c2723bdeb571c6bfd47b442ed43aa0d75040e`  
		Last Modified: Mon, 04 Aug 2025 20:55:35 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fce29546c0b8766546dae99257960231b8123dc6b24f8ebfbdcf848feb69e4`  
		Last Modified: Mon, 04 Aug 2025 20:55:38 GMT  
		Size: 13.6 MB (13574277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6f548079258132fb8fb18e5ddb0b54c55bcb199c02bfce1d4d46ee0680ded4`  
		Last Modified: Mon, 04 Aug 2025 20:55:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027f1ffa0ad01d1be12e89112fe7a33ad7f0fc5ba9ec67ce97166522c9876f47`  
		Last Modified: Mon, 04 Aug 2025 20:55:37 GMT  
		Size: 19.9 KB (19930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f070aecbd589bb80bcb59fcf5d05865b376897146f878dc33dfe5f167866fd`  
		Last Modified: Mon, 04 Aug 2025 20:55:36 GMT  
		Size: 19.9 KB (19931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f6dd209b019814b430a67ab4b09728f93214ab509e17945129919c4eba888`  
		Last Modified: Mon, 04 Aug 2025 20:55:36 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddff3e391ca6553310578f4e99f9e708c5ecbb14cc817f7ad9e42f0305f28b5`  
		Last Modified: Mon, 04 Aug 2025 21:16:29 GMT  
		Size: 8.8 MB (8834885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c7c49dcb53165e2b532838571e9fd27061de87bdb3bcad4998e53e5b278dfd`  
		Last Modified: Mon, 04 Aug 2025 21:16:28 GMT  
		Size: 1.0 MB (1006356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e968eee911f39ec7087fdc2a07ed25cea24f1242f817fa369d510defde82fbf`  
		Last Modified: Mon, 04 Aug 2025 21:16:29 GMT  
		Size: 10.0 MB (10000957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e852212afb617cf182c5f2b51bfa4bccc54d344294172f6c46120cfce16b8e2e`  
		Last Modified: Mon, 04 Aug 2025 21:16:28 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41710cdf3694ce61e37a392885971cf28775884a4c0232893503e8772b74227f`  
		Last Modified: Mon, 04 Aug 2025 21:16:28 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa655cbde0b4d3bcf4ba035a9d9b8117de9168451fb62a62c2edd9042c960c62`  
		Last Modified: Mon, 04 Aug 2025 21:16:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef681fef0998805d3ec8f674884ef8e95c6fb5f3ea1dde489c363fadd09004e0`  
		Last Modified: Mon, 04 Aug 2025 21:16:29 GMT  
		Size: 4.3 MB (4345875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9375ef73d3178eea28b7c0f017f6345f428700e1c0eb9b40c8e7c3d34259a0e`  
		Last Modified: Mon, 04 Aug 2025 21:16:28 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3974c56579629ec5e054ca3f24e360941cb225a4e8c6b958e4b94f0d1e4624`  
		Last Modified: Mon, 04 Aug 2025 21:16:33 GMT  
		Size: 917.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:7e7ee1cba32057c5e31a05d9dcee36356a82a8caeece6f941ca493ebf1206730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e5152e971937377c7041f22e4edbacdea33952455c52110c502ec5c6bd13d4`

```dockerfile
```

-	Layers:
	-	`sha256:634dd917557c70953bb4627f49c23edd6bfdc967ecc66119bc9f57d70ebaa3d3`  
		Last Modified: Mon, 04 Aug 2025 23:29:26 GMT  
		Size: 55.5 KB (55527 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:5b13261422e66c72e3eb3dd3306981fcd6ff74cfb5a5014c1adcd2b1b1cd8c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58133885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17a72ac66f0c7cc6dc1269b29424e492946cf1a4242598fb7bdf9dfa6e2452b`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.24
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7afea3ff1a55cd1792a8e64481f14518dfcb576dfa3d19bf97e598dc725a314`  
		Last Modified: Tue, 05 Aug 2025 01:24:26 GMT  
		Size: 12.6 MB (12599881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce8edbb87bbd2dae7350f982fef8786dab63c95b1cdcaa6447b211ea5dd6d6`  
		Last Modified: Tue, 05 Aug 2025 01:24:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345e094929378315708a186dd96aec526fcce0b74800d7da428c1fc526a69f7c`  
		Last Modified: Tue, 05 Aug 2025 01:27:58 GMT  
		Size: 13.7 MB (13733436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67a689b009152557ab3f5e3109a568cd2181e27a9a8880e5f8424106b5647af`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e438da494fff08dd7155b6f3c5929f50cfe9230d3084485a2d94bfbb89b11ec2`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 19.7 KB (19738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965b1a291960272c429bc9fd3e8ad7ffeda0dbceea98e9de56c1679d92ab972f`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecad038c628b170712953ffd695fd9e7205f2b61a0cd789750a5a06c2f96ba4e`  
		Last Modified: Tue, 05 Aug 2025 01:27:54 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd8574486b6a630d88b0aa33eef51e5e3f838d7b93879a460720112e3f6228`  
		Last Modified: Tue, 05 Aug 2025 06:00:28 GMT  
		Size: 9.2 MB (9190951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a9a638116aa564882593509d9aab1fab395b73de679292e53b6ca47569cc33`  
		Last Modified: Tue, 05 Aug 2025 06:00:27 GMT  
		Size: 951.1 KB (951091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd536a6ec05054aaa0773d0264d53bbb09589cb99d35c0e712d9f85bd950c1b`  
		Last Modified: Tue, 05 Aug 2025 06:00:28 GMT  
		Size: 9.8 MB (9822741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761ae22e3fa09b44a23a95c934b0ae257ee4596e822a0ccd64b493ea9a0cffd9`  
		Last Modified: Tue, 05 Aug 2025 06:00:27 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082d99915eed7a9ecb6c378ad74fc2c03534d83e71342d73a2a3b1be63c0dd31`  
		Last Modified: Tue, 05 Aug 2025 06:00:27 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab81012892483aa6f7edd85777c548cb1b5b7642084f85966ed85533366b38e`  
		Last Modified: Tue, 05 Aug 2025 06:00:27 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747db5e5a853b83710ff03bada91a67fb601caf62a2fec39757a547268c14f74`  
		Last Modified: Tue, 05 Aug 2025 06:00:28 GMT  
		Size: 4.4 MB (4438710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ac6e91e36bbf648708cedb34a2097ea1d2531c979c3782968b71ab687ca1e5`  
		Last Modified: Tue, 05 Aug 2025 06:00:26 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3cab295a11df1d0b21387f9ba65377604d5b872f443ce684170e70ca72554c`  
		Last Modified: Tue, 05 Aug 2025 06:00:27 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:a474b042b15721f9176c76478341b0bece61fbbf03521b17da033ee3939ae602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9f95f9cbb93a8577d1b4dbe78d5dd94a6c4141d1d721d97c90e4bac38e13c0`

```dockerfile
```

-	Layers:
	-	`sha256:90d0cf6cd631a3cf2905ed2f3c2b5cbe1965596fcb17e939fb780ae363055040`  
		Last Modified: Tue, 05 Aug 2025 08:29:14 GMT  
		Size: 55.6 KB (55590 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; riscv64

```console
$ docker pull friendica@sha256:808ac5747a6f57630d889eb0e8090c5e5a31dba927b0537c6acf51b0aabf16c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55724184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e192e37d97f62bd4aeb3042e244a83ca70a9f2fca3563f66af2e9a4ecb1c027`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.24
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a201b0a16aadc2a7c27ca0b373c85630463930fde99bd3c73f103ab676945d2`  
		Last Modified: Tue, 05 Aug 2025 12:57:01 GMT  
		Size: 12.6 MB (12599871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24220ce5963ab886efe9c3b3f66ba547029509a02a6800ed1f96dd054b509f70`  
		Last Modified: Tue, 05 Aug 2025 12:57:00 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f524b7a4013d49f1672e3def14da703786da1c7f1e3bfd8287705fa4b7f7d9`  
		Last Modified: Tue, 05 Aug 2025 13:51:36 GMT  
		Size: 12.8 MB (12760936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b19de0d3435de422114fee898a6b066f70ee28ecfd5f589638e2dd921f1b9e2`  
		Last Modified: Tue, 05 Aug 2025 13:51:38 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7e96cf40ae551ebddd54c87ea502aef0be1094aafd9756757f0938d43bc2d6`  
		Last Modified: Tue, 05 Aug 2025 13:51:35 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fe0ec7d18971f49b97f267bc624a19192d37ac9a1a0211e5465c4fad6d585d`  
		Last Modified: Tue, 05 Aug 2025 13:51:35 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f97d9049337329d8dd279f3212dfcc82651729e891bcffe27adcdcbebd199c`  
		Last Modified: Tue, 05 Aug 2025 13:51:37 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b27faf9a8f50f0e926ac0bd81d738396b9cdd7db008fb954caa038df57ce5c`  
		Last Modified: Wed, 06 Aug 2025 09:44:18 GMT  
		Size: 8.5 MB (8543807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861e14b153409154238d4ad4eae8c21de38c9716ceb62b22d9a6f80cf3c811bc`  
		Last Modified: Wed, 06 Aug 2025 09:44:17 GMT  
		Size: 1000.7 KB (1000654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c3a0d5717db25f11f873601c2bb117d4f5d48ab70b57367dd7b352babfda88`  
		Last Modified: Wed, 06 Aug 2025 09:44:19 GMT  
		Size: 9.3 MB (9251501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb9fcc63e284e7af6a3c4aa6291aacccc6b95c5bd81133274ed83c832e141e0`  
		Last Modified: Wed, 06 Aug 2025 09:44:18 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5583ee057a1890ae6e917fed1d8f5e955e15ded8e1e32a0ae1dfc73bea33578`  
		Last Modified: Wed, 06 Aug 2025 09:44:18 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcba5a72cf3bcfbee893460e2d5b9061d3c18f1f84ff85ed2ca85a7597cc45b`  
		Last Modified: Wed, 06 Aug 2025 09:44:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d125a80d75769965dc03ab9204f7068a1a254072deed1e43ca451368fd8ead`  
		Last Modified: Wed, 06 Aug 2025 09:46:08 GMT  
		Size: 4.4 MB (4401624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda70c8fdfde573a4fec38c6281a53418fc1cf548573ddd00e8b47e27017531e`  
		Last Modified: Wed, 06 Aug 2025 09:46:07 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fb5afa08193937959845f495cc9e424b0ef29a4ef1061e9f2d7b55b7fd73c1`  
		Last Modified: Wed, 06 Aug 2025 09:46:08 GMT  
		Size: 920.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:943b866c8bf62204bd32358f5112511c51138d5006d0b4d959fa80520c74cf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 KB (55598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c897a5f7e82690224a44c27b95111724c9acdd10a2276fd52f7897b329dbe48b`

```dockerfile
```

-	Layers:
	-	`sha256:6a1830b165ab80767252d870531554a023b33ce25b6e0aaffe438879e9cf9502`  
		Last Modified: Wed, 06 Aug 2025 11:28:00 GMT  
		Size: 55.6 KB (55598 bytes)  
		MIME: application/vnd.in-toto+json

### `friendica:rc-fpm-alpine` - linux; s390x

```console
$ docker pull friendica@sha256:bfa1b0604c8d079cf870be067f1fe13b89fc6326441bc903214fc325ee7326ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57454974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becc0691f27f878013cbdc5481d957d5abc5769450ff07fa09df2355f8c57e58`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 26 Jun 2025 02:21:47 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 26 Jun 2025 02:21:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_VERSION=8.3.24
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.24.tar.xz.asc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_SHA256=388ee5fd111097e97bae439bff46aec4ea27f816d3f0c2cb5490a41410d44251
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Jun 2025 02:21:47 GMT
WORKDIR /var/www/html
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Jun 2025 02:21:47 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache         rsync         imagemagick         msmtp         shadow         tini; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp         intl     ;         pecl install APCu-5.1.24;     pecl install memcached-3.3.0;     pecl install redis-6.2.0;     pecl install imagick-3.8.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=60';         echo 'opcache.jit=tracing';         echo 'opcache.jit_buffer_size=32M';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;     ln -s /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     echo access.format = '"%{REMOTE_ADDR}e - %u %t \"%m %r\" %s"' >> /usr/local/etc/php-fpm.d/docker.conf; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     mkdir -p -m 775 /var/www/data;     chown -R www-data:www-data /var/www/data # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/html]
# Thu, 26 Jun 2025 02:21:47 GMT
VOLUME [/var/www/data]
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_VERSION=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
ENV FRIENDICA_ADDONS=2025.07-rc
# Thu, 26 Jun 2025 02:21:47 GMT
RUN set -ex;     apk add --no-cache --virtual .fetch-deps       gnupg     ; # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY *.sh upgrade.exclude / # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
COPY config/* /usr/src/friendica/config/ # buildkit
# Thu, 26 Jun 2025 02:21:47 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 Jun 2025 02:21:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2523afe7bac87b158b525d19c04b257f3c07e08691519ce8330dd437653643c2`  
		Last Modified: Mon, 04 Aug 2025 23:37:17 GMT  
		Size: 12.6 MB (12599878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78df3cd97ddbf126a4a6dfd5bf63960fc6ccf9adfdb9aa202edcc51b19c13c2`  
		Last Modified: Mon, 04 Aug 2025 23:37:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851854bea31942fe2c53199a441ecdcdab06a3e076fe408512317e67f5b4a771`  
		Last Modified: Mon, 04 Aug 2025 23:41:14 GMT  
		Size: 13.2 MB (13210677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b8257fc0b983043ce66078653ca13abb7f9a5fc1ab5a2c0c153f5a15001dd3`  
		Last Modified: Mon, 04 Aug 2025 23:41:12 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3938a4241c29aafc2b6a7e97e8b4850970dd6104375af53a1e3ed200d5eec5a`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78755911dfc20b138109d2303255ac2c16fb7ded0a53fe627fc8a508dbe07e8e`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f0c15c5819db3959fbf66a1cba899ae66e9869e1113c660149c00934a42fbe`  
		Last Modified: Mon, 04 Aug 2025 23:41:13 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc398be8f11d7a8b5866a8f767c500430dd6f11630362fdc0bbb78eb30f1fd38`  
		Last Modified: Tue, 05 Aug 2025 03:31:46 GMT  
		Size: 8.9 MB (8907261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c425ca812eaafb33d732ef7861324c19c288539ad1ea5001c1a7ff7d218682f2`  
		Last Modified: Tue, 05 Aug 2025 03:31:45 GMT  
		Size: 995.2 KB (995239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a59522c16225ede0d9aacf58158a1f7569f4440c1ee23f388156f3c00c2c369`  
		Last Modified: Tue, 05 Aug 2025 03:31:48 GMT  
		Size: 9.8 MB (9759955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890ac3fa2df5605a1e2000487d28032c10b7e99f09ff23d5a44abb2e005e284a`  
		Last Modified: Tue, 05 Aug 2025 03:31:44 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04522ff55f713cc840afae7de836120619db848fa8eb3c25a1a75ed9007d5bdd`  
		Last Modified: Tue, 05 Aug 2025 03:31:44 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a980551482458e356f229d1bdebd92b3541c2e8a671e210368fa9bfda9e66836`  
		Last Modified: Tue, 05 Aug 2025 03:31:44 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3225ffe3a9300f3162f68fc876a1ffc17c786752eaf3700d097d98f05bd53a`  
		Last Modified: Tue, 05 Aug 2025 03:31:46 GMT  
		Size: 4.6 MB (4598335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02a209de7ef34cd90af6d5313ba069254f1cbbefede6a69d9be98672248cdf0`  
		Last Modified: Tue, 05 Aug 2025 03:31:45 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae60e0398c35bf2cebf34c2573bd921b4cec5ab6ccbe167d157686e2b44e4ec`  
		Last Modified: Tue, 05 Aug 2025 03:31:44 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `friendica:rc-fpm-alpine` - unknown; unknown

```console
$ docker pull friendica@sha256:6d665835fc5b361fa88fde97af050767efebd6319330037f1d6e2767d1e80390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 KB (55545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5ced8050df1db4d0f09a8469f03e1e7891ca339c4e2a70a917e60f1865517b`

```dockerfile
```

-	Layers:
	-	`sha256:723f8cb5cda63ca717afa83caf65012a1987797ac7dff440858faed69276fe2b`  
		Last Modified: Tue, 05 Aug 2025 05:29:44 GMT  
		Size: 55.5 KB (55545 bytes)  
		MIME: application/vnd.in-toto+json
