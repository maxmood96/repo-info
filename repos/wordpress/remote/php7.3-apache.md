## `wordpress:php7.3-apache`

```console
$ docker pull wordpress@sha256:348b849b4a8ce80731d1a826227ecce80f847ad3d91dac9bffb95daba2c601f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `wordpress:php7.3-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:09896da45a0f954c8c67906be05182a0270cb25e0ff2a0f70975f92e032f94f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214441526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af65e632533fde36e69fb3677c7103a10d61a23d90235b0f40b8587f1584dca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:38:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Oct 2021 04:38:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Oct 2021 04:38:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:38:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Oct 2021 04:38:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 12 Oct 2021 04:45:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Oct 2021 04:45:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Oct 2021 04:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Oct 2021 04:45:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Oct 2021 04:45:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Oct 2021 04:45:17 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 12 Oct 2021 04:45:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 12 Oct 2021 04:45:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Oct 2021 04:45:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Oct 2021 04:45:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Oct 2021 08:01:15 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 12 Oct 2021 08:01:16 GMT
ENV PHP_VERSION=7.3.31
# Tue, 12 Oct 2021 08:01:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Tue, 12 Oct 2021 08:01:16 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Tue, 12 Oct 2021 08:01:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 08:01:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Oct 2021 08:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Oct 2021 08:08:40 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 12 Oct 2021 08:08:41 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Oct 2021 08:08:43 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 12 Oct 2021 08:08:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Oct 2021 08:08:43 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Oct 2021 08:08:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Oct 2021 08:08:44 GMT
WORKDIR /var/www/html
# Tue, 12 Oct 2021 08:08:44 GMT
EXPOSE 80
# Tue, 12 Oct 2021 08:08:45 GMT
CMD ["apache2-foreground"]
# Tue, 12 Oct 2021 19:44:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 19:45:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 		--with-webp-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 19:45:48 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 12 Oct 2021 19:45:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 12 Oct 2021 19:45:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 12 Oct 2021 19:45:56 GMT
RUN set -eux; 	version='5.8.1'; 	sha1='21e50add5a51cd9a18610244c942c08f7abeccd8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Tue, 12 Oct 2021 19:45:57 GMT
VOLUME [/var/www/html]
# Tue, 12 Oct 2021 19:45:57 GMT
COPY --chown=www-data:www-datafile:76be5fadb2e2d2b7a74d2770397579cd1402963fdca23912220f983ef906f582 in /usr/src/wordpress/ 
# Tue, 12 Oct 2021 19:45:57 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Tue, 12 Oct 2021 19:45:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 19:45:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b15dfd3cfa205395e33cb9ea4155c38a2a83a7acee7cb46fb9c169fcbe7411`  
		Last Modified: Tue, 12 Oct 2021 09:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64625c2e355fe69d0228e8a97fd6a1eb71879d7abe06240beec04e919e259c02`  
		Last Modified: Tue, 12 Oct 2021 09:04:08 GMT  
		Size: 91.6 MB (91605096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275a8dd8f3587f8c1fe7fc1f672f2e0757e95d18a018a5378cca93b98312415d`  
		Last Modified: Tue, 12 Oct 2021 09:03:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1c8ccc797aa9ff6819e95d6b867b2696860e31d2cac35e904316766ac9b44d`  
		Last Modified: Tue, 12 Oct 2021 09:04:43 GMT  
		Size: 19.2 MB (19235736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaf98f0c33af1f7822072ae2d18f8296d65b117192dbef2026b4bca3737656d`  
		Last Modified: Tue, 12 Oct 2021 09:04:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e7c544c3e3203131f005689418e38d82298c3bc2bce4db3efe927345f6e34e`  
		Last Modified: Tue, 12 Oct 2021 09:04:39 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8494c08e58ea8c63c28c8a0c7b4d6d60065b20071363b91aeafc1c3c69ca847a`  
		Last Modified: Tue, 12 Oct 2021 09:16:26 GMT  
		Size: 12.5 MB (12483815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcc8a5fd482580990a81465e2ed304c800f23625bf3a5013e0566e98e6a4fb9`  
		Last Modified: Tue, 12 Oct 2021 09:16:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f64edd244f05215172b2a7bd31f641ea839ba2f241c8e416266d1f62850d6e5`  
		Last Modified: Tue, 12 Oct 2021 09:16:26 GMT  
		Size: 14.6 MB (14621966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bd87f1fa92cef2143cade8ed9719b35c9b1ba9a1152d47c655ce98a4f98aae`  
		Last Modified: Tue, 12 Oct 2021 09:16:22 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352b198f8907eeda8007b89cb2f3c2aeb372dba0eb1adfbfbc6f61c23d269033`  
		Last Modified: Tue, 12 Oct 2021 09:16:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bc91f6e9a03e06754c2c87fccdca2a02ba2a8ad75871316bdbb70582fa4785`  
		Last Modified: Tue, 12 Oct 2021 09:16:22 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfcde10b381a138cef213e05ad0cfef34ee9f34333e72eb5c757545556ec62a`  
		Last Modified: Tue, 12 Oct 2021 09:16:22 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada29b4c1418b55b681116538ef819f7052ccaa2ef0e9c425a8c6468d31d37a`  
		Last Modified: Tue, 12 Oct 2021 19:56:32 GMT  
		Size: 19.0 MB (18982137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb337629241a5f42705554f14cf2f292e814c4f379aeab188ff2ea86d8f8ddc`  
		Last Modified: Tue, 12 Oct 2021 19:56:31 GMT  
		Size: 11.2 MB (11209892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f847ce8cd8a94e0a398fc5d8223bd2d36f326c94b7a182866ed85de95f60c5f`  
		Last Modified: Tue, 12 Oct 2021 19:56:28 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f329bc65b61725e4d2bf00ec0621ba7bcb0dbcac33407ad6f0bdbccc68e6fd`  
		Last Modified: Tue, 12 Oct 2021 19:56:26 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6829cc8ab8c476c3aa67de53506ab2099f976148ada7cd759df2be14c52f423a`  
		Last Modified: Tue, 12 Oct 2021 19:56:26 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98eeb01bbe21cec643d0e5456603abf490a141af393ee58c44a02ad09989bc3a`  
		Last Modified: Tue, 12 Oct 2021 19:56:29 GMT  
		Size: 14.9 MB (14915619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b641924cb334f0baabdb3f723846ee2a6b3854abc388493637667f49993b57a5`  
		Last Modified: Tue, 12 Oct 2021 19:56:26 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0ef6b440e1dfb691ff79a397b7f2f098f577bfc6c0b17e55b93b7cbdad70b5`  
		Last Modified: Tue, 12 Oct 2021 19:56:26 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.3-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:31006b6f45549ab4a486dfd3c4b54e126eb199594aee5136e8b70a128e9acda4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190325965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f728d8fc4cfea0450ab7a8aff281e07deaca9a658fec6b766cdb807ce6f7f6fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Oct 2021 00:50:30 GMT
ADD file:fb1afabdc1f93b4866b4c4d696f272b4888519cb5bf35eb7ed1a4c021d1a04c8 in / 
# Tue, 12 Oct 2021 00:50:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 07:37:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Oct 2021 07:37:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Oct 2021 07:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 07:37:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Oct 2021 07:37:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 12 Oct 2021 07:43:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Oct 2021 07:43:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Oct 2021 07:43:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Oct 2021 07:43:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Oct 2021 07:43:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Oct 2021 07:43:57 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 12 Oct 2021 07:43:58 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 12 Oct 2021 07:43:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Oct 2021 07:43:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Oct 2021 07:43:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Oct 2021 10:01:25 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 12 Oct 2021 10:01:26 GMT
ENV PHP_VERSION=7.3.31
# Tue, 12 Oct 2021 10:01:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Tue, 12 Oct 2021 10:01:27 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Tue, 12 Oct 2021 10:01:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 10:01:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Oct 2021 10:06:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Oct 2021 10:06:14 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 12 Oct 2021 10:06:15 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Oct 2021 10:06:17 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 12 Oct 2021 10:06:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Oct 2021 10:06:18 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Oct 2021 10:06:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Oct 2021 10:06:19 GMT
WORKDIR /var/www/html
# Tue, 12 Oct 2021 10:06:19 GMT
EXPOSE 80
# Tue, 12 Oct 2021 10:06:20 GMT
CMD ["apache2-foreground"]
# Wed, 13 Oct 2021 07:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 07:21:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 		--with-webp-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 07:21:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 13 Oct 2021 07:21:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 13 Oct 2021 07:21:20 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Wed, 13 Oct 2021 07:21:28 GMT
RUN set -eux; 	version='5.8.1'; 	sha1='21e50add5a51cd9a18610244c942c08f7abeccd8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Wed, 13 Oct 2021 07:21:29 GMT
VOLUME [/var/www/html]
# Wed, 13 Oct 2021 07:21:29 GMT
COPY --chown=www-data:www-datafile:76be5fadb2e2d2b7a74d2770397579cd1402963fdca23912220f983ef906f582 in /usr/src/wordpress/ 
# Wed, 13 Oct 2021 07:21:30 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Wed, 13 Oct 2021 07:21:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 07:21:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5c9bab66abc5c53391435f6fd66e0ff3571295d568f45ac7d2dc480bcbfd56e8`  
		Last Modified: Tue, 12 Oct 2021 01:06:07 GMT  
		Size: 28.9 MB (28899715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569af31a3f546449c97619c10ce4bf50f7b5b53264865389d304aac632e1a590`  
		Last Modified: Tue, 12 Oct 2021 10:53:46 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa45e316719e67a0a4586c32f9f5226e0c60cc548199b5b6a4da1ef6ff38799`  
		Last Modified: Tue, 12 Oct 2021 10:54:22 GMT  
		Size: 73.7 MB (73684492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be2abc1db535bad2c3b042ee74207b681476c834f649b7f8435aebd6e2e76c8`  
		Last Modified: Tue, 12 Oct 2021 10:53:46 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4273f5c9ea07a27eb93a031e207cfaa52ddb62a6854f5c4895ec96fbcb049915`  
		Last Modified: Tue, 12 Oct 2021 10:55:13 GMT  
		Size: 18.5 MB (18525831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf2d473f376456fa9bbb3ac6543042b9d8e6690e10e9f0c0dfb504d2cfd89f4`  
		Last Modified: Tue, 12 Oct 2021 10:55:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd3b22adc21293942029cb70d452ee01d91e7eab707e2ac5bddd1ef4d5e586c`  
		Last Modified: Tue, 12 Oct 2021 10:55:03 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb228941585d0bf930a9789c2adb8adf719e01b91c664a7981ede4f72266420`  
		Last Modified: Tue, 12 Oct 2021 11:16:33 GMT  
		Size: 12.5 MB (12482226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd098369336321682b2a63d6c461bdb95a381012f93779171ecde8f783de6f`  
		Last Modified: Tue, 12 Oct 2021 11:16:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ea8c09a02711aab9c260aabf8835368104a77f6dcff7e66ad6ba61a20648d7`  
		Last Modified: Tue, 12 Oct 2021 11:16:39 GMT  
		Size: 13.7 MB (13671643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb4eb87a23b4b8914bcda2563b23ae7a1902e5332e28dc54b6bcbff182256f3`  
		Last Modified: Tue, 12 Oct 2021 11:16:28 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355593a5642f99787370e608d23f9d22e80ea541063c282ddcb7b50b3621ae27`  
		Last Modified: Tue, 12 Oct 2021 11:16:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30a20d2dd12cf49a6a7ae4940efa41a088ef36b5d54e1b8bacb31a7491a99aa`  
		Last Modified: Tue, 12 Oct 2021 11:16:28 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828df60073889be49df78b8406316be402645247d3eee5e3813081832713509e`  
		Last Modified: Tue, 12 Oct 2021 11:16:28 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6d840e4a0b6825ca9683fb0cedd3e9213a848e56c2ca11b61768a9d756d02e`  
		Last Modified: Wed, 13 Oct 2021 07:40:52 GMT  
		Size: 18.6 MB (18565809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5901f31083534636884a9265e72f6d9d3607fbec854512971cfc0bcacc2168`  
		Last Modified: Wed, 13 Oct 2021 07:40:44 GMT  
		Size: 9.6 MB (9550653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497506fa63f3076b354c290b1504b8ce85c2b1b49912f1de85097a3a18e890e3`  
		Last Modified: Wed, 13 Oct 2021 07:40:38 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7aa035a797db8114796de0ff23292b7d60f59de67f562766a316580a44426b8`  
		Last Modified: Wed, 13 Oct 2021 07:40:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028f6a8942e16f5223643ad90a8fa3fa192b68523a57ddec1685123bb0d8a474`  
		Last Modified: Wed, 13 Oct 2021 07:40:37 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8691c11c767a8870869a60e36644843d2b880b8d38c2db77074f1540bc08f1e`  
		Last Modified: Wed, 13 Oct 2021 07:40:49 GMT  
		Size: 14.9 MB (14915615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8adc4b0f29f91168c732a984b0625016ab5704ed25c42d44824498fe41dded`  
		Last Modified: Wed, 13 Oct 2021 07:40:36 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e52c6c87faf4f86ee5a27f200ee0eb8a7bb8025724d19ba3314a4903daeb6f`  
		Last Modified: Wed, 13 Oct 2021 07:40:36 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.3-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:1a163d49d2a5929e87873c9572c85c314f27887dc6bee76641641af37be8fd99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181013855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314000c1e9b5218b11c3ecbabdb77b46586ea27ab423e8b281247a46e8b54d8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 30 Sep 2021 18:03:01 GMT
ADD file:129e2106788d883a456b145d9aff00c3003ee3480901a30318933b46961d31f3 in / 
# Thu, 30 Sep 2021 18:03:02 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 07:11:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 01 Oct 2021 07:11:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 01 Oct 2021 07:12:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 07:12:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 01 Oct 2021 07:12:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 01 Oct 2021 07:17:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 01 Oct 2021 07:17:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 01 Oct 2021 07:17:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 01 Oct 2021 07:17:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 01 Oct 2021 07:17:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 01 Oct 2021 07:17:36 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 01 Oct 2021 07:17:36 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 01 Oct 2021 07:17:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Oct 2021 07:17:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 01 Oct 2021 07:17:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 01 Oct 2021 09:44:55 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 01 Oct 2021 09:44:55 GMT
ENV PHP_VERSION=7.3.31
# Fri, 01 Oct 2021 09:44:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Fri, 01 Oct 2021 09:44:56 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Fri, 01 Oct 2021 09:45:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Oct 2021 09:45:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 01 Oct 2021 09:49:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 01 Oct 2021 09:49:31 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 01 Oct 2021 09:49:33 GMT
RUN docker-php-ext-enable sodium
# Fri, 01 Oct 2021 09:49:35 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 01 Oct 2021 09:49:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 01 Oct 2021 09:49:36 GMT
STOPSIGNAL SIGWINCH
# Fri, 01 Oct 2021 09:49:36 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 01 Oct 2021 09:49:37 GMT
WORKDIR /var/www/html
# Fri, 01 Oct 2021 09:49:37 GMT
EXPOSE 80
# Fri, 01 Oct 2021 09:49:38 GMT
CMD ["apache2-foreground"]
# Sat, 02 Oct 2021 02:56:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 02:59:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 		--with-webp-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 02:59:45 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 02 Oct 2021 02:59:46 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 02 Oct 2021 02:59:48 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sat, 02 Oct 2021 02:59:56 GMT
RUN set -eux; 	version='5.8.1'; 	sha1='21e50add5a51cd9a18610244c942c08f7abeccd8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Sat, 02 Oct 2021 02:59:57 GMT
VOLUME [/var/www/html]
# Fri, 08 Oct 2021 00:29:41 GMT
COPY --chown=www-data:www-datafile:76be5fadb2e2d2b7a74d2770397579cd1402963fdca23912220f983ef906f582 in /usr/src/wordpress/ 
# Fri, 08 Oct 2021 00:29:42 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Fri, 08 Oct 2021 00:29:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Oct 2021 00:29:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:aad43ac6bd46b2cab91485c8f1dac6a985df690af3e431e9e0b9fd57ad5ed423`  
		Last Modified: Thu, 30 Sep 2021 18:19:26 GMT  
		Size: 26.6 MB (26571924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc04cef8f8627fec47e2a3eb3b9a38bb4c4290ed46d7e305378d7149b2e930b0`  
		Last Modified: Fri, 01 Oct 2021 10:42:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86a525f93386992c2bfae8402f2b99aa5ac77277c8167221477a7ffc2a1e490`  
		Last Modified: Fri, 01 Oct 2021 10:43:36 GMT  
		Size: 69.3 MB (69315051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c523bc9f9ff25debed4e73699365ed85865b8a8ff27ec75d66da9ab56f01925a`  
		Last Modified: Fri, 01 Oct 2021 10:42:53 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d798e63debefa1fee1bb05d3904c730c2780cddf75e24de5f3e835af989a917b`  
		Last Modified: Fri, 01 Oct 2021 10:44:24 GMT  
		Size: 18.0 MB (17974946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bab41e11063c31d140920e1c2cdfae340af788d0b64f6bbfc5ae31a290bf81`  
		Last Modified: Fri, 01 Oct 2021 10:44:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74492d78af3e011543f46f756da40bb4e0f0eabe90825f8154ae6a7d828b9638`  
		Last Modified: Fri, 01 Oct 2021 10:44:14 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c4929387a8b76dcff1682d94adfc26c241fd0a5048aefd6e3e59d6d7f8ba9f`  
		Last Modified: Fri, 01 Oct 2021 11:05:21 GMT  
		Size: 12.5 MB (12482106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4e0c70c9a936948c00da3efef45be21d364dec3b5a201a4f80fab7d84417c0`  
		Last Modified: Fri, 01 Oct 2021 11:05:17 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e824d2cd41d1dfdb9712364fa4ca88f231016140cc4822f0d92c8024414f33`  
		Last Modified: Fri, 01 Oct 2021 11:05:25 GMT  
		Size: 13.0 MB (12973858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e49c616703aed806498255a9c828822b3eee9ae0804dace3db3909246734a69`  
		Last Modified: Fri, 01 Oct 2021 11:05:16 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69098e3ad21c9a202189cbd275c8dd3bd1153127063cbcc7d0d12dd88c5bd721`  
		Last Modified: Fri, 01 Oct 2021 11:05:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aa8a4922f683d14ba9ed38f929aca17e1deb34b316796c23ca084fec3c9348`  
		Last Modified: Fri, 01 Oct 2021 11:05:16 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6504526a7fa7cffe0dd09a953a91fb6a1794eb7e27be115d3533177ce5bd4ad`  
		Last Modified: Fri, 01 Oct 2021 11:05:16 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdb34487d885c27f8da5ea80906f07b424fb613024dade569b2b62abb10781`  
		Last Modified: Sat, 02 Oct 2021 03:32:42 GMT  
		Size: 18.1 MB (18112243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf5359e9b18d23f8045104133228651337fc5bf54be6f9c6c2943069ef703d9`  
		Last Modified: Sat, 02 Oct 2021 03:32:34 GMT  
		Size: 8.6 MB (8638141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7635095e3d5bb646ea84a8e40ec4a24a579a04dc267f0166965fbb81bd103c0`  
		Last Modified: Sat, 02 Oct 2021 03:32:30 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3791d7368339fe74ea1579fa1ff2f02d0f10b093b80f7f7f8a7bc760cd9c1e85`  
		Last Modified: Sat, 02 Oct 2021 03:32:28 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b761eb2c79f86996ed198de5df3866c6a6839de8fcb299d309a429e9fb773dad`  
		Last Modified: Sat, 02 Oct 2021 03:32:28 GMT  
		Size: 19.5 KB (19506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a909d19a18385f5605a8f5bd9263f999a1428425c565c8f89cc0855b9991e`  
		Last Modified: Sat, 02 Oct 2021 03:32:41 GMT  
		Size: 14.9 MB (14915621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb24fd0afce321d4d0ef5006dd74ccbeaef8d0dc4eac0e037aab8912f38333bd`  
		Last Modified: Fri, 08 Oct 2021 00:40:37 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8039e5b6390fdd85b54872a5d1806fa4d741d540ab88143c2b16332a759b5050`  
		Last Modified: Fri, 08 Oct 2021 00:40:37 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.3-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:b552aaf6d0c026409deb5564aae5b45e42227b14d02d06213ef52b0f58159af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205890112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86377a9a86e5e246198aac8b4883bbbb90b2a839ebfcfa4a46c3189b7ca20b32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:43 GMT
ADD file:6472ab63529e688735f77634402740e08fdbd5bfa788c150915027993df7e8ec in / 
# Tue, 28 Sep 2021 01:40:44 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 08:40:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 28 Sep 2021 08:40:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 28 Sep 2021 08:40:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 08:40:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 28 Sep 2021 08:40:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 28 Sep 2021 08:46:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 28 Sep 2021 08:46:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 28 Sep 2021 08:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 28 Sep 2021 08:46:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 28 Sep 2021 08:46:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 28 Sep 2021 08:46:34 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 28 Sep 2021 08:46:34 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 28 Sep 2021 08:46:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 28 Sep 2021 08:46:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 28 Sep 2021 08:46:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 28 Sep 2021 10:29:41 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 28 Sep 2021 10:29:41 GMT
ENV PHP_VERSION=7.3.31
# Tue, 28 Sep 2021 10:29:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Tue, 28 Sep 2021 10:29:42 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Tue, 28 Sep 2021 10:30:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 28 Sep 2021 10:30:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 28 Sep 2021 10:32:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 28 Sep 2021 10:32:12 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 28 Sep 2021 10:32:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 28 Sep 2021 10:32:13 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 28 Sep 2021 10:32:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 28 Sep 2021 10:32:14 GMT
STOPSIGNAL SIGWINCH
# Tue, 28 Sep 2021 10:32:14 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 28 Sep 2021 10:32:14 GMT
WORKDIR /var/www/html
# Tue, 28 Sep 2021 10:32:14 GMT
EXPOSE 80
# Tue, 28 Sep 2021 10:32:14 GMT
CMD ["apache2-foreground"]
# Wed, 29 Sep 2021 08:02:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 00:51:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 		--with-webp-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 00:51:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 01 Oct 2021 00:51:52 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 01 Oct 2021 00:51:53 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Fri, 01 Oct 2021 00:51:55 GMT
RUN set -eux; 	version='5.8.1'; 	sha1='21e50add5a51cd9a18610244c942c08f7abeccd8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Fri, 01 Oct 2021 00:51:56 GMT
VOLUME [/var/www/html]
# Thu, 07 Oct 2021 22:12:07 GMT
COPY --chown=www-data:www-datafile:76be5fadb2e2d2b7a74d2770397579cd1402963fdca23912220f983ef906f582 in /usr/src/wordpress/ 
# Thu, 07 Oct 2021 22:12:08 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Thu, 07 Oct 2021 22:12:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:12:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2f8871a8654eb1158cb626f8dc69992dba7e4bd8796fae6aa7cf967f951f5fe9`  
		Last Modified: Tue, 28 Sep 2021 01:48:25 GMT  
		Size: 30.1 MB (30055408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fde038d1d179badf8983debd43730ffa4f219c58b954a2a7e6e40ef6fb4bef`  
		Last Modified: Tue, 28 Sep 2021 11:03:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5c30d0e4e57d9f789bd00fb9136dfb0e8362285ad6c7cd1b60e8df9495cd81`  
		Last Modified: Tue, 28 Sep 2021 11:04:04 GMT  
		Size: 86.9 MB (86921153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6438a4ca98d26b0746da0821bfa516803f9bb8491c4cedea24b02ae3886baf`  
		Last Modified: Tue, 28 Sep 2021 11:03:45 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79f3e6de014e3b5b08769ff011c6974b63280c3dc11f99385010eafabf3bed4`  
		Last Modified: Tue, 28 Sep 2021 11:04:42 GMT  
		Size: 19.1 MB (19140118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b353c0d7d33e60f571615e44a5d177bdd0095bb6f8bb81cb4e19eda85f4dd2ba`  
		Last Modified: Tue, 28 Sep 2021 11:04:38 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48112d673c74db75a7fb4ed585fdf08478ea5e055f32adc4355513ef329550fc`  
		Last Modified: Tue, 28 Sep 2021 11:04:38 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fa9f02c851334f1d95c8c13f64f8b9c9a82be64a521381c2ef150592e9800`  
		Last Modified: Tue, 28 Sep 2021 11:17:49 GMT  
		Size: 12.5 MB (12482844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc87b40b6f15625c231e22776883bfa66b1f63eb4cf776601bee4ad358bbc3b1`  
		Last Modified: Tue, 28 Sep 2021 11:17:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af063ed98f660ecfacec6d5f6500179a70c9e701350607d880b19a4d8f71109`  
		Last Modified: Tue, 28 Sep 2021 11:17:49 GMT  
		Size: 14.2 MB (14219281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac96302a212228fa0b2f2fac5e40df1bb13449d4d31d5c8f990a9f4a7cb6c6c`  
		Last Modified: Tue, 28 Sep 2021 11:17:46 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3b5c717faca36f38e7992a823b3f803d07b59d32858cc8516a9cee8be6ff25`  
		Last Modified: Tue, 28 Sep 2021 11:17:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd352333fc8f2750842ef2188fd5fc6b1ccdf81a739cc879d538bbf26ee8e916`  
		Last Modified: Tue, 28 Sep 2021 11:17:46 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084895755d942a66347d5dcd082a1880e8f7be523291e001ade4a9364ef0a270`  
		Last Modified: Tue, 28 Sep 2021 11:17:46 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a29891afa0910eef07078a6f0b820eeb66363dd3e061fca23a68c1d0bc7eb3`  
		Last Modified: Wed, 29 Sep 2021 08:13:30 GMT  
		Size: 19.0 MB (18954601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf10f7af03abffee5be7442e12fc7b7b061c8ec32db96e4a49080da5177450`  
		Last Modified: Fri, 01 Oct 2021 01:07:43 GMT  
		Size: 9.2 MB (9171164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c12c11d05112a45adacdab566bcb09c7e997f6f3f7d8432caca4bcae60fbb84`  
		Last Modified: Fri, 01 Oct 2021 01:07:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ec4f053c8268863da3652901588a705ff7b48e4b65b0bed5c1eedc302cc969`  
		Last Modified: Fri, 01 Oct 2021 01:07:40 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72b0e5836e0e10426cf0d1d38a1f38ff7e49ea6e3a3479490bc3474192b697c`  
		Last Modified: Fri, 01 Oct 2021 01:07:40 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4b11f9c815151e48a4beb4a7f144b7517fd59e02009cabda879cfb14df2052`  
		Last Modified: Fri, 01 Oct 2021 01:07:43 GMT  
		Size: 14.9 MB (14915606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aee3a1aba63ea280e2632ac6e5ee08f367ab2b1689178f55a52db0fc9979aeb`  
		Last Modified: Thu, 07 Oct 2021 22:18:18 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65e727eee85ba4f192148a94503dae9a1ac7bd667946bac298f87a9c8c25fbd`  
		Last Modified: Thu, 07 Oct 2021 22:18:18 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.3-apache` - linux; 386

```console
$ docker pull wordpress@sha256:e3b7a3b45303b69f67c7f1a5c8cfbdfa4d20732c1deff41aa933829d60caa2d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (217003870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b648bede192d97ee1320519dcdc4a210e2d47b410682d7f1173c2043d0fef790`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:47 GMT
ADD file:42196ffa4c70af8d9f1e7b74edb3bb92d47296acf989adf615e8208230f8bd0c in / 
# Tue, 12 Oct 2021 01:39:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:16:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Oct 2021 18:16:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Oct 2021 18:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:16:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Oct 2021 18:16:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 12 Oct 2021 18:23:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Oct 2021 18:23:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Oct 2021 18:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Oct 2021 18:23:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Oct 2021 18:23:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Oct 2021 18:23:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 12 Oct 2021 18:23:26 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 12 Oct 2021 18:23:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Oct 2021 18:23:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Oct 2021 18:23:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Oct 2021 20:55:02 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 12 Oct 2021 20:55:03 GMT
ENV PHP_VERSION=7.3.31
# Tue, 12 Oct 2021 20:55:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Tue, 12 Oct 2021 20:55:03 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Tue, 12 Oct 2021 20:55:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 20:55:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Oct 2021 21:00:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Oct 2021 21:00:29 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 12 Oct 2021 21:00:30 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Oct 2021 21:00:32 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 12 Oct 2021 21:00:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Oct 2021 21:00:32 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Oct 2021 21:00:33 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Oct 2021 21:00:33 GMT
WORKDIR /var/www/html
# Tue, 12 Oct 2021 21:00:33 GMT
EXPOSE 80
# Tue, 12 Oct 2021 21:00:33 GMT
CMD ["apache2-foreground"]
# Wed, 13 Oct 2021 06:33:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:35:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 		--with-webp-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:35:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 13 Oct 2021 06:35:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 13 Oct 2021 06:35:14 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Wed, 13 Oct 2021 06:35:19 GMT
RUN set -eux; 	version='5.8.1'; 	sha1='21e50add5a51cd9a18610244c942c08f7abeccd8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Wed, 13 Oct 2021 06:35:20 GMT
VOLUME [/var/www/html]
# Wed, 13 Oct 2021 06:35:20 GMT
COPY --chown=www-data:www-datafile:76be5fadb2e2d2b7a74d2770397579cd1402963fdca23912220f983ef906f582 in /usr/src/wordpress/ 
# Wed, 13 Oct 2021 06:35:21 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Wed, 13 Oct 2021 06:35:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 06:35:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:87318d165b5c0fdf05c8ccf97d83084f56b4608075a3335b1a46c76295b82753`  
		Last Modified: Tue, 12 Oct 2021 01:47:39 GMT  
		Size: 32.4 MB (32370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d7b55744f495c4538bc35e1935df5ce5a3ac7584169b9dadb5641beaa08fc6`  
		Last Modified: Tue, 12 Oct 2021 22:06:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55f1f83e7520231f01d19a9decf9941bac0dc2290dbc514216b787edacfb1f8`  
		Last Modified: Tue, 12 Oct 2021 22:06:55 GMT  
		Size: 92.7 MB (92716556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff493eb0e3106a89b7c5f55740e05ffe39bde5673df81dea4f0a8609627c220a`  
		Last Modified: Tue, 12 Oct 2021 22:06:16 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae05156eebdd94107900118e3da52a91e1b61ce12bcd59c1e08419517ed5ed90`  
		Last Modified: Tue, 12 Oct 2021 22:07:49 GMT  
		Size: 19.7 MB (19713810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df85d9bc98416a8f2cf28362008d41b0704f55c78064c00824a48889ca88f620`  
		Last Modified: Tue, 12 Oct 2021 22:07:39 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c77e1860324939b5cb12581995bd0f576c4290473ab64d2d7d8f695aac3821`  
		Last Modified: Tue, 12 Oct 2021 22:07:39 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e953d604221d52f3c188acbe22cd058661cf8f380516e63b5770e851d0f933`  
		Last Modified: Tue, 12 Oct 2021 22:25:52 GMT  
		Size: 12.5 MB (12482968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8cdb6b75dcb7b6e68cd5a6fd0b2ea391d5c2a45f6c3467d4e4f12a5982b0c4`  
		Last Modified: Tue, 12 Oct 2021 22:25:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7069d2aedd43cf905aeb91acf757f8e1a66886fcfadca9a1e86702926069a9de`  
		Last Modified: Tue, 12 Oct 2021 22:25:54 GMT  
		Size: 15.0 MB (14998973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6245e92ead374a3e171048e3c51cafbbe0942e2d490d4317d09b93c1538089`  
		Last Modified: Tue, 12 Oct 2021 22:25:47 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a857a9cc1fb535bbb40bae4b37f97d00f235cc20a93a4cb556fc459fd895824`  
		Last Modified: Tue, 12 Oct 2021 22:25:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c1ba37da7c96f7213d0a7183f438f8f3f97ff94de49e4d157a7cde17a34f96`  
		Last Modified: Tue, 12 Oct 2021 22:25:47 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a1493d45d729b49a0298415c6b379bd1c33c77b223f968fa7f4f0e68751af3`  
		Last Modified: Tue, 12 Oct 2021 22:25:47 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3d5944276d8862121f1438e0b8ea4daeb59fd08fca111890bfa4c42359e23b`  
		Last Modified: Wed, 13 Oct 2021 06:49:30 GMT  
		Size: 19.3 MB (19328238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247585aac6beae6d5050bff5ec26d3ba3ab4e69425b1257db0c5662ff8940184`  
		Last Modified: Wed, 13 Oct 2021 06:49:27 GMT  
		Size: 10.4 MB (10447401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72520a0a634d4ff0271e88064de2c7000ec452ae736c45d0cc2d48e5f2d60aa`  
		Last Modified: Wed, 13 Oct 2021 06:49:21 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cf6c8486bfc1a9fdc87c72aeeb9ba2fe013d452d404051f8c900c8bb0c1b72`  
		Last Modified: Wed, 13 Oct 2021 06:49:19 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a345e246dc116f6075141ee8e668dfe2362264681ff99c0235a7ac41ed706f2`  
		Last Modified: Wed, 13 Oct 2021 06:49:18 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a00b7eee7a7fa98a0fea75c13ef6628b24450753ab4c18999b864281478bb3f`  
		Last Modified: Wed, 13 Oct 2021 06:49:27 GMT  
		Size: 14.9 MB (14915624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475c43dd6103fb7e48067b47e425050819ace2f2d9f8de305d7322866a618ee3`  
		Last Modified: Wed, 13 Oct 2021 06:49:18 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70192d7d2e5b12a90f3a7856358086377d8c68fa22f1f85b35334de633e076b`  
		Last Modified: Wed, 13 Oct 2021 06:49:18 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.3-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:d939f4245f8a24a6c919d1e0cb8127690dcce83426ea35afacd409b3ae1bac16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189945716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3616d4ac04afcf78e83e25636526d70b33c9df75e71a9ba22d5f2f71d21b9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 28 Sep 2021 02:10:40 GMT
ADD file:43593ef3d79c9b74a92e318d44aacb578f6f8d835dd72665e057bbfe73df1a93 in / 
# Tue, 28 Sep 2021 02:10:41 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 18:07:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 05 Oct 2021 18:07:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 05 Oct 2021 18:08:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 18:08:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Oct 2021 18:09:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 05 Oct 2021 18:22:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 05 Oct 2021 18:22:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 05 Oct 2021 18:22:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 05 Oct 2021 18:22:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 05 Oct 2021 18:22:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 05 Oct 2021 18:22:45 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 05 Oct 2021 18:22:46 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 05 Oct 2021 18:22:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Oct 2021 18:22:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Oct 2021 18:22:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Oct 2021 23:20:44 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 05 Oct 2021 23:20:45 GMT
ENV PHP_VERSION=7.3.31
# Tue, 05 Oct 2021 23:20:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Tue, 05 Oct 2021 23:20:45 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Tue, 05 Oct 2021 23:21:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 05 Oct 2021 23:21:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Oct 2021 23:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Oct 2021 23:29:11 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 05 Oct 2021 23:29:13 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Oct 2021 23:29:15 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 05 Oct 2021 23:29:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Oct 2021 23:29:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 05 Oct 2021 23:29:16 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 05 Oct 2021 23:29:17 GMT
WORKDIR /var/www/html
# Tue, 05 Oct 2021 23:29:17 GMT
EXPOSE 80
# Tue, 05 Oct 2021 23:29:17 GMT
CMD ["apache2-foreground"]
# Wed, 06 Oct 2021 06:05:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 06:09:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 		--with-webp-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 06:09:08 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 06 Oct 2021 06:09:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 06 Oct 2021 06:09:13 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Wed, 06 Oct 2021 06:09:23 GMT
RUN set -eux; 	version='5.8.1'; 	sha1='21e50add5a51cd9a18610244c942c08f7abeccd8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Wed, 06 Oct 2021 06:09:24 GMT
VOLUME [/var/www/html]
# Thu, 07 Oct 2021 22:44:20 GMT
COPY --chown=www-data:www-datafile:76be5fadb2e2d2b7a74d2770397579cd1402963fdca23912220f983ef906f582 in /usr/src/wordpress/ 
# Thu, 07 Oct 2021 22:44:21 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Thu, 07 Oct 2021 22:44:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 22:44:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1f46ea49e27fccc580c8910db39ba7f51ae208a8d24d46a33140afa92ea3d955`  
		Last Modified: Tue, 28 Sep 2021 02:20:45 GMT  
		Size: 29.6 MB (29627871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb3954c2ebaa7beddbb1101815a7e2a32441a3dd24b13ee9da76118a5dc9930`  
		Last Modified: Wed, 06 Oct 2021 00:44:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5fb416109a5c1e554a74a010df8337b5919d464aebb4afddf07e51b1ecefce`  
		Last Modified: Wed, 06 Oct 2021 00:45:36 GMT  
		Size: 72.0 MB (72015417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c0cb3c9d612552ab5732ac5d43475333eb653f4cc692430fb9de69a48fe4fa`  
		Last Modified: Wed, 06 Oct 2021 00:44:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4d309af0d905fd49bcd5a77fc83b9b57f1f09249749c40e1caa924b6c9eccf`  
		Last Modified: Wed, 06 Oct 2021 00:46:24 GMT  
		Size: 19.1 MB (19128821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a64a67d39d32bd7f74f1c4ef9a2c6a215d9c0d3e9e3255baaa8c82a4a50166`  
		Last Modified: Wed, 06 Oct 2021 00:46:11 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af3ddc372b285ad8badb325503acf7ee26fad2f1fe9aff2eda73883f52a633c`  
		Last Modified: Wed, 06 Oct 2021 00:46:11 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cd9cdbb656cbb9984ba602f39d99c8d6ca8cd2e610cce0aa57129ef475fb2d`  
		Last Modified: Wed, 06 Oct 2021 01:03:16 GMT  
		Size: 12.5 MB (12481110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a6d99458b1433117ec94955a656e4e0adf478ba998abd33eee84e2d65e10e`  
		Last Modified: Wed, 06 Oct 2021 01:03:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8997966f78b29711345ae4c3f95dd198ffc922468cc9b9564c12085c2c67a295`  
		Last Modified: Wed, 06 Oct 2021 01:03:22 GMT  
		Size: 13.8 MB (13816690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a5bd0827ac1fa33605d82d0161746f32e493605fb36700d176c912ec82a2cb`  
		Last Modified: Wed, 06 Oct 2021 01:03:10 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5936f1bc28f0f82da607151d3b60857c8b605935df956792854120aef1d56d9f`  
		Last Modified: Wed, 06 Oct 2021 01:03:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d000361198dc4d6f7c52a0a755d9d47377f05aa1a6f6e950e9373301b569e`  
		Last Modified: Wed, 06 Oct 2021 01:03:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2864b7f46dc4ddbe9b04a87726b1d44da51ba473fec4fe81cb0146be23485232`  
		Last Modified: Wed, 06 Oct 2021 01:03:10 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112c04c77366bf53fcc2da544b0b05c76995972aa37e9df1ce8edcd284639f78`  
		Last Modified: Wed, 06 Oct 2021 06:25:22 GMT  
		Size: 18.8 MB (18794959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc67b9519aed01f4b74ab66ba8d42174c3b0b12256687ce84010bea036a078d7`  
		Last Modified: Wed, 06 Oct 2021 06:25:15 GMT  
		Size: 9.1 MB (9135409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf48aee877b1c46e8f53d70808c364a17c6187fc210fac2c5a2dd7559627dca`  
		Last Modified: Wed, 06 Oct 2021 06:25:06 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3320b33ebdd6a395d526f4fa501e2013e4db186a6596962bfd77dd333b2687f4`  
		Last Modified: Wed, 06 Oct 2021 06:25:04 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb4f090562541a856c73f31ff85c17d897376782509ca5f307b206a61f7503b`  
		Last Modified: Wed, 06 Oct 2021 06:25:04 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1417effc65f4ad633f842df2d7c206384163604f553d8c261489af24cf9d554d`  
		Last Modified: Wed, 06 Oct 2021 06:25:18 GMT  
		Size: 14.9 MB (14915587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e16b93d1155cf89f64ed225ba9fd11b8a84de08e7a63625b94c6970873519bd`  
		Last Modified: Thu, 07 Oct 2021 22:46:49 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3555e3708bde0c8c3fb5f5327ebaee30e23952faa4e29896af980e6abb7abfd4`  
		Last Modified: Thu, 07 Oct 2021 22:46:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.3-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:8c96b4b943a92b87c926813ca296c97619db1b2c528aa588d2ac47b60715ceac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215841981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbd373741a4deec0f6c8b78ca2bf4b0c578c5f5553697b9e178e4d50657eaf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 04 Oct 2021 17:55:01 GMT
ADD file:f4b696a766a0d9a808c171a1d5db4f0877b0a784649d63bf461dfcf54b532239 in / 
# Mon, 04 Oct 2021 17:55:06 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 01:45:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 05 Oct 2021 01:45:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 05 Oct 2021 01:47:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 01:47:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 Oct 2021 01:47:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 05 Oct 2021 01:55:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 05 Oct 2021 01:55:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 05 Oct 2021 01:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 05 Oct 2021 01:57:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 05 Oct 2021 01:57:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 05 Oct 2021 01:58:02 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 05 Oct 2021 01:58:06 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 05 Oct 2021 01:58:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Oct 2021 01:58:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 Oct 2021 01:58:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 Oct 2021 06:28:05 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 05 Oct 2021 06:28:11 GMT
ENV PHP_VERSION=7.3.31
# Tue, 05 Oct 2021 06:28:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Tue, 05 Oct 2021 06:28:15 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Tue, 05 Oct 2021 06:29:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 05 Oct 2021 06:29:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 05 Oct 2021 06:35:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 05 Oct 2021 06:35:56 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 05 Oct 2021 06:36:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 05 Oct 2021 06:36:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 05 Oct 2021 06:36:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 05 Oct 2021 06:36:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 05 Oct 2021 06:36:35 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 05 Oct 2021 06:36:46 GMT
WORKDIR /var/www/html
# Tue, 05 Oct 2021 06:36:51 GMT
EXPOSE 80
# Tue, 05 Oct 2021 06:36:56 GMT
CMD ["apache2-foreground"]
# Tue, 05 Oct 2021 11:36:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 11:47:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 		--with-webp-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 11:47:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 05 Oct 2021 11:47:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 05 Oct 2021 11:47:41 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 05 Oct 2021 11:47:58 GMT
RUN set -eux; 	version='5.8.1'; 	sha1='21e50add5a51cd9a18610244c942c08f7abeccd8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Tue, 05 Oct 2021 11:48:05 GMT
VOLUME [/var/www/html]
# Thu, 07 Oct 2021 23:30:02 GMT
COPY --chown=www-data:www-datafile:76be5fadb2e2d2b7a74d2770397579cd1402963fdca23912220f983ef906f582 in /usr/src/wordpress/ 
# Thu, 07 Oct 2021 23:30:03 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Thu, 07 Oct 2021 23:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Oct 2021 23:30:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c3b7af0ed242d09d9fee2dfc48d4553d58ad90c5fb862ab58fb89e2d04c5b922`  
		Last Modified: Mon, 04 Oct 2021 18:07:32 GMT  
		Size: 35.3 MB (35272408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6aef7065ca3933c32fa8c4fad08fc385ce147b8cdb7f12a172631879a94abf`  
		Last Modified: Tue, 05 Oct 2021 07:34:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4056d122da13ad71fa0284fad0761840406b2cf7c046cf3a92b5b098173fa875`  
		Last Modified: Tue, 05 Oct 2021 07:35:08 GMT  
		Size: 86.6 MB (86625016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5563e6630ce488d5935573050ec48d7b3b5b99ba4ab0ead49ff959e1b7f3f3bb`  
		Last Modified: Tue, 05 Oct 2021 07:34:43 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43072e2b56c39d6e91c91f84e4654e315ff55f5dc1050bd1569ca2ec192af4be`  
		Last Modified: Tue, 05 Oct 2021 07:35:53 GMT  
		Size: 20.4 MB (20434454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09d780911cd947542ace4fd9ef18d825e0dbcaca9c4fc8be04f21434111c604`  
		Last Modified: Tue, 05 Oct 2021 07:35:44 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17152c917b11509232ded392598447cebe5c09655a87d7b17149f033d205005e`  
		Last Modified: Tue, 05 Oct 2021 07:35:44 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69a957959665ccf1c5206962d02ba49b8c55daff66bd580bdd99e6abd999e7`  
		Last Modified: Tue, 05 Oct 2021 07:50:08 GMT  
		Size: 12.5 MB (12484104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55c7c1ae7241ed1c4cfc65365fb5967de74dff7597d19013873617228ed2464`  
		Last Modified: Tue, 05 Oct 2021 07:50:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d864529f7d72052a9cb81ea166b7d29123e2bc023f29d8fd0b26e6187f1580`  
		Last Modified: Tue, 05 Oct 2021 07:50:08 GMT  
		Size: 15.6 MB (15614004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e1f7e88f5650c99ff19a9fde8b61f069dce7b1e07bb603fff7d603bc8939b`  
		Last Modified: Tue, 05 Oct 2021 07:50:04 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7e529a886119b7d99d18468f0bafa896c0c81ff1d5f78ba153501c15eddc3d`  
		Last Modified: Tue, 05 Oct 2021 07:50:05 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2d79dd8ef3f33b2190e5ec2ebcd0515bb56d663894c19cfaa3b010db0192fa`  
		Last Modified: Tue, 05 Oct 2021 07:50:04 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94bccb8eddd07366acd4a0131c89deb19288e84fc06ee99f0560a4c55b81c4d`  
		Last Modified: Tue, 05 Oct 2021 07:50:05 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb59357fc8d7739f8abf9fd7533efb7ac03b326101c76dad0c7b5ab2b8c4c9e`  
		Last Modified: Tue, 05 Oct 2021 12:50:08 GMT  
		Size: 19.8 MB (19822548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2d7fa66954ecb2f198abd72e545208c700e477806c0ac2a934f32d3b6af67d`  
		Last Modified: Tue, 05 Oct 2021 12:50:05 GMT  
		Size: 10.6 MB (10643852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186d150d43502f9792282e918449dee34185277927170352d324889c762b5f3`  
		Last Modified: Tue, 05 Oct 2021 12:50:01 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aaa502332150d9e62b3634a758785a47fedd40196f2d7345b4fc0d1843bfc1`  
		Last Modified: Tue, 05 Oct 2021 12:49:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31eb1dc0dfefd3c383cf4886faa94ddf86402ff6990c9ac897e97eae4efa567`  
		Last Modified: Tue, 05 Oct 2021 12:49:59 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fa6df28ac1479a593a82d94448864d21e16bb4e0eb94eac62f5f6fec987ceb`  
		Last Modified: Tue, 05 Oct 2021 12:50:02 GMT  
		Size: 14.9 MB (14915620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e305813f0b184221bc4b84cdbfcb529893c71ddfff56bdc852cc150f5e2d726`  
		Last Modified: Thu, 07 Oct 2021 23:37:09 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8566e24ab53010a283f2f5f1e5014d0456fcdda21aaf695338785ccd1752b247`  
		Last Modified: Thu, 07 Oct 2021 23:37:09 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php7.3-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:42e8ff8623c0fc3047fa926def4aee4d3dbf2bf17b5e397b868804b46a297720
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189673820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206cdcc6ee69b83c45b77c3732d128870e7373c6dc2fdfa947c084a2c4e1ef8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:27 GMT
ADD file:6038dd6db57fb05c3d39c02c3379667ccd2989e7667ff773a8020fe6a69a760c in / 
# Tue, 12 Oct 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:42:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Oct 2021 01:42:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Oct 2021 01:42:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 01:42:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Oct 2021 01:42:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 12 Oct 2021 01:46:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Oct 2021 01:46:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Oct 2021 01:47:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Oct 2021 01:47:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Oct 2021 01:47:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Oct 2021 01:47:13 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 12 Oct 2021 01:47:13 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 12 Oct 2021 01:47:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Oct 2021 01:47:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Oct 2021 01:47:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Oct 2021 03:19:39 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 12 Oct 2021 03:19:40 GMT
ENV PHP_VERSION=7.3.31
# Tue, 12 Oct 2021 03:19:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.31.tar.xz.asc
# Tue, 12 Oct 2021 03:19:40 GMT
ENV PHP_SHA256=d1aa8f44595d01ac061ff340354d95e146d6152f70e799b44d6b8654fb45cbcc
# Tue, 12 Oct 2021 03:19:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 12 Oct 2021 03:19:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Oct 2021 03:21:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		${PHP_EXTRA_BUILD_DEPS:-} 		libargon2-dev 		libcurl4-openssl-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Oct 2021 03:21:13 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 12 Oct 2021 03:21:14 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Oct 2021 03:21:14 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 12 Oct 2021 03:21:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Oct 2021 03:21:15 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Oct 2021 03:21:15 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 12 Oct 2021 03:21:15 GMT
WORKDIR /var/www/html
# Tue, 12 Oct 2021 03:21:15 GMT
EXPOSE 80
# Tue, 12 Oct 2021 03:21:15 GMT
CMD ["apache2-foreground"]
# Tue, 12 Oct 2021 09:22:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:23:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype-dir=/usr 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 		--with-webp-dir=/usr 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:23:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 12 Oct 2021 09:23:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 12 Oct 2021 09:23:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 12 Oct 2021 09:23:33 GMT
RUN set -eux; 	version='5.8.1'; 	sha1='21e50add5a51cd9a18610244c942c08f7abeccd8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Tue, 12 Oct 2021 09:23:34 GMT
VOLUME [/var/www/html]
# Tue, 12 Oct 2021 09:23:34 GMT
COPY --chown=www-data:www-datafile:76be5fadb2e2d2b7a74d2770397579cd1402963fdca23912220f983ef906f582 in /usr/src/wordpress/ 
# Tue, 12 Oct 2021 09:23:35 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Tue, 12 Oct 2021 09:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 09:23:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ded751c48f72503973be01be2794cc039490f22b039b8ac106e9f17de4980742`  
		Last Modified: Tue, 12 Oct 2021 00:48:05 GMT  
		Size: 29.6 MB (29641215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e93f54c1a4ac2c0a445018626dbf2035ae9fff49f85693b56f619e876603022`  
		Last Modified: Tue, 12 Oct 2021 03:44:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a448f945ae4e9abe53c27b72c40f075c61a2ff21977f7b57567f443ad7dee68b`  
		Last Modified: Tue, 12 Oct 2021 03:44:34 GMT  
		Size: 71.6 MB (71618360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3bf3e5f5ecd4bafce85def29ee5490f29b810e95829c3702cc4157280350e6`  
		Last Modified: Tue, 12 Oct 2021 03:44:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fa8915dfded42c17fc2ad80a47a873711c8d6200aebee325a829c59c4f6d62`  
		Last Modified: Tue, 12 Oct 2021 03:44:55 GMT  
		Size: 19.1 MB (19052069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed0ccfb17f6bd74cac8f31177eeda092942c5553a73e2168a9dd660804dce37`  
		Last Modified: Tue, 12 Oct 2021 03:44:53 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25b2206fa558b0b5f7444116a8a5f096797010e47f17c377157fdbcd748edab`  
		Last Modified: Tue, 12 Oct 2021 03:44:53 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8b73e1a15d083f93a0150527b9faffc882c6370445cef23d4a31493d20b7e`  
		Last Modified: Tue, 12 Oct 2021 03:53:22 GMT  
		Size: 12.5 MB (12482463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c37add56ac272d4760eafe70bc79410aa1b7beceee672ad17c4d4e68a409893`  
		Last Modified: Tue, 12 Oct 2021 03:53:21 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc7c346e05c308a50e826487e36fa997dbbc64041d02ce20564d964e561bdf8`  
		Last Modified: Tue, 12 Oct 2021 03:53:22 GMT  
		Size: 13.8 MB (13838222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cfb85675e96d81c3ff3f99fa960fad8f5c2205810bd2e23a2b31068e39b531`  
		Last Modified: Tue, 12 Oct 2021 03:53:20 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7b590d6a5480609d65b12338413092f72053f368543ae5ca728c0028f252ca`  
		Last Modified: Tue, 12 Oct 2021 03:53:20 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bac7dfaeb9be66b2355962744fbcca6f8a911d2dcad6857ab7b7795855fe8ed`  
		Last Modified: Tue, 12 Oct 2021 03:53:20 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ddfdfc23916b9dc21d7a288d80641f9c49ddc6f71ea55c5f35f13c79a4e3`  
		Last Modified: Tue, 12 Oct 2021 03:53:22 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34092a940857c5ef9c33b03694385bddd3c5f7b5749c46ed0debc793e4b8d5aa`  
		Last Modified: Tue, 12 Oct 2021 09:31:35 GMT  
		Size: 18.9 MB (18907179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2279ed8fec8f48e1494b5991168c5dda59a2cfb2d413f4d1de3e28466214be`  
		Last Modified: Tue, 12 Oct 2021 09:31:34 GMT  
		Size: 9.2 MB (9188751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cd61bba820963b8f3ec0d63f01fd28bb7b41c2fdf81900d982319af3ef4652`  
		Last Modified: Tue, 12 Oct 2021 09:31:32 GMT  
		Size: 374.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d4c2f9e12bc372aa7caeae10291e3fdfa0eea874a7d2c6ee95f4087b91fa78`  
		Last Modified: Tue, 12 Oct 2021 09:31:31 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532e70bd7e4487e4f483063d8ad51ef62a4cf6b77896c1c520c64ee27e351eda`  
		Last Modified: Tue, 12 Oct 2021 09:31:31 GMT  
		Size: 19.5 KB (19498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508b54f6355d67d0bf052ae2f0c4bbad05816574832d21daab7fae6ce1a996d`  
		Last Modified: Tue, 12 Oct 2021 09:31:34 GMT  
		Size: 14.9 MB (14915604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbcad580d3ed3b87391cd6a8d7eaaa6fe11ade437d5bff1839a9c6f4684453f`  
		Last Modified: Tue, 12 Oct 2021 09:31:31 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee07c906a21aea5656f113b7fcec06b4baaccf35dc9c186da76cc2cea88cadb`  
		Last Modified: Tue, 12 Oct 2021 09:31:31 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
