## `wordpress:beta-6-php8.3-fpm`

```console
$ docker pull wordpress@sha256:b72e16b89bf3e2714bf6870e407eec8e54fdcbabd0a19f932559676396465f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `wordpress:beta-6-php8.3-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:59a18b824695c4f8e9e0835a7825c8eeb6d21e032865c9f3e4d3916da79e7ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237536232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda0171460fa96837111bb811895c2ac5b1bbd8af48136f21eb19ff9b9953a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:39:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 08:39:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 08:40:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:40:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 08:40:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 08:40:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 08:40:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 08:40:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 08:40:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 08:40:03 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 08:40:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 08:40:04 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 08:40:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 08:40:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 08:52:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 08:52:06 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 24 Apr 2024 08:52:06 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 08:52:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 08:52:07 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 08:52:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 24 Apr 2024 08:52:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Apr 2024 08:52:07 GMT
EXPOSE 9000
# Wed, 24 Apr 2024 08:52:07 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93478d4793284c7a75389488e31ab45acb8ea56f8ba474bdb2359ecd2132177`  
		Last Modified: Wed, 24 Apr 2024 10:13:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74cc574d0d2183a964ea5880bba6308b7653c4cc7ff2010beb2c1b157168a3a`  
		Last Modified: Wed, 24 Apr 2024 10:13:18 GMT  
		Size: 104.4 MB (104357707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4782e138a9004836453694f515681a93d6635ab26f05b7f2dfea2baa4b761ad`  
		Last Modified: Wed, 24 Apr 2024 10:13:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72980e991018cb55cca4e1bf5d177442f8432e4c8b584133c8d282abdb754939`  
		Last Modified: Wed, 24 Apr 2024 10:13:02 GMT  
		Size: 12.8 MB (12783748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0739b3e118e8079b707823a34a23759bf4b30ffd144873ed74cee4c6a06c6e`  
		Last Modified: Wed, 24 Apr 2024 10:13:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ab69fda4a4b0b514a4dd41eedd48be9d350c619034eb95b217f9276d080c45`  
		Last Modified: Wed, 24 Apr 2024 10:14:23 GMT  
		Size: 28.0 MB (28005827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb69beb6c01c2498ba97f3679dbef0fe5bdbf3e4ec44ad3e86fb56a883a30276`  
		Last Modified: Wed, 24 Apr 2024 10:14:20 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f03d7ae14a349bb94e85cce710562ee3ff7de9958acff072ff1205522c134c2`  
		Last Modified: Wed, 24 Apr 2024 10:14:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d781b3f99b6b8848c3088b435c07969ee0d6764929537c14d3dbfdf655b80a`  
		Last Modified: Wed, 24 Apr 2024 10:14:20 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646fe0b774946dd94b733f47486b28c0d3fd68e93150dd6b0cc1dbf8fbcc152c`  
		Last Modified: Mon, 06 May 2024 23:06:55 GMT  
		Size: 26.4 MB (26378433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900d36ecc7a1938fd567505a664ba42e01d965efaf5d82251a9e591a3aa6cb8a`  
		Last Modified: Mon, 06 May 2024 23:06:55 GMT  
		Size: 12.3 MB (12314289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376e153f1a7211965f664d41cadf47760c73be739f0f553509cf8cc4cbdce4cf`  
		Last Modified: Mon, 06 May 2024 23:06:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c933843fc0c8268f50c78e39866ca487f9f985cb2e27d4c9caf51ebd95f684`  
		Last Modified: Mon, 06 May 2024 23:06:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cc7dc9bb608b72c4773b3aa88bce521ef2a1d3c1eab3f0ce05ecf15673dffa`  
		Last Modified: Mon, 06 May 2024 23:06:56 GMT  
		Size: 24.5 MB (24528040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8c8c848ba70c0878f904a18798fac0a4e1dd19f591f286ba8b4bad851ed1dd`  
		Last Modified: Mon, 06 May 2024 23:06:58 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67b2f656d2de1a3b3626f086cf6e8520822959907afb42ff8a5c7733d25818c`  
		Last Modified: Mon, 06 May 2024 23:06:56 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:0eedae6cb5f41bc9c91f14252376e24f9dd9cb939bbfbe9ccb6db9a6a1799cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7499004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34ed189be4159c23aa66f1268bdf03f4f0919beb8f6d372878fd64e80e26ca9`

```dockerfile
```

-	Layers:
	-	`sha256:c6aad95acaf2e14932c3a375de8052f2ec832cfcfdef9aea330e28dcce57456b`  
		Last Modified: Mon, 06 May 2024 23:06:54 GMT  
		Size: 7.5 MB (7450013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e465f8f94791fe382bfcf188ac09b7e1a5d6166ef6bfc14dc3357136ac4d1a27`  
		Last Modified: Mon, 06 May 2024 23:06:54 GMT  
		Size: 49.0 KB (48991 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:139aa8c9b197d7e8e225e259243b4b4d1d5d3ebf668baec3942c465d3f0cfecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208485018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80690ee04f45901526486c07620aa21479e53380013e4f610530edf06923232`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:28:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:28:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:28:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:28:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:28:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:28:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:28:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:28:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:28:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:28:48 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:28:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:28:48 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:29:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:29:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:40:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:40:08 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:40:08 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:40:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:40:09 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:40:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 24 Apr 2024 05:40:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Apr 2024 05:40:09 GMT
EXPOSE 9000
# Wed, 24 Apr 2024 05:40:10 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51615e4309fe3f4243f2ebef6416ed0e259fcf7a77c1f51cddf26fd9000fe2de`  
		Last Modified: Wed, 24 Apr 2024 06:54:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd9c023e8b6e6486532460ab3244084445f053e19ee8775bb4689b0143f0f00`  
		Last Modified: Wed, 24 Apr 2024 06:54:34 GMT  
		Size: 82.0 MB (82002419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685ffe3d3616a8f8c773f8043a67a418c185c5fdb6f4d767631349a391587a00`  
		Last Modified: Wed, 24 Apr 2024 06:54:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4c9e31680024e29e84ef3d51c7fa7e9f6bcdc89f8d375929d7833720263608`  
		Last Modified: Wed, 24 Apr 2024 06:54:18 GMT  
		Size: 12.8 MB (12781574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9211fa155e40745384a18230e5afed634e57f1efd81e4e68a30e878f9496320d`  
		Last Modified: Wed, 24 Apr 2024 06:54:17 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5120dc3436381bdbdb69fffa6eec36c0c8a981dd336d84608a7617d289a84f6`  
		Last Modified: Wed, 24 Apr 2024 06:55:44 GMT  
		Size: 26.5 MB (26489993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ea83f35671022afc7f1603747b0540c747aeeb7e4e30ef8313abe8a39917ac`  
		Last Modified: Wed, 24 Apr 2024 06:55:39 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa25efb1cf8ad31ecd8b196ce84a4040a85df5c02875f4a05f23757601897c3b`  
		Last Modified: Wed, 24 Apr 2024 06:55:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1f8f27cafa09c984892d36ece35289b45ee0bcb29b33401e75dd3fee68dbe0`  
		Last Modified: Wed, 24 Apr 2024 06:55:39 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb094e498a0288e4de51412e39ca3fec87be124080e52be28fa919deb9e0c064`  
		Last Modified: Mon, 06 May 2024 23:29:55 GMT  
		Size: 25.8 MB (25827911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73044d452416bb1d09657387f70873fd86705442cd32cee8250048b68c9dbda9`  
		Last Modified: Mon, 06 May 2024 23:29:54 GMT  
		Size: 9.9 MB (9927364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6858158604663a30df8c220fa4736d1fbc29837a60f4a818a1b08bffa2687972`  
		Last Modified: Mon, 06 May 2024 23:29:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cc131e1949385bceae4512263890baa0ff07fa82ae3320ad24df98a5ecc139`  
		Last Modified: Mon, 06 May 2024 23:29:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8667bc073ce6661ceaac7bb55dc2d9a71ea2caa8acbf801efd0591b06a68c5`  
		Last Modified: Mon, 06 May 2024 23:29:56 GMT  
		Size: 24.5 MB (24528009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7520163d8c856b933c3934d1be305f0cf74e79a2b76a5334ddc84dadc6886ba`  
		Last Modified: Mon, 06 May 2024 23:29:55 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29873ff9e20c9318730f8b6fce792d2f17d23905db463290584136c42d890004`  
		Last Modified: Mon, 06 May 2024 23:29:56 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:00abab9798e6110f83978a27fa6b3c345d656dc3904b89c6e38fd3491b666291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c1dacf020ee6c323fe63778887ae9214cbdc125583fa1ca8fdb7d32e4d337a`

```dockerfile
```

-	Layers:
	-	`sha256:77d478c5ca444bb713cc0867466a0057faf1409bcd6ef292e7aa0aff03b6f9a0`  
		Last Modified: Mon, 06 May 2024 23:29:54 GMT  
		Size: 7.3 MB (7257531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d89295b979af57facabaa985b29c7d2b20638723726c23a49a49ba14f0537dd7`  
		Last Modified: Mon, 06 May 2024 23:29:54 GMT  
		Size: 49.1 KB (49106 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:db128922b5dce23d8943d0a09c3ea3d4415785ef40b5d8620b7fde9d7776c8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197957288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fb90cd05f31ce963409c011c98622091a7490213a7a7b86ec3002d41f9cc86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:09:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 07:09:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 07:09:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:09:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 07:09:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 07:09:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 07:09:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 07:09:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 07:09:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 07:09:34 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 07:09:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 07:09:35 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 07:09:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 07:09:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:18:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 07:18:37 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:18:38 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 07:18:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 07:18:38 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 07:18:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 24 Apr 2024 07:18:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Apr 2024 07:18:39 GMT
EXPOSE 9000
# Wed, 24 Apr 2024 07:18:39 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c91bdb9ec5d9afc1dbdc1c85af855e0b737ff91427b0514d37a85344a78a418`  
		Last Modified: Wed, 24 Apr 2024 08:24:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52001de386fe0b3894ce8d75ba5565b1243274c815093bec2a9dda136b5b6715`  
		Last Modified: Wed, 24 Apr 2024 08:24:12 GMT  
		Size: 76.2 MB (76172843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4113642f4fdf30b4a570807775f684e30125c2e03565c8a73486d8562dc49e8c`  
		Last Modified: Wed, 24 Apr 2024 08:24:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee9652a1aedabdf59f6635d2cf09d5cf5dcee461e73b8635344e59bbe781771`  
		Last Modified: Wed, 24 Apr 2024 08:23:59 GMT  
		Size: 12.8 MB (12781525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4199a3931471a90172d302214ddf5a784a853bf6746c5c182087130519fff2be`  
		Last Modified: Wed, 24 Apr 2024 08:23:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421e8a4aeab29fb0fc5f5d246b524db4fa508b0871e592ac49b712a8960ee234`  
		Last Modified: Wed, 24 Apr 2024 08:25:25 GMT  
		Size: 25.6 MB (25596207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524af989ea23d7a1acbe4b921d14475e80b4086dccd39f4d54aa7eccc222c84f`  
		Last Modified: Wed, 24 Apr 2024 08:25:21 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989409476b2e1f7f9b31bb30b2fb4c62541582ad20f86d7f4c0cd164b84f8184`  
		Last Modified: Wed, 24 Apr 2024 08:25:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2a4847ca121f1041eb9f3d1950f09d84fbffc2f83f84d1ae0a48890ce57d0f`  
		Last Modified: Wed, 24 Apr 2024 08:25:21 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d59392a04a525b2686e443c6ded06503135588538322a54eec7ce7837353c1`  
		Last Modified: Tue, 07 May 2024 00:25:44 GMT  
		Size: 25.2 MB (25165919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27d5f1eaa285f9140efbe7e171b116f5dc3a8e631c9a86f83260c579594a194`  
		Last Modified: Tue, 07 May 2024 00:25:43 GMT  
		Size: 9.0 MB (8954606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d31f6747d22d01e9273f1227067785f9892b3ee067010e5345d38681ccf8529`  
		Last Modified: Tue, 07 May 2024 00:25:42 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5add300a8b4235a09ca41ab42437df92a28cac7c3e08bcb71796aab2a959f5`  
		Last Modified: Tue, 07 May 2024 00:25:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117e5ec150c97ba2ae0ebfe16f380a7dbc2c92d88c217f58575cc658cbd6b819`  
		Last Modified: Tue, 07 May 2024 00:25:45 GMT  
		Size: 24.5 MB (24528030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79938402b9c7a9bad3ae8b77e6495939a4d0c72983f6a83cc36ae607307553df`  
		Last Modified: Tue, 07 May 2024 00:25:44 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1ce8e513477e9158930b9474cb26345d84543c0923db9dfcb8d650161c6adb`  
		Last Modified: Tue, 07 May 2024 00:25:44 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:b6308402f9d9b2cecdfc0264555757696b69d0ecdf2f332b68a4f5acea01d863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7309541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c33d522e6f9b967e1836289f3cd68a8676796402bc5f483b683e50bcff3225f`

```dockerfile
```

-	Layers:
	-	`sha256:199061d45f81c8a9d0cca6cc382f9a4a1f5f12822c1e648b735a90ea1609353b`  
		Last Modified: Tue, 07 May 2024 00:25:43 GMT  
		Size: 7.3 MB (7262059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67c0560eef0222804bc511c9578c6e34b5054341104eab27fabb6b23847d7dc`  
		Last Modified: Tue, 07 May 2024 00:25:42 GMT  
		Size: 47.5 KB (47482 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:6ab58d05d301135a425b9c72c97a13ad153db75ea330ccbf8ddd76c8a315d63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245619860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977f987cc0cb0ef4cf009aff12740d249cb1336b3095c05a8eb8d9627ddd8f0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:38:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 04:38:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 04:39:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:39:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 04:39:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 04:39:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:39:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:39:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 04:39:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 00:08:26 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 00:08:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 00:08:26 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 00:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 00:08:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:19:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 00:19:37 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:19:37 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 00:19:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 00:19:38 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 00:19:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 00:19:38 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 00:19:38 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 00:19:38 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b17d6e35656ac020a43a3f9453f06b61a9c61212e0437b31bac9d2b974cb4d`  
		Last Modified: Tue, 12 Mar 2024 06:57:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8431cb294ec999c969b368afe1f6bb5484654b2ce2932cb1a6780d9c52781090`  
		Last Modified: Tue, 12 Mar 2024 06:57:29 GMT  
		Size: 98.1 MB (98126016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735009beb2cceac6bf57add7c26d3a77c8d92fc49ea5e05d8b2452e84a09b61d`  
		Last Modified: Tue, 12 Mar 2024 06:57:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8376d41ffc33d3f6756982ffc2262455681a7c10e9dd2dfbf95bcab9943131`  
		Last Modified: Sat, 16 Mar 2024 02:14:03 GMT  
		Size: 12.8 MB (12758010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb144c769940e4df2a8da73ef4f6ba677606186eb5657a6faff8a3edc1bb7a79`  
		Last Modified: Sat, 16 Mar 2024 02:14:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12f944e900cc4b940c8e0ef9f572a2e9c3b82fbcc090ddd7d3c90fdf2d7a31c`  
		Last Modified: Sat, 16 Mar 2024 02:15:18 GMT  
		Size: 28.0 MB (27950522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882c452df34d4800d01af00633904bbc8dd68fdabe141e975f8585fd9602d893`  
		Last Modified: Sat, 16 Mar 2024 02:15:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ad9aa333d36c57bb88413ffec31e5c723b397b6ceeecef12179ca24c6e98a7`  
		Last Modified: Sat, 16 Mar 2024 02:15:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce83973359a79f08b8cddd42cd87bd69c157b8201d8654aa87345f0dbf16073`  
		Last Modified: Sat, 16 Mar 2024 02:15:15 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a717bcae1c798688e8564d2da0492fd9548c2c3e82681638ab832abc784a8b`  
		Last Modified: Sat, 16 Mar 2024 19:51:16 GMT  
		Size: 26.3 MB (26288140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97deefffc62e926914c97a6b00666d031127296869ed8e606d149ef186104c25`  
		Last Modified: Sat, 16 Mar 2024 19:51:16 GMT  
		Size: 26.8 MB (26797890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2cb33ef86ba97c1d1f98f3e72e00a1dabc7dad9dab0c53e1a105bf085db0d7`  
		Last Modified: Sat, 16 Mar 2024 19:51:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3935b0f44919b9ee6f135e8807588274c33f4644864feb55bf66f0124062e325`  
		Last Modified: Sat, 16 Mar 2024 19:51:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3891eb47324a2694f1a264c38cc7981722a9579e1fc8e527ceef960c87acc8f6`  
		Last Modified: Fri, 29 Mar 2024 00:56:36 GMT  
		Size: 24.5 MB (24525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8c4f107ec13ae15a45f4c3c3b0f3dc008acf41d0038f474fd276bc2883a73a`  
		Last Modified: Fri, 29 Mar 2024 00:56:35 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d71c6ea73f1717fa0d89cdbcf396ef5afd99859788bd6a4a03a812df1792d6`  
		Last Modified: Fri, 29 Mar 2024 00:56:35 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:609bb1005069cc2cc45ed1613471f8d85b0cfd4d3b7a3a02532b93a590101543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8544575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d12f37ff9ff7de0846f2087fd6113ae55e3dcdf528f5f907df97e1fb3f7cef6`

```dockerfile
```

-	Layers:
	-	`sha256:bffaa15a4777f7a8af2f1d79b56f396588cd9e44500965fbd81384b4a7f49361`  
		Last Modified: Fri, 29 Mar 2024 00:56:36 GMT  
		Size: 8.5 MB (8497580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e29396abec3a22efc6e0a883ba22a808af502eda3d3a92ac810d0746bd412dc0`  
		Last Modified: Fri, 29 Mar 2024 00:56:35 GMT  
		Size: 47.0 KB (46995 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:bd2977598a506c163cc2615b9089a5322180ddc222a8335527ed0ac482581b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235768635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c36f00e51674a5d69834111e720c9fc4bc94a04dd256cf5169390f2b43cda22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:02:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:02:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:03:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:03:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:03:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:03:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:03:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:03:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:03:25 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:03:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:03:25 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:03:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:03:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:24:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:24:26 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:24:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:24:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:24:26 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:24:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 24 Apr 2024 05:24:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Apr 2024 05:24:27 GMT
EXPOSE 9000
# Wed, 24 Apr 2024 05:24:27 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb1b3a226af34ddecc6d2893906c2c06039ad4a2e8de3b340d85dce69d80022`  
		Last Modified: Wed, 24 Apr 2024 07:36:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492e3888464375d37ac47d192dc5edd8fa2a1146cc5b3542c21ca67bc5e080e6`  
		Last Modified: Wed, 24 Apr 2024 07:36:25 GMT  
		Size: 101.5 MB (101522095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a318120f6f010a0842e1a7d0c601c50a55f8f3822db28e6889a943b1e1c103`  
		Last Modified: Wed, 24 Apr 2024 07:36:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b810686c6e879713c1a82783630d00ad6109e79a913a203d35b10165d7755ac`  
		Last Modified: Wed, 24 Apr 2024 07:36:01 GMT  
		Size: 12.8 MB (12782793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7332826e6bbcf5429b46a9d8342ef20c7de7deb67480929d3aa37de75e1e6b1`  
		Last Modified: Wed, 24 Apr 2024 07:35:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba6b2b88754efa8631f7a52bb83998060adeb0f8935d62b0a7292f68ea422b1`  
		Last Modified: Wed, 24 Apr 2024 07:37:40 GMT  
		Size: 28.5 MB (28521864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff99fd4f4b7bd29da05dc569d6be0b1d812c6a234bb040e2fb6822b9f96c2b5b`  
		Last Modified: Wed, 24 Apr 2024 07:37:34 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4449dad78a76bafdb5740f033c54aa6fa8ba18f198894b10aba865f142bd9c65`  
		Last Modified: Wed, 24 Apr 2024 07:37:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333d64876246ef1efc3fa15395cd389b7731385a94c63db0d550a15f3a6425d`  
		Last Modified: Wed, 24 Apr 2024 07:37:34 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a86772132ce40fd37a811450e6faa59e9f317821350fe8fdc01b91ff0c868f`  
		Last Modified: Mon, 06 May 2024 23:07:10 GMT  
		Size: 26.8 MB (26832673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edd858960f539ebd166e544c6bf8d72b88d2e6b3092b52dce54766b2ad8e7ce`  
		Last Modified: Mon, 06 May 2024 23:07:09 GMT  
		Size: 11.4 MB (11400292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c94295c60f14454def694d620fbcf32288badeb82d1ea2dd3fe8295ef2d7388`  
		Last Modified: Mon, 06 May 2024 23:07:09 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0852afd36741d27e2beed2d7c0da6396d2fe4ccb77652aa85297d618f0df9b7`  
		Last Modified: Mon, 06 May 2024 23:07:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ee019b5998cee9ccec74c341e6c918cc33f9a16b81e58c16fa5a43e56942ed`  
		Last Modified: Mon, 06 May 2024 23:07:10 GMT  
		Size: 24.5 MB (24528022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2cafd4aa098c0670620d8a9aba2b12c58ee13ff3714f1d929238f1ce27a62b`  
		Last Modified: Mon, 06 May 2024 23:07:10 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b427af6f8efd308797cd88e84e276f156bca212e27460d37db7748071122fb0`  
		Last Modified: Mon, 06 May 2024 23:07:10 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:7beb44f3c3c2f538a434cdb8ac857ab2bea991f7182c1c8e7dce0a283fa0e39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c832a7a0d85a3be87b69eea75ca656874ed0f050eb5597478f35fdd5853565`

```dockerfile
```

-	Layers:
	-	`sha256:55b4aa30cf264d348c3fdfbb93312c8acca75ebdc19bb547de6d8727edb7daed`  
		Last Modified: Mon, 06 May 2024 23:07:08 GMT  
		Size: 7.4 MB (7430189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea65333597fb47f8428e2306da3f46fcf31aa251d7759e5d8d576f2d67e4034`  
		Last Modified: Mon, 06 May 2024 23:07:08 GMT  
		Size: 48.9 KB (48949 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-fpm` - linux; mips64le

```console
$ docker pull wordpress@sha256:71c7911148a3bb04d5c0552f9a7338b7949726f5cdb0def248f7a94496f42a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209242936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d64ac8fdc0c38e9cdeee1fe2ab12050e15d48553e373145f4e4b5fa27f06f31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:50:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 10:50:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 10:52:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:52:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 10:52:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 10:52:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 10:52:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 10:52:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 10:53:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 10:53:05 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 10:53:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 10:53:11 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 10:54:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 10:54:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 11:42:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 11:43:01 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 24 Apr 2024 11:43:08 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 11:43:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 11:43:15 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 11:43:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 24 Apr 2024 11:43:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Apr 2024 11:43:29 GMT
EXPOSE 9000
# Wed, 24 Apr 2024 11:43:33 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2dfa3d36c21ae20eadd92525e61517d0277ef14398994b215d50f524e69655`  
		Last Modified: Wed, 24 Apr 2024 17:08:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a61fb25c010a33f1a3c4b6a08fb02be6a6c0b5d22d9b3ce52a1dd1c356a0024`  
		Last Modified: Wed, 24 Apr 2024 17:09:13 GMT  
		Size: 80.5 MB (80474735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239652ab0a80c5dad89154985f8ceec71b76e056f18e7dcb6ffaea27e8984b59`  
		Last Modified: Wed, 24 Apr 2024 17:08:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbfe6739523c914b8dce40cef9def998289df098825e2e3677b84cabe9d4f89`  
		Last Modified: Wed, 24 Apr 2024 17:08:17 GMT  
		Size: 12.6 MB (12575859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c381a4e328f9906fa4df3752da8c3977efd8fe4e9431ef31f8843e51e4a6d27`  
		Last Modified: Wed, 24 Apr 2024 17:08:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdc2777041909d8ba891507a5e7916e66bad6bdca9364ea9d5ec939b9ecc34e`  
		Last Modified: Wed, 24 Apr 2024 17:10:57 GMT  
		Size: 26.9 MB (26898486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253d75a5514ee71d96c90394c142696fd81232d8ee33722337a857a99f1b506a`  
		Last Modified: Wed, 24 Apr 2024 17:10:40 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cce549466f847e2d87264cdd135140210b2e671d99bb057ae6eb0303cb613c`  
		Last Modified: Wed, 24 Apr 2024 17:10:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7305c35438e433f25241bbc2bb078e0dbca187e6e3235d18d1ec14e74c5f1b`  
		Last Modified: Wed, 24 Apr 2024 17:10:40 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11116065716893637a993ed4f1731035f7713d5da39fbfe1cf6c45436c11ff0e`  
		Last Modified: Tue, 07 May 2024 00:34:21 GMT  
		Size: 26.2 MB (26158674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c15505719aaafa2794639ded5e3b2977ce3e3626a31f40dd822631a6f34eff`  
		Last Modified: Tue, 07 May 2024 00:34:19 GMT  
		Size: 9.4 MB (9445312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7cf4c8ad37549b14829f3ccb9f7ddc2d9a21c021b1f42badf0a3ab857e84d3`  
		Last Modified: Tue, 07 May 2024 00:34:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd03878b207a8533d362ed7e2c741646c5ac58170670ffa2d3253b6ab7042b7`  
		Last Modified: Tue, 07 May 2024 00:34:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60055472da76d5b42cfc72f00734f122980e4ebe2cdd64ee164d0971b6a51a14`  
		Last Modified: Tue, 07 May 2024 00:34:22 GMT  
		Size: 24.5 MB (24528011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0974a3bd2c332d054921753dd9c0654a95ee5070e5e3c68bd3aeba5c560e46`  
		Last Modified: Tue, 07 May 2024 00:34:20 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db24fb5981e30c894f30b8d110d9c4a592062bc2121d7fdc5fc15b3aee94db16`  
		Last Modified: Tue, 07 May 2024 00:34:21 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:4b9f41c3bc36243ab29cc3098e9ab28577700249d1c426d1b66ea7690dae0f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 KB (48835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9042ef89ec85342b49142e60efcd0ff7cfe5b562e1d94ebb4a5c51e284d352`

```dockerfile
```

-	Layers:
	-	`sha256:c88a6b6a16fc716e2ff4e576d26278d62c44f986ae4d7e51ff2f51ff8a68a659`  
		Last Modified: Tue, 07 May 2024 00:34:18 GMT  
		Size: 48.8 KB (48835 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:60de7973caa5b7293e428d7652d765e1a114dd691b2e516319e3256916971c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259464396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e9c0b44170e97f56f1bd6a8abf8ddd4ee48f8dd6c38c76dcd3b905ccb3b1cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 03:44:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 03:44:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 03:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 03:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 03:48:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 03:49:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:49:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:49:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 03:49:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 05:05:35 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 05:05:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 05:05:36 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 05:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 05:05:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 05:15:37 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 05:15:38 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 05:15:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 05:15:38 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 05:15:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 05:15:40 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 05:15:40 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 05:15:40 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729fb27eaa92097ad878499ec6403a23c58d8214dac659ab72a1e323819ef57a`  
		Last Modified: Tue, 12 Mar 2024 08:08:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cce4a728b9ae2c7eefcd9b8c3b9dc1d62b72c1c071f16bc427f26b3053a56b1`  
		Last Modified: Tue, 12 Mar 2024 08:08:52 GMT  
		Size: 103.3 MB (103313606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40564a51615fdea74995b1c4e47872bc1cb06986eab253f3b5c5bb070cb76e`  
		Last Modified: Tue, 12 Mar 2024 08:08:34 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc110c1819e8e9b1f8c67f617946089e534d91dac700a08433eff464c93b9fc`  
		Last Modified: Sat, 16 Mar 2024 06:51:42 GMT  
		Size: 12.8 MB (12758048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e612c0fb9481197e24785f9677716d176dd51833aa75020aba2bd9efcb869e0`  
		Last Modified: Sat, 16 Mar 2024 06:51:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afca75ea349f8264aa8336723f4193089fb7ce951d0ad5b29ab2a3a9f884974`  
		Last Modified: Sat, 16 Mar 2024 06:53:06 GMT  
		Size: 29.1 MB (29068725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7844a3145ca8988b225038adac7664b9a0a73fc60d6cd5e571aa484bf66a1496`  
		Last Modified: Sat, 16 Mar 2024 06:53:02 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc5222e45a5ba417787a783041c232ba93a9e5cb6464548be7d2a1eeeb1a038`  
		Last Modified: Sat, 16 Mar 2024 06:53:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b8a5a4a37ad95f66130687c3ebc6c84ea173695cd9e46438d9bb66a2dcf5a8`  
		Last Modified: Sat, 16 Mar 2024 06:53:02 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac582c6b8921bdde9950d8f0032f22d4b0c3855ec8020e7bfb0b62cfc8789aef`  
		Last Modified: Wed, 20 Mar 2024 01:43:00 GMT  
		Size: 27.5 MB (27477929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e3a30914be5cec6d5e4238c38bfaa55e6b9021ff4dd80e0375cd96201ce4b`  
		Last Modified: Wed, 20 Mar 2024 01:43:00 GMT  
		Size: 29.2 MB (29184227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8247f20341248ada9068990f14badd51355984a8cae19a60ca09a8e109e646`  
		Last Modified: Wed, 20 Mar 2024 01:42:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2f4e9a255e33d2966bf2449e969c507a01fc2e383e7a24cd0e6ce74c139830`  
		Last Modified: Wed, 20 Mar 2024 01:42:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f267a7abcac6c445cda38b0045e3fa4cad0f0b400ebc6b60f352f3599e6b97`  
		Last Modified: Fri, 29 Mar 2024 01:19:35 GMT  
		Size: 24.5 MB (24525136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562bd3f8f4bd3a3a0f31c997df0722dfb8c9ff9ddaddf0a59f699954b9df8557`  
		Last Modified: Fri, 29 Mar 2024 01:19:34 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d571dd4c7557932dfffb267d44ad7fb2af51047488a901246d956c278c30cc8`  
		Last Modified: Fri, 29 Mar 2024 01:19:34 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:d4bb1f013e8ee5971c93c4be8d0b8eb4c28f652614381355d2fd63bc5226ddcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8495089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb10ad9a096146c5d6d4589f1ab516b274dd739f9749c3164adc62b544fe788c`

```dockerfile
```

-	Layers:
	-	`sha256:5c241bdc300ea3c22ec4fc670878d1aff9498ade2fd8cfc2abdc93123ff06e72`  
		Last Modified: Fri, 29 Mar 2024 01:19:34 GMT  
		Size: 8.4 MB (8448050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927dc23c59e27d5e6071a5046fa5e406dea05368a73fb1f3e84da12864404355`  
		Last Modified: Fri, 29 Mar 2024 01:19:33 GMT  
		Size: 47.0 KB (47039 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:d6ac31eb0414628c55e8f35b5c0a65427d7a4659c56d6a50d6b44e3f74e738c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (208042247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fddbafbb0fb99e8ee4f5899b553c2d72e503760a1a60e8daf8d82cdf2ac4643`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:36:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:36:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:36:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:36:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:37:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:37:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:37:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:37:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:37:01 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:37:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:37:01 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:37:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:37:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:45:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:45:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:45:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:45:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:45:51 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:45:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 24 Apr 2024 05:45:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Apr 2024 05:45:52 GMT
EXPOSE 9000
# Wed, 24 Apr 2024 05:45:52 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8edc12e84d8fff112a0cc3d177d3fbe96c3567532a93e6384157c2eca202975`  
		Last Modified: Wed, 24 Apr 2024 06:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f846cc9ad0f18ccaaa8385881df6be477a6820ff7756d3e4df0aba7fa367e0e`  
		Last Modified: Wed, 24 Apr 2024 06:53:24 GMT  
		Size: 80.8 MB (80813871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4c9301a2fdb185845ccb97a1038e220c172bf60a536388eeb18182a3a295a0`  
		Last Modified: Wed, 24 Apr 2024 06:53:11 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145ef1385bcc47e6def89590293d227c4a4cc47955e44aabef544fff13a640f`  
		Last Modified: Wed, 24 Apr 2024 06:53:11 GMT  
		Size: 12.8 MB (12782119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179cad1d94d9f124205b77f36f71f8e9af076ff701089fcc075819780de518a8`  
		Last Modified: Wed, 24 Apr 2024 06:53:10 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e10a999001f16e54b245a71d88f879b5238683179e1b2a272cf8848e525c4`  
		Last Modified: Wed, 24 Apr 2024 06:54:16 GMT  
		Size: 26.9 MB (26925542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95f9824cb9b9cce79f6514af44b360c0d05f0166cec3d1aedf2c333e5b764c`  
		Last Modified: Wed, 24 Apr 2024 06:54:12 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251008435f45f1a982d2529c6b50d1edd8e8e3d713881660861ab317a5f8baa4`  
		Last Modified: Wed, 24 Apr 2024 06:54:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5c7369199b1195151d0d87687cd06830ad21880c250a454ed7505a6f162947`  
		Last Modified: Wed, 24 Apr 2024 06:54:12 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e3603fe3688373527160d905baf2f6c19a0070b319f49c441e80ce9037bc4`  
		Last Modified: Thu, 25 Apr 2024 12:09:16 GMT  
		Size: 26.0 MB (26020186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f84c611eb10ed24b38a39450ea6e02763dba872afa0a1d729f4a095b9ce2fb`  
		Last Modified: Thu, 25 Apr 2024 12:09:17 GMT  
		Size: 9.4 MB (9442418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f452bb0d2d8feaacef67996926690f2663ef8c86625ff41f40565fb76e9762`  
		Last Modified: Thu, 25 Apr 2024 12:09:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19e7b28bfa0022b6ecce9042a55f850abdaefd7b74264708d6d8ef7f5340f57`  
		Last Modified: Thu, 25 Apr 2024 12:09:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfc7900c8f16f928283baa6957d3bf1429a6487f4ade7840ac657d1b97e2b06`  
		Last Modified: Tue, 07 May 2024 00:17:11 GMT  
		Size: 24.5 MB (24528042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a935f04fa081db663ee46b6c3ffe4449f0f9f4704d659e04d448a9368f3a2f`  
		Last Modified: Tue, 07 May 2024 00:17:10 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794c55d5229772d765046d0a804e66b6de51fabd20ae975cc0c8a53c4f35c3c4`  
		Last Modified: Tue, 07 May 2024 00:17:11 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:bd5635303c5d0a7286d62adcf7d7f63878cea0e43b624c9b1ad657552b8e1c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b452815635445f96d544e9ae5856d727e189a056f590abeec01f79ac0b1edd`

```dockerfile
```

-	Layers:
	-	`sha256:1e05c3c2971df9433549af4c00fb33d7def7b907c2c8243733e4f2abf41368bc`  
		Last Modified: Tue, 07 May 2024 00:17:11 GMT  
		Size: 7.3 MB (7281959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea24ae6d4675c2207c07a95412558b122573c4933f05babfc46bffa8782fb77f`  
		Last Modified: Tue, 07 May 2024 00:17:10 GMT  
		Size: 47.4 KB (47352 bytes)  
		MIME: application/vnd.in-toto+json
