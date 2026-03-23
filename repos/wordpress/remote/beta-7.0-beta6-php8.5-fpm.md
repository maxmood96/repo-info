## `wordpress:beta-7.0-beta6-php8.5-fpm`

```console
$ docker pull wordpress@sha256:cd31b8662f56d0c7b745f4e985e394819cdc31c6e00d59a4582c6949bd604682
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `wordpress:beta-7.0-beta6-php8.5-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:26ee602c3628642fda67abd4c716e1313e1e5bf661b9210f56927dbdc00a321c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269689154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039f1fc1067f68310fe758fbbb24fa2fbd57084fc16cd1adc8987b120da999a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:37 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:37 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:37 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:23:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:23:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:26:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:26:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:26:31 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:26:31 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Mar 2026 22:26:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:26:31 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Mar 2026 22:26:31 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:58:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:59:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:59:47 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:59:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:59:49 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:59:50 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:59:50 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:59:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:59:50 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:59:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:59:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bfc04276de842bbd7ec663f5ed69e77e5e06a79c1b340f21b562e8d6676991`  
		Last Modified: Mon, 16 Mar 2026 22:26:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d7a9f06d959e4d7c9ea3dc71b17405c3444e2af02440637b3db72cb6aaa55f`  
		Last Modified: Mon, 16 Mar 2026 22:26:55 GMT  
		Size: 117.8 MB (117843317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd6a0fe53a46bd299465c450245565cbb8cbda47d3dc88a12d9aa281159b8da`  
		Last Modified: Mon, 16 Mar 2026 22:26:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639661be175104eeaa882eac399a5bbffdc0d3afdc20f5a2f6e85afe8d530a52`  
		Last Modified: Mon, 16 Mar 2026 22:26:52 GMT  
		Size: 14.5 MB (14496660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8056ae48a9894976068f38a28021aa2f284b7b980b96793ca1db74dc4a94fd6e`  
		Last Modified: Mon, 16 Mar 2026 22:26:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fb90563f01b699c7cd724271e4318382359f7e13ca47016628a2c78172789d`  
		Last Modified: Mon, 16 Mar 2026 22:26:53 GMT  
		Size: 15.1 MB (15098265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ef16d987156c59cfad436a97fadfa4832762d3d24ed9f5982291e82d37623`  
		Last Modified: Mon, 16 Mar 2026 22:26:54 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fbbfa49dcff0fdd0ba7d54d5b151448748a111df97cda6891af8cc7ba42a79`  
		Last Modified: Mon, 16 Mar 2026 22:26:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735209b1f637ab11aca2f4541ad80ad70befcc0dd1059b23be1e909fcc0a4092`  
		Last Modified: Mon, 16 Mar 2026 22:26:55 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3ea610cf480be390c7f02fdc10478ae9de7a5c050a8af9e893426f7d24b338`  
		Last Modified: Mon, 23 Mar 2026 18:00:14 GMT  
		Size: 33.1 MB (33077307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af139e950c923ec54bb01a98e12a1f4f5d5b148ce0f90dd7218d696a08323f79`  
		Last Modified: Mon, 23 Mar 2026 18:00:14 GMT  
		Size: 30.0 MB (29957853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b130ec1a540a3a6217117e1088f26a40be1d0af4cc0fafda3363220fa199e9`  
		Last Modified: Mon, 23 Mar 2026 18:00:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12687d43e56defe02e0ed64bae15032e5200e5349cb131122022b92e2ca7e7d`  
		Last Modified: Mon, 23 Mar 2026 18:00:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799a5fbea2438e329b5bec048241b38f5a5000b518552b107ee4e982934afae9`  
		Last Modified: Mon, 23 Mar 2026 18:00:16 GMT  
		Size: 29.4 MB (29422225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3322ee78b2a0e5cfd2c020335f23f0baf16d264f5489946f547ae887ef362841`  
		Last Modified: Mon, 23 Mar 2026 18:00:15 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b5bd72261a54d588bf4c64abcdb5287b45830e92324f06d35eb5e79bd41beb`  
		Last Modified: Mon, 23 Mar 2026 18:00:16 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8d387ad30f2250172fbb445085b1a8d54cbb3474f30d2af3b750edb7fe3116`  
		Last Modified: Mon, 23 Mar 2026 18:00:17 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-beta6-php8.5-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:67ee6c91ebf9c4c9578b8a8150a289f39be570b80105aea977cbee23fdc062f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8220198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7d6f1a3fc4d934cd65aca5f14ab474d04ddbb7c68cd8a1d513159c5dd18dd6`

```dockerfile
```

-	Layers:
	-	`sha256:1636fff704026852e698805a1c82dc8663ec113abe3fedf662ca47b8644c2d3c`  
		Last Modified: Mon, 23 Mar 2026 18:00:09 GMT  
		Size: 8.2 MB (8169104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e178c859690672f0521d31e4da645d04cb551020be56cd2d52b4603e9672a3d`  
		Last Modified: Mon, 23 Mar 2026 18:00:08 GMT  
		Size: 51.1 KB (51094 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-beta6-php8.5-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:19d9f2b228e638e0b29cd1728191ea3fdcba4afbd4fb1671d500a70e7396b160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237457693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3a1dcb455fa636ccc5cd64da621adf86f594fe667e6dc93cc1db11d957f0e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:21:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:21:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:21:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:24:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:24:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:24:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:24:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:24:44 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:24:44 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Mar 2026 22:24:44 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:24:44 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Mar 2026 22:24:44 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:57:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:00:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 18:00:36 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 18:00:36 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 18:00:39 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 18:00:39 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 18:00:39 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 18:00:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 18:00:39 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 18:00:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 18:00:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67109b30418fade3cc247e45c3ed938e25be0887dc5b7ec9711757e13eb729f6`  
		Last Modified: Mon, 16 Mar 2026 22:25:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a3c18230f4eb7ef08a545aad6852c10d8471e14a4d66cfdea78863ade20f5c`  
		Last Modified: Mon, 16 Mar 2026 22:25:05 GMT  
		Size: 94.9 MB (94883918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f024949353510a8bb767480fa0e00918e2116ae0cbcd9ef7117e3f35ca10f`  
		Last Modified: Mon, 16 Mar 2026 22:25:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a67da1a8eabfa87f90849a92a85f212a608c65b2dd9a9b923706542cb7b76a6`  
		Last Modified: Mon, 16 Mar 2026 22:25:03 GMT  
		Size: 14.5 MB (14494472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d46768580041f34d74fe736aeba039335202d383860acf912e360acefe1245a`  
		Last Modified: Mon, 16 Mar 2026 22:25:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d65fad78ad43449a0a7e59961307208f1d5c279513285bc309043f167f1609`  
		Last Modified: Mon, 16 Mar 2026 22:25:03 GMT  
		Size: 13.1 MB (13122243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06ebc1bcaed70d309696e7194176e81cc7abf6a4e77c948134631546ab834df`  
		Last Modified: Mon, 16 Mar 2026 22:25:04 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dfca7ed1a04266c251e5f4619be684dba07e45239ad0a38d39e12d8f7ad80c`  
		Last Modified: Mon, 16 Mar 2026 22:25:04 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897d04c797925cff1f411176731d929cf475cc795762f82e77b6f14278c1a417`  
		Last Modified: Mon, 16 Mar 2026 22:25:05 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce61fa8b7455eedd3455765cbda8edc1ee3ba47cb18b08a0a36ed76d8b02ac55`  
		Last Modified: Mon, 23 Mar 2026 18:00:56 GMT  
		Size: 30.3 MB (30251589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd6cf509f47333bceeacdbe2fb782e13dd93aa450ff274e1b7c45a470ef6681`  
		Last Modified: Mon, 23 Mar 2026 18:00:55 GMT  
		Size: 27.3 MB (27321530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae75201d652fe4515d38299324f60914b622c9afeabbfd7219a8971b52983f9`  
		Last Modified: Mon, 23 Mar 2026 18:00:54 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c33df996907a106b206d86a1249c1064544e1a7c42e38cc738bc7fc053d534`  
		Last Modified: Mon, 23 Mar 2026 18:00:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09feb9be707c306131bdf6a3875e5e67014ed01f84065d55250f8962c5f10053`  
		Last Modified: Mon, 23 Mar 2026 18:01:02 GMT  
		Size: 29.4 MB (29422248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff0c824ec1389c96ae85fac5c479b7a0194a2b18ea6f9f41c6c66e8ed5b3e02`  
		Last Modified: Mon, 23 Mar 2026 18:00:57 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ec6828b99fdb257a77749d33d55e7df575fe85b23fd4b6d467896d1097107`  
		Last Modified: Mon, 23 Mar 2026 18:00:57 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff57cc3713237e1aa7708ed5070e0d88c099a90d3206ad77cf0ed7e0cfa0afa`  
		Last Modified: Mon, 23 Mar 2026 18:00:58 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-beta6-php8.5-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:a7ac864e2ac1d87ba3b522d67d1c30c3557e48bbceb38e890422a9bbb457423a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8013849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9aeadc49f80aacfd77445042a6d09943f4f915a9e3358acd18aaaae1e6f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:013dc1ca540058072423b66a7f6e7add314c7ffcaa080419c287405b433ac9f0`  
		Last Modified: Mon, 23 Mar 2026 18:00:54 GMT  
		Size: 8.0 MB (7962619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357dc6fb0df042fc7381588480ac0799128355a2670faa2311f1089142aa4603`  
		Last Modified: Mon, 23 Mar 2026 18:00:55 GMT  
		Size: 51.2 KB (51230 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-beta6-php8.5-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:0bc191c1f03d216cb47bb763d6d7f9645e2afe51ff374339ee3853859ba01eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223698063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc40c75e330d2df0c55a5be9eec533cebf50805a24aee8ba7d63ef7bc7c53c85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:26:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:26:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:26:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:26:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:26:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:26:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:26:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:26:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:26:18 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:26:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:26:18 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:26:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:26:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:29:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:29:16 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:29:16 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Mar 2026 22:29:16 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:29:16 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Mar 2026 22:29:16 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:01:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 18:01:36 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 18:01:37 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 18:01:39 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 18:01:39 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 18:01:39 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 18:01:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 18:01:39 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 18:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 18:01:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dbcf12a041762aec487c7ae193b0f00cf952314493809750d8365c46111289`  
		Last Modified: Mon, 16 Mar 2026 22:29:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7f2142d5912fe46a835758bde4e52b74e23c1ece70c00eba610f183a57a971`  
		Last Modified: Mon, 16 Mar 2026 22:29:35 GMT  
		Size: 86.2 MB (86246355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f1ed7ad022b6a4265a9804fc09ad6373c3fdeedf57c44ae6dbc687354c4d68`  
		Last Modified: Mon, 16 Mar 2026 22:29:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837622fa908720b6d4ca1cb3a652967045cdd894cebf9139ad22fcb6d6bb4e27`  
		Last Modified: Mon, 16 Mar 2026 22:29:33 GMT  
		Size: 14.5 MB (14494523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db83328c63729fe3168f385e4f1f42acccd4a6e810b495db6133ae4e8d046242`  
		Last Modified: Mon, 16 Mar 2026 22:29:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fa1952c5e14b21db0235881d81d76189b4f7109c60c524ae1c94b04a80a58a`  
		Last Modified: Mon, 16 Mar 2026 22:29:34 GMT  
		Size: 12.4 MB (12421785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1540e4c6aeff2f5316d0e9862ea6c93b36ca7deb4c0730a5efca2279f6404008`  
		Last Modified: Mon, 16 Mar 2026 22:29:34 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76c200d485eef207be29c417fbc7f566acd97c58d87ada41ea78a28b4093332`  
		Last Modified: Mon, 16 Mar 2026 22:29:34 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36132803f5e2ce3adc804cc7ac21fd6f7df8668b5e6fd6e5268e026b77efe00`  
		Last Modified: Mon, 16 Mar 2026 22:29:35 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a497737ff5a2ca091439ebbebc262dfa551c0c6620da41a00a7984914173da`  
		Last Modified: Mon, 23 Mar 2026 18:01:55 GMT  
		Size: 29.1 MB (29134092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c73ad3e34539956cdef03aceca4ca659c87ad972c1c8840eb5e1144673bd3f0`  
		Last Modified: Mon, 23 Mar 2026 18:01:55 GMT  
		Size: 25.8 MB (25751533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37c784862d050d90fe56baeec3151ae2a4dcb61f416e4c0374ebe3d777ffa3b`  
		Last Modified: Mon, 23 Mar 2026 18:01:53 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb25d3876ee1fbcb0a5c1e11b6b8b313805d7812d14301c971fffef939441333`  
		Last Modified: Mon, 23 Mar 2026 18:01:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19686c17a2d07c70e48010c429bddf6a976a8b5a9c8cf121a3f772aeec35be7c`  
		Last Modified: Mon, 23 Mar 2026 18:01:55 GMT  
		Size: 29.4 MB (29422233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525c5190f6d18bd8000da4a7456a80bea56089c0a9c98efa99614ff4872745c`  
		Last Modified: Mon, 23 Mar 2026 18:01:55 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007260aeaa144913b127d46318bb4cff4cba606c636011148778444684187d9`  
		Last Modified: Mon, 23 Mar 2026 18:01:56 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b9ca0dbb53c430ef52625244b06ce98c3880a70b4caeca46d9f58585923758`  
		Last Modified: Mon, 23 Mar 2026 18:01:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-beta6-php8.5-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:9ee668e9f52e1462e9e6db928facb1941d60c6448d6e2fe81661527f87131725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8018654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f6f3a93af64cc4aba69ebfd68161a329b3ed66d83a0fa9ef78dc2e33e40b8d`

```dockerfile
```

-	Layers:
	-	`sha256:b4a8c60b4f587bfdc99cf4c86db3ddf6b93d5919add4052e69f632e9f97dd028`  
		Last Modified: Mon, 23 Mar 2026 18:01:54 GMT  
		Size: 8.0 MB (7967425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcabc13500a4a0dc67eabe0108df788d93367244a0d34b884244b372ebaa2892`  
		Last Modified: Mon, 23 Mar 2026 18:01:53 GMT  
		Size: 51.2 KB (51229 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-beta6-php8.5-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:a8569095d79e48f55bb7147d0713b4ac4ae9fba26c6e2b99d7dc7fd3336ab1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261769324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10169f8e17fe72ed9b6b5a7e0cac19e08f6c25407e1ab9edc1d25e86d436a38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:30 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:30 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:23:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:26:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:26:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:26:52 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:26:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Mar 2026 22:26:52 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:26:52 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Mar 2026 22:26:52 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:59:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:59:35 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:59:35 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:59:37 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:59:37 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:59:37 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:59:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:59:37 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:59:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:59:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf55292cba35574d976334818d78ae3296742b3703fb0c9b5562caaa88ae8679`  
		Last Modified: Mon, 16 Mar 2026 22:27:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6647f2d9b55b99772381739d5db354a3ee8f29887906be17b2011f4fb71ca72e`  
		Last Modified: Mon, 16 Mar 2026 22:27:15 GMT  
		Size: 110.2 MB (110164985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aea9d42a7f8f60d35ec4e7a9ff0938f5a47c223e702f44e839d20c1a6d951ba`  
		Last Modified: Mon, 16 Mar 2026 22:27:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c575bcb5449a00a9b955f8f3eb70faa13c8f6b28e935e39029bd18a1bd3ab5`  
		Last Modified: Mon, 16 Mar 2026 22:27:13 GMT  
		Size: 14.5 MB (14496280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43f89fc05ad2c41b812c3657664471d81b593f2b21bd93c4c818ab212c7a767`  
		Last Modified: Mon, 16 Mar 2026 22:27:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745b9664baabf9927bfa00ea18ee8c5f9ab0703e6083f79259b04df4d350294f`  
		Last Modified: Mon, 16 Mar 2026 22:27:14 GMT  
		Size: 14.7 MB (14674477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d178e628fdfc7d01543fb8b1a4f0c78abcb0794ad022da455169c2ab019360a`  
		Last Modified: Mon, 16 Mar 2026 22:27:14 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1596368d1785c3870c6f89b177744d9151ac4b3f848e7db494e96a5f2d8dff92`  
		Last Modified: Mon, 16 Mar 2026 22:27:14 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aafa5fdeffee721753cbaba88f77314b85dde1a299676a34b52c93be2b6670`  
		Last Modified: Mon, 16 Mar 2026 22:27:15 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9910df2b11f156564fae5ce198bee3008705a12d360c12c367adcf478b272616`  
		Last Modified: Mon, 23 Mar 2026 17:59:55 GMT  
		Size: 34.6 MB (34577695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c97070b618d2280dd10a7cab451a6a4f6c9268a27d65ddf6f3ccaf1ec5bc202`  
		Last Modified: Mon, 23 Mar 2026 17:59:54 GMT  
		Size: 28.3 MB (28277207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70b045878797a345a721c86a4f8523df446a6bfe0af034e036b9f499a0c74f9`  
		Last Modified: Mon, 23 Mar 2026 17:59:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396de371ac33c8caaaad8fecc9ed1ea355aa8eadf2242d1952b7aa49056ba63f`  
		Last Modified: Mon, 23 Mar 2026 17:59:53 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8793f0d29febffcf6488605416fa9738129bd9e53efdb5e17eedc50777f9a4`  
		Last Modified: Mon, 23 Mar 2026 17:59:55 GMT  
		Size: 29.4 MB (29422228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b64baa87b8d9af443b7ae9f7f92ddc7d48e0898c669d2ffe46a2437ff3b62cc`  
		Last Modified: Mon, 23 Mar 2026 17:59:54 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40ae2908942be3df0ff93ee0201492bbfce08d5e92c3ece49aec867d93545e9`  
		Last Modified: Mon, 23 Mar 2026 17:59:56 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db9f5853e666e4f71bf6acae618a35da88796daacdf88524e1670f7ea2bc656`  
		Last Modified: Mon, 23 Mar 2026 17:59:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-beta6-php8.5-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:19bd4c48e865da8c2937930202d771890194525ee253d1fafd6999f42f188daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8316834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1a8bd9c611b8f83c5abe504178aa371d01bfbccfdfa6b6dbc802830af5ae2b`

```dockerfile
```

-	Layers:
	-	`sha256:09829a4d972af5432e0d71ae44209c8d671bc128d2016acd7273e902f1a77f55`  
		Last Modified: Mon, 23 Mar 2026 17:59:54 GMT  
		Size: 8.3 MB (8265562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d951f11405f425b7807728b4e0f6baa6afdbe30e58d62e30b657ddce3ebb7a`  
		Last Modified: Mon, 23 Mar 2026 17:59:53 GMT  
		Size: 51.3 KB (51272 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-beta6-php8.5-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:6bf29c3c0f1927d075120acc19c98ff88f1610546d23d764f8234f8a0ca7b4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267350177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8019ccf3ae8900647d8bc6fe9a2cf58e4ce839b0dabc5ba917fea0588a92687c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:19:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:19:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:19:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:19:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:22:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:22:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:22:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:22:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:22:33 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:22:33 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Mar 2026 22:22:33 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:22:33 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Mar 2026 22:22:33 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:53:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:55:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:55:33 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:55:33 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:55:35 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:55:35 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:55:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:55:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:55:35 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:55:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff18cd405b0077f8c0cc220744ee2fd3352b9a92a1ec478206127eeeaedf01`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6834162b03896936de217cd3bc496c3a3bbc10417cad5f4f6f4c703fc07e4c`  
		Last Modified: Mon, 16 Mar 2026 22:22:54 GMT  
		Size: 116.1 MB (116144065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa4986b735ced1046b1a93e12899e1fc9147484cbe2cf1d6e2ff6e99e61ed8`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca82738ce9e1d09bbc572a9240b4b21edbf2c037ed8ef29fca5e2e209cc5f073`  
		Last Modified: Mon, 16 Mar 2026 22:22:52 GMT  
		Size: 14.5 MB (14495737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa55962f7c9d74d98b5b72393ade078c3f06d38e58ada18dd561ca915aa9f1f1`  
		Last Modified: Mon, 16 Mar 2026 22:22:52 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fbd612b57e4757f72c3057b86b42b7d9020b85fad7c646505fe06af6aeb00b`  
		Last Modified: Mon, 16 Mar 2026 22:22:53 GMT  
		Size: 15.4 MB (15426738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cdc1b6b9eacdbca532f0754b9ce89ef2891aab442be86e8cdc760b5aa7aa8b`  
		Last Modified: Mon, 16 Mar 2026 22:22:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58db258898f1bb98ccbe650b905643d88c7a4d0c7c29a153202c4d4724773904`  
		Last Modified: Mon, 16 Mar 2026 22:22:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541aab7ddce49d10d3ba45532145196263f48e165dd574903c1437af21cb80db`  
		Last Modified: Mon, 16 Mar 2026 22:22:55 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e6da58b7d6761cde09d69d970bd2a1bede175bf1ba6ec94e7c9891d7c579fe`  
		Last Modified: Mon, 23 Mar 2026 17:55:51 GMT  
		Size: 32.5 MB (32530575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a22f755ae6f361f61e72cb72216b27fc3bbc93b9bb3f1a29d8eaef67ad5d62d`  
		Last Modified: Mon, 23 Mar 2026 17:55:51 GMT  
		Size: 28.0 MB (28021644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04aacf1d11ecf71e894c60f895f2b19040c1b21d1a582e81ca68beaa6cafa3f`  
		Last Modified: Mon, 23 Mar 2026 17:55:50 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351f41fb5e2eddb208c43f34b5989c2ea77fb2b51048f19917f947ced52bb418`  
		Last Modified: Mon, 23 Mar 2026 17:55:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7b5d061ed155189a33822cdbdb38ee5539a47e8f7f1caa0b7c0ff505009d6e`  
		Last Modified: Mon, 23 Mar 2026 17:55:52 GMT  
		Size: 29.4 MB (29422237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfce14985375d0d26219dba8524a8b2c8439b94fec7275aba3c9e243a38540ac`  
		Last Modified: Mon, 23 Mar 2026 17:55:51 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1473c71faee621380bee1c1b7e2c232b5f82c666f6d8f1a9f7c045496179f9ce`  
		Last Modified: Mon, 23 Mar 2026 17:55:52 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c3d44c66ad13113bb7b9bd132827967fc6e5014e1e46e310d893f71da084d`  
		Last Modified: Mon, 23 Mar 2026 17:55:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-beta6-php8.5-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:1bd388ffe340b7c422d89b765c659ed760c1f37ff60a28aee819afb866823f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c7b1cc439ee131e4b1d5ec7a6f2dbb44117bea2f9bb7f9f7256bf886ad50d8`

```dockerfile
```

-	Layers:
	-	`sha256:b935572ecfffc82e21fd64b52ad2e1596a31193b74a769b19f34998e0b41e05c`  
		Last Modified: Mon, 23 Mar 2026 17:55:50 GMT  
		Size: 8.1 MB (8142156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d74587694bfabe8c8c34857fcb86d4fc9ce0286e5700cbcb9b0a8c6c75d4c58`  
		Last Modified: Mon, 23 Mar 2026 17:55:49 GMT  
		Size: 51.1 KB (51052 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-beta6-php8.5-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:867e91a9ffb6506492bdc758c450a6112e94d88867f2db7e8ef7841c1f5ba1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264692028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855e802a2fc4df847469115af04abcd5eb7575216f7cfd79b33d21a9c64b2c2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:08:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Mar 2026 00:09:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Mar 2026 00:09:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Mar 2026 00:09:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHP_VERSION=8.5.4
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Tue, 17 Mar 2026 00:15:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 17 Mar 2026 00:15:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 00:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 17 Mar 2026 00:19:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 00:19:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 17 Mar 2026 00:19:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 17 Mar 2026 00:19:24 GMT
WORKDIR /var/www/html
# Tue, 17 Mar 2026 00:19:25 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 17 Mar 2026 00:19:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 00:19:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 17 Mar 2026 00:19:25 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 18:15:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:19:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 18:19:29 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 18:19:30 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 18:19:33 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 18:19:34 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 18:19:34 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 18:19:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 18:19:35 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 18:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 18:19:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb03c46c4e3a31e2b4f495c9335dc55280c3ab8757fca7a09e34292dd392624`  
		Last Modified: Tue, 17 Mar 2026 00:14:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b32d1fdb741701192f7fb2aa3e0f0fe279555c73025c4d8e2bfe3afe82dca7`  
		Last Modified: Tue, 17 Mar 2026 00:14:55 GMT  
		Size: 109.6 MB (109598843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c8e58deeac398c483ddeffcafbfedcad200b501b9842a4972a58d96d41f222`  
		Last Modified: Tue, 17 Mar 2026 00:14:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b774b60bd18a475b9690e672b174b06068262b069659f65d12a078c43064a8f5`  
		Last Modified: Tue, 17 Mar 2026 00:19:50 GMT  
		Size: 14.5 MB (14495959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512866702aa1aadf8fe9116afeaebafa016bd81b74c028c375d83a8bec14315`  
		Last Modified: Tue, 17 Mar 2026 00:19:50 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abba38e4d2439b95b1337ac4c997ce3d9b00b8edf94355d620bb4eb02843f3f7`  
		Last Modified: Tue, 17 Mar 2026 00:19:50 GMT  
		Size: 15.2 MB (15219880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3c9aa6a29b83265a97930462a77c03f721750729bf1b9aafd7b1ecda81e671`  
		Last Modified: Tue, 17 Mar 2026 00:19:50 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28795876fa64d77bd91c94d18c8f6091a03c7faf4e2d94f7153b360ecefede7`  
		Last Modified: Tue, 17 Mar 2026 00:19:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e1bb19af38fbd393ad70745cd14647d86f8318cddb8cbdc2b1018cf6cdf8b`  
		Last Modified: Tue, 17 Mar 2026 00:19:51 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f722fc230a0fafb77517427bff5fd550ee85d04cb75fa4324c327adf0e79573`  
		Last Modified: Mon, 23 Mar 2026 18:20:12 GMT  
		Size: 33.1 MB (33079021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1cab24b0b53d41c7c10a8f8cb7c170c59776e4625a16a7ba77196c8bb3bc16`  
		Last Modified: Mon, 23 Mar 2026 18:20:12 GMT  
		Size: 29.3 MB (29265183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4df093ea9c3662591a43fd5f5402a0003bdbfe96942a07bcd9e63315acf83f`  
		Last Modified: Mon, 23 Mar 2026 18:20:10 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4305b36b6a5b6d1e6e7e74c8a58896bce9f3e9f7a34e192f5abc3faaa64320b1`  
		Last Modified: Mon, 23 Mar 2026 18:20:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde61331c4b59e1762c62bec258507e3bd5729d3878d7cc56ffb8287f8c33dda`  
		Last Modified: Mon, 23 Mar 2026 18:20:13 GMT  
		Size: 29.4 MB (29422253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cd2f9179ab2cabfc9bfeda6fdb8cefa97457d5f4de8a2a121ead3263a8dcc7`  
		Last Modified: Mon, 23 Mar 2026 18:20:12 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd968dddf2b66873ced20f8379566c119ac1c3b0dc4ccbd1a28e6d34e03049`  
		Last Modified: Mon, 23 Mar 2026 18:20:13 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2282c35b4d0294426d7a37792f09869f81cbc9c41b8a25b1212030f80dff7ab`  
		Last Modified: Mon, 23 Mar 2026 18:20:13 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-beta6-php8.5-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:e64ecb74dc5a57b2645d3a05a326cbd7bca70397d46aaea127726e92add26629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8221001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9a8a00fcc8a5e9bfbc4337aefa0a9d2a0d967c2c07efcc96cde0bf816b18f8`

```dockerfile
```

-	Layers:
	-	`sha256:6b2f4dd02b70ee6a86046561ac9bf33c3ed12ab8d8f876312bf4850100aff3d1`  
		Last Modified: Mon, 23 Mar 2026 18:20:11 GMT  
		Size: 8.2 MB (8169853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e29ffcde4bf815ade74b4dca00077879b146f00419c55fce1dbf243f43ea4293`  
		Last Modified: Mon, 23 Mar 2026 18:20:10 GMT  
		Size: 51.1 KB (51148 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-beta6-php8.5-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:e6a0d4054f97c8e750213e86292f7d8a39c698b160aaff9814018299f002e2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239597221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806a06b55029940da40718b969deb7608596a8f62a33693eac733592dfa87954`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:24:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:24:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:27:38 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Mar 2026 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Mar 2026 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:56:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:58:06 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:58:06 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:58:07 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:58:07 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:58:07 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:58:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:58:07 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:58:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:58:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e46e1620cd3c7b7f036b3a3391ed3db0eed8e0946fff1e1c7a8addcb819cdd`  
		Last Modified: Mon, 16 Mar 2026 22:28:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868826499ca4d1a10f9f3e2de04ae7b4901b5b977edec1a6ab8f3e89e3e34448`  
		Last Modified: Mon, 16 Mar 2026 22:28:09 GMT  
		Size: 92.6 MB (92572934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e80ff3c161d147a6f738605c2420c1c12dfb5085d94b0bd3c6c19c7f6225ebf`  
		Last Modified: Mon, 16 Mar 2026 22:28:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46395d7dd05cb2b945f9bd7e8e20ee4eb4e032abd6cbc7155969c6923eb6017c`  
		Last Modified: Mon, 16 Mar 2026 22:28:07 GMT  
		Size: 14.5 MB (14495251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c96f24e449920b3b121e350829ec71ed0083be87193e18b6a5cc9458581d85`  
		Last Modified: Mon, 16 Mar 2026 22:28:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf22a13f025ea7af25a04213822b691c1e6a8389b87ea5156d3a3a13ab7908c`  
		Last Modified: Mon, 16 Mar 2026 22:28:08 GMT  
		Size: 14.4 MB (14403054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01d5727455eb5f28276f3adbb175526538c76d264ea23053c373cc9b0991f6a`  
		Last Modified: Mon, 16 Mar 2026 22:28:08 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3c2e6e52d60b1afb03323ce4acf421f026fd40d9916ced3991e9b0689f789f`  
		Last Modified: Mon, 16 Mar 2026 22:28:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de17a702659a5abdac7997e366b955386c2f24256da84b2b232a919da372fc3`  
		Last Modified: Mon, 16 Mar 2026 22:28:09 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4da8639db12f7438183054aea651385af4f565c51ec3d3b978719df61195c7a`  
		Last Modified: Mon, 23 Mar 2026 17:58:29 GMT  
		Size: 31.5 MB (31523261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5d71167ddc0fa10e18dc5ed5e03a70787a150bb8fab93abf703fd329236471`  
		Last Modified: Mon, 23 Mar 2026 17:58:29 GMT  
		Size: 27.3 MB (27327169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f8f834818d3c77f59c8d3bf925b2a6c8e6e3c99acd1b51782f2366b444c2e9`  
		Last Modified: Mon, 23 Mar 2026 17:58:28 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fa2c6726aafaaed944a14e6582ab7887269ee9db43c8057333518b7a598981`  
		Last Modified: Mon, 23 Mar 2026 17:58:28 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b20b3561e11638c00ae35216eeff76a21e7e829f2abe1b8121c4f68a5dc6b2f`  
		Last Modified: Mon, 23 Mar 2026 17:58:29 GMT  
		Size: 29.4 MB (29422249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d6f00f9d55f2d51fcf412d35e917d73ab1aab43b00ab3b603b6f2836aa456f`  
		Last Modified: Mon, 23 Mar 2026 17:58:29 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad89c2defc24f6407d7ea3bcfe44f3a2e3584ceac0d4c9e0acb918f3e4ecbe5`  
		Last Modified: Mon, 23 Mar 2026 17:58:30 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca6db3925f3d773d2f82bbff4ac213ea6f8b8f0a308f14f1ff951010ea87adb`  
		Last Modified: Mon, 23 Mar 2026 17:58:30 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-beta6-php8.5-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:f6a7ff3189dc79feac19082202e557f9ec19bc83fdb49501b3098211e65ca571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7939339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51de482e25a2490ca3b48e215b9dc6fb5056b8cebff4c4087ba2e03d6db5d130`

```dockerfile
```

-	Layers:
	-	`sha256:23089877e27a66c3c3fc58e0a105f0bc5c5172889c1e9292d5973dbd8fcc2d0c`  
		Last Modified: Mon, 23 Mar 2026 17:58:28 GMT  
		Size: 7.9 MB (7888254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8a6c4f41c9ab353c48f7cc87e1579bdb8461779c9ebde92145cf861500eb09d`  
		Last Modified: Mon, 23 Mar 2026 17:58:28 GMT  
		Size: 51.1 KB (51085 bytes)  
		MIME: application/vnd.in-toto+json
