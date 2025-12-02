## `wordpress:beta-6.9-RC4-php8.3-apache`

```console
$ docker pull wordpress@sha256:163b5f1fa990d93672bc507d378c90f8858c37426b2c60224cea8aaa423c9152
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

### `wordpress:beta-6.9-RC4-php8.3-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:2f09f18334f24267bfaee40676e4a53cbf213bb302cd53fc55380a7bebe6b93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263604973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9c0b0e6608dd344d111b13f9f71c43c838d255a6fa36c4aa788d98d58df534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 19:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 19:46:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 19:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 19:46:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:46:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:46:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 20 Nov 2025 19:46:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 20 Nov 2025 19:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 20 Nov 2025 19:59:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 20 Nov 2025 19:59:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 20 Nov 2025 19:59:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:59:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 19:59:44 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 19:59:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 19:59:44 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 19:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 19:59:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:02:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:02:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:02:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:02:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:02:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:02:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Nov 2025 20:02:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:02:31 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:02:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 20:02:31 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:12:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:14:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:14:02 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:14:02 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:14:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:15:53 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:15:53 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:53 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:15:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:54 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:15:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff292d92bef83ffec9666e45f901f0d30bf38f82f60acab0ecb997e8f209816`  
		Last Modified: Thu, 20 Nov 2025 19:50:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d3fccd4e77db6611a31b994365100d8af0f883a67d8b7c764372ec5781a716`  
		Last Modified: Thu, 20 Nov 2025 19:50:45 GMT  
		Size: 117.8 MB (117837773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e42a571877751a680881ab35d3ee6a970fc353cd0918c52e1490714ee015935`  
		Last Modified: Thu, 20 Nov 2025 19:50:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1786c40e6ef688eff9dfaa8bd892244bf3725770b0506de2e71f182d6b844488`  
		Last Modified: Thu, 20 Nov 2025 20:03:03 GMT  
		Size: 4.2 MB (4224512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d546c1d12a7f5b1adab9d18b80ae819f29d952c39962df4402bda1cb79ea27a8`  
		Last Modified: Thu, 20 Nov 2025 20:03:03 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64709930f96860c86fb81dd91764fa02cd08583f4f7eb509cf639f26056e9120`  
		Last Modified: Thu, 20 Nov 2025 20:03:03 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a33af9a2e4b89743a10d32f6eab4fc58855a83d9512ba38a9e0310663cf477`  
		Last Modified: Thu, 20 Nov 2025 20:03:05 GMT  
		Size: 12.8 MB (12770181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95356b5f4836991a9fb3cc9f738d39937b0d2c555d283d47149662b05c25303`  
		Last Modified: Thu, 20 Nov 2025 20:03:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3cf1a078fa60e6b409a1eed7a94e8660328ac457c46a38fe7c0d75a9b8489b`  
		Last Modified: Thu, 20 Nov 2025 20:03:06 GMT  
		Size: 11.7 MB (11713316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba783666fd704a0b7dbd9db31dc04c1c02064ed311178468b9bee41dddfe76d`  
		Last Modified: Thu, 20 Nov 2025 20:03:03 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387c70da0b5e0a67a052f2b9e459a8aaa819274dc722c62ed8b241b2afe43211`  
		Last Modified: Thu, 20 Nov 2025 20:03:04 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c8c18e18cea5af6368e7e123beb0a26a16ac13dfab72185cea35439364b186`  
		Last Modified: Thu, 20 Nov 2025 20:03:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9ad8b7fb7ab8a2543831c595e629dcc722ca43301aaa06f3caa3f73d1e778`  
		Last Modified: Thu, 20 Nov 2025 20:03:04 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e701ee4b7b2017978b3f4b61f9bb8434f84a2e8e86cfc0c843ec7a959450649`  
		Last Modified: Tue, 02 Dec 2025 01:14:45 GMT  
		Size: 26.3 MB (26297218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d867254d438f52e86680db969d7211c6092d815121c257a19fe6d0509144cf`  
		Last Modified: Tue, 02 Dec 2025 01:14:47 GMT  
		Size: 33.9 MB (33931201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17988f9e24c91bd427accabe638fbfca5c926ffc5867ac327124b7b113373348`  
		Last Modified: Tue, 02 Dec 2025 01:14:45 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f4c48d5338a38b381fa53bff45357d5b41d68d3765a4598fdf7f1d39bdae5a`  
		Last Modified: Tue, 02 Dec 2025 01:14:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbc612be48fbba1bd72e9b3210b724dd07d04cad523e298effd767fa27b2551`  
		Last Modified: Tue, 02 Dec 2025 01:14:43 GMT  
		Size: 18.8 KB (18798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126dca9879109535687e4fbec1474b786d5ac12e3d7d084be993cf62fb9e8d43`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 27.0 MB (27024640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abcc5efac817da3d0535969a91005aa777277b16dbb5e0b1d3bb08f6ba65194`  
		Last Modified: Tue, 02 Dec 2025 01:16:28 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba550f76ee32a49fa0db124d2f89aedb3f0c648c060b3f4ef7755688d69dded9`  
		Last Modified: Tue, 02 Dec 2025 01:16:28 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326904dc441b15b2323c72e5478d4eab088d291c37f549d508598b8e762634fd`  
		Last Modified: Tue, 02 Dec 2025 01:16:28 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:3ccd5a0cab1475dc734c7fc6487504a90021c51247772e4bd9e4e17a2a4db4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8742065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efc080f1fa2f17c29f3b3eb654e6c96624178efd6da5abdfb4f55103f044525`

```dockerfile
```

-	Layers:
	-	`sha256:9cdb6eba2f80732e6cd4c21501a10971e90664a7a093e48e1747b57047bceb3c`  
		Last Modified: Tue, 02 Dec 2025 02:24:20 GMT  
		Size: 8.7 MB (8674126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675382f5ca5302760eaf35c7ab67c37936c2bcf997a3fe8ccb22d8c9dbe84a57`  
		Last Modified: Tue, 02 Dec 2025 02:24:21 GMT  
		Size: 67.9 KB (67939 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:6dabf44f3d7ac5e3a55d61e04b00018fab951619178b830ede9d5b01d016d684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233103168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7eb646094e128ca0aafc92986f42ea21d17b9e946c82a60d6989c968f37fd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 19:45:14 GMT
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
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 20 Nov 2025 19:45:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 20 Nov 2025 20:02:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 20 Nov 2025 20:02:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 20 Nov 2025 20:02:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 20 Nov 2025 20:02:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:02:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:02:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:02:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:02:12 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:02:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:02:12 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:02:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 20:02:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:05:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:05:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:05:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:05:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:05:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:05:21 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Nov 2025 20:05:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:05:21 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:05:21 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 20:05:21 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:08:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:10:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:10:24 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:10:24 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:10:24 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:14:36 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:14:37 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:14:37 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:14:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:14:37 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:14:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:14:37 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da33d5eae4dbfed4d5c047e03116c9ae48796afa779edf11242b9c767eea5ef`  
		Last Modified: Thu, 20 Nov 2025 19:49:34 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6385696a4ea9e0ac36a6e9a75073a3d3d9346b1a39300fc52c76f1b5cce81b43`  
		Last Modified: Thu, 20 Nov 2025 19:49:43 GMT  
		Size: 94.9 MB (94874576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a055088953430a77e16c3c0d2fa58db0698987df6ad113dff27edee70550df`  
		Last Modified: Thu, 20 Nov 2025 19:49:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca98f16c6bea8b0ab11ed22e4e1c3ff5f6d8a64dda103d1157231cda6605a9ec`  
		Last Modified: Thu, 20 Nov 2025 20:06:01 GMT  
		Size: 4.1 MB (4082078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbb5c7caa677606cb998ab6a2e81a08f5f4c11a7cc384ed54ab40846a3c5a92`  
		Last Modified: Thu, 20 Nov 2025 20:06:01 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f707abcf2a1ad87c23a7bbfe8595ac433378cd7cdfd19140b6cbdba617c71be0`  
		Last Modified: Thu, 20 Nov 2025 20:06:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a059f33aebfcb3fb416a35898e35b15d30af8e58f92fe2764728e226bd913a1c`  
		Last Modified: Thu, 20 Nov 2025 20:06:03 GMT  
		Size: 12.8 MB (12767655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b03d7083f4e19b68913b3c342820360e581ba60aa848ea5eba3585ed02587`  
		Last Modified: Thu, 20 Nov 2025 20:06:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f434f854c6b591684ce67cc328cfd3ef484397fd798f1ebee929912c33e4cffc`  
		Last Modified: Thu, 20 Nov 2025 20:06:04 GMT  
		Size: 10.6 MB (10597444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae79f27165b5c65c286c452197c8de19262d94a4ab75fb091d3380016f4f6077`  
		Last Modified: Thu, 20 Nov 2025 20:06:02 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278fad67f36754cfe9b8f773ab7871a40781c80717a554e5a27fcfa8955f421a`  
		Last Modified: Thu, 20 Nov 2025 20:06:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0645806118122c6d4b6773a9ce1ec005a15f9673cb5488d1779efa8651600fba`  
		Last Modified: Thu, 20 Nov 2025 20:06:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9737820ee92a99ab15c7527f715bd3e5e90384fe8ffa4ba11ab4e907893668e4`  
		Last Modified: Thu, 20 Nov 2025 20:06:03 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af6a98350cedd751bddc99b6bb32171ee066ae272d3ed9f589ad916b9cd26ac`  
		Last Modified: Tue, 02 Dec 2025 01:10:51 GMT  
		Size: 25.7 MB (25728388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc64a67e7309b8e1c0eb8e0280e4534d56e12eeb40cac68f2105c6fd031deed`  
		Last Modified: Tue, 02 Dec 2025 01:10:56 GMT  
		Size: 30.1 MB (30054577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327fba7c665a4527e7b9d597b7426456dfed7db32f02dcac67fe7120d4571aa1`  
		Last Modified: Tue, 02 Dec 2025 01:10:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc6344bb056c3c6daa22c6f5da02a146f4d5bbee547218448fff643ad463262`  
		Last Modified: Tue, 02 Dec 2025 01:10:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e48f5cbfc69ecb65478d2eb3d8e1f9f649c1ec810fc15cbb5a03053ecc60b`  
		Last Modified: Tue, 02 Dec 2025 01:10:49 GMT  
		Size: 18.8 KB (18798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f0e9e045175030f449692508d6ee075063b8206214e088f4fd019011c0728c`  
		Last Modified: Tue, 02 Dec 2025 01:15:14 GMT  
		Size: 27.0 MB (27024644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6308ba9f7d828bdde18deb3242e800a1c56114dbf9310da6c2b59ff49e2d408f`  
		Last Modified: Tue, 02 Dec 2025 01:15:11 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27de4bd9e9ab3a98bdd1a25352a405a0d09ff6173d62e69c4c8ba39a08cc9d49`  
		Last Modified: Tue, 02 Dec 2025 01:15:11 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854daf0e90fd176d59ef26d2d8ce422b5401623f5a018474579164c2640074cc`  
		Last Modified: Tue, 02 Dec 2025 01:15:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:233a6beb673fcc742f759354d297b33a9484d5e95712d1b91976433dd74a8910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8541406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e2e36a0fbaafb72eb8d0b84796ea4800a294ce2a6d1602da8ee37842c4caa`

```dockerfile
```

-	Layers:
	-	`sha256:674a7746567e148d89d9740df6084b39ae3da73e6c7944c5dea216e9aca6ff7c`  
		Last Modified: Tue, 02 Dec 2025 02:24:33 GMT  
		Size: 8.5 MB (8473223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29cd4f2b19a9a8eadf3e1ad2978d99ac6cef264db04b3dfcc87261585a8711a5`  
		Last Modified: Tue, 02 Dec 2025 02:24:33 GMT  
		Size: 68.2 KB (68183 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:86ea85c1f06aa71401122d0992bc15fd12ba7b14201d583a2cae7e7eb8757d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219374673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b6262ed7c4f39f9b1f4fc922fbf71bc835b65ba1f306cf22c34abaa0c14926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 19:53:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 19:53:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 19:53:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 19:53:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:53:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:53:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 20 Nov 2025 19:53:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 20 Nov 2025 20:14:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 20 Nov 2025 20:14:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 20 Nov 2025 20:14:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 20 Nov 2025 20:14:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:14:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:14:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:14:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:14:33 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:14:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:14:33 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:14:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 20:14:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:17:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:17:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:17:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:17:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:17:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:17:21 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Nov 2025 20:17:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:17:21 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:17:21 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 20:17:21 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:19:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:21:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:21:19 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:21:19 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:21:19 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:21:21 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:21:21 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:21:21 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:21:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:21:21 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:21:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:21:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4207f644b97b37f2ab0bf7d81cbc684b64a52c02cedad6e2fed0d44c39361efa`  
		Last Modified: Thu, 20 Nov 2025 19:57:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16b803d0a60cf3c12d7e6784c6d720e16a9946ad154fb5ba098fcbfdef40759`  
		Last Modified: Thu, 20 Nov 2025 19:57:30 GMT  
		Size: 86.2 MB (86246363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d00bef26d538c25959d6ef4c49ef4f719f0996ee1689ac2fae980a9145c71f9`  
		Last Modified: Thu, 20 Nov 2025 19:57:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6a1cdaa429887081eefaf13dd8a603b29f987b9568ec1b926b6396b702a91d`  
		Last Modified: Thu, 20 Nov 2025 21:04:55 GMT  
		Size: 3.8 MB (3752415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f769b6485c79f640982840eba0cbede4c043389e9762bab875e35e0af61cb0`  
		Last Modified: Thu, 20 Nov 2025 21:04:43 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea5beaab0ec56954115142e363f12903793b306b17c2ae7768185e5d65bc54b`  
		Last Modified: Thu, 20 Nov 2025 21:04:44 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08119ae8bb24aa107b603f757c89c8c3f789c9200c3b551366d97345c2799ec`  
		Last Modified: Thu, 20 Nov 2025 21:15:37 GMT  
		Size: 12.8 MB (12767768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c57eeeac370f4488e098c91de38a0d7105b63401c1327d9b9eab07967beddcb`  
		Last Modified: Thu, 20 Nov 2025 21:04:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f031345f1af1b1bb24614f55b59831ba8599ce2b84b647064674481df112cf80`  
		Last Modified: Thu, 20 Nov 2025 21:15:35 GMT  
		Size: 10.1 MB (10069793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761154238aae063bfeceab329144bd0b6d79243b6d995ab04b56d9cb08669b70`  
		Last Modified: Thu, 20 Nov 2025 21:04:43 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b489e4698ba710defd78e06414ad9f7c751c0f713d0f485686b735faffe69c09`  
		Last Modified: Thu, 20 Nov 2025 21:04:43 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59151031d284887d34a524ed66722f724cdb39453470be17dd68f7ccd548595c`  
		Last Modified: Thu, 20 Nov 2025 21:04:44 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934c89e27103e6ecf2f0bbb2ce043607c68a1a598d1f34f2a3c20c0d9b5727c0`  
		Last Modified: Thu, 20 Nov 2025 21:04:43 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050ac385f0ac3d5c153c77bb92ec5c8c80c74b6ddcf2bee408b84b1ef1590a9a`  
		Last Modified: Tue, 02 Dec 2025 01:21:37 GMT  
		Size: 25.1 MB (25077771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02570b01938e4c6f45eebe03270d4648cdfa2e086ceaa2f417a135a5bddaac8`  
		Last Modified: Tue, 02 Dec 2025 01:21:37 GMT  
		Size: 28.2 MB (28196306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c56b375c0256df45440e274b61da3516bad9107dbc8aa1f4df1427f61dbc52d`  
		Last Modified: Tue, 02 Dec 2025 02:59:36 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a49c179d74debe574803107944306081fc9ced8034faef0df4bfd8da0a5bbf6`  
		Last Modified: Tue, 02 Dec 2025 02:59:36 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4a8e9b0ba1881d4ab6c9b7c64f95ca23e1fd50bd7c750e9adb5286c837fddf`  
		Last Modified: Tue, 02 Dec 2025 02:59:37 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050ce559fe7c288c616a9b4cbc31f29359580612665eb96a04843cd6c2ba3dc1`  
		Last Modified: Tue, 02 Dec 2025 01:21:38 GMT  
		Size: 27.0 MB (27024651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44527297a3cfa8ed1ab3dd63f73296337c0076b675b63b07f09be4fe032a3b75`  
		Last Modified: Tue, 02 Dec 2025 02:59:36 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da931ed2b56948c1f217a79fa311c2633de68e4315ef1077fb553caacd253700`  
		Last Modified: Tue, 02 Dec 2025 02:59:37 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35000cc585719a795fdc2cb0aaee6b40306a1f2ecc6cb4143bfedfcb06b66530`  
		Last Modified: Tue, 02 Dec 2025 02:59:37 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:31bac622ba5e00a2cdd4cbd34abe4558c620658cdf5e24cdf413be95a9511da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8546234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9a621b2d55532994871cc642f625b639b7c11195d0b368248d765aeb6d1e7`

```dockerfile
```

-	Layers:
	-	`sha256:784c708530faf7d6375e1b8eddae167d299367d9e189b9d2ecba485ce7a39e3d`  
		Last Modified: Tue, 02 Dec 2025 02:24:41 GMT  
		Size: 8.5 MB (8478051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85869f2bc88dd991edab0f8703ef0e78b2efd985eb77f2d1d230a9db8ecb816d`  
		Last Modified: Tue, 02 Dec 2025 02:24:42 GMT  
		Size: 68.2 KB (68183 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.3-apache` - linux; 386

```console
$ docker pull wordpress@sha256:6b018b85660b588a6142db9f5343a254b8497d729b5fc8d66ce9da458ba5cea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262204506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce23a269dd9ab80b56412ed076bbb99ea036f9a87e4530929f2f169f743851c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 19:47:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 19:47:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 19:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 19:47:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:47:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:47:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 20 Nov 2025 19:47:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 20 Nov 2025 20:00:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 20 Nov 2025 20:00:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 20 Nov 2025 20:00:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 20 Nov 2025 20:00:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:00:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:00:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:00:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 20 Nov 2025 20:00:49 GMT
ENV PHP_VERSION=8.3.28
# Thu, 20 Nov 2025 20:00:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.28.tar.xz.asc
# Thu, 20 Nov 2025 20:00:49 GMT
ENV PHP_SHA256=25e3860f30198a386242891c0bf9e2955931f7b666b96c3e3103d36a2a322326
# Thu, 20 Nov 2025 20:00:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 20:00:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:03:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:03:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:03:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:03:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:03:58 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Nov 2025 20:03:58 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:03:58 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:03:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 20:03:58 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:11:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:13:22 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:13:22 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:13:22 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:13:22 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:13:24 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:13:24 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:13:24 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:13:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:13:24 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:13:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:13:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5c20d5206b4e860942dc5c1e31bac5d7824529271062ddf00c0effbb48907`  
		Last Modified: Thu, 20 Nov 2025 19:51:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d38eea69d449dba729795f7bbfe658eab27fde7077861a080578f7ac41211f`  
		Last Modified: Thu, 20 Nov 2025 19:51:56 GMT  
		Size: 116.1 MB (116138585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43367fd57690128acfb97fa0b5a5bc66d6e0e7368d242776b34ce08d6483ffd0`  
		Last Modified: Thu, 20 Nov 2025 19:51:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e530c130200b51acf8eb7bff8e1dc172ba18abe9d76187a390431785944588`  
		Last Modified: Thu, 20 Nov 2025 20:04:26 GMT  
		Size: 4.5 MB (4455988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254209266877c2c77edaa3b2b473774f8f9c98c03c8cdd2e45b1bb2c2a4d477`  
		Last Modified: Thu, 20 Nov 2025 20:04:25 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d28559665feb423d18edc3d22647ce5f6f9bacbf4b7d1048c3b93f8d7ec75b`  
		Last Modified: Thu, 20 Nov 2025 20:04:25 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aa2d0f0534949417e60671e516a415d11e2f8c8670887046ef3434a078d177`  
		Last Modified: Thu, 20 Nov 2025 20:04:27 GMT  
		Size: 12.8 MB (12769214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced8eb9b29728802199796dc3efe172ac5c0739160bf65a194605081a45ce437`  
		Last Modified: Thu, 20 Nov 2025 20:04:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d882fe635d101038074c6147bdb8c01ebc3766184f662c00c5651f31d643cf56`  
		Last Modified: Thu, 20 Nov 2025 20:04:28 GMT  
		Size: 11.9 MB (11919441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4599062c3ce82fafaa890a16aa96976dc089744e88c91ce627bf901874fb411b`  
		Last Modified: Thu, 20 Nov 2025 20:04:25 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa3decdb6b8cb9c5492a5bb67ec7c96542ad8cd0ed625212a0761da8a6f6d46`  
		Last Modified: Thu, 20 Nov 2025 20:04:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7982cf63b3c1bf004bb6b7b12af05bfa6820a3beff54693010a4a2393fa3d`  
		Last Modified: Thu, 20 Nov 2025 20:04:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7eca7152b5194bb1872abdafea5c541f4000301c439eeff7812be3e26b04c5`  
		Last Modified: Thu, 20 Nov 2025 20:04:26 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d29251810fa22ca56db6d42b6976f0e1d7eef7be2b14d8ab0853c61115986ee`  
		Last Modified: Tue, 02 Dec 2025 01:13:43 GMT  
		Size: 26.7 MB (26747445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf86923545795268a3c662122a05316bead40ef2cca3cea9297ea1b2a0b524f`  
		Last Modified: Tue, 02 Dec 2025 01:13:43 GMT  
		Size: 31.8 MB (31826471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e3a3e9b6b7fd7c6e289d1ec4c109f27067ba8ad692981451ee2c4bdb38e7e5`  
		Last Modified: Tue, 02 Dec 2025 02:07:24 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37da8793bbb57904ab059c241b99b034531bb827a12261077b9417764d6c5ec4`  
		Last Modified: Tue, 02 Dec 2025 02:07:23 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611d07d02284ec22b3fd58c7b6f1cc56b8d58a928073508d7d8f74b90058a826`  
		Last Modified: Tue, 02 Dec 2025 02:07:23 GMT  
		Size: 18.8 KB (18799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95376c9a2d0aeaaf9af4cebca41eeb75ed21522d1ff4b1fb978c3cf090384f7`  
		Last Modified: Tue, 02 Dec 2025 01:13:44 GMT  
		Size: 27.0 MB (27024636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e8aa7c80b67afa79e8817ed200cf9a30cbf0091161ba4381eb1ca15a6e2dcc`  
		Last Modified: Tue, 02 Dec 2025 02:07:24 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b86577c246fec71e64a62728877f5c76d9c3378a1c7e1888f34a254d30a763c`  
		Last Modified: Tue, 02 Dec 2025 02:07:24 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e370342f7e282383513496c062110578ac76bb6c171a931da952499d86e0f45`  
		Last Modified: Tue, 02 Dec 2025 02:07:23 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:e6a0be148f966721b696c6b9ea3b4fcfb0b957f2d0ef02b39fe474011a691fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8714932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadf7108714220bd62b2ef80b21e2a114513e822c73c9cc1777e7dbb934f6cd1`

```dockerfile
```

-	Layers:
	-	`sha256:038809afe59fbf7b8054008a3f1ff5fb2c8b5c7aee3726474e982e9d922447d2`  
		Last Modified: Tue, 02 Dec 2025 02:24:55 GMT  
		Size: 8.6 MB (8647098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469934f6ecbdd5791bb70e677ac9df113bf01c24f9e199aa6d9470b540741ef2`  
		Last Modified: Tue, 02 Dec 2025 02:24:56 GMT  
		Size: 67.8 KB (67834 bytes)  
		MIME: application/vnd.in-toto+json
