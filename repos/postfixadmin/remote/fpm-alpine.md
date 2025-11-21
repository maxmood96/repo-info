## `postfixadmin:fpm-alpine`

```console
$ docker pull postfixadmin@sha256:16aec67153ddbbad42aa55891d3394ef15135607f2b268cca6270af8ffde0da6
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

### `postfixadmin:fpm-alpine` - linux; amd64

```console
$ docker pull postfixadmin@sha256:fbf5a2344e9f738027c9b9290067560cc3ba34e7d6383b83c11a0ef72289d86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36397393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5371bfe12b6f467a493089e74e8ec86b845a1dbb2d700814a034cfeca47dd528`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
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
# Thu, 20 Nov 2025 20:32:15 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 20 Nov 2025 20:32:15 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Thu, 20 Nov 2025 20:32:39 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 20 Nov 2025 20:32:39 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 20:32:39 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 20:32:39 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 20:32:39 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 20:32:41 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 20 Nov 2025 20:32:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:32:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Nov 2025 20:32:41 GMT
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
	-	`sha256:388b8354cd13a33c834a771f5fcdac20acf84cc7f80439da29dc5c277610cd1e`  
		Last Modified: Thu, 20 Nov 2025 20:33:01 GMT  
		Size: 483.7 KB (483730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddcb6d8d2aee5c6870a782e143eaccb15400b196cff559038b3542da70f4afc`  
		Last Modified: Thu, 20 Nov 2025 20:33:02 GMT  
		Size: 822.6 KB (822571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e69dfd11f0b6db202d7a6d9a35bbd97d7584121d164b4fa0126bf57a0a6cda`  
		Last Modified: Thu, 20 Nov 2025 20:33:02 GMT  
		Size: 1.9 MB (1871587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c710c4e406a025696b8c13fe4637d54ee7c93dfbdfcb781c70c94dbabca541`  
		Last Modified: Thu, 20 Nov 2025 20:33:02 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:6c260d3df23f328d7598ee074c80bcf13d0ec2b3fdda17486a623f770c606ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe109ff743424a68728bf052033983773546ce74585a54e449d82af0a1181140`

```dockerfile
```

-	Layers:
	-	`sha256:41d559585ba1f0ae121f91e1323ec88adb0f5cfe1385a88c1c86c464c073b1e0`  
		Last Modified: Fri, 21 Nov 2025 00:12:16 GMT  
		Size: 26.0 KB (25995 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; arm variant v6

```console
$ docker pull postfixadmin@sha256:1394839ab056e5d9f7db8ed007d43591dfa94d7e5aa5ba41d1ee79baaddd213b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34755489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e6f920ec9fe50db26cdcf190cb1aecbb1f8e0344b0878f4c5d983e2af22003`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
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
# Thu, 20 Nov 2025 20:19:54 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 20 Nov 2025 20:19:54 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Thu, 20 Nov 2025 20:20:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 20 Nov 2025 20:20:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 20:20:27 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 20:20:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 20:20:27 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 20:20:30 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 20 Nov 2025 20:20:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:20:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Nov 2025 20:20:30 GMT
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
	-	`sha256:cb17d04c5d9ecd03e0089536271fa6d74223150c9629d9eb871f756e69a9b180`  
		Last Modified: Thu, 20 Nov 2025 21:19:26 GMT  
		Size: 483.3 KB (483318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f25e9bdf04e94f815fd48b584841be5bd69b9cc282e5ff4e65e69e43ced4831`  
		Last Modified: Thu, 20 Nov 2025 21:19:30 GMT  
		Size: 802.1 KB (802121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb873aa3f890b8dd354735e4fa9fb27eab9400bdd2cc63f3b5d10ecf09aad49`  
		Last Modified: Thu, 20 Nov 2025 21:19:34 GMT  
		Size: 1.9 MB (1871588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c1eb4421d9422a2be4ecab569e756febd073333ad1f4285510802eb0fcf20`  
		Last Modified: Thu, 20 Nov 2025 21:19:48 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:1f872bc2e60a6a37d037d5c177893fbaaee29a031905e185af83ed89e9c02a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e5947a27df04acb6396f0164a2cf3f40b48bacae090d53c766885af736c787`

```dockerfile
```

-	Layers:
	-	`sha256:830f7e3927a268714032c5f1bf6f8d02b7de182b4ea1410f43df9083d65c49a6`  
		Last Modified: Fri, 21 Nov 2025 00:12:19 GMT  
		Size: 26.1 KB (26102 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:d12347130b538e7af349b53f2700bcb0257f17583649f448cf6849da39f35e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33505152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a07f4b20390b3a0b5ac6b0e33987d24ee532faeda73fb5c5268e9a6c67527a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
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
# Thu, 20 Nov 2025 21:19:37 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 20 Nov 2025 21:19:37 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Thu, 20 Nov 2025 21:20:07 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 20 Nov 2025 21:20:07 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 21:20:07 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 21:20:07 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 21:20:07 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 21:20:07 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 20 Nov 2025 21:20:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:20:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Nov 2025 21:20:07 GMT
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
	-	`sha256:9b9bbc678f1bd34819786ccd52a0e87f7d4545c8f23a2ddf413e178d212e482a`  
		Last Modified: Thu, 20 Nov 2025 21:20:19 GMT  
		Size: 443.8 KB (443771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc22125ac26827062972b321ef0b95dbbdfcf042c74a89f2b0247a72023eee`  
		Last Modified: Thu, 20 Nov 2025 21:20:19 GMT  
		Size: 750.6 KB (750614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74fd644ff05f4cd81f33d2812d1e5803fc982f6b32d1c8b78aa03906224611`  
		Last Modified: Thu, 20 Nov 2025 21:20:19 GMT  
		Size: 1.9 MB (1871587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a78592bf3e5b422f0cd05ecf0b482b3d1e542bd4927c496af8e7490781c1def`  
		Last Modified: Thu, 20 Nov 2025 21:20:19 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:f248b24a6c3ed3bffd387e56355ae9d6196dc13b751dee5c66d8669f65354b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9ebd06f122e3ae6837759da0d3bfef5b2914e9c05e9ed3bee7937cfedfebb0`

```dockerfile
```

-	Layers:
	-	`sha256:52c6751624c96f08fea53b43316e550211566f46961f8498024c8193355bf276`  
		Last Modified: Fri, 21 Nov 2025 00:12:22 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:7b59ff125385ceb16adf341521965c57f6267d4cc5c9752c698f3b0cc913c061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36769734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ae6dcd0496610f41929db2286341fa1df304d00c85b3871bea5678b3313952`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:51:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:51:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:51:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:51:51 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:51:51 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:07:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:07:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:12:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:12:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:12:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:12:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:12:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:12:25 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:12:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:12:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:12:25 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:12:25 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 21:12:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 20 Nov 2025 21:12:55 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Thu, 20 Nov 2025 21:13:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 20 Nov 2025 21:13:22 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 21:13:22 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 21:13:22 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 21:13:22 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 21:13:23 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 20 Nov 2025 21:13:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:13:23 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Nov 2025 21:13:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ec9d497168c549f2247fd034c53ae139ca2119ecd169d3a5077266764ebcf`  
		Last Modified: Thu, 20 Nov 2025 19:56:09 GMT  
		Size: 3.5 MB (3466799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde06d6c5e70a5cd4927c1f451661d460ce59d50f974cfd99a3519403c77059b`  
		Last Modified: Thu, 20 Nov 2025 19:56:05 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c198bfe2eba5c7b8b21f18d0c4fdd9cad93e4814a31f7100bc8afb71b2465b`  
		Last Modified: Thu, 20 Nov 2025 19:56:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524019b6333c4e36a1499d6131d3324651f4924a560c3b305865bb94dcd94e`  
		Last Modified: Thu, 20 Nov 2025 21:12:48 GMT  
		Size: 12.6 MB (12625108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdbef2d2bb560ad1d6c0839bf15838b36b8c60fda6529f5df5db5a706dae8df`  
		Last Modified: Thu, 20 Nov 2025 20:59:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bc2dd1281e4af866e33344fde1ab06f6772dd60a339f4143ef2793b835253e`  
		Last Modified: Thu, 20 Nov 2025 21:12:48 GMT  
		Size: 13.3 MB (13253989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e908f43d29d26402f2fcfdd92afe250a07c73344b45ae245383fb7d4d8cd61c0`  
		Last Modified: Thu, 20 Nov 2025 20:59:00 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315c65f1e13f98b02c115418626c8ddb2104d45bf46522975ff99b42f7abc4e9`  
		Last Modified: Thu, 20 Nov 2025 20:59:00 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e716b32e913ac69abdfb20074604fe686a1079d6e0eac41cc23c1910504812e`  
		Last Modified: Thu, 20 Nov 2025 20:59:02 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53799599c74521714ef292d858efb3f79d299482722509361fb06f58a57f24e2`  
		Last Modified: Thu, 20 Nov 2025 20:58:59 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6543f8c0d0396359e7b0f6e62f545c246ce6a63f459d1f21bf693b5d19c997b0`  
		Last Modified: Thu, 20 Nov 2025 21:14:56 GMT  
		Size: 539.4 KB (539425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeefea84920f28dbbe40834829ca753673366a488c73b370f1147e28422486d`  
		Last Modified: Thu, 20 Nov 2025 21:14:56 GMT  
		Size: 820.1 KB (820088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8a32309766b21e520876413f07bfbcf57e011fd41527afb3a19b785c53f552`  
		Last Modified: Thu, 20 Nov 2025 21:15:01 GMT  
		Size: 1.9 MB (1871586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bb9f247dce92b5bb6c62f782349e14afbb46a33082d3feade0b8a4d4bf5c06`  
		Last Modified: Thu, 20 Nov 2025 21:14:56 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:c141a4bdf5f0097694716a67a07b5aea678592273bc4331aebd8d4fdc5827063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360f8181f4ae359cf308f4e06f07a97b89d56a66539fed5650cb737bead7385b`

```dockerfile
```

-	Layers:
	-	`sha256:cb2fbdd3f9c68dce4b9f6adba31929f341706ba43eb1ae77c18bbb4bfb77b418`  
		Last Modified: Fri, 21 Nov 2025 00:12:25 GMT  
		Size: 26.1 KB (26129 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; 386

```console
$ docker pull postfixadmin@sha256:d13e51507c2fd9429d01282fc3e539654dcb603980bf87f5bd3410efd9ed37e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36624990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e173fd945b92a1748a23b797c9b955c28ff7fc182796170f809e6d38bff4851`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
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
# Thu, 20 Nov 2025 20:26:40 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 20 Nov 2025 20:26:40 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Thu, 20 Nov 2025 20:27:05 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 20 Nov 2025 20:27:05 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 20:27:05 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 20:27:05 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 20:27:05 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 20:27:06 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 20 Nov 2025 20:27:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:27:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Nov 2025 20:27:06 GMT
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
	-	`sha256:5e0b8106483deea2e480a802d042a7356cb766b79e10e6d1cdcdf462ae106432`  
		Last Modified: Thu, 20 Nov 2025 21:23:08 GMT  
		Size: 491.4 KB (491436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcfc05e7acfe6b6e9f3a53715fa18adbcb284dfda23afe69a240be339f392df`  
		Last Modified: Thu, 20 Nov 2025 21:23:07 GMT  
		Size: 856.9 KB (856887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55b2827f1a9df15db7413d2754922f764181f9cc574e90eb53bc884e4898395`  
		Last Modified: Thu, 20 Nov 2025 21:23:05 GMT  
		Size: 1.9 MB (1871586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c794f565f6c163485ff65aab1faae3b2420ef05bd283febf7f1315ad38fa2e`  
		Last Modified: Thu, 20 Nov 2025 21:23:10 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:279b92c011d56d9bcb30ecdc519ee9cf37430d9e154effbccc4727172231121d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab2d13d14f67ddaf65520aa3ad2c5ca11d25f30e51c6deb1ed18652cc2c8f33`

```dockerfile
```

-	Layers:
	-	`sha256:7295e060df4faa96ebeb61f8ed85bd8fcaf8af771302c168d4124b1a9de94fcb`  
		Last Modified: Fri, 21 Nov 2025 00:12:29 GMT  
		Size: 26.0 KB (25960 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:c02bd15acc81728ab12e628341e44af6e182ea40863f8251e7eed146b765aabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37076169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f26e361a18e8d17118ed259441e0c6048c3ed03522f2d98576d8e52baebe199`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 00:51:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 09 Oct 2025 00:51:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Oct 2025 00:51:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Oct 2025 00:51:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_VERSION=8.3.28
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 09 Oct 2025 00:51:44 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 21:20:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 21:20:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:29:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 21:29:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:29:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 21:29:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 21:29:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 21:29:54 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 21:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 21:29:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 21:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 21:29:55 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 22:15:58 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 20 Nov 2025 22:15:58 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Thu, 20 Nov 2025 22:16:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 20 Nov 2025 22:16:46 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 22:16:46 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 22:16:46 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 22:16:46 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 22:16:48 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 20 Nov 2025 22:16:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 22:16:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Nov 2025 22:16:48 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53971e004648f8982fc3b37775bc935a3e17a526dffea78cab354e2849bfd0d`  
		Last Modified: Thu, 20 Nov 2025 21:25:17 GMT  
		Size: 12.6 MB (12625110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd2a999bdbd1916d536ced797c2f38b0416bdf9b4e4d63ebb04063c3aefe64`  
		Last Modified: Thu, 20 Nov 2025 21:25:16 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ebd17c49beb1ea4ab18f7e8e27dcc03d329a184e14b1e7777d271f3777db7`  
		Last Modified: Thu, 20 Nov 2025 21:30:16 GMT  
		Size: 13.7 MB (13737190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8faaf33b461bd94b5b6b94ae859b9d46ed4b89bf9fedd33d4eba5039c7037af`  
		Last Modified: Thu, 20 Nov 2025 21:30:15 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00983a40cc1e11404d5947d0d2295acd834ead990652b9e4560c1d79132f6997`  
		Last Modified: Thu, 20 Nov 2025 21:30:15 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df143cd827d82f9423db96861cf0cd96f0c06bbffabc927d66ef1fc7096df2ff`  
		Last Modified: Thu, 20 Nov 2025 21:30:15 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda55e1c6e511a0ecf8615a6eaf4bef9c53f19936f40e103ecc82630277c17de`  
		Last Modified: Thu, 20 Nov 2025 21:30:15 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7e0b075724f8736671189bde88f14715ff1a9e753f326c4f358258ddbff5ca`  
		Last Modified: Thu, 20 Nov 2025 22:17:04 GMT  
		Size: 550.5 KB (550529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb331890e7b6825e64a28a8eccd58cbefcf22c04ec63662aebd15bc49bc74aa3`  
		Last Modified: Thu, 20 Nov 2025 22:17:04 GMT  
		Size: 890.1 KB (890130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bbdca2abb22e06f2c419993e8f057d61a9611178ebbf3c0cfa7eb57a1e0741`  
		Last Modified: Thu, 20 Nov 2025 22:17:05 GMT  
		Size: 1.9 MB (1871585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57de00703759ad30b7ecb8ea8d30397c1bec45fef6a5008be8b0653846ba99f8`  
		Last Modified: Thu, 20 Nov 2025 22:17:04 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:17b5ab1702b8137ec4badb83885114777238279c7e85a2551f0652aa729565de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a801fce45d3a608685cf241ae29b93a6de73a8a4bcf5307113d8700265718e`

```dockerfile
```

-	Layers:
	-	`sha256:43f7010957b4b06ea1668276fdea7390501e9070aed09e7df400ed30de347585`  
		Last Modified: Fri, 21 Nov 2025 00:12:34 GMT  
		Size: 26.0 KB (26044 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:d385cb15ae29b000c29422afcc442a026506771cfef2c3e572b604dcdbea05a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35759329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c9ee2224d7d29a9cdcb0e49dfc90f37826880bda9ccb3e81cd03fdade9ada`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["/bin/sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.27
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d54dfa6f20c012ec1b31e6cb19c53eb8fd6d8e104546d5ef0507028dfdcc6ed`  
		Last Modified: Sun, 26 Oct 2025 05:51:36 GMT  
		Size: 12.6 MB (12613795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e5ef1aa2bfd252b5bbc94697c4c929664b6273fd0e19a578588996462e8ae9`  
		Last Modified: Sun, 26 Oct 2025 05:51:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac4d972f12530d0bd018fbca7c05fa84eb80ae639fbfb0b8009ac520b3ec8f2`  
		Last Modified: Sun, 26 Oct 2025 06:47:34 GMT  
		Size: 12.8 MB (12766231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9462277756b2dbeb02532018df17541f2556746d5ea91230249e8e0a03f53`  
		Last Modified: Sun, 26 Oct 2025 06:47:33 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a642279ed750cda945680614b0f326716ccd5240124b77408847b2a2a7d64c96`  
		Last Modified: Sun, 26 Oct 2025 06:47:33 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f02da76612826c4300d7c7200dcbc0c9a675d5534c2c5445b20e305995dec21`  
		Last Modified: Sun, 26 Oct 2025 06:47:33 GMT  
		Size: 19.9 KB (19860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75622e78ad33604ce5f7f507ad64ed16cbe2d810835f77294f73616d3549537c`  
		Last Modified: Sun, 26 Oct 2025 06:47:33 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3ab5faaa36e6ccee8fd3b42379fb7ae7b1d5cdca967eece954c63697892061`  
		Last Modified: Mon, 27 Oct 2025 01:17:39 GMT  
		Size: 495.5 KB (495527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f4a708e09067188705c1dc181ca71d91c008788c046348794ae7a65c335125`  
		Last Modified: Mon, 27 Oct 2025 01:17:39 GMT  
		Size: 842.0 KB (841985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e7e31195a9ed5c386f18cce1a1c8016a43504a20b0c13d6ee7464fb4a9b89e`  
		Last Modified: Mon, 27 Oct 2025 01:17:40 GMT  
		Size: 1.9 MB (1871586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eecd3bddab69345c5b887de0631d1b5c53aec89f244aace45193394de2d558d`  
		Last Modified: Mon, 27 Oct 2025 01:17:39 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:0eb6544fb91d7c6d2eedc7546a767a4868557f9cf8ffb54c899e17510b896f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57bebbf3e7098a474fc8b45a017b7373591bb3b276b93ea67ced6bc64f7d4af`

```dockerfile
```

-	Layers:
	-	`sha256:821651c4383724cf0f8fb7cf3540232c06784f15b39c239e2fe7b6d923764172`  
		Last Modified: Mon, 27 Oct 2025 02:10:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; s390x

```console
$ docker pull postfixadmin@sha256:efc7d159c03dac6e4e4d9534c40d5629aff3851f9754527531c9e1037ebe5d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36473338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbb0df8d9643ff02bca40c58ae52a7c4dc7c53d632b2d3ac640b89503cbe079`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 17:48:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 14 Nov 2025 17:48:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 14 Nov 2025 17:48:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 14 Nov 2025 17:48:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:11:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:11:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:11:11 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:47:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:47:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:52:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:52:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:52:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:52:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:52:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:52:41 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:52:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:52:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:52:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:52:41 GMT
CMD ["php-fpm"]
# Thu, 20 Nov 2025 21:15:52 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 20 Nov 2025 21:15:52 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Thu, 20 Nov 2025 21:21:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 20 Nov 2025 21:21:10 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 21:21:10 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 21:21:10 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 20 Nov 2025 21:21:10 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 20 Nov 2025 21:21:10 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 20 Nov 2025 21:21:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 21:21:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 20 Nov 2025 21:21:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf21615e7c59e15e1f62a5a7808d0f5410d99d33eb1fa9e2321034798c88c649`  
		Last Modified: Fri, 14 Nov 2025 17:53:52 GMT  
		Size: 3.7 MB (3692784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4246c35005445d4bbee50c8ecfabf7bfff37a35458ccab55f059ef588e7d1b15`  
		Last Modified: Fri, 14 Nov 2025 17:53:51 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cbf8f8851344a16a8334b41749b8f5de7602e34ddb78157ce3902c37e8a59a`  
		Last Modified: Thu, 20 Nov 2025 20:43:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c247a5593e1221a6d015cb4f96ffae67e1d2dc99228574ed713bc504ad1292b`  
		Last Modified: Thu, 20 Nov 2025 21:15:33 GMT  
		Size: 12.6 MB (12625128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484fcf9bd55b21ece798cfb747a1954931fcddd9f84d8768994b4f622dd43456`  
		Last Modified: Thu, 20 Nov 2025 21:15:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c336bf7c35208c2f44ddea792a1e9375bb16ba33e6192986091634fac4da295`  
		Last Modified: Thu, 20 Nov 2025 21:15:32 GMT  
		Size: 13.2 MB (13214353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9db0c567cb04d71830fb67e4ee1e1fb6dc37ab2b776f9cf91878fa4f1d3328`  
		Last Modified: Thu, 20 Nov 2025 21:15:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032bf3f23f3f8b52b6bb6b36ec5126ea583f47dac060e0acf8b9435c14bec4ac`  
		Last Modified: Thu, 20 Nov 2025 21:15:31 GMT  
		Size: 19.9 KB (19878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e312fe8b12a5384db61e662e16d3872e08e339d82b7ea9d89cf24e85b180dc2`  
		Last Modified: Thu, 20 Nov 2025 21:15:31 GMT  
		Size: 19.9 KB (19875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce95a1304df61591b93a604356999c24f3ed863b111b0d5429baec808f4d79c0`  
		Last Modified: Thu, 20 Nov 2025 21:15:31 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8c94404255ae8e32d03a09426e657e0faebe217edd3e2c03e9330c5e9cd054`  
		Last Modified: Thu, 20 Nov 2025 21:21:25 GMT  
		Size: 512.6 KB (512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0c24574cd34d493c4db522914e037a6ef56fd1bf96128cd55cc51f532da885`  
		Last Modified: Thu, 20 Nov 2025 21:21:24 GMT  
		Size: 853.0 KB (852963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19182c0324e494be9743805f509e4e6e6259a0f58547ff938f2f80e3f31f5722`  
		Last Modified: Thu, 20 Nov 2025 21:21:25 GMT  
		Size: 1.9 MB (1871586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592f118eabc7193ea9aa358735c262b05c0693a5c0e234ff5cc2ce8574fe4fba`  
		Last Modified: Thu, 20 Nov 2025 21:21:25 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:8f0f28dcea27687c80153b21a049e2cbc1bf99d8ba730383382eec3705ff6c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3c7b81361d6db27384c822b055bae99c9e086e79b62ed2ade14d4635770969`

```dockerfile
```

-	Layers:
	-	`sha256:347a072b83fafe2651c86f189e151d23c0fd4b182a382607700e78517ec19931`  
		Last Modified: Fri, 21 Nov 2025 00:12:40 GMT  
		Size: 26.0 KB (25995 bytes)  
		MIME: application/vnd.in-toto+json
