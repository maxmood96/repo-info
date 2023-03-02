## `wordpress:beta-6.2-beta4-php8.2-apache`

```console
$ docker pull wordpress@sha256:e6064a4ba2cdced6aebf60dd94ed29571ef05c1e811f9cfa22c69b8a14e42036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; mips64le

### `wordpress:beta-6.2-beta4-php8.2-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:dbc0f6ad60f6f6f50e79d902da1e8bd86bc2a354e8f424c258dd49a173028b4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193734485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff4d5c760e093419217e45c0a47f45ea79b986fd9c28206ce430b9751b1af05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 02:10:54 GMT
ADD file:0bcd66a6a099cdb6e018ddc0f00270be93dccd3be6167ce36e9efc99c31549d9 in / 
# Wed, 01 Mar 2023 02:10:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:30:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 01 Mar 2023 07:30:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Mar 2023 07:31:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 07:31:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Mar 2023 07:32:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 01 Mar 2023 07:46:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Mar 2023 07:46:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Mar 2023 07:47:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 01 Mar 2023 07:47:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 01 Mar 2023 07:48:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 01 Mar 2023 07:48:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 07:48:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 07:48:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Mar 2023 07:48:15 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 01 Mar 2023 07:48:18 GMT
ENV PHP_VERSION=8.2.3
# Wed, 01 Mar 2023 07:48:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.3.tar.xz.asc
# Wed, 01 Mar 2023 07:48:24 GMT
ENV PHP_SHA256=b9b566686e351125d67568a33291650eb8dfa26614d205d70d82e6e92613d457
# Wed, 01 Mar 2023 07:49:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 01 Mar 2023 07:49:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 01 Mar 2023 08:03:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 01 Mar 2023 08:03:14 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 01 Mar 2023 08:03:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 01 Mar 2023 08:03:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 01 Mar 2023 08:03:27 GMT
STOPSIGNAL SIGWINCH
# Wed, 01 Mar 2023 08:03:30 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 01 Mar 2023 08:03:33 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 08:03:37 GMT
EXPOSE 80
# Wed, 01 Mar 2023 08:03:40 GMT
CMD ["apache2-foreground"]
# Thu, 02 Mar 2023 01:28:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 01:37:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 02 Mar 2023 01:37:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 02 Mar 2023 01:37:20 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 02 Mar 2023 01:37:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 02 Mar 2023 22:14:36 GMT
RUN set -eux; 	version='6.2-beta4'; 	sha1='5e0d13e507a7feebaec4a7159b055ae93d2c2271'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Thu, 02 Mar 2023 22:14:41 GMT
VOLUME [/var/www/html]
# Thu, 02 Mar 2023 22:14:46 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Thu, 02 Mar 2023 22:14:49 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Thu, 02 Mar 2023 22:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 22:14:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:89f6b45a7afd174bf0d443156831cacd9e6a26c834ad62610b6db53c731d257f`  
		Last Modified: Wed, 01 Mar 2023 02:18:50 GMT  
		Size: 29.6 MB (29634488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedae9eae022237deb536811a40aa3220ab22e8580c9e98415584086eaf1cea`  
		Last Modified: Wed, 01 Mar 2023 10:24:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194bbf1dfa35868e1855d2e14e246d7ad794c9a67424ffa08b595d716c666d1f`  
		Last Modified: Wed, 01 Mar 2023 10:25:19 GMT  
		Size: 71.8 MB (71814695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e6ed7f1ea9ca964a9b48bfe8f9497a1301a8420115c7f3f2e229a526e60f5a`  
		Last Modified: Wed, 01 Mar 2023 10:24:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961d5470c2e5e68c2929a398d79e3f12a1c269594ddf68693bdc4bd66f87f73a`  
		Last Modified: Wed, 01 Mar 2023 10:26:15 GMT  
		Size: 18.9 MB (18940588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0f861ee20f2935dd0a3056f2fa76dc1c14844fa83fed02df24804839c3f16`  
		Last Modified: Wed, 01 Mar 2023 10:26:03 GMT  
		Size: 441.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9570dbd31e5ea26b9a54f3effa1d3c9ab423f75476275f02971981a5cdfcf6ff`  
		Last Modified: Wed, 01 Mar 2023 10:26:03 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da94ea1cee9689b3ba31277cd4b6559e96de5fb9db4e6f2f30673a3113ca322`  
		Last Modified: Wed, 01 Mar 2023 10:26:07 GMT  
		Size: 12.2 MB (12160426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2481f553528f524f864b65c649a188422b2f5ce9c45aac00d69c4b307965f8c4`  
		Last Modified: Wed, 01 Mar 2023 10:26:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d4b690271f0a94e0023304b298dacecac3bc104057762dc2c019524bd670cb`  
		Last Modified: Wed, 01 Mar 2023 10:26:09 GMT  
		Size: 10.5 MB (10462717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efc606dd3250f51b992cfb860d4cfb87a4c10e755cdbc1d4f6a0de3a7667d37`  
		Last Modified: Wed, 01 Mar 2023 10:26:01 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd62ac7690f2c61be1578c9ea57d2829a1572ec66fcf06e45259bf28347d3cc`  
		Last Modified: Wed, 01 Mar 2023 10:26:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d47ad01cea659f290e5639157f2b06893a464df59e33ee16b09ce82ef00d76a`  
		Last Modified: Wed, 01 Mar 2023 10:26:01 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed3be4ed23fa3bece4e8e82f343ee93d9470c9859ac07a5a20cbf5e24885fc`  
		Last Modified: Thu, 02 Mar 2023 01:57:10 GMT  
		Size: 18.8 MB (18801139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd32eda433b50a4aab35f33d2859ca5d29a1a085cc5fcccc9ac4a346b6782f0`  
		Last Modified: Thu, 02 Mar 2023 01:57:03 GMT  
		Size: 9.0 MB (9049700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6df5d36a210f480c936c1a4b26aeb719a20fe9b23f806fe39dea8055ba0f4cc`  
		Last Modified: Thu, 02 Mar 2023 01:56:56 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944044eda73c8c5259501f7a47000264451960b32b2d9ef89f50c36a499f4413`  
		Last Modified: Thu, 02 Mar 2023 01:56:53 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865bddad0fc4cf638303c99cbd8ef93b86efa60aab4fc0aae631384f98362a4c`  
		Last Modified: Thu, 02 Mar 2023 01:56:54 GMT  
		Size: 19.5 KB (19498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2fa00ebf717ed35f4fb4308f5e3279705cb368a03475bf5628b7a86ea12af4`  
		Last Modified: Thu, 02 Mar 2023 22:23:07 GMT  
		Size: 22.8 MB (22840923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae910509e2e73bdc9a426a2b89198153b22f2dec5b5fd1469f689e1a41dfd2bc`  
		Last Modified: Thu, 02 Mar 2023 22:22:54 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff50ad121be02bb9ebb385e0f969622520b5b86a3a2d3f0e36eac4ca7445d958`  
		Last Modified: Thu, 02 Mar 2023 22:22:54 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
