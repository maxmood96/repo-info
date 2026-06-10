## `mediawiki:stable-fpm-alpine`

```console
$ docker pull mediawiki@sha256:43f618a0cfe2a45788de95b4ff0ee1ae9e21c8d0282bc3426b1e48941a685ed7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `mediawiki:stable-fpm-alpine` - linux; amd64

```console
$ docker pull mediawiki@sha256:41167725ddcbbb6d848e1b7934dda10afeda04401f73751a316081c19a57aba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151323681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89b2a91d21be782bdb6b810c172e35489fc42f4bfa527a28a77d9f6e758eae8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:54:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:54:59 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:54:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:54:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:54:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:54:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:54:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:54:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:54:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 10 Jun 2026 20:54:59 GMT
ENV PHP_VERSION=8.3.31
# Wed, 10 Jun 2026 20:54:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 10 Jun 2026 20:54:59 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 10 Jun 2026 20:55:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:55:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:57:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:57:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 20:57:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:57:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:57:53 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 20:57:53 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 20:57:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 20:57:53 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 20:57:53 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:16:56 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Wed, 10 Jun 2026 21:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 21:18:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 21:18:08 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 10 Jun 2026 21:18:20 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Wed, 10 Jun 2026 21:18:20 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Wed, 10 Jun 2026 21:18:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:18:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec32276f514c7e39bb42907f40a521c4e006601a9e5afb5ecd3f6a04a230189`  
		Last Modified: Wed, 10 Jun 2026 20:58:00 GMT  
		Size: 6.0 MB (5975994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5c83316eae9f0de618afa33d62ff00703e4792b8dcd9dc9b2d3aaa01ef8ea3`  
		Last Modified: Wed, 10 Jun 2026 20:57:59 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737e33fd4f8579da776fcfd6a62cf37570707efbdf6aff9191962bd499c4664a`  
		Last Modified: Wed, 10 Jun 2026 20:58:00 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdbac2ab6b7187aec9ed90039cde785485d7326c20f95bb5c1a51ed18de0538`  
		Last Modified: Wed, 10 Jun 2026 20:58:00 GMT  
		Size: 12.6 MB (12627105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd98fea5ce10eb98c8650a5347e3122cb66eb2e410f257f781915719ead0e5d`  
		Last Modified: Wed, 10 Jun 2026 20:58:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb62ad979968b827554c2ade46a7caacd31868af1a2b1536be51e9b993b54c`  
		Last Modified: Wed, 10 Jun 2026 20:58:01 GMT  
		Size: 13.4 MB (13417858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b5be1aeba23ca22b57658b365ae31bc5d695bd5b2bfe5cfa3786c47286a96b`  
		Last Modified: Wed, 10 Jun 2026 20:58:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e572fdb9db1e36011acd40535cb668db3511e4740b322603b9bb8b67f319485`  
		Last Modified: Wed, 10 Jun 2026 20:58:02 GMT  
		Size: 23.2 KB (23248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69796231b084c6504faa422c90d8fbb1a40268837f252e7dbda975a6369a14ef`  
		Last Modified: Wed, 10 Jun 2026 20:58:02 GMT  
		Size: 23.3 KB (23256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e452f1c2bc4de03f651d647e5fa79f4f4f5116cf2b76d243244cb315e6363f46`  
		Last Modified: Wed, 10 Jun 2026 20:58:03 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb45c478ac210ca2812d3a33a0d070bb261c6c4e39cdb6ded4d61293bd4e9916`  
		Last Modified: Wed, 10 Jun 2026 21:18:37 GMT  
		Size: 27.5 MB (27541229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990dfce81d204a16cd3979f4141bf4c8878197b007b267f739baae56c29b34a7`  
		Last Modified: Wed, 10 Jun 2026 21:18:37 GMT  
		Size: 5.1 MB (5133445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41ceba98ac1e44d958e757a9c422f98bd87fb7c61fa4c07ad6d7246342fb67e`  
		Last Modified: Wed, 10 Jun 2026 21:18:36 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba5620c042136440c76577b67cfa73b4a90b1702a6a2ddeff8f9296bf0d7d99`  
		Last Modified: Wed, 10 Jun 2026 21:18:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65529be8a92dc48b0c00be9115a01cc348a663634ba6084ec1beb52e0a540862`  
		Last Modified: Wed, 10 Jun 2026 21:18:40 GMT  
		Size: 82.7 MB (82700958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:6feb1602ac9e60ce37c4bd503787664d1dfddce2c7c159def4013eb282e0e87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 KB (33118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7a63526f8bb7a4e6ea690ed0482201e335696e418c98903db714361c67bcf0`

```dockerfile
```

-	Layers:
	-	`sha256:551653ae9b227ea14643134a1c97cb1163b92b8919daf051dbf6a4fc1d8d789b`  
		Last Modified: Wed, 10 Jun 2026 21:18:36 GMT  
		Size: 33.1 KB (33118 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; arm variant v6

```console
$ docker pull mediawiki@sha256:e84e06b80fc1e35fc45e2e6ef2ff2329a988d615f91ec785b7ec4c3a7d2a51d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147985693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5602c5f44db6e516bf18e1d551affbe1d1e456e6c15c4c424f3e00de729393`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:51:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:51:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:51:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:51:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:51:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:51:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:51:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:51:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:51:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 10 Jun 2026 20:51:32 GMT
ENV PHP_VERSION=8.3.31
# Wed, 10 Jun 2026 20:51:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 10 Jun 2026 20:51:32 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 10 Jun 2026 20:51:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:51:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:54:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:54:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:54:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 20:54:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:54:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:54:16 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 20:54:16 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 20:54:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 20:54:16 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 20:54:16 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:38:17 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Wed, 10 Jun 2026 21:39:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 21:39:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 21:39:47 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 10 Jun 2026 21:40:00 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Wed, 10 Jun 2026 21:40:00 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Wed, 10 Jun 2026 21:40:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:40:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5387cf4f353a8a69ee0d5a46eb61b1d4aea2b2cba7fbf321ef716ea0476859f6`  
		Last Modified: Wed, 10 Jun 2026 20:54:21 GMT  
		Size: 5.6 MB (5569118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f1a8813e3f14c4dc26f00eeaf0520fc30b01c2097e23f29b04ea572f3fa1aa`  
		Last Modified: Wed, 10 Jun 2026 20:54:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137ca99d770c366396b3816a987874434afce7fe38cdd70a15e0f9ad79daf159`  
		Last Modified: Wed, 10 Jun 2026 20:54:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303ede8d8c6201cc33a09156c9dc8c0550d82c51870c6ef6052b7d1f57eac064`  
		Last Modified: Wed, 10 Jun 2026 20:54:21 GMT  
		Size: 12.6 MB (12627123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de69ad511f40abf159a33ca5e2a80ecb2adbdaf559fba9d00e2421c8508e317b`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbbb7c146164df9d977a10998e3c5040d327845ce78de97d912ff5ae610e688`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 12.2 MB (12160697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbb6847119afb2d1eff7cfe80232506388f7c702a3857bf46d6419ce6556a3b`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b50176c223a5ea39fe4062fbc6e6bbb94d263017a08941b16d36616001ad20`  
		Last Modified: Wed, 10 Jun 2026 20:54:22 GMT  
		Size: 23.1 KB (23061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bcbb7a53fa98a361c1f5d14bed06607416ed7bc8ed25d99620a3de8263082c`  
		Last Modified: Wed, 10 Jun 2026 20:54:23 GMT  
		Size: 23.1 KB (23074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41669de66fcc3949886500b9187c6bd60fdb6d7010417dceb6d902a19c44e52d`  
		Last Modified: Wed, 10 Jun 2026 20:54:23 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bd1510437952eb8a9794a022887a05cd18a4d807e4bff7c940d552bd7206e0`  
		Last Modified: Wed, 10 Jun 2026 21:40:17 GMT  
		Size: 26.7 MB (26670057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f29db1bf7edbc86acfed3076f253ac1683b1186b13f0d6b8aa050cb1373d95d`  
		Last Modified: Wed, 10 Jun 2026 21:40:16 GMT  
		Size: 4.6 MB (4622216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68e261feeb404c5ea3ec78be9d3b3aee873e13d8506ae99b988ebcc2a7970ad`  
		Last Modified: Wed, 10 Jun 2026 21:40:16 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac5e69000114fb48ce9358530416d01a3997084da63d01068dbd1a3f60274b8`  
		Last Modified: Wed, 10 Jun 2026 21:40:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eef2edfc14b1078b84cf8cc16b687e5abf97d062659bb8d704a953278adfd2`  
		Last Modified: Wed, 10 Jun 2026 21:40:19 GMT  
		Size: 82.7 MB (82701200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:d5ac53daef94493fb4d6ac9d5f41205ba43f2ab39461165b7213b8b66895600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308c22d8d9ab72034db93933a09e9c10489c3c31baeae0c0dd535231aeeedd1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ef3794b0f81606e08cb267cabcf24a0fc29cf0baaa9829cf415058827f227c7`  
		Last Modified: Wed, 10 Jun 2026 21:40:16 GMT  
		Size: 33.2 KB (33242 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:963f572c0d607c468b51dc98b485cbbb847044049f4f717950b97f83bc009b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145324149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46115d5d6aecaec287d082892e7c2281534aeacbbedf2c3ef1d1d5de28e8eb78`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:02:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 21:02:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 21:02:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 21:02:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 21:02:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 21:02:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:02:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:02:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 21:02:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 10 Jun 2026 21:02:01 GMT
ENV PHP_VERSION=8.3.31
# Wed, 10 Jun 2026 21:02:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 10 Jun 2026 21:02:01 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 10 Jun 2026 21:02:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:02:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:04:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:04:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:04:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 21:04:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:04:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:04:48 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:04:48 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:04:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:04:48 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:04:48 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:39:56 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Wed, 10 Jun 2026 21:41:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 21:41:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 21:41:05 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 10 Jun 2026 21:41:19 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Wed, 10 Jun 2026 21:41:19 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Wed, 10 Jun 2026 21:41:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:41:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0731e27f9e8271fd2237bcd98fe4786dcbd1f6a1a6c2c877ff8974436c3c09`  
		Last Modified: Wed, 10 Jun 2026 21:04:55 GMT  
		Size: 5.2 MB (5223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712bf7278e87f5112c94eeb3da699c48c010376d6d0cc8814745bc1371e595f9`  
		Last Modified: Wed, 10 Jun 2026 21:04:54 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348b80bb6c2f046a4b8b367cdc7b6a54874e7ac53b7ab9563523d5d0eb60af51`  
		Last Modified: Wed, 10 Jun 2026 21:04:55 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fed4f8ca2790c130cdd80a517daa8ede90074b5ea066c159a1dd1335101014`  
		Last Modified: Wed, 10 Jun 2026 21:04:55 GMT  
		Size: 12.6 MB (12627127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ae182f177b9d02cdb8ddb29d63817b28154e778e38dcdeb9e040835bf9d9de`  
		Last Modified: Wed, 10 Jun 2026 21:04:56 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0570239213b40453c1e4803af91034c262a76b68e5d616b98568f5863c767`  
		Last Modified: Wed, 10 Jun 2026 21:04:56 GMT  
		Size: 11.4 MB (11444052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a3d6b95480a75524986d426b19fb995d2dd8048e9baa045a0e59509315310c`  
		Last Modified: Wed, 10 Jun 2026 21:04:56 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff5602a39c7ec5447b3267b9f27d4d20eaa8af1fde1f501c90d4510a9d7a6fb`  
		Last Modified: Wed, 10 Jun 2026 21:04:57 GMT  
		Size: 23.1 KB (23067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca98d2e1a48f026caaff16e851a7a043a6ef900d962335311a59ab29ce4e4db`  
		Last Modified: Wed, 10 Jun 2026 21:04:57 GMT  
		Size: 23.1 KB (23079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651639bfa636ca567e27d354bbec97b1c3e3149dc1879e7f0c12907375ab9967`  
		Last Modified: Wed, 10 Jun 2026 21:04:57 GMT  
		Size: 9.2 KB (9246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd3718397db3fa6ec0e429429fc888d1b7bb96491d7b72f72b8980329ae7b0`  
		Last Modified: Wed, 10 Jun 2026 21:41:36 GMT  
		Size: 25.3 MB (25278785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d02a65ac913a137d9f52b8134016783ad2305f27e953e35adb7fbdb0ef09d3`  
		Last Modified: Wed, 10 Jun 2026 21:41:35 GMT  
		Size: 4.7 MB (4703342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a97fa419f418dd46db40f760ee2c0f3845307e7d8a1c2f8dff06ec821ee7176`  
		Last Modified: Wed, 10 Jun 2026 21:41:35 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e2c01f3ca8502a4daa6fa7dda49e3783cfb8b6093993224cec7bc04a27df52`  
		Last Modified: Wed, 10 Jun 2026 21:41:35 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b79d01713e10c21b50d054173f7b58e681d971fc878d136f06da90955ffcef9`  
		Last Modified: Wed, 10 Jun 2026 21:41:39 GMT  
		Size: 82.7 MB (82701355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:2c51544677a5a387722d2dea0f3a73b516db51c032175137537635000c4915dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe25ec2bc76d39049219d937b679f767268e0cfa489f231c8be8b8885f256e1`

```dockerfile
```

-	Layers:
	-	`sha256:4c7f1f18989071d16c4cd55caaa4ca152d4ec1c1fe6b4680576227887a16d4f0`  
		Last Modified: Wed, 10 Jun 2026 21:41:34 GMT  
		Size: 33.2 KB (33242 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:34a10ca99224e0a1a43c44de22a670aaaf4947f3537961c4eeb2f4f8d1db4757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151694631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8432ee6d99f24a331b5de806c758031fd756101d7314394201653c5188e323fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:58:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:58:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:58:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:58:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:58:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:58:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:58:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:58:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:58:04 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 10 Jun 2026 20:58:04 GMT
ENV PHP_VERSION=8.3.31
# Wed, 10 Jun 2026 20:58:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 10 Jun 2026 20:58:04 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 10 Jun 2026 20:58:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:58:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:02:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:02:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 21:02:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:02:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:02:24 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:02:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:02:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:02:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:02:24 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:12:24 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Wed, 10 Jun 2026 21:14:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 21:14:42 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 21:14:42 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Wed, 10 Jun 2026 21:14:55 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Wed, 10 Jun 2026 21:14:55 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Wed, 10 Jun 2026 21:14:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:14:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b103c1838737025c23a365cd41c737f39d1620402be753aaad4c25b11153c81`  
		Last Modified: Wed, 10 Jun 2026 21:02:31 GMT  
		Size: 6.3 MB (6287170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c43298a21067e3eba51cfd01e61b0fad9bb70908c45942b830e410dcc8414e`  
		Last Modified: Wed, 10 Jun 2026 21:02:30 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc20d0deef19337028fd6845f609b923a4082c90c233f7e04885e06f417e149`  
		Last Modified: Wed, 10 Jun 2026 21:02:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f97dfc8416aea1ad9488fc591265299b84ed5382bb18b1b92c154d8a2cd1575`  
		Last Modified: Wed, 10 Jun 2026 21:02:31 GMT  
		Size: 12.6 MB (12627087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4382ad26a6c1d47bace661e4e750cc0022bd704732f685d8430993f87b5e40`  
		Last Modified: Wed, 10 Jun 2026 21:02:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0903316829b6a042117f94d3d59fe26f0ff6471dd6887626b4160ebcb1a541`  
		Last Modified: Wed, 10 Jun 2026 21:02:32 GMT  
		Size: 13.3 MB (13318071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a432ac28a1490f98e33f88f77d7c7e7aac9f03e61b43ff25432c542ea9f1f7cc`  
		Last Modified: Wed, 10 Jun 2026 21:02:32 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa71525130487c1ba37f679c2340c4ba9b7edbd1a368b9aa4af3744914ba093`  
		Last Modified: Wed, 10 Jun 2026 21:02:33 GMT  
		Size: 23.1 KB (23052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7657fc1b5da4e87366e578606d1b42338093a596034e5b7274bcedbb1fcfba02`  
		Last Modified: Wed, 10 Jun 2026 21:02:33 GMT  
		Size: 23.1 KB (23067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cf54c45b9f931c0f0080fc6f15c548050922264d2c6f79cc410f4ca3881592`  
		Last Modified: Wed, 10 Jun 2026 21:02:34 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc8a8f7cd9c6c3b81e70eb470c3a908f27c805b72f1d76636f26ffa87b4f9b9`  
		Last Modified: Wed, 10 Jun 2026 21:15:12 GMT  
		Size: 27.1 MB (27081286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835aa0beeeea4d0e6218a6ab7ee9567e8723dbc55621f8e0fe7713cc3fa6fc72`  
		Last Modified: Wed, 10 Jun 2026 21:15:12 GMT  
		Size: 5.4 MB (5417621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14774306bc921faf2a1e12388e8ed8ba531eafb5fa341cef82bc837d45779730`  
		Last Modified: Wed, 10 Jun 2026 21:15:11 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d6fe07c1d162714f6469e321e9028e0f931aa0a89af2f1041df64c2f2ad46f`  
		Last Modified: Wed, 10 Jun 2026 21:15:11 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73328e1f4a8ea1bf07411c696c78909ac7a764b4a42914a54eea1801ca8bea69`  
		Last Modified: Wed, 10 Jun 2026 21:15:14 GMT  
		Size: 82.7 MB (82701119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:68bf5772042c25098aef61645a1530833f73a216683c6c1d35d390d86b19601b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef71a2d2a035d8b8352437280d929fdc5e03d473d3622b500485ce0a624339d1`

```dockerfile
```

-	Layers:
	-	`sha256:786ecd3cad12c37bb54756edca55cb6f5ca7d2b647beafb8390ffaa5ed77e58e`  
		Last Modified: Wed, 10 Jun 2026 21:15:11 GMT  
		Size: 33.3 KB (33270 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; 386

```console
$ docker pull mediawiki@sha256:38f2ba751c98d372af7272bea97af67b9b285eaedd3c99d337c214c9f128e111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148916787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a512c4f3c45b6d1f7a64460f9d667770204f89f2003219750e8e82e2fa10322`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 16:46:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 07 May 2026 16:46:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 07 May 2026 16:46:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:46:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:46:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_VERSION=8.3.31
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 07 May 2026 16:46:38 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 16:46:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 16:46:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:49:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:49:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:49:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:49:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:49:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:49:28 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:49:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:49:28 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:49:28 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:49:28 GMT
CMD ["php-fpm"]
# Thu, 07 May 2026 17:28:27 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Thu, 07 May 2026 17:29:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 17:29:50 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 07 May 2026 17:29:50 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 07 May 2026 17:30:03 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Thu, 07 May 2026 17:30:03 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Thu, 07 May 2026 17:30:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 17:30:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517d4cfdee78c5c9457650f428bb6e5d5ab018e6fb26ffa2ec66c2676cb3a7a0`  
		Last Modified: Thu, 07 May 2026 16:49:35 GMT  
		Size: 3.6 MB (3625754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056a9d559723cd4dffbe25d95535c2d92b2f50373a78d8e9a4b93cad5aa14485`  
		Last Modified: Thu, 07 May 2026 16:49:35 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de11264937c4b4c11c636386176f3d3ea2a01e7eb4166d3945e00bbf2e56f023`  
		Last Modified: Thu, 07 May 2026 16:49:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4b83ce3931910f3664ee9d405d162be2605be0c5cad1a36fb3a2bd4cb33e4`  
		Last Modified: Thu, 07 May 2026 16:49:35 GMT  
		Size: 12.6 MB (12627231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9086ad56ab8d3b34d2a98c06b12ccb46551b0d864bdb7eaef6695216b7f150e`  
		Last Modified: Thu, 07 May 2026 16:49:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3980f7710a7b9dc8a5e447a361daa2f9e40d0e5d9eb759e2827a84dacb1986e`  
		Last Modified: Thu, 07 May 2026 16:49:36 GMT  
		Size: 13.6 MB (13627339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f850cf1308be3544cac4480add58b7dd1eb0985545b4eccadc3ad5c84177e28d`  
		Last Modified: Thu, 07 May 2026 16:49:37 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03185b775002f31e1c61457ddb183e927ffc0b7f57ab05b91d15177f5df211ac`  
		Last Modified: Thu, 07 May 2026 16:49:37 GMT  
		Size: 23.4 KB (23380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c6ddd905c3508fa85e8f101e42d137b016e94a6a0c5162cbc812080048d130`  
		Last Modified: Thu, 07 May 2026 16:49:37 GMT  
		Size: 23.4 KB (23405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8bdde6d4a064c6551a59477bdd1d3653786f545d922285a1c7c020bb4f126`  
		Last Modified: Thu, 07 May 2026 16:49:38 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b405825dc9270253e7dd2789f1848e23d6a5c75bc3e0ca2d20564a41fb5e73e0`  
		Last Modified: Thu, 07 May 2026 17:30:20 GMT  
		Size: 27.4 MB (27350683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95af4a3327ac345d874aaa52c0d62766c666dadfd7dde8ae7d2c0b801ef4b6e`  
		Last Modified: Thu, 07 May 2026 17:30:19 GMT  
		Size: 5.2 MB (5232933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98135f00e8242a537632e404e4d5f8b53c448742cb661bec458238898f35a969`  
		Last Modified: Thu, 07 May 2026 17:30:19 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c8cd2c367adce60b05bd139d09c4bb3afab9d3359bbb276cce97a8f161a8e`  
		Last Modified: Thu, 07 May 2026 17:30:19 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bcaa7a33533b8222c1aff95e63b76a69db30bbaf80fc4b8bb4569ca89138c3`  
		Last Modified: Thu, 07 May 2026 17:30:23 GMT  
		Size: 82.7 MB (82701794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:859cd43f0a3bbe89d0be8ce17ed8f7ce74c9a0bc05e43ba2328f801ad324831d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 KB (33083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781f441d47f776c374c5000aa48113911979baa1d709e3cc563d1d05fbbcd09a`

```dockerfile
```

-	Layers:
	-	`sha256:6f8f2e538b7c8eaf81735199c8f43622ee472277c91344a93c5d58eb0e1fa49c`  
		Last Modified: Thu, 07 May 2026 17:30:19 GMT  
		Size: 33.1 KB (33083 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:stable-fpm-alpine` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:91f35f036cf5665dded174daa9836a2a26032a9f2579598e31289b240ceb3486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150253430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26abe3dc74ceb71d4e3d4736d762c296e901a50567f5e006027a1506bf38eda7`
-	Entrypoint: `["docker-php-entrypoint"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.3.31
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 07 May 2026 17:28:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 17:28:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:33:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 17:33:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 17:33:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 17:33:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 17:33:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 17:33:42 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 17:33:43 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 17:33:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 17:33:43 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 17:33:43 GMT
CMD ["php-fpm"]
# Thu, 07 May 2026 20:40:15 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Thu, 07 May 2026 20:42:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.28; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 07 May 2026 20:42:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 07 May 2026 20:42:03 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 07 May 2026 20:42:20 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.45
# Thu, 07 May 2026 20:42:20 GMT
ENV MEDIAWIKI_VERSION=1.45.3
# Thu, 07 May 2026 20:42:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Thu, 07 May 2026 20:42:20 GMT
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
	-	`sha256:10550b23dfafde9e9ca7140cd4f44ed81df25bd43058acec76dc26b1db48065f`  
		Last Modified: Thu, 07 May 2026 17:32:07 GMT  
		Size: 12.6 MB (12627245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737e37e33cf749d1ac30273eb0d697585403e8a518a3cc360635c9c999c0ea59`  
		Last Modified: Thu, 07 May 2026 17:32:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb11cc2b81ca630b32856b1982be4476b8ffd233c035ae48c0b7c6d7981895bc`  
		Last Modified: Thu, 07 May 2026 17:33:56 GMT  
		Size: 14.2 MB (14214490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd6eeec7669df81501f5f4f31deb25c89a58b925947ac6689c3c2a314a01564`  
		Last Modified: Thu, 07 May 2026 17:33:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8d26d5a0f1eaa91e62e87c974a951150616f75cfd7fec4c78419aeb19f9f6`  
		Last Modified: Thu, 07 May 2026 17:33:55 GMT  
		Size: 23.3 KB (23280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7004ad95c52b34210aef71979dd36498d114230eb26ddb3ebae211bca2152`  
		Last Modified: Thu, 07 May 2026 17:33:55 GMT  
		Size: 23.3 KB (23301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009e435e02ee8359ce5b2a623e7f151ffe9644be2c85387b16fa6ef0698cb0f4`  
		Last Modified: Thu, 07 May 2026 17:33:57 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b1abf4645967988d023cf320633f5634e7f64b043a1b03381aac6a09314d0`  
		Last Modified: Thu, 07 May 2026 20:42:48 GMT  
		Size: 28.1 MB (28111932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92caf119cc9afd15d844e2f341714d7ce405e52ec51eab8d32e9ec2e260a3cd`  
		Last Modified: Thu, 07 May 2026 20:42:47 GMT  
		Size: 4.9 MB (4939490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eda14e78c364b9cce5882b8f88f1414e5139f3293cd7974940d0fe6ad3de367`  
		Last Modified: Thu, 07 May 2026 20:42:47 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23c5f952f21ebb8093bff3823353e958a5fb25ac5bb5d6e13ef3351ff3a2f2e`  
		Last Modified: Thu, 07 May 2026 20:42:47 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261d5ddf40a491396bdcc2c81cf2988b30985f29d5644992fe0eafa39682a8dc`  
		Last Modified: Thu, 07 May 2026 20:42:50 GMT  
		Size: 82.7 MB (82701834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:stable-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:a8786ea382c77d50e1b6ba5f409fc0e01d5943eb3c86905d5df1b19f0277c0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa4c2fda827d2a1a19c58959c36f0e2ae5a808c7a19cceb23e4598e07a08028`

```dockerfile
```

-	Layers:
	-	`sha256:604e391b7be16fd17367309eedc9c72cea7393e96b081871b93e92b77b940854`  
		Last Modified: Thu, 07 May 2026 20:42:46 GMT  
		Size: 33.2 KB (33164 bytes)  
		MIME: application/vnd.in-toto+json
