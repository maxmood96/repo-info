## `wordpress:php8.3-apache`

```console
$ docker pull wordpress@sha256:6e074675381267450c05b07ce49f5962054b5e31295350bfd842e2ad871a701a
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

### `wordpress:php8.3-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:ea396bb5a4145e82077be61f1ec11c74334841b9c59730fa01b58e65fe546655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243947163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c485e74b4f058e3aebfd7d9979e61e2adbafd97548cd2797b19a689aa0787d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:57:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 02:57:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 02:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:57:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 02:57:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 03:01:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 03:01:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 03:01:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 03:01:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 03:01:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:01:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 03:01:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 00:01:21 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 00:01:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 00:01:21 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 00:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 00:01:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:51:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:51:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:51:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:51:03 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	version='6.5'; 	sha1='fe10ab388318fa5a0085aff48b2b7590cf8b93f9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
VOLUME [/var/www/html]
# Fri, 05 Apr 2024 21:51:03 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de14226e1706b621fe796af63b375db247a2490752558ed4f5ea40648234129`  
		Last Modified: Tue, 12 Mar 2024 05:25:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aaf617d1d2bc41efbec77e9f05370e6f35d8f4363fb26fa04883ec538b7d66`  
		Last Modified: Tue, 12 Mar 2024 05:25:37 GMT  
		Size: 104.4 MB (104355586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ba065e262ff15c57d91609cae32d80920edac1e9b0826e0d8cf5f0f3c60107`  
		Last Modified: Tue, 12 Mar 2024 05:25:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ecae067f5d5cbf3c2a3cf42d5677472bc8cc633b8ccea33d011749bb84661`  
		Last Modified: Tue, 12 Mar 2024 05:26:03 GMT  
		Size: 20.3 MB (20303886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f1b407f7499799755557f8769bbeb98d0573d6092913d5303cf951acdace0b`  
		Last Modified: Tue, 12 Mar 2024 05:26:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1b2cfb806df514ad4cf5cffa00c66aaa6322c1ef8f3b1c597592771925569b`  
		Last Modified: Tue, 12 Mar 2024 05:26:00 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7214a7d8b094ac5c57e27a6253262bf227c0bd2f9e15b0a2baa340c33f2a8b67`  
		Last Modified: Sat, 16 Mar 2024 02:33:29 GMT  
		Size: 12.8 MB (12777091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e055f8d0e6b4159ee0c461adbf769594edd20f18c9452f610634d55c779222`  
		Last Modified: Sat, 16 Mar 2024 02:33:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2adce70ba4934293ed8a734c9c827caaede11f651fb3cf724a14ae7267f590c`  
		Last Modified: Tue, 09 Apr 2024 00:21:53 GMT  
		Size: 14.2 MB (14239668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e912b8b465ae4a7829c47a3875d8ff2e2ca0a08e3961f5710b989a9dbdf2d9f`  
		Last Modified: Tue, 09 Apr 2024 00:21:51 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49e5c4f7abb56c3429113396394cfa71fadfdda29c1bdd965be90e4f009b28`  
		Last Modified: Tue, 09 Apr 2024 00:21:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1283bfaff8bdaa80cf95accba0f03f4e237ba98147738bb34cac764e085e9080`  
		Last Modified: Tue, 09 Apr 2024 00:21:51 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c6f6c84c284b990cfee124850eb17360d1c40d7b9543f72aa145874cb2480f`  
		Last Modified: Tue, 09 Apr 2024 01:53:57 GMT  
		Size: 26.3 MB (26254946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd4e501b455091929e28681309a86167e933eec605d24bc2f31c70cc3dfc36a`  
		Last Modified: Tue, 09 Apr 2024 01:53:57 GMT  
		Size: 12.3 MB (12337202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585e2e59f65c0ca3602da24ac3e68aee71762e29fc292a5ebf0aa7ccc85727a5`  
		Last Modified: Tue, 09 Apr 2024 01:53:56 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532b9f902a384ed7e70c5b6c14ac8518fcdcdaeece2d1f51a281658403021c08`  
		Last Modified: Tue, 09 Apr 2024 01:53:57 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977fcf3c0c3baba229cdcb374d2b275af81d23416922ba8d43982860492a05e0`  
		Last Modified: Tue, 09 Apr 2024 01:53:57 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ee428cc296a939b8c5425926be8ca27a31a0454836fb8241329005b65f97c1`  
		Last Modified: Tue, 09 Apr 2024 01:53:58 GMT  
		Size: 24.5 MB (24525029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a1a0a1bc40f81852f5df4e71bb055bd921daba8b40b13b83d604e3e77cf815`  
		Last Modified: Tue, 09 Apr 2024 01:53:58 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb20f7e9f4335c04007c47a614ea6ee29aa127d6c79914f66e5cf1f3d93d234`  
		Last Modified: Tue, 09 Apr 2024 01:53:58 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:773d77009e7d2f9edd1039561f7f58b81829863c4804a7777db5737c3dd8f514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8017028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8830fb20519c6c79989aa70daf964d36be9e515bfdf3495d3480e98608095975`

```dockerfile
```

-	Layers:
	-	`sha256:8149dbb721681a2da9c66b2e31a5ac4fcc8f7f4060a339f965594b17d5aa956c`  
		Last Modified: Tue, 09 Apr 2024 01:53:56 GMT  
		Size: 8.0 MB (7955373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4320644d1e1d7216c69a185b91dcb06ad7a6e03039b99fed2b6b9b0c075f5b2`  
		Last Modified: Tue, 09 Apr 2024 01:53:56 GMT  
		Size: 61.7 KB (61655 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:1b131e510c5bc127ce9fee6af6fa0c6a202a8beb7112ef9a8d9c6fe2deacd285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214514505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6a4eb161e523a1c0a29de732c9b6eec7155b4aae9d2ad8326344032da94e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:47:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 01:47:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 01:47:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:47:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 01:47:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 01:50:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 01:50:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 01:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 01:51:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 01:51:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 01:51:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:51:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:51:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 01:51:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 15 Mar 2024 23:51:46 GMT
ENV PHP_VERSION=8.3.4
# Fri, 15 Mar 2024 23:51:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Fri, 15 Mar 2024 23:51:46 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Fri, 15 Mar 2024 23:52:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 15 Mar 2024 23:52:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:51:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:51:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:51:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:51:03 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	version='6.5'; 	sha1='fe10ab388318fa5a0085aff48b2b7590cf8b93f9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
VOLUME [/var/www/html]
# Fri, 05 Apr 2024 21:51:03 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d115fea1b4a8106e263db629be1619e1687e09620739ce2ec2b09ef0f7216b`  
		Last Modified: Tue, 12 Mar 2024 03:51:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e1c5741512c603cc1e5fdb27395ab09059c53c3871664e3c0fa08051670462`  
		Last Modified: Tue, 12 Mar 2024 03:51:27 GMT  
		Size: 82.0 MB (81999306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a94ea1638e6635c0e4c239bab002203d65e36eb7b12bb6d9fdfece6154dc1`  
		Last Modified: Tue, 12 Mar 2024 03:51:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3328c6af612c3f7b6b1a513414b09fa7245d3b85239f38bbcc86311ab073ba`  
		Last Modified: Tue, 12 Mar 2024 03:51:52 GMT  
		Size: 19.6 MB (19608292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc33c91c9d6d19b16182a5fd63f18bd28413c720fd6f8873b8680eaab541a13a`  
		Last Modified: Tue, 12 Mar 2024 03:51:49 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03347d119d00160ae7ff93fb281dbde1a946587dcfab5c36cf718aff026bb858`  
		Last Modified: Tue, 12 Mar 2024 03:51:49 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b152e11a76d1fb876a2861008d31fa6214b43216924b5cc03d677c9063df25`  
		Last Modified: Sat, 16 Mar 2024 00:54:19 GMT  
		Size: 12.8 MB (12774980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651411cf7877943e32eee083774f7e13d7c76f542bbe39b214fa091fd21e1ee8`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232637e888e3de568284a5940e325ff7e8e5b72a402ffd153255897a29d863ac`  
		Last Modified: Tue, 09 Apr 2024 00:39:49 GMT  
		Size: 13.0 MB (13037214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756eb7306f1996693e87efafa390acc685df0839497fd310115cccd1aa4f9a1f`  
		Last Modified: Tue, 09 Apr 2024 00:39:46 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af21edd42a14102f3cfee05925ddb4f8a6f71fd5e89f1fe02efe33c063cefc30`  
		Last Modified: Tue, 09 Apr 2024 00:39:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cde4a7f15a5d33a9e6af5e998f4ca31a64399843f8a8e12bc17277a4cc4ae5f`  
		Last Modified: Tue, 09 Apr 2024 00:39:46 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a37020c77f8e3879b838b9e79af4de57f52676a2bcd6d3b7db885a5e2f0f88`  
		Last Modified: Tue, 09 Apr 2024 07:27:06 GMT  
		Size: 25.7 MB (25706400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8251b2482cbf627222940c71daffbdf5fa0a394abb8cfaa96749ced11f273e62`  
		Last Modified: Tue, 09 Apr 2024 07:27:06 GMT  
		Size: 9.9 MB (9949698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f57af4db774f0e8b19885f8a07eef8e94e077a28bdf66fd898bb211d4fbd4be`  
		Last Modified: Tue, 09 Apr 2024 07:27:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1ff270ff20969f6d63abf7fa05b3644b15e6f9e8658c5f833e1c2c77f70291`  
		Last Modified: Tue, 09 Apr 2024 07:27:06 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e013c1ea84542753e27b27c8bc56189ac6ab5cd61d881540a7595e1e4de45`  
		Last Modified: Tue, 09 Apr 2024 07:27:06 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e2773627a295733379bab4af7cd6bf6fc825643b059410a7d2efa56125943c`  
		Last Modified: Tue, 09 Apr 2024 07:27:08 GMT  
		Size: 24.5 MB (24525030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916e61c863837fce981a88cdabf3321c2ddda70ae92fe0c16685904d6209ef01`  
		Last Modified: Tue, 09 Apr 2024 07:27:08 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7a016fafef45a532852f00a61536dc5bc9f69d3a2958386825b1ace0753a2e`  
		Last Modified: Tue, 09 Apr 2024 07:27:08 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:7fff27ea1c108b420b8f263865f1c1c3c28430cdabba8810e07b5b853f56ecea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7824734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda7ee4cdea993b92966255caa6819f7caee7579e02ada752b1fd6258fa932e1`

```dockerfile
```

-	Layers:
	-	`sha256:ff37e506ca4fc841e9fdcaddaee99065baca78559d78dc947364a43aa861ae6a`  
		Last Modified: Tue, 09 Apr 2024 07:27:05 GMT  
		Size: 7.8 MB (7762929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462858fd4ceca28d7894624ce7ac055461c513d13c67f86cdb69214dbb9ad0ee`  
		Last Modified: Tue, 09 Apr 2024 07:27:04 GMT  
		Size: 61.8 KB (61805 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:1587cfb9b599124ba8bcdb43a76d2fd94098247741143a7a96e0de7425acc925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203430126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e82fb4b57a78b5f844e0c250eb7c8ccf46430363277526142c650b8c891be8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:23:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 07:23:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 07:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:23:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 07:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 07:26:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 07:26:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 07:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 07:26:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 07:26:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 07:26:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:26:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:26:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 07:26:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 08:42:17 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 08:42:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 08:42:17 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 08:42:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 08:42:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:51:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:51:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:51:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:51:03 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	version='6.5'; 	sha1='fe10ab388318fa5a0085aff48b2b7590cf8b93f9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
VOLUME [/var/www/html]
# Fri, 05 Apr 2024 21:51:03 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd82a33324e79052aa5fed0978c223b7d05b5a41532eca869d5602ee24d0c7c`  
		Last Modified: Tue, 12 Mar 2024 09:24:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57829c9789b8ee6e6ebe4a80c39f9393df7fcf20975d1d8135fc2142cad63d8`  
		Last Modified: Tue, 12 Mar 2024 09:24:42 GMT  
		Size: 76.2 MB (76169934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1e9e48950eb6ede1065099dd2b976917707ffa4953e5c351638a845668823`  
		Last Modified: Tue, 12 Mar 2024 09:24:29 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98245a88fa6adc9fd93e0af245463b9d9dc7cbea417c92646663e9f7375ffa93`  
		Last Modified: Tue, 12 Mar 2024 09:25:08 GMT  
		Size: 19.0 MB (19045529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff6ef8d01cdfd6ba1026fbed3898bbc602bc4e92c1a6879b933c622d36a7a42`  
		Last Modified: Tue, 12 Mar 2024 09:25:05 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b18f3b6afb527e3463e62dae0e34a48ea21bcfdf1bfb8a5bbe5c978746c3e6`  
		Last Modified: Tue, 12 Mar 2024 09:25:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c13e4abe30135f25b1010ee9f887b3248bdce6838a576b4f0132925aa13902a`  
		Last Modified: Sat, 16 Mar 2024 10:57:32 GMT  
		Size: 12.8 MB (12774944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da4081b4f9b9bd64f5fc59aaa3f520ae67b4cdc1d79b1b7376256aa156e4a7f`  
		Last Modified: Sat, 16 Mar 2024 10:57:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdb2e35364a5387522580da12a96bfbf58afe57154d15e5662d3a06751f7cfc`  
		Last Modified: Tue, 09 Apr 2024 00:48:12 GMT  
		Size: 12.1 MB (12113262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598d20c7bc8dba1d249eeb20b6e3ff1f2f866d7a338430c92722b6d7a75ad204`  
		Last Modified: Tue, 09 Apr 2024 00:48:09 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ad093cc7794ce09be1e3ed0c3d11eba7a7f1507b6850e52d625b697a3731f6`  
		Last Modified: Tue, 09 Apr 2024 00:48:09 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1275aaf1bd1ea5bc59064bd7084a670dc4df2f2e3c304e1aac3f5e2653d50ad6`  
		Last Modified: Tue, 09 Apr 2024 00:48:09 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9631f9c35c17004e515c62e59e2c92655acb599fbad62c34d6ea4e0babc2f3f6`  
		Last Modified: Tue, 09 Apr 2024 10:43:18 GMT  
		Size: 25.1 MB (25077806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e3114a9c006e7bdb69e8f86877194c4639609d642b62e1abfbac4d8f8f6b67`  
		Last Modified: Tue, 09 Apr 2024 10:43:17 GMT  
		Size: 9.0 MB (8977334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31446031e5e591cd9d8ff8ff232e1eff283b67380736037db5dc43ec3e2c8bad`  
		Last Modified: Tue, 09 Apr 2024 10:43:17 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba532aff4467d049982a51e9cbe09b93f9944bf0c37ed8554b53f14bb8e60873`  
		Last Modified: Tue, 09 Apr 2024 10:43:17 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c38943ab3407e0d83a7b06a704d236d1b2df62e2c1e009ff590bfb0923bb24b`  
		Last Modified: Tue, 09 Apr 2024 10:43:17 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a0b4c10e679119c3080b9426209e6c5c7b9831c969a317dc674516acf31e7d`  
		Last Modified: Tue, 09 Apr 2024 10:43:19 GMT  
		Size: 24.5 MB (24525025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ac2ae99cbfbf0f9b5910ac11a6c981965b264b6cd916040e34db44a3508be3`  
		Last Modified: Tue, 09 Apr 2024 10:43:18 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae140bd7c459f8285ebe2c7aaef25e8081eb91376c1708602deaff0d09f9ef9`  
		Last Modified: Tue, 09 Apr 2024 10:43:18 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:c71d427bd37b34bd7d32bbc333b5d77fe7b2ef08dc711f71c20c347f10da3159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7827183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f356b89e1e42fcbeeabc103c4ab284315f758eef45ecf32804d56c7a969ba7f`

```dockerfile
```

-	Layers:
	-	`sha256:675f8603849dc37956969a9cd94b027fae841665f16f595a70bb01525d5da09e`  
		Last Modified: Tue, 09 Apr 2024 10:43:17 GMT  
		Size: 7.8 MB (7767485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610133159fddfdd6c5da4063bb5de6331558b94f4846a46499750acb78426c4c`  
		Last Modified: Tue, 09 Apr 2024 10:43:16 GMT  
		Size: 59.7 KB (59698 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:be3460a4e528839a829308e8e3741cfad2364fb93b906db3889a57b0e5ef24ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235712105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bd7532d970de5dc43a6becf2ce29b6ff2c52d209bef739e879b93f1108910a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

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
# Tue, 12 Mar 2024 04:43:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 04:43:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 04:43:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 04:43:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 04:43:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 04:43:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:43:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 04:43:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 04:43:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 00:12:19 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 00:12:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 00:12:20 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 00:12:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 00:12:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:51:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:51:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:51:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:51:03 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	version='6.5'; 	sha1='fe10ab388318fa5a0085aff48b2b7590cf8b93f9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
VOLUME [/var/www/html]
# Fri, 05 Apr 2024 21:51:03 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:036053896963520b5ce13f9151d0ad3dd4aff6d300c0cf85402700844e48dff6`  
		Last Modified: Tue, 12 Mar 2024 06:57:52 GMT  
		Size: 20.3 MB (20305130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9751366e208c9511ed7ed698080806c444f2effdd9f321b90fa1055b14a79e9`  
		Last Modified: Tue, 12 Mar 2024 06:57:50 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f53fc5dec6a2ddf288e227b9388cda0cb816d4b7e952c795bb0af42afafc9c3`  
		Last Modified: Tue, 12 Mar 2024 06:57:50 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbb17f699a977d67cb733affc5e0bc56692d887469e79d005d87dbc7b23e437`  
		Last Modified: Sat, 16 Mar 2024 02:14:49 GMT  
		Size: 12.8 MB (12776790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24557a80713a659f9964cd9cbde716c7d86a28814ffa1ce36710f5ecd97acc8d`  
		Last Modified: Sat, 16 Mar 2024 02:14:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223fa27517357fc18751fb6d12fb271724e38d337c7699cb94df935b41036542`  
		Last Modified: Tue, 09 Apr 2024 00:23:39 GMT  
		Size: 14.6 MB (14648167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffad0df0e9285a1df3c935d2aaa282b02ad66b40ec1e6d61714d36d00ac72b6`  
		Last Modified: Tue, 09 Apr 2024 00:23:36 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d614d25e59e1e78d3c1797189c2514a87d6c905b49f4768ca49e5efd21eb94`  
		Last Modified: Tue, 09 Apr 2024 00:23:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875424564cb69b5e92c05a1bc96a7aa7bf1622a16014aa82ec1dd875b10c00a1`  
		Last Modified: Tue, 09 Apr 2024 00:23:36 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0ec630f5c3728ba467b98ce13ba81447d2f9ff671903d0fb0f4d9880d54e01`  
		Last Modified: Tue, 09 Apr 2024 09:13:47 GMT  
		Size: 26.2 MB (26176727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff02079ee7aa3f75d2db6d622274448cd422965f554d2079a31007555d1e903`  
		Last Modified: Tue, 09 Apr 2024 09:13:46 GMT  
		Size: 10.0 MB (9968241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78086819c081feb5a5032f7fdf294b1191c18dbe508adc34ce8b162fac7f0cf3`  
		Last Modified: Tue, 09 Apr 2024 09:13:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c634eeea43e0c70161369deb9bdba242473f0517052e3a934a056ac2b608077`  
		Last Modified: Tue, 09 Apr 2024 09:13:45 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5aa6d0d622d0cb93418423eac0ba0d117e6b51c9b8e78429f42424602c714c`  
		Last Modified: Tue, 09 Apr 2024 09:13:47 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834999b24de9612637a432fce97a0e3fc12a28034a610aadfdf7a59a0184d5ac`  
		Last Modified: Tue, 09 Apr 2024 09:13:48 GMT  
		Size: 24.5 MB (24525036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b39b158ec30c207aaf0901f790e0addac411e1f8b2f9351d347450ce497663`  
		Last Modified: Tue, 09 Apr 2024 09:13:47 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044512df9fafa244e726b7087b655b4dec4ca61907bca191ebf63e97d80ffb4a`  
		Last Modified: Tue, 09 Apr 2024 09:13:48 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:f825404f66faabc41ad215ce1174acb45c50f611edc02f6f238f829d12fe5c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8043615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52efcf4aaaa7cff84bf4a67442021674b85d48b521a8e41fc31db33a0792cdea`

```dockerfile
```

-	Layers:
	-	`sha256:2c32ea2b24a7325778856caaacd4ede9e9a9788fec01eefde37592a265cda846`  
		Last Modified: Tue, 09 Apr 2024 09:13:46 GMT  
		Size: 8.0 MB (7984066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c992669510e7d8bece411cb985e894f07f0711ee9ec9cc1fcd782e031825ac0`  
		Last Modified: Tue, 09 Apr 2024 09:13:45 GMT  
		Size: 59.5 KB (59549 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; 386

```console
$ docker pull wordpress@sha256:9f02c218c04e74301c19692803eb974fb5146d828630ce65eba15a7ae9d88557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242611915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d463041c0218cfc06101ad651b8e286e66b54ffcf1a1b1369fc54c4aa542a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 01:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:39:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 01:39:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 01:46:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 01:46:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 01:46:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 01:46:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 01:46:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 01:46:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 01:46:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 01:15:57 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 01:15:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 01:15:57 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 01:16:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 01:16:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:51:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:51:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:51:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:51:03 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	version='6.5'; 	sha1='fe10ab388318fa5a0085aff48b2b7590cf8b93f9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
VOLUME [/var/www/html]
# Fri, 05 Apr 2024 21:51:03 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc8b418f2e8ebe03c4a8d60a403099d5bd9956664693b358caef9096763fabd`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f25d2333bd6d54c124fa174175081a9c95780122966ffb6532bd93757a9bd`  
		Last Modified: Tue, 12 Mar 2024 05:53:38 GMT  
		Size: 101.5 MB (101519737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6e71adc002ea9786257601b0d391da402881cf3c46d70b1bf238b5e218a47`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589ac2ec3c620e7a371533497b0cfd74ea84db2b079763c0c27f094625f447cf`  
		Last Modified: Tue, 12 Mar 2024 05:54:05 GMT  
		Size: 20.8 MB (20826115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef95ebea38d5ed66df38918c6398211026347c3a649d8cc4c3d081f4e7c6290`  
		Last Modified: Tue, 12 Mar 2024 05:54:01 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea05f91953dd8b5d5da845bf416fd786a74c12a214cd690ab7a3fe6bc5a5774`  
		Last Modified: Tue, 12 Mar 2024 05:54:01 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1935c5d0444873785b5095449427db54198de964b4641c4e6721b621f8fd23e`  
		Last Modified: Sat, 16 Mar 2024 04:56:03 GMT  
		Size: 12.8 MB (12776106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a8bb9071613093e32e9c74f9a34749c4949254b1421ee78d8b4b8b0e7c8ee7`  
		Last Modified: Sat, 16 Mar 2024 04:56:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f285a4d95073af3e7880bbbe01db6cf9019512745843ced20f0acb9637f642`  
		Last Modified: Tue, 09 Apr 2024 01:52:40 GMT  
		Size: 14.7 MB (14668660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666652d558f63e37c6ce40efd2eba5794f4e914a28d9774ab45c47ada692c1bc`  
		Last Modified: Tue, 09 Apr 2024 01:52:36 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3fb052a27812256dfe648f8568d9980ce23af4cad415b0c8c91f031b9fb469`  
		Last Modified: Tue, 09 Apr 2024 01:52:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3db4ed19d5dbd94a576a0ad1eb7071ffa0da77b902565a9223acfec69ddef3`  
		Last Modified: Tue, 09 Apr 2024 01:52:36 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1edeb30a1c513c307e511cd2f0849d2d9524ccf0bfdcb3956f6c8618afbe98`  
		Last Modified: Tue, 09 Apr 2024 02:54:46 GMT  
		Size: 26.7 MB (26701514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6790c18a220448403b3c55cbb197124b90695e88aa928a319813d3c52d1020`  
		Last Modified: Tue, 09 Apr 2024 02:54:46 GMT  
		Size: 11.4 MB (11423293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721896ee8451601c0565aa186f3f748e9e3ce4dc0da88f403045a31ecf654c6d`  
		Last Modified: Tue, 09 Apr 2024 02:54:45 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970535ad9242da2ef844d8c14ea4cf65a85d826f50b1a39d366c1b8cb0b06fb5`  
		Last Modified: Tue, 09 Apr 2024 02:54:45 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa30b72707a17b7c1d99da0ef61b01e5c3510a6f1eb290fad12f9caeac2680b`  
		Last Modified: Tue, 09 Apr 2024 02:54:46 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ed8bd1afeddef024db2aeebae9a3c006dde51ab58b4f906d79ed9efd0730d2`  
		Last Modified: Tue, 09 Apr 2024 02:54:47 GMT  
		Size: 24.5 MB (24525037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba6f38ae9e139fea95097540e2f9a942ece3627ba590f6b1928cd434409abe5`  
		Last Modified: Tue, 09 Apr 2024 02:54:47 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d518648c29f43acd9998c6adacd5fe9674f541a1b935afd591253844db222ea`  
		Last Modified: Tue, 09 Apr 2024 02:54:47 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:035b6e75f066d188a7a327d3a8db92f29c0cb203b345c3f493f4141841658d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7997096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73406d2878404820bfc7424b9f1728bc137954260800719d38949042286592a9`

```dockerfile
```

-	Layers:
	-	`sha256:32918eb14a62b9da412dbc3a91a7ca4ea4d738f87922ff1d1571e84cf9bfdf00`  
		Last Modified: Tue, 09 Apr 2024 02:54:45 GMT  
		Size: 7.9 MB (7935499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40368cc1d7db81c82a9742ed3cbe578aab47b99ea47e02b4d24d515a86a7ef3`  
		Last Modified: Tue, 09 Apr 2024 02:54:45 GMT  
		Size: 61.6 KB (61597 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:350d67208f656969d1bc03f0388c703df8a4e747de98162a072d4116b58f4867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216132590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c4fdada0fc9d2941ba4b202736f2850d4ab853cb5be1fe07ea6d8ebded2a60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:04:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 07:04:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 07:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:06:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 07:06:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 07:23:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 07:23:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 07:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 07:24:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 07:24:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 07:24:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:24:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 07:24:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 07:24:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 00:28:20 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 00:28:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 00:28:28 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 00:29:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 00:29:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:51:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:51:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:51:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:51:03 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	version='6.5'; 	sha1='fe10ab388318fa5a0085aff48b2b7590cf8b93f9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
VOLUME [/var/www/html]
# Fri, 05 Apr 2024 21:51:03 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ad2ee86d932791e83ef3c48546f89d80fb95dbd7bde823e4a9130d9736fb56`  
		Last Modified: Tue, 12 Mar 2024 17:21:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59af68362cd81b3b6952f94bf5c46f86937fd9ee619806471611d4b37183a423`  
		Last Modified: Tue, 12 Mar 2024 17:22:26 GMT  
		Size: 80.7 MB (80667080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4246e7c869e89c6228ff595bb4f1a52c830d5330d9f60d1e5f4618e5f6810f4b`  
		Last Modified: Tue, 12 Mar 2024 17:21:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeefc470438982acc7af1e3500db532d2a0137661a5afa9cedc9d47c72b00a93`  
		Last Modified: Tue, 12 Mar 2024 17:23:11 GMT  
		Size: 20.1 MB (20054112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1debd2235578eaa9b06654657c84e6a19afaadba378c1984d6c326e658889d`  
		Last Modified: Tue, 12 Mar 2024 17:22:56 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a08577e3528f333903f82af2b816db146e6ed1a4a8ac828fd1be1f7eac7e617`  
		Last Modified: Tue, 12 Mar 2024 17:22:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e60dd0d0e92f0e06676c2f4f1ba9d04d661a34be7da3784c70f0d8517ecb78b`  
		Last Modified: Sat, 16 Mar 2024 04:22:30 GMT  
		Size: 12.6 MB (12569862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e747d3b0ed99c6ce9361605b40b2c517f3df2744743d957ec8807f7347416a5`  
		Last Modified: Sat, 16 Mar 2024 04:22:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f32d70ccef23a3a1a946dc6b2835becbb89e64843e4f07b48a00f33d8764314`  
		Last Modified: Tue, 09 Apr 2024 08:11:31 GMT  
		Size: 13.7 MB (13676461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b162babe96cf145953160673c8ba27782728b13831aa2ff89387325f65790cb`  
		Last Modified: Tue, 09 Apr 2024 08:11:20 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dcd7a5cba8c30376bd4fa9733b93a0231258bb4093cb9dcdcf83b6b3f26840`  
		Last Modified: Tue, 09 Apr 2024 08:11:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9e4667bea5ec895ba1d20f463782f76002edc6acae67e6bc72059d6718ffa0`  
		Last Modified: Tue, 09 Apr 2024 08:11:20 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d0a5fe5692308ce0232e5947fc156668bfd22b823a1f0cc525b4d04af788b4`  
		Last Modified: Tue, 09 Apr 2024 20:50:49 GMT  
		Size: 26.0 MB (26023454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9ed0924689edf1220e8a13d6fde0b5e96363d03128b84c9c0f390d4ed17f25`  
		Last Modified: Tue, 09 Apr 2024 20:50:47 GMT  
		Size: 9.5 MB (9467909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e3628bf2f68f36360799df4128d722f349007825fc77b252f58a1df2a50fd3`  
		Last Modified: Tue, 09 Apr 2024 20:50:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d4fc9d52780493dcfb3f836cf37af26de962ba6f4f918517fa646c0f4c426b`  
		Last Modified: Tue, 09 Apr 2024 20:50:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c37fe1d1cba2b9baafca8b5cfd8399c2240b05d990130a3f94c755bce423099`  
		Last Modified: Tue, 09 Apr 2024 20:50:48 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa18c953f9bab6962a29e2143e5879aaf6370547423396b2c8e8e21a29949c`  
		Last Modified: Tue, 09 Apr 2024 20:50:51 GMT  
		Size: 24.5 MB (24525009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50c8b2e48cfb22ff6c57440dc370b5ba5d82a8bf9cef3bd22fd583454717b18`  
		Last Modified: Tue, 09 Apr 2024 20:50:49 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d5e752fda1ce4d1e0cfc31c23a09676802ba47c20b8851898b0e6b1d666185`  
		Last Modified: Tue, 09 Apr 2024 20:50:49 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:564d63066eb57ff3164cbb622110687fcd75ae07d877a015879a82cec0550976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 KB (61532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628c4ccaaffd52797bba510344461093cf559b08e3f382208301603f3d0768ad`

```dockerfile
```

-	Layers:
	-	`sha256:1950027bd72063a228aa038f0f9adeef0203b32be3fd9f96c35c5e3cdf1ab985`  
		Last Modified: Tue, 09 Apr 2024 20:50:45 GMT  
		Size: 61.5 KB (61532 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:46a2f1c4e5f1ecc0b35ef399a5948c79d917ac21890f900e4dfb63719f6c9552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249092277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecc0d18f0dd01af58cdb7d6cf227d97542f18a37920415b84debfcc5198e06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

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
# Tue, 12 Mar 2024 03:57:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 03:57:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 03:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 03:59:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 03:59:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 03:59:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:59:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 03:59:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 03:59:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 05:09:00 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 05:09:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 05:09:01 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 05:09:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 05:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:51:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:51:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:51:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:51:03 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:51:03 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
RUN set -eux; 	version='6.5'; 	sha1='fe10ab388318fa5a0085aff48b2b7590cf8b93f9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
VOLUME [/var/www/html]
# Fri, 05 Apr 2024 21:51:03 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:51:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:51:03 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:62d0172ecc888b93bd448b82bc6d9f857b3d92b715a3dbf98063659ae5aeb9c4`  
		Last Modified: Tue, 12 Mar 2024 08:09:23 GMT  
		Size: 21.5 MB (21490020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3644f81176bc8772d0ef995fb85eb87ab44e5d4ec0edc420255e9c461846490`  
		Last Modified: Tue, 12 Mar 2024 08:09:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136812f7b93f984042c6fc7d609a2cafb56b8f103e463590d92b4795c71c2dbe`  
		Last Modified: Tue, 12 Mar 2024 08:09:20 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e67f5595b7de15188478931c65794ac1c7b434c36bebc6d1e255dd46e2c9706`  
		Last Modified: Sat, 16 Mar 2024 06:52:36 GMT  
		Size: 12.8 MB (12777061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8659ec72138fbabda29e6ff83e16c45108aba907ac83b102d82f356d7d45bd9c`  
		Last Modified: Sat, 16 Mar 2024 06:52:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f501cc3881e34ff12e8820eb65394041b05332362491adc9b5558701b72113`  
		Last Modified: Tue, 09 Apr 2024 00:24:12 GMT  
		Size: 15.2 MB (15240461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba70e5b14f6814915fc55811f296ac36c73473b49b462c91e646de3a2dc7603`  
		Last Modified: Tue, 09 Apr 2024 00:24:09 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402109fc89c84ea1630eb93eb1ca3428d60fa4e2f70b63d73036f043b3b94a14`  
		Last Modified: Tue, 09 Apr 2024 00:24:09 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcc4cecb72de59aa206bb197039ebd67800535d878f84cba34b8249e6360ef7`  
		Last Modified: Tue, 09 Apr 2024 00:24:09 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb56e73625b7f7040cd3d1bae8730dad1206d878421e1654b06f018beee2da7`  
		Last Modified: Tue, 09 Apr 2024 07:32:21 GMT  
		Size: 27.3 MB (27341758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c934f182eee729478e9697443e2e4c4a5f8981013dadc0ef5aa230df2f26ec3`  
		Last Modified: Tue, 09 Apr 2024 07:32:20 GMT  
		Size: 11.3 MB (11255720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0115820736b34068b83f9d727ed9cb973bcde2f24f08730888ab2aba2c7a66b3`  
		Last Modified: Tue, 09 Apr 2024 07:32:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4eadc9dfe61c27c690b7cb1dfe8702eeacb4342d919490ffe31be6a252f7b3`  
		Last Modified: Tue, 09 Apr 2024 07:32:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78047365746b0475242bdd2ad72216162fc87c1821d2aa70cca3c0858b5baaae`  
		Last Modified: Tue, 09 Apr 2024 07:32:20 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17ae38365ea61f9581def755c9e6250f1f54234d87af7e9bee2cac2fd2b06e`  
		Last Modified: Tue, 09 Apr 2024 07:32:22 GMT  
		Size: 24.5 MB (24525030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302746ca917d6e62dcd2fce32f7d0bda6d4764128b5cdd781f2c8954a60af5e1`  
		Last Modified: Tue, 09 Apr 2024 07:32:21 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5cd9e30c3aa528927a2eeae4a103a2ab8d9e76f9383150991f933543c9e86e`  
		Last Modified: Tue, 09 Apr 2024 07:32:22 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:6090832a998e8e0f8d8ff14bce686af5bc21559cf6e36ae204251559f358b3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7993825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e324c83b9fca65c3d75843af6c1eaa4600010c30acd0e9f4057df8845e68cf30`

```dockerfile
```

-	Layers:
	-	`sha256:666749e69cdfc693a9bcf5f19dc39cb9704d610929762f575d1f04fdb966617e`  
		Last Modified: Tue, 09 Apr 2024 07:32:20 GMT  
		Size: 7.9 MB (7934206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85bf5254094a02a6df45445ff97a936c5fb178ad655e2a073e8f38d703080b1e`  
		Last Modified: Tue, 09 Apr 2024 07:32:19 GMT  
		Size: 59.6 KB (59619 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:631a0de6a3574e50f49e8b35ffc3f2f43c46ac477cd0e16d797d7e485ff9aeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228024304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2208e9478e35c4a775c5fc738821608c21a6e2c237e1ca9a2c52cb9bcb9fa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 08:04:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 12 Mar 2024 08:04:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Mar 2024 08:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:05:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 08:05:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 08:09:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Mar 2024 08:09:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Mar 2024 08:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 12 Mar 2024 08:09:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 12 Mar 2024 08:09:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 08:09:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 08:09:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 16 Mar 2024 11:44:56 GMT
ENV PHP_VERSION=8.3.4
# Sat, 16 Mar 2024 11:44:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.4.tar.xz.asc
# Sat, 16 Mar 2024 11:44:57 GMT
ENV PHP_SHA256=39a337036a546e5c28aea76cf424ac172db5156bd8a8fd85252e389409a5ba63
# Sat, 16 Mar 2024 11:45:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 16 Mar 2024 11:45:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:48:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 11:48:13 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:48:13 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 11:48:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 11:48:14 GMT
STOPSIGNAL SIGWINCH
# Sat, 16 Mar 2024 11:48:14 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 16 Mar 2024 11:48:14 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 11:48:14 GMT
EXPOSE 80
# Sat, 16 Mar 2024 11:48:14 GMT
CMD ["apache2-foreground"]
# Tue, 02 Apr 2024 19:05:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Apr 2024 19:05:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Apr 2024 19:05:43 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 02 Apr 2024 19:05:43 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 02 Apr 2024 19:05:43 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Apr 2024 19:05:43 GMT
RUN set -eux; 	version='6.5'; 	sha1='fe10ab388318fa5a0085aff48b2b7590cf8b93f9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Apr 2024 19:05:43 GMT
VOLUME [/var/www/html]
# Tue, 02 Apr 2024 19:05:43 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Apr 2024 19:05:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Apr 2024 19:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Apr 2024 19:05:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d4ad3e3b59b6f54b9dcef6cff0e4615b6fa3f96f1de12d8fbeb94f7acd29b7`  
		Last Modified: Tue, 12 Mar 2024 11:15:26 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83835687d69ef2513b8d805100ebc4726b162f3aa9efd0cddf617127b689d25`  
		Last Modified: Tue, 12 Mar 2024 11:15:38 GMT  
		Size: 80.8 MB (80808055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e8349341cc698ac8bb86ba42ea145c47faa3f81cf9c660f105f493fc148300`  
		Last Modified: Tue, 12 Mar 2024 11:15:25 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f500bb0818505be871db98ada53fff2905523f39443d3b8203de073d18275d0a`  
		Last Modified: Tue, 12 Mar 2024 11:15:58 GMT  
		Size: 20.1 MB (20083383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e602f9cc745a947e1f5e2c99c194cfdeb52cdca3fd07aa735f0135752b146e3`  
		Last Modified: Tue, 12 Mar 2024 11:15:55 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f8dc84c4882804775f8abd94bf231325b2f7e4b4812cc6aba73dfb838aad26`  
		Last Modified: Tue, 12 Mar 2024 11:15:55 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925e51f8f2392ba205e8269f4a629423e00632bd9d22f9567591ecf347757483`  
		Last Modified: Sat, 16 Mar 2024 14:16:22 GMT  
		Size: 12.8 MB (12775321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18d99a5ad0c94a57859e5024ab90517f7272395a3036615032a457f39d16ef0`  
		Last Modified: Sat, 16 Mar 2024 14:16:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b6e56493ad974af511225ab349754d6f81f996d7abf2c57cc198f6c4669dde`  
		Last Modified: Sat, 16 Mar 2024 14:16:22 GMT  
		Size: 10.7 MB (10663121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda4e6e0a73f9324686dbbde89cd8a6c56058a42a154cb6b4046a9d10924ce77`  
		Last Modified: Sat, 16 Mar 2024 14:16:20 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a919f1a0093dd1c6e0bc671863919b1df4fc6de94c6c389a4dd26bd796bf745`  
		Last Modified: Sat, 16 Mar 2024 14:16:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f533efa5d87246f329e6f3ea119c6c15af4150c592ec300b42452d4b7e3a7`  
		Last Modified: Sat, 16 Mar 2024 14:16:20 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9070108b5480269d255e7fcae501c539a99bd2fa4ad8c02b4001f63735640bab`  
		Last Modified: Sun, 17 Mar 2024 16:20:06 GMT  
		Size: 25.9 MB (25899671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f78228019456c101ebdebe1fbd55f2c68f7053c24f49a694a24add4a3fa63b`  
		Last Modified: Sun, 17 Mar 2024 16:20:05 GMT  
		Size: 25.8 MB (25751494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3f4ee1ea747fe4b5271eb565d5b3e289847182b2a94ac055b199403ee22698`  
		Last Modified: Sun, 17 Mar 2024 16:20:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0598ce84b9651ee933d5d0de285449cc05aa64d1af4db3577115a6f474fe25a0`  
		Last Modified: Sun, 17 Mar 2024 16:20:05 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fedc37a1cd64f7c9d153d868c5200514899d65bd6bf08853fee3998f778c1e`  
		Last Modified: Sun, 17 Mar 2024 16:20:06 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fbb607cafe55a0c22f892e80e3e2f25fe61c4b12055bb56ccb7a4b9e355972`  
		Last Modified: Wed, 03 Apr 2024 22:08:58 GMT  
		Size: 24.5 MB (24525006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73818bb9ac9f6f05b12d77b3c36b37f77688f8dc015440e0c256fbb15d38c1a4`  
		Last Modified: Wed, 03 Apr 2024 22:08:58 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d19a3c809c53ed4dbae12339c1da36edf998976d4909dab6099e124a811e1d3`  
		Last Modified: Wed, 03 Apr 2024 22:08:58 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:7bc2d69cee2b14ef6b9185e0d85d15c66c8724866383d4fc1dcb92f6f4b6f079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8855709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c04c504502cb5645fd118e73b2bdda3ffa6050ad13b3e4aadcf3cf9c0e84fd5`

```dockerfile
```

-	Layers:
	-	`sha256:2e854e1fdc0196a68b1749cf2441be83e7adc8d90abebbe9a79ac2d62573110d`  
		Last Modified: Wed, 03 Apr 2024 22:08:57 GMT  
		Size: 8.8 MB (8796250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9b9445bcc98400b799333b273e13c226fd6d032d8b08f737fabbd046dbbf66a`  
		Last Modified: Wed, 03 Apr 2024 22:08:57 GMT  
		Size: 59.5 KB (59459 bytes)  
		MIME: application/vnd.in-toto+json
