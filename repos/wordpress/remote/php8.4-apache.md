## `wordpress:php8.4-apache`

```console
$ docker pull wordpress@sha256:355adc2632ae894670b1c08b88a850613adba3c82d9b1bddc3c7ed0896fc4e1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `wordpress:php8.4-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:05a5d78ec7f68faadbc384093ec1e2535089e20dbb69c31f3829e14d0f332825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251689170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff738e9e25e402b56ac463d5cc24555c25945c89a2cac2d636a1080c94b046cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0RC2; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
VOLUME [/var/www/html]
# Thu, 13 Mar 2025 21:35:04 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 21:35:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b069e2d43501290d4ad74c8269ede22610b6037a2f8db5bb0b3f5f8afaa8a07b`  
		Last Modified: Fri, 14 Mar 2025 00:13:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4ebbec22188b7dea8beff0cac83eb0fe3dfbb6ad088beed36eec6a28f254ed`  
		Last Modified: Fri, 14 Mar 2025 00:13:05 GMT  
		Size: 104.3 MB (104345638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591e2fd0e37ef23e048552a6a70f468f9c9f20f9302b751f697a8fc605d735aa`  
		Last Modified: Fri, 14 Mar 2025 00:13:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea39dbc215574baac0dc8b9832e2fd5ab997eef1690141e61c8998c582dde5aa`  
		Last Modified: Fri, 14 Mar 2025 00:13:04 GMT  
		Size: 20.1 MB (20123733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6827e040502694db6b0615c59d267f26aa3da510c003bb98471216979855b034`  
		Last Modified: Fri, 14 Mar 2025 00:13:04 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9823796ab7fb8a7691ccace17cac32ade94649430a51f6aafb2e62fd651161`  
		Last Modified: Fri, 14 Mar 2025 00:13:04 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fe2996e66b86d721762fad1a663cc820268a8241d0aaedbdcf056fad3cbfc0`  
		Last Modified: Fri, 14 Mar 2025 00:13:05 GMT  
		Size: 13.7 MB (13733138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac59bdfc6c0f7c5ef19c11fd6bc849f634bdbe253232149f04fd6fe243dd2924`  
		Last Modified: Fri, 14 Mar 2025 00:13:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3160fc0d00e10c0802627939ac07d5008ae36b6780d2437e98428678d17cea6`  
		Last Modified: Fri, 14 Mar 2025 00:13:05 GMT  
		Size: 14.2 MB (14162278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b365602aea53faf5827a3f6bf9b02e7a2dff8d4916d00b2f86833d9ff28eab18`  
		Last Modified: Fri, 14 Mar 2025 00:13:05 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0047b9e644656f35889bb8e20276d79fab7eccaa85e763d5f0d4c2152548e5d0`  
		Last Modified: Fri, 14 Mar 2025 00:13:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8809fb74d31bc69301e69f8277e1e8bd8386e7ddf373b00a111f244e1dbef140`  
		Last Modified: Fri, 14 Mar 2025 00:13:06 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469e3cde455122333b0ee463d6114aa38a62fbb77621e501818fe3f17a1eae63`  
		Last Modified: Fri, 14 Mar 2025 01:12:38 GMT  
		Size: 26.3 MB (26253941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1e8df332cc825e56ef7bc5d25cdf062f9bf3ade35050bc9efefa59d01e10e0`  
		Last Modified: Fri, 14 Mar 2025 01:12:38 GMT  
		Size: 18.1 MB (18063513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fa0b3f8fb9d2be2c48845bfbd7f6e1c49f6a5485bbd7ad8cac8bf94fdcc4ae`  
		Last Modified: Fri, 14 Mar 2025 01:12:38 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a213dbbcf63a7e4c3cdddb36023dc97918c35b07173d26ee02dc79d633165c`  
		Last Modified: Fri, 14 Mar 2025 01:12:38 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c6c4233a4328a01601f0a44aa00ac913accfee4f03dfd6cee8633ba03c9a37`  
		Last Modified: Fri, 14 Mar 2025 01:12:38 GMT  
		Size: 19.1 KB (19149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba269b5ef2175aa4000584d844e4654a3016222a90b6c002bb106e9e293370f1`  
		Last Modified: Fri, 14 Mar 2025 01:12:39 GMT  
		Size: 26.8 MB (26758081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ad7393d2f42f7f76fadd718c4e8fed1dfb5d514e4d7e225d3c1aef685d5382`  
		Last Modified: Fri, 14 Mar 2025 01:12:39 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fd045b2966bef8aa20ba8fc124b3085f2def146c6d6ad655b449814992b884`  
		Last Modified: Fri, 14 Mar 2025 01:12:39 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:eb63e6e022db88cfd497412fa5a79797efafe4bfa26ef990fc8ee5a208ea214b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8170320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d0c304baf37678465a582c217b9ce784343070867c824329e4836494bb38ed`

```dockerfile
```

-	Layers:
	-	`sha256:6dfadce31a80d33310f61100252cb8b823b98ad42c13098ac792b7cf92b8c538`  
		Last Modified: Fri, 14 Mar 2025 01:12:38 GMT  
		Size: 8.1 MB (8111541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca045131d4baaebdddd7182adb36d558b034f2aebf947ba221b4476027520e0`  
		Last Modified: Fri, 14 Mar 2025 01:12:37 GMT  
		Size: 58.8 KB (58779 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:c83b826d1dbe6ef74cac9e78ab8cd4d67187c61b730b7e06507cc367643abbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220133380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910b8fae22cfd4ac7c0792fc6fd7a3df2b7df936d35709055f7f32da8539ade0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0RC2; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
VOLUME [/var/www/html]
# Thu, 13 Mar 2025 21:35:04 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 21:35:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3014e21b6e4396df02c7cc3c5f126fa29d531fa5a1ad0b40b80de6794ae2694`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e0a56f6198eb0af5102ce28eda7b5a34384f5b54701b7346487229bff9e9c`  
		Last Modified: Tue, 25 Feb 2025 02:51:20 GMT  
		Size: 82.0 MB (81993202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24b0f2499da71327f565769347ea1f63e9070dfa8385025f0465d80e603c361`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a0010d00b089e3a34b60fddcac813cd3a1211368d868b76aa3c52acf85f39`  
		Last Modified: Tue, 25 Feb 2025 02:55:46 GMT  
		Size: 19.4 MB (19419190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836efc0ee062aca6556d741fb3e390ca6b509fc639049bef1cfc24e29616d566`  
		Last Modified: Tue, 25 Feb 2025 02:55:45 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb27253beef75bf260f9071d9fb96a1614335f2b1af270afddf706a8142cb7b`  
		Last Modified: Tue, 25 Feb 2025 02:55:45 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9832968e755b597e468f9c8779ae5ec9c7e0c77622ec9696aff11807250fb2a6`  
		Last Modified: Fri, 14 Mar 2025 00:29:23 GMT  
		Size: 13.7 MB (13731598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b789993f01330ce3c6b1a77297b8e90e62ffdad5d70d74843b60a7dbefb1e8`  
		Last Modified: Fri, 14 Mar 2025 00:29:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d803af272757d6de79ff1cbf599cdfd0355590912651ecd2a2ba7d15f632e0`  
		Last Modified: Fri, 14 Mar 2025 00:29:23 GMT  
		Size: 12.9 MB (12917619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a1d69ef51bb0e20d2d78f3ca83c614ca5010794c67c7619ccf86b428fdb9c3`  
		Last Modified: Fri, 14 Mar 2025 00:29:22 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ded74a4412f3ad7346950e5235570429a926c4f637c5710917881ebc4c4efe`  
		Last Modified: Fri, 14 Mar 2025 00:29:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6cdbcaa75fe85e4a7dd99b9a703de372f9c04db57b1fe7d8b65f03fdd3013`  
		Last Modified: Fri, 14 Mar 2025 00:29:23 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e549dd96688ee0b15cdeb72f67a28678abb14219fb42540fa704462d3b1161`  
		Last Modified: Fri, 14 Mar 2025 01:51:07 GMT  
		Size: 25.7 MB (25704066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dac4338fe68360f59c89242ac17a42a9276391ffeb8589e3fad73b01e0f0cab`  
		Last Modified: Fri, 14 Mar 2025 01:51:06 GMT  
		Size: 13.8 MB (13839405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf956600d62293b7d8976bf9baaed05f90dee29023063e4ddf4b85a5cd78ac03`  
		Last Modified: Fri, 14 Mar 2025 01:51:06 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3454a51a6c15897a8066b984710c34acc06b28bed4417562f2780eb9a297c291`  
		Last Modified: Fri, 14 Mar 2025 01:51:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a0983a25810aeb82058ef3d20b1f38f5d1776a2a5df04230425dfc733f7102`  
		Last Modified: Fri, 14 Mar 2025 01:51:07 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c93738ebd1832e8bfcc8535855fec98051691caf2e43aaf5d8b4c7c67d4bf8c`  
		Last Modified: Fri, 14 Mar 2025 01:51:08 GMT  
		Size: 26.8 MB (26758091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fe67c8afe4b0244f860e18378e5ddd0532116b354b7a0c8760c7263fe5304e`  
		Last Modified: Fri, 14 Mar 2025 01:51:08 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7961670afecf6efe7e70d54f9b2a4426abd656464c5716e3c1781e8a0da4dcfe`  
		Last Modified: Fri, 14 Mar 2025 01:51:08 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:88cf8bab16a3e0ef7f4efe25c95165997166d974fb469784756976687694f4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7976663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d706390e47764f5cf43bda724a20cbb893281d3d2545323c3ab4bf80d95ec99`

```dockerfile
```

-	Layers:
	-	`sha256:fb0a253808af88c48b03b856e8dfeca6d49235a4ad5a3bad7bb04a23979284ad`  
		Last Modified: Fri, 14 Mar 2025 01:51:05 GMT  
		Size: 7.9 MB (7917720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b6bdafed78ba7df57de020f6afe4268f0a074cb6d56da8d236007b3b0a68d9`  
		Last Modified: Fri, 14 Mar 2025 01:51:05 GMT  
		Size: 58.9 KB (58943 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; 386

```console
$ docker pull wordpress@sha256:7459b94d5fd444679d26256d2eaacbd58a0e9270824a42101765bd3eb8ec3a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247070326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e8dd29f399a8f22ad00d463a9de0a0ba23bc2dab9d86765f7fcc4cce75beea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0RC2; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
VOLUME [/var/www/html]
# Thu, 13 Mar 2025 21:35:04 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 21:35:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547ef44dd8ab1b0eff4c3646430bd5a364ab555e2d7ebc211662fbce80309cde`  
		Last Modified: Fri, 14 Mar 2025 00:12:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8927b01f292a50f7f01edc05b6540a1ee6bdec78d06fd3a1b524db2b6954554`  
		Last Modified: Fri, 14 Mar 2025 00:14:04 GMT  
		Size: 101.5 MB (101513553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a011b190d2fb5fad684fc22c2adc2a14c9d15b05ad1e7d6389e514818d6ad081`  
		Last Modified: Fri, 14 Mar 2025 00:12:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37db90f92ba08de825459e92cedb1d207b3de07629898b195539ff2e926cb6f9`  
		Last Modified: Fri, 14 Mar 2025 00:14:01 GMT  
		Size: 20.6 MB (20638485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2b8d44ae1819a465595d3e57c92b35530dea994599df50cf82a91f68383350`  
		Last Modified: Fri, 14 Mar 2025 00:14:00 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262d8c864b351afee932a7994ddbabf2c1bee7486ea0723591d5348ecde40fcb`  
		Last Modified: Fri, 14 Mar 2025 00:14:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919971b79bebd9ef34fee0b86a0cb060a46f0e9ca11325af2458007501716129`  
		Last Modified: Fri, 14 Mar 2025 00:14:02 GMT  
		Size: 13.7 MB (13732365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d78442a94e1082427c8e7c8dbc3961cb80256ce0cab07f2ae15de37a28dd33`  
		Last Modified: Fri, 14 Mar 2025 00:14:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c078101da34c5dc8a6f865518a9c83c93797f379f55beca0e5f25b3a297a17aa`  
		Last Modified: Fri, 14 Mar 2025 00:14:03 GMT  
		Size: 14.5 MB (14454546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51586e16f9be56c1013eb6ee00fa0800a5a4112ec39840a16147072cf2eb8b7a`  
		Last Modified: Fri, 14 Mar 2025 00:14:02 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d236c0c082897a6fac0dc1bcb7ae08b44d4d3f4664523c0537b435b59f568f`  
		Last Modified: Fri, 14 Mar 2025 00:14:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd3479f3c61d27e9f1728c10704e58d1d6d98e7e775e5e6fb7e3028df405a9`  
		Last Modified: Fri, 14 Mar 2025 00:14:03 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1903ae36b63519141afb205093c6f9e53681903e7e1a64465d638bdbf2467c33`  
		Last Modified: Fri, 14 Mar 2025 01:13:05 GMT  
		Size: 26.7 MB (26700627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20612cfcd3aec6b506e64ac27241006812026fc73aae3457b3a3b9b31527938e`  
		Last Modified: Fri, 14 Mar 2025 01:13:05 GMT  
		Size: 14.0 MB (14048510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4296e028abd07949a8ef69107623f114f8dbc46eb0ecfa7b9d6cacb83a3ae`  
		Last Modified: Fri, 14 Mar 2025 01:13:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcafb9983b596fd5c64a2a1fb835d32df6ae2a49686f3be3ad066a5b2241b20`  
		Last Modified: Fri, 14 Mar 2025 01:13:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eecf9354b611b661d0ad6c523c9a1a2602509487f6b34151484d3363cae123e`  
		Last Modified: Fri, 14 Mar 2025 01:13:05 GMT  
		Size: 19.1 KB (19147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c910c6e0446ba2c6b17514b3071c40036964e704d0a345882f8909b2f682dd0`  
		Last Modified: Fri, 14 Mar 2025 01:13:06 GMT  
		Size: 26.8 MB (26758085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7a2ef51311ecdcb8bf56e715360ed56cb03d06504165f8c96a558633f413e4`  
		Last Modified: Fri, 14 Mar 2025 01:13:06 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f3f21ecc0412519ab473f81603406c3458908cb23fd8802b677422c1c19f66`  
		Last Modified: Fri, 14 Mar 2025 01:13:06 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:5203b73e56fd3d43011ca3ae6b1f9033b3ed58420c28bdd7affe8e9c8bf383ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8143454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4048130101ea505ef81be66dc00f322bcbb80955eee7e41fab7b1be0b431e2ad`

```dockerfile
```

-	Layers:
	-	`sha256:1c999b378ed6d837987edb04fd38175045b2671326ed7392b7a65d8d9d71fbd8`  
		Last Modified: Fri, 14 Mar 2025 01:13:05 GMT  
		Size: 8.1 MB (8084737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff103ffa2b5ca7928b94f9ee97b64106ece081481e84bc91039c8180ba321dde`  
		Last Modified: Fri, 14 Mar 2025 01:13:04 GMT  
		Size: 58.7 KB (58717 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:c73a5c4dc7f5bbf343e6ec51b7ebba671fe458bed67ca2adc8afafdb1213071e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222383102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcacf7b83ea3f4077df880c8efca913c47da338c15378e07141b871fe891238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0RC2; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
VOLUME [/var/www/html]
# Thu, 13 Mar 2025 21:35:04 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 21:35:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d36a7b1e0c4904256c3222f554e2f9053a6ce6cb06dac686a36004c2968943`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878fe44e60469208a4e6a6cc56a06ba4bd6418ae0d09468c66a29bce7fc35e03`  
		Last Modified: Tue, 25 Feb 2025 04:23:25 GMT  
		Size: 80.7 MB (80668722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03653780888887368ef36859920d833d269d38c1e54ffb86bae392b6bfcfde65`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d16225b42033fad2e17de37197d7ddf58740cc1e834d88386251e1203d6bc`  
		Last Modified: Tue, 25 Feb 2025 04:43:12 GMT  
		Size: 20.1 MB (20069161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0240d2561c08c1860eeebaa66951069a40fc7b7c112653504c26fe56fc8e30`  
		Last Modified: Tue, 25 Feb 2025 04:43:09 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f085555607131ca41617fae1213ab0cb04ab6a67ce34f84c32f46a658c22f736`  
		Last Modified: Tue, 25 Feb 2025 04:43:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f94c390d6b4a7fa6bf26aa53e7bd4712729436c4139870653408280176a68e`  
		Last Modified: Fri, 14 Mar 2025 02:27:22 GMT  
		Size: 13.7 MB (13731336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd6801b6a4928d64cf5e3521b72f7083ace4376268efc1ad1690f7826ec48aa`  
		Last Modified: Fri, 14 Mar 2025 02:27:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760e8a5f44af1dfb56b7c95d360fb4a8de2b2df272200c18fb6c6714ab0f243a`  
		Last Modified: Fri, 14 Mar 2025 02:27:23 GMT  
		Size: 13.1 MB (13062436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119f206cceb2f4f049b0ba16ea9c2184a4b499aa4b9c04a6182d5053509f5d47`  
		Last Modified: Fri, 14 Mar 2025 02:27:21 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a21653f572a8c9e956b13fd47dbb1c6a2592d4f2819e9db94c1aacb77b21f1`  
		Last Modified: Fri, 14 Mar 2025 02:27:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67dd3f13a1ccb60e4ebc8bcfc42be99bbec13de320a525acfefa836323a940f`  
		Last Modified: Fri, 14 Mar 2025 02:27:22 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85eedb5a2cb6ee7b6de46f3920f7a6274a9639f44d16e7b66932525bd32a65a`  
		Last Modified: Fri, 14 Mar 2025 08:55:05 GMT  
		Size: 26.0 MB (26022193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b591cfb7e5dc3a65b6e6536a392abadbba43cdb74bffad7cd0eeae77ec1cc1d`  
		Last Modified: Fri, 14 Mar 2025 08:55:04 GMT  
		Size: 13.5 MB (13547875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b6f50eb534d96e457e7749928299973f36932997ba4f1dd7c80fab6c786e2c`  
		Last Modified: Fri, 14 Mar 2025 08:55:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74142c66f70ac974862bcb5185735f39368954b59a6cac8df374334b1dee687`  
		Last Modified: Fri, 14 Mar 2025 08:55:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5825c5b3355bc096e4cd62750d7fd22fd7c26758d65a54433cb7ce5ab2ae09`  
		Last Modified: Fri, 14 Mar 2025 08:55:03 GMT  
		Size: 19.2 KB (19164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c7baa32d58575fe5df6cab282f75c321b2d00935a2f00d6193190a04a8fc9`  
		Last Modified: Fri, 14 Mar 2025 08:55:06 GMT  
		Size: 26.8 MB (26758105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7eed9197bfe0584943e09cb8e734c28f8c3f6402267516fb3b6bd980f0694ea`  
		Last Modified: Fri, 14 Mar 2025 08:55:04 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ec0dc7d1f3daea35e2c9df94fc524d56b54f9dfb1d6ae356cc22aad0b97ce4`  
		Last Modified: Fri, 14 Mar 2025 08:55:05 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:46db97e8075197d8dca4d8021c592aa2efe8aa53354936b48fc4a1e0e3306ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 KB (58672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3347a2885f5cfa886252fcde9de14c6aa56fffba382391ec9796ef6534979bcb`

```dockerfile
```

-	Layers:
	-	`sha256:fd741eb84229bc7b5bb274b5dd25ca018238b4a553b3c57ac59a8bb69eb6c3a5`  
		Last Modified: Fri, 14 Mar 2025 08:55:02 GMT  
		Size: 58.7 KB (58672 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:0c102a8722d12004cb13fd434f5229abdeec695856ec112d5833671368a648aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255328983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c666bb0166ce97d856b377799a0f854f21001ea9ee05f6384a842e7a5835867`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0RC2; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
VOLUME [/var/www/html]
# Thu, 13 Mar 2025 21:35:04 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 21:35:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bbbae4d2dc0350f7df1634e33daf64fe78cb672182650c700a26750b33b64c`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f7bed916e76b3a3b176b4e6a5bcfe6e10e39a6c423be8fc3575115d7b1e06`  
		Last Modified: Tue, 25 Feb 2025 02:59:28 GMT  
		Size: 103.3 MB (103323545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9943a0d5cef1bf22e1a6d5df4b38af8052474c28fe7d9188d33c9e0190742`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5eba5668f315d2ef7f70338fc89daecbca191bf9b5b6622280439ff5ceb4a7`  
		Last Modified: Tue, 25 Feb 2025 03:04:11 GMT  
		Size: 21.3 MB (21308442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bec4fde36a5fc026717bc0e1c4a8f85c6397c11d730b4d345fdb0b5014cc45`  
		Last Modified: Tue, 25 Feb 2025 03:04:06 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca66cb544073b521bd3bcd518135c4cf977a5939323c5191473a1b8a2a09cd05`  
		Last Modified: Tue, 25 Feb 2025 03:04:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6929432e6ae319b1471cb20d50034aa658f02f33bb2f0553793c5295fe3e97d6`  
		Last Modified: Fri, 14 Mar 2025 01:34:27 GMT  
		Size: 13.7 MB (13732761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94367e18b9aea7fbfd4e9bd9e38a65ee4c3346f12d2a71f7120908449a2ffed4`  
		Last Modified: Fri, 14 Mar 2025 01:34:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbad57bc03278cf036ec4e36d54f652e3717a311dcf27b5fc7b64b57f4ed639a`  
		Last Modified: Fri, 14 Mar 2025 01:34:28 GMT  
		Size: 14.6 MB (14580441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e287236d84bd02cc3a7073654dccc80aff99d14a8e66ae4ce1b47d2adb5f2ea7`  
		Last Modified: Fri, 14 Mar 2025 01:34:27 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929be59810363357654e5298a6854036d57847fc050b1669849a2c7e8b8f248b`  
		Last Modified: Fri, 14 Mar 2025 01:34:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27155f2e68dcc7977b90b3ab7507a18829f349545a199454652cc78898e71400`  
		Last Modified: Fri, 14 Mar 2025 01:34:28 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80820bf44ae468d393fa7a7e1a842a03268d9f2bd3611992ee5767dea4a285a7`  
		Last Modified: Fri, 14 Mar 2025 03:18:45 GMT  
		Size: 27.3 MB (27339121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a0491689509fd1c332f17c3bc035963cfec452334e88285f27431aa87347ea`  
		Last Modified: Fri, 14 Mar 2025 03:18:45 GMT  
		Size: 16.2 MB (16204677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8301cd0412d768217349ae055f0ea37032e5fb14be4730603884a699adf472`  
		Last Modified: Fri, 14 Mar 2025 03:18:44 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0fa869fb30463e73f791518100bb1c985d330a632f1d7b9bd745122dd7ae21`  
		Last Modified: Fri, 14 Mar 2025 03:18:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ec9ad2a10b6a5099658071e62f9c1ab9b30737b8a160763b28a73575123013`  
		Last Modified: Fri, 14 Mar 2025 03:18:45 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f2967357009dea8aa718431f92c577ae76ae2d64b228c17f9e090a7516584c`  
		Last Modified: Fri, 14 Mar 2025 03:18:46 GMT  
		Size: 26.8 MB (26758109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93f8fde3aecb21bf75a35a7719edab22af0f3e0e703d1ade88afc787e00f11d`  
		Last Modified: Fri, 14 Mar 2025 03:18:46 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683fc0872a122ce2202a7ea47aa6ef03799d2d25e9e514c65f47508a47345985`  
		Last Modified: Fri, 14 Mar 2025 03:18:46 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:8437a2ac2aa3bfcd0ec0782667038996d036b391503d6cbe5fabf2b0ccd496ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8149303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acbbac81d93c39f9ed01fba127a57ebe54be7bb3fb407dec0e36dfa66299107`

```dockerfile
```

-	Layers:
	-	`sha256:4991c9acfad906fcc71dbd0763cd8b7744e6b6bb1c80815bb8b0523a4d94c766`  
		Last Modified: Fri, 14 Mar 2025 03:18:44 GMT  
		Size: 8.1 MB (8090446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0065a90bb0ee114dd831f14c35be27bbc2e5a08d3997e25d7eed8623a8542a6b`  
		Last Modified: Fri, 14 Mar 2025 03:18:43 GMT  
		Size: 58.9 KB (58857 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:05d1bb3ec2eb59f9cd13a96a429d0ba5c8c6d94c5ca9f7d9cd0150fdbbc86efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221565732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9759de8e58f285fcfb5cc6a6a02fa95d24d3424f572edfb2510121cd8ca9eb4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0RC2; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
VOLUME [/var/www/html]
# Thu, 13 Mar 2025 21:35:04 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 21:35:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Mar 2025 21:35:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83dfaf87e0f897b620f8faafcd35d93785d305460fb8a1f24f178152dc8ef4`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382c1a79d42d9a6f73ff6106cec8445a8fb8bc6a78380c02024ff5e71c740938`  
		Last Modified: Tue, 25 Feb 2025 02:47:06 GMT  
		Size: 80.8 MB (80817122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd5ce3ea58656e03c29355d087376523130702c7a182e93a6e6c775d2e795dd`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca9e9fc0029c44454cc7b3021d275f272be12d935e5bcbf513a001e160df1e`  
		Last Modified: Tue, 25 Feb 2025 02:50:57 GMT  
		Size: 19.9 MB (19895168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312727822926b01c3ea7b38ae79e9f14f546dab08bbfd780821249610ae4aa7e`  
		Last Modified: Tue, 25 Feb 2025 02:50:56 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d51730a67b490b800306ddce51f95b7fc9ec61621c6c0c350bd502364beda8`  
		Last Modified: Tue, 25 Feb 2025 02:50:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574e16cfbeb19b33ae20d591d360d1bdd44ccc908a8bffa151f348bbcffe3e0a`  
		Last Modified: Fri, 14 Mar 2025 00:25:06 GMT  
		Size: 13.7 MB (13731926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6103727b10cc92035a6c829ff4bf66bed4f290eea12ebf6acc49b43ecb163ac1`  
		Last Modified: Fri, 14 Mar 2025 00:25:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b7dcda751df4f836a323bc13396d83eb081d7621c62d0a879435f3456d6031`  
		Last Modified: Fri, 14 Mar 2025 00:25:05 GMT  
		Size: 13.5 MB (13538832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca35bbd60a0f29a39f02aabd2e2a37f35ef6f6d99fb60004d65f74fc8c26705`  
		Last Modified: Fri, 14 Mar 2025 00:25:05 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2204fcfc165f4a340105c964e5758823f6861e4e9ee2fe3a1c828c4a052293`  
		Last Modified: Fri, 14 Mar 2025 00:25:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce95df89c008a3cd966ac1b10555999aa6c881f404202159cecc11068fea8c78`  
		Last Modified: Fri, 14 Mar 2025 00:25:05 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c12afc6689e94ce94ac2341029d6ef6a5170c9145e2c7dd6a48358ff242e0a6`  
		Last Modified: Fri, 14 Mar 2025 03:45:02 GMT  
		Size: 25.9 MB (25899300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4dca2cdc6f032a14feab599235a8e87fd675c53ba3761ac984f17bb933fa75`  
		Last Modified: Fri, 14 Mar 2025 03:45:01 GMT  
		Size: 14.0 MB (14030884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74924471e6eed0f2f4898edb774b964c72ab9c46ee57a82383167593fa0a538`  
		Last Modified: Fri, 14 Mar 2025 03:45:00 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c157d962357a7ddf4a2cedea04b83c01609172955149de0ebb2281521e9b60`  
		Last Modified: Fri, 14 Mar 2025 03:45:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6897af525264f4bae9407c893b3c55c99cf337697f5309196024ed803a0cab83`  
		Last Modified: Fri, 14 Mar 2025 03:45:01 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413feb4aa7788088b979751dd0950034efdd60661e9f3e93b2a7605c9fccc8cf`  
		Last Modified: Fri, 14 Mar 2025 03:45:02 GMT  
		Size: 26.8 MB (26758073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5634edc58d45c31f3a00c7119002f26a6706db30744a40dfa86446452d540b9`  
		Last Modified: Fri, 14 Mar 2025 03:45:02 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0e4aca2435b4b8d6876ac52a41ffebbe617ae525da31ef1d56324c77bcf62f`  
		Last Modified: Fri, 14 Mar 2025 03:45:02 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:e427d08dfb666a5754e2a663a6c3c8d21b6dd7b81af0d3834c48458869973207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e01b0cda6f198679127a3b70de768256f529beb20fcad134089acde7e75e32`

```dockerfile
```

-	Layers:
	-	`sha256:445439bf1e16ffb17f79b7dac1f79a15f1422c67aba3a8a0596e73941d6dfaeb`  
		Last Modified: Fri, 14 Mar 2025 03:45:00 GMT  
		Size: 7.9 MB (7941652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc5e9a0cdb1505beb8d4f90151111988aa1490b1503f5903b4deae4141b418d`  
		Last Modified: Fri, 14 Mar 2025 03:45:00 GMT  
		Size: 58.8 KB (58770 bytes)  
		MIME: application/vnd.in-toto+json
