## `wordpress:beta-6.7-php8.3`

```console
$ docker pull wordpress@sha256:f9c34b720228b2350ed7f5fa349b498e7946a749ff4164aa67ff86b2169b5591
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

### `wordpress:beta-6.7-php8.3` - linux; amd64

```console
$ docker pull wordpress@sha256:2067eaad8fc84b50ef0b8aabec87ca12f49a5fac82944a58fa6804bc30d6545c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254263495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625c1c917c6e32fd6eaa4662314bc184e69452ba5aa33a55f5c96e3119054aec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cfff3ac3828405d24e930ee4fd9bef0d039dab5acf83a12ae5540389b5b716`  
		Last Modified: Mon, 28 Oct 2024 22:05:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8db7ba2fb3103d018fb5dcfb21aca235f7e95c85bfd9ce83c3ee381c4521a4`  
		Last Modified: Mon, 28 Oct 2024 22:06:08 GMT  
		Size: 104.3 MB (104344860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd6dcf9c5c42a814580667cac758dcfb9b7f7a4049ab7d76fbc5a0afae9b6af`  
		Last Modified: Mon, 28 Oct 2024 22:05:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2133690866dea0b1ccd88420437854da3432c3d5cc74d354272d3fee4f7ac7c`  
		Last Modified: Mon, 28 Oct 2024 22:06:04 GMT  
		Size: 20.1 MB (20123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab50bae3de53daf73b7bde21369f9705e34ac11afece0cd460eef52720e3d42`  
		Last Modified: Mon, 28 Oct 2024 22:05:32 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c650d175379c75354d46cfacfbc2c76d5ca7bd13d65ededd1bed51f0f33f80`  
		Last Modified: Mon, 28 Oct 2024 22:05:32 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09dc258c3220d1bfef062c2e0ac519b744d8822d7176512af7833d5983ac0c3`  
		Last Modified: Mon, 28 Oct 2024 22:06:04 GMT  
		Size: 12.6 MB (12612396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dd36c07ca0c6e652164e5b0b5b083506bb351b45ffd5b39a46b0165df5c76b`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e299a01471fdbc8d7486de408362bfd30e03503dd7e40b312a00f5e1c140ee50`  
		Last Modified: Mon, 28 Oct 2024 22:06:05 GMT  
		Size: 11.6 MB (11644451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e31c3cda9f13cb49b553342afd57c0699028eb2fe3e8f307ab6b40d91afe5b`  
		Last Modified: Mon, 28 Oct 2024 22:06:05 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d404a37f1edeb502368a756fb1b451ab70e9fed13f32c9a2ef0d63982cb06ebf`  
		Last Modified: Mon, 28 Oct 2024 22:06:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2340e96d8144dfa165f7523c8bbbe3210ab56a8d6860f5d194238c95b1545f`  
		Last Modified: Mon, 28 Oct 2024 22:06:06 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff2dfe74e9fde668a31fc809e143bf25d2b15d251e2cb79dcfc226102bda3d2`  
		Last Modified: Tue, 05 Nov 2024 20:37:51 GMT  
		Size: 26.3 MB (26255145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0692a6733bf40f885043b6acb078c0e4a91a50c04d881ccca4df52e249a6c099`  
		Last Modified: Tue, 05 Nov 2024 20:37:51 GMT  
		Size: 17.5 MB (17475100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befe73d2c38131b52ae3ad02f5d0abce9dcd259cece354262565dffe79681ddc`  
		Last Modified: Tue, 05 Nov 2024 20:37:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff0d4bdf4b4f8610594291ce9d4277a14ed195fbe62bb16380084c57901d072`  
		Last Modified: Tue, 05 Nov 2024 20:37:51 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2f248fa58c62641f35186a409ba3cd12d9ce2414fde61539c33d67f836504c`  
		Last Modified: Tue, 05 Nov 2024 20:37:52 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57bab0e9a0d8ebf5ab71e1ccb0cd2005e406e1a884e983b5feeabbed2229457`  
		Last Modified: Tue, 05 Nov 2024 20:37:52 GMT  
		Size: 32.7 MB (32651965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3c3509ea6924f5793611945ea25fdb30bb08c067f0cd249fd87e7db2f9650f`  
		Last Modified: Tue, 05 Nov 2024 20:37:52 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dee6d6577902395484563e108a42a61581b7ae9b53acc5bb76e881b7d3e1b65`  
		Last Modified: Tue, 05 Nov 2024 20:37:52 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:c70ba0d06f8d58110681c1609bddff9c8e4950eda20979329c70812196b673a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8183963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa37b6ca56d4f63c07bce456fe26b3b1728a6d5217b59e38828327e64d2182`

```dockerfile
```

-	Layers:
	-	`sha256:3152604ae5c9b2cf3e0eb963ca1e9fc243a31184f1f542a537298e1c175bd38a`  
		Last Modified: Tue, 05 Nov 2024 20:37:51 GMT  
		Size: 8.1 MB (8123174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd801e8eb137728f209205f165359eab4c02e426abbd0652fc39602a07508d2a`  
		Last Modified: Tue, 05 Nov 2024 20:37:51 GMT  
		Size: 60.8 KB (60789 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.3` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:47c7418fba2d06fa09dada6cee043cfc2df3e7e0c63533cf2d352495dd1ec6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223187362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e13d7904b8065869d09cc941201a5c9c7743fe32407307d9d462c4aac9238e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:28 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 17 Oct 2024 00:54:29 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cbfa5cbebed9fd7c8f34077debdb42c371f3e9ff0874a76eeecaeea391fff`  
		Last Modified: Mon, 28 Oct 2024 22:06:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d7de8ee38de821e7a2d49fddb538f63c035fac91b992f00ac7bf6b39d25964`  
		Last Modified: Mon, 28 Oct 2024 22:06:33 GMT  
		Size: 82.0 MB (81993591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b072383a75b21caa7c43d077f84a4e9c721b6f8b19ab0e9df353f53ab84ca`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e85e77875bb273fe263ad3f33329ff4aec330e79ddf1f8063eaa30810787f5`  
		Last Modified: Mon, 28 Oct 2024 22:12:37 GMT  
		Size: 19.4 MB (19418870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4c981efad954cf32a3908ca82953214cd6071fec1c979b34181c63546ebf8`  
		Last Modified: Mon, 28 Oct 2024 22:12:36 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9718dbae37263d9bc8d722584725ce8dcc3e716cb937ff6b85801f56374c88`  
		Last Modified: Mon, 28 Oct 2024 22:12:37 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b1a29cc545983561254f8ba18abc141ea2e6d3eeaf8ce5ca57a237cc3c17b7`  
		Last Modified: Mon, 28 Oct 2024 22:34:03 GMT  
		Size: 12.6 MB (12610442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec18a82a7a7255efb1bfe6d44b6f1a80567419deebc156f9b8b44990304bce43`  
		Last Modified: Mon, 28 Oct 2024 22:34:02 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cdef8fb29609e6866d9d5885a6101b4fde850704efdacd700c7f96b3b974f1`  
		Last Modified: Mon, 28 Oct 2024 22:34:03 GMT  
		Size: 10.6 MB (10611630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d81c7889ace79e09c5dde8016ccd6855dc652439695f3ea4e679f8b722b1960`  
		Last Modified: Mon, 28 Oct 2024 22:34:02 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39b8355d91777cb6df3f75a06c9e30bfcd4870f76dc5b1e9dab30f91f6e4479`  
		Last Modified: Mon, 28 Oct 2024 22:34:03 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ce16f950f9cbacee6d8daae67bfced71203093c06cd1e740374b4290ce1c03`  
		Last Modified: Mon, 28 Oct 2024 22:34:03 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061f2ad066c640ec7c5a4b4cf26641f132e9e7c5bbbe682049c5b6c8d81fe0ce`  
		Last Modified: Mon, 28 Oct 2024 23:49:40 GMT  
		Size: 25.7 MB (25705169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26765d442d2e84d450467fcd32b961126192c2971514a0326e234c0a45f1ab40`  
		Last Modified: Mon, 28 Oct 2024 23:49:39 GMT  
		Size: 13.3 MB (13278857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fb233945bd4b51c1e0216d40d4c005c68ec4216593e81c0eddb040cab1f335`  
		Last Modified: Mon, 28 Oct 2024 23:49:38 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8f38805751d2efff55d3f0b13e922530cb0df7719ec73a41ba6e074fa49d09`  
		Last Modified: Mon, 28 Oct 2024 23:49:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fcfc2f10a5823619eb0689f333fa9238001ab289fffcc1a1dd8aeae12e9ae6`  
		Last Modified: Mon, 28 Oct 2024 23:49:39 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f02b1657ba3d38988356c8915de4f7ba214b4774ad92528efa92c9f693836f`  
		Last Modified: Tue, 05 Nov 2024 21:02:38 GMT  
		Size: 32.7 MB (32651964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1467046dd7af116c2767d6c671d963af0cc005ae48c2107b0213793cd5f4b8ea`  
		Last Modified: Tue, 05 Nov 2024 21:02:36 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbaef7325c0beb26e3af5cb07506fdf5ce789a620bbabe11daf4220e189024e`  
		Last Modified: Tue, 05 Nov 2024 21:02:36 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:40e3e30f0aec5b7ecd9ac630e6426718dc5cea093cd5c31699dd825ccb304864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7990063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd50edde33adac096a169052424c7f9ba55c33625f648d42a36a32f6afd2d44b`

```dockerfile
```

-	Layers:
	-	`sha256:6df8a9d1bf5cce9e78744b28cf48978c74a5879b950d1576400025032713c715`  
		Last Modified: Tue, 05 Nov 2024 21:02:36 GMT  
		Size: 7.9 MB (7929056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03252995b64b7a881913fafa2482307de8f0141947cc8b087c9cf6fa1fbefb8`  
		Last Modified: Tue, 05 Nov 2024 21:02:36 GMT  
		Size: 61.0 KB (61007 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.3` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:ee2ff229c248ad5595268031acff3bc38041dcb2f724037cb901354f73bd7f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212184164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93042d3db01d56ebe4fea8351c22a00079559d437489764ffe466c8e767e93a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcfcb380cfbd1992d2f15637ef37999cbc4f9934874d34a17b217098fa8c2f4`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63df587ed65ffaf4f0e56a3ade450a0c2f4bd0ec52cb90e0193d9ec9a394a939`  
		Last Modified: Mon, 28 Oct 2024 22:06:06 GMT  
		Size: 76.2 MB (76163014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f4e906cd29de73704abed83d01761162847c368f1a7c597dc584fd985a75c2`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42cf4a791cfd52dd382314b8b0f4cbf7a46e61d6c6c664a4299bfc5656b5a8`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 18.9 MB (18857494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bf1529cc0e5c50582fc58382ef311e785b9a8a182db98e8831efef019fe199`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fca32620845d0574b19199a5b046dcb2260722f191ef3f55c582ed51287e788`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0630ce9e3aaa266d2df0b1e9e5009773fc344179fcbbdc3c987ab82450387b02`  
		Last Modified: Mon, 28 Oct 2024 23:30:35 GMT  
		Size: 12.6 MB (12610499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bd15aa423dbdcbbbd98dadb62b179877c124f11bc9bb03222d8995f3669280`  
		Last Modified: Mon, 28 Oct 2024 23:30:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627abc4c4bccfad0a0915bef0ba0d58524652cd1fcd05584cd49db7964a1a132`  
		Last Modified: Mon, 28 Oct 2024 23:30:35 GMT  
		Size: 10.0 MB (10034205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e56d05bd57bac3d4ab16d5e10722de498ef0bca97cc0669f14df01d2392354`  
		Last Modified: Mon, 28 Oct 2024 23:30:34 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf8b59e4942575a63273f5e258bdd03dfb1a7963a2088c10ca1799c1234867f`  
		Last Modified: Mon, 28 Oct 2024 23:30:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bacf6d5a906379e0013ea3f46279d0cede9b58e86d920c1e03391a14abc2e2`  
		Last Modified: Mon, 28 Oct 2024 23:30:35 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2511aed5f747b0b7c6b839b81d3f83e2aaa4bd1cb1fd412064833f7c10e833b4`  
		Last Modified: Tue, 29 Oct 2024 02:13:10 GMT  
		Size: 25.1 MB (25075442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198dfbec4d1b2953e0ef8c2ee59b776df91307048463d89177bf5efa08eeba45`  
		Last Modified: Tue, 29 Oct 2024 02:13:09 GMT  
		Size: 12.0 MB (12043814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5360bacf2c82213c0530aac087b4ef54a02a22d2ef50340d328f31d4507cb2a4`  
		Last Modified: Tue, 29 Oct 2024 02:13:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f3be676480e364949f5e21e06de53488a2950225888d2cf69fc5c441ace93b`  
		Last Modified: Tue, 29 Oct 2024 02:13:09 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964a2d4ef8d1b77db78a2e220017792b983de784dd98c8194511c9575cb6ab1b`  
		Last Modified: Tue, 29 Oct 2024 02:13:10 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb940aab614b483632e2c9aa0ddd6b3127170b7041e68481501b9acf1c2b418`  
		Last Modified: Tue, 05 Nov 2024 21:05:25 GMT  
		Size: 32.7 MB (32651944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3dee9da90e366b287da690762dd7214b35132081bb4a6dc1e335b281767ed2`  
		Last Modified: Tue, 05 Nov 2024 21:05:23 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f79eefb87a23babad7c66483f1a6821b4826f7ac4554444d054d73d9fa1ba0d`  
		Last Modified: Tue, 05 Nov 2024 21:05:23 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:efc47654399c86c250c7145201131d0d49d6061d254edd9ee5f90b7625318f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92fbc806ebfa3e31e2e26acf36e9250615d998a39f067bb895ff9e0580742ad`

```dockerfile
```

-	Layers:
	-	`sha256:c92c6f9ca497405e783ef3a0eb659cd64ba8a82e59f59d472de05012e9e09138`  
		Last Modified: Tue, 05 Nov 2024 21:05:23 GMT  
		Size: 7.9 MB (7933750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bed61bc61e39426afbc647c5506e823a8fe3acea10396dcb7e5ecbd308951a5a`  
		Last Modified: Tue, 05 Nov 2024 21:05:23 GMT  
		Size: 61.0 KB (61007 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.3` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:bd1a9d7ba48f37f4ea37c74eafebe03ee5118760164d655680ffb33531e9bdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244292834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3a5de8cba1982ab2a3742b3d8ba8a96101bddf17c63d5becaf639583a3aca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f5f021e5979c9f49d4bfc61d4b51dff54ffa783b2a965cb659aa81fbf0b65a`  
		Last Modified: Mon, 28 Oct 2024 22:59:26 GMT  
		Size: 12.6 MB (12612106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1387efb6f59c9eca2d22debdcb1eb527f52da30bd703bb31e516b0850e3e4bf3`  
		Last Modified: Mon, 28 Oct 2024 22:59:26 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ea53faaa910f15c25f22f658929e0b6444fc6450881a22409b75e1efe756a7`  
		Last Modified: Mon, 28 Oct 2024 22:59:27 GMT  
		Size: 11.6 MB (11632895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50f3506085861dff9ffcf6f69e40ed438af7618d5f6bfd400e9e8eea6144bf4`  
		Last Modified: Mon, 28 Oct 2024 22:59:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f407f6179bd45372e92c2f843c93d72cf1dfde5c810b2559c8959ab87cd20a`  
		Last Modified: Mon, 28 Oct 2024 22:59:27 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc3d61d383c6ba372099294cd437adefb4fa757547c04ecb1c7aac947b99c87`  
		Last Modified: Mon, 28 Oct 2024 22:59:27 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d486b99a085ae10d48c0be9f687dff0c3adac5fb7586fe7d89b2879f275d94d0`  
		Last Modified: Tue, 29 Oct 2024 02:13:51 GMT  
		Size: 26.2 MB (26171664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b88de85b3a8f9794e1c338f7db5269bff007dd1d44a57d35e320a9db17167`  
		Last Modified: Tue, 29 Oct 2024 02:13:51 GMT  
		Size: 13.8 MB (13787341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61f8a3cb8d1270f0e4fb9f99873417aff35a7eb1126e0f7496ce0fccdd1c82f`  
		Last Modified: Tue, 29 Oct 2024 02:13:50 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc752ca78a8cc8a489ef6cc08cc369280d03e0a30703da89d7aac7b0bcf9f80`  
		Last Modified: Tue, 29 Oct 2024 02:13:50 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f7da4b726b4cd24fe4a7be01abf0f051a5694b00f6f712e761c0d0096ccd6d`  
		Last Modified: Tue, 05 Nov 2024 20:27:53 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23e15273e0c07a3000593d7db9d6134318d5308afdf2bceef69dfa5b30b9b9`  
		Last Modified: Tue, 05 Nov 2024 20:27:54 GMT  
		Size: 32.7 MB (32651965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c228daa6f3f63f905274a0924bbf0ed878c796b70f02f547cae0025779279`  
		Last Modified: Tue, 05 Nov 2024 20:27:53 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c4f503770fa1e38eb033a46bd36aee688e9a42aa882db749c5a6f8c72d128a`  
		Last Modified: Tue, 05 Nov 2024 20:27:53 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:16cfc4ed60a50c79292708d5999b71f48523f62f9b4f3ac46700815399eb4fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d73435d79067c1275682660e76983c92edb10abb034013fd8d8d7384b7109a`

```dockerfile
```

-	Layers:
	-	`sha256:25188ec3fa16ac00236a4269d999a54407bc1a4fdf7a8e8b28a782efd0f492f4`  
		Last Modified: Tue, 05 Nov 2024 20:27:54 GMT  
		Size: 8.2 MB (8152021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0658238762ba4225868fbc22ca627b3fc07dee5d91558f94ed908ac2a2667a`  
		Last Modified: Tue, 05 Nov 2024 20:27:53 GMT  
		Size: 61.1 KB (61060 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.3` - linux; 386

```console
$ docker pull wordpress@sha256:3e070ce1efe49ed439711ebbbdb214edabdaac52cbc5f5e9e82c0cc8bd0c8f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249640918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b250c97d6b532c4e603c6a213e88a5ca24013aae8727e08479cc27e3f57c160b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329eb31a4f93e9d41ddca528693079d4cac38e0e0cd7acbbf24dbaad04c807e9`  
		Last Modified: Mon, 28 Oct 2024 22:05:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00991a5c316faa9083955727f89b3e04028027ea095f4ebc8fe11c24701a97a5`  
		Last Modified: Mon, 28 Oct 2024 22:06:29 GMT  
		Size: 101.5 MB (101516947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479896864efa784a35768f05f72ff5585dc52a8377de29499449cbfb93d21b3`  
		Last Modified: Mon, 28 Oct 2024 22:06:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2640e1a07ee466e0bec0bd6b84574579a011598fea39c2b18beb22edef0bbf`  
		Last Modified: Mon, 28 Oct 2024 22:06:26 GMT  
		Size: 20.6 MB (20638451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee53c118cbbb1b6e4c239e0ea5db3ae393013c5d5e24367a20635acd0b7056ae`  
		Last Modified: Mon, 28 Oct 2024 22:06:26 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0e769040ccb1546ac0d4ed3ad58ed10b689426fbff5aee2e0dd81cf1be3d27`  
		Last Modified: Mon, 28 Oct 2024 22:06:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239b6469dc8348d269f3caefba6ac2834c0bf5e9e3e1dd1409d160af8979d0b`  
		Last Modified: Mon, 28 Oct 2024 22:06:27 GMT  
		Size: 12.6 MB (12611408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49c86746ac71d54d5b69263b64615f0f52f3f5a92a9518a6d9cf39118f2a04`  
		Last Modified: Mon, 28 Oct 2024 22:06:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd46df7b7a27b3a684a3fa865fd47872c6cb79ae483e1e3403eaa666b2c624d`  
		Last Modified: Mon, 28 Oct 2024 22:06:28 GMT  
		Size: 11.9 MB (11862577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8bf4f8e802f4327016a09002d598e17cb81c8dd98f8134854c2b43f9bb82ae`  
		Last Modified: Mon, 28 Oct 2024 22:06:28 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceac382e0107f09c9d4f4f29c19f2ec27777333386b4927599ca03b496829569`  
		Last Modified: Mon, 28 Oct 2024 22:06:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69d6b970e9e74cad9e394a1b0e7707cf00b0673458fc3da783321cdb83b4753`  
		Last Modified: Mon, 28 Oct 2024 22:06:29 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff0cfe7300ab4c4264b5bdd7d5d306aa6e5e948424b6a3d0d3fafc503c0d321`  
		Last Modified: Tue, 05 Nov 2024 20:38:09 GMT  
		Size: 26.7 MB (26696256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23fb398afd27ff661d40583420d7a222c780d75509210ea60f76f880cb02749`  
		Last Modified: Tue, 05 Nov 2024 20:38:09 GMT  
		Size: 13.5 MB (13489525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a665653ae75403d6ac2d3adeb0ffc22800c9351a7f11894d5f23510dff15ee8d`  
		Last Modified: Tue, 05 Nov 2024 20:38:08 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccaf4f77e994c80a834b7849fe3a42cb7637fe6c6dd493940507f0f4738e1cb`  
		Last Modified: Tue, 05 Nov 2024 20:38:08 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dac32ff7f022e78a3b96430a60b8d0334ea65742119d18c6d420ffe0d60e93e`  
		Last Modified: Tue, 05 Nov 2024 20:38:09 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a44515ea040ab4ebee74825cba44fdcba00bfb64c9b875ac77903d38edb30e2`  
		Last Modified: Tue, 05 Nov 2024 20:38:10 GMT  
		Size: 32.7 MB (32651960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035663183a0dc5d96d66b3e606579326ca162d1a8771b82c86da418e04929d01`  
		Last Modified: Tue, 05 Nov 2024 20:38:10 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a81bbe9a5ab250e75a0960a378bb758896f1617267c9eb258112241b10fd54`  
		Last Modified: Tue, 05 Nov 2024 20:38:10 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:0e676fdf1422ff1d1887c390c29996c2ffd6081c57e4cbbd5217bb7724ece6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8157111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0705d3328eb361448cf51f00ee4373510ae3e50dd4311ccd26c3b64cec261f4e`

```dockerfile
```

-	Layers:
	-	`sha256:560c6182eda1986c9b4fb3d34c85245616f2e092c3d9cd22e942320a992f228e`  
		Last Modified: Tue, 05 Nov 2024 20:38:08 GMT  
		Size: 8.1 MB (8096384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bd8755b9132ba72a5cd730c14e2c38f2192b84ddcbbddff43caf750bb92c3b`  
		Last Modified: Tue, 05 Nov 2024 20:38:08 GMT  
		Size: 60.7 KB (60727 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.3` - linux; mips64le

```console
$ docker pull wordpress@sha256:e2947defeb378e283699e487020bf632a8a4c9a0353e20f2f5df724ecabac549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224852147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7813c02c74c94ac24078607f6d424847247c8950b1c805dc0bca6c0a3a6b925`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:35 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 17 Oct 2024 01:09:40 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75971b85139441fe144cb93dcb63eda60c20b8b82bcc4cc161a345662be6e248`  
		Last Modified: Mon, 28 Oct 2024 22:20:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54a087649536e7da942bb23de64ede6ba55259b78328b804de7695cf731369`  
		Last Modified: Mon, 28 Oct 2024 22:20:39 GMT  
		Size: 80.7 MB (80666666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d1ae69be6bff3b5f486ce83dc2a01329491bc64c77e183361743695495d62`  
		Last Modified: Mon, 28 Oct 2024 22:20:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805e4def2c522f97a948ff0a106d6753819d71887cabeca9b1ab8355a0ec3f5`  
		Last Modified: Mon, 28 Oct 2024 22:40:31 GMT  
		Size: 20.1 MB (20069130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f108a36b91c4b30f45222f94048f45b028abb9cbd4872f312cc17b7ebdf9e0a`  
		Last Modified: Mon, 28 Oct 2024 22:40:28 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badc8de30d0eaabcca7399faec8b52772f4a699389c0f6ee67d901929b205efb`  
		Last Modified: Mon, 28 Oct 2024 22:40:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d400c1cac071f6746ef45b67a5a977e40c885b3cb960647f01d37f2a19bcdf`  
		Last Modified: Mon, 28 Oct 2024 23:51:57 GMT  
		Size: 12.6 MB (12610143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9454b9633f46c864059147bcb08f5762c5e87395c30bc281e9621e28907b0d`  
		Last Modified: Mon, 28 Oct 2024 23:51:56 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8f56a3eb0c8180952ec7904eb7f44d2af333abc7242bf73d814bfed601a4f`  
		Last Modified: Mon, 28 Oct 2024 23:51:58 GMT  
		Size: 10.7 MB (10715039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56e98166416195e72f7b4873364c2f4e2d33158814ae1284b4f39f124a8f858`  
		Last Modified: Mon, 28 Oct 2024 23:51:56 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a6c7e9e96a53de414e24a1cfbdd3a2383547edce544f88fa8a74baec13d64d`  
		Last Modified: Mon, 28 Oct 2024 23:51:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f5c8ff575e778c3693662175f2c1e4e7b39077eb37f369f5e0e01b76e26e90`  
		Last Modified: Mon, 28 Oct 2024 23:51:57 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4e7a3b717194f1f71c03b7f6434dda2e707d703547bf1d27137bec0dd20538`  
		Last Modified: Wed, 30 Oct 2024 00:31:27 GMT  
		Size: 26.0 MB (26025523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa0e0c45eab27f17ec1823c8f50faec419caa8bf1ff59a2bb99b4ff2e441a4`  
		Last Modified: Wed, 30 Oct 2024 00:31:25 GMT  
		Size: 13.0 MB (12959350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3199a8af7012412a6178d5bf5ee0256dc3c82fa23d407e0d90750f332d97884f`  
		Last Modified: Wed, 30 Oct 2024 00:31:24 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936355ca64e1a40dbac6745263c2ceec3428e20e26b0b9b41070015a4b62590b`  
		Last Modified: Wed, 30 Oct 2024 00:31:24 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb540d909e92e7d07454cd3fbf31dacbaed79a668616c4aa3aab8db7c0f467f1`  
		Last Modified: Wed, 30 Oct 2024 00:31:25 GMT  
		Size: 19.2 KB (19162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78abdf25656d975423e22a2d7ccaab9085a8bf0fe78105a86a12f469bb61b59`  
		Last Modified: Tue, 05 Nov 2024 20:44:55 GMT  
		Size: 32.7 MB (32651965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0edd9054d255f2f2fdc0d19f58bd1c743eb05e03cf2475f0975d110c5de171a`  
		Last Modified: Tue, 05 Nov 2024 20:44:51 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabc03393dbdbe426d8504e99b8ab40807816a995cb893ed929037b484b33919`  
		Last Modified: Tue, 05 Nov 2024 20:44:51 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:8e6b8f12ef2122a6928b152bdafaba2fd239a4a2fa4dd6558f908ef7968c1148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 KB (60736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dcc45910c07593bf437d88888007c6f6b488bec4f937d54df7940ede41d985`

```dockerfile
```

-	Layers:
	-	`sha256:58caae53cf6be86fcd48f1164bd350a9b18ad602db6450c7d6c0218afe214e6d`  
		Last Modified: Tue, 05 Nov 2024 20:44:50 GMT  
		Size: 60.7 KB (60736 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.3` - linux; ppc64le

```console
$ docker pull wordpress@sha256:6256a3ab9bbed6d04defc5618ac1409e2b16377fca8da350745f1ca0922c92c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258073796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92943b5dbabf404109eacdb39ec949e789af35015b4b5be45d4e9f38e7382437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae56eb39d7a6f0865b2b2c1e759158f7f32cb38431cf0b9f4a53e75069829a`  
		Last Modified: Mon, 28 Oct 2024 22:03:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc191720824d9a8274cc0a9d7a4e17b74deb924b9ba62a638fcfe329b1cb843a`  
		Last Modified: Mon, 28 Oct 2024 22:03:58 GMT  
		Size: 103.3 MB (103321639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e65ebf34f6eed8b3368c7c37216f302c7b19e10d99d1c5ebd90d00bbf57cd63`  
		Last Modified: Mon, 28 Oct 2024 22:03:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ca7c4e1c934a05195ae2806efa08495b749078e5060a107b69954c9e8831f3`  
		Last Modified: Mon, 28 Oct 2024 22:09:18 GMT  
		Size: 21.3 MB (21308341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afeb891a5f261be3057466eac9022a1bd1afa1a3773815828cd1caeb277139c`  
		Last Modified: Mon, 28 Oct 2024 22:09:17 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6afdb35491d58f7d16d1d4ace112bba4fb8ba8a1702dbad4ec8737e9e449f6`  
		Last Modified: Mon, 28 Oct 2024 22:09:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9c1662c1cd31c1b30da28d8a64d154191c62c8f67160fc0a128bf44732975d`  
		Last Modified: Mon, 28 Oct 2024 22:44:13 GMT  
		Size: 12.6 MB (12611804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176f2372ce1117548afc0e0c9c94d3ea66369918814c22c7e2225d00583fca3d`  
		Last Modified: Mon, 28 Oct 2024 22:44:12 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb01cf1c872c3320163513026ee4b59b59fd44aade2a4e52c085bdb61c1769e2`  
		Last Modified: Mon, 28 Oct 2024 22:44:14 GMT  
		Size: 12.1 MB (12061036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d09e36eb35cc217a3f1050664d124ec2c35c549490327fd1c2716993eadb32`  
		Last Modified: Mon, 28 Oct 2024 22:44:13 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2c222712debb08cb59b5b2e7fc0afdaf37961b8aff5ba982fef2f95cca9b9c`  
		Last Modified: Mon, 28 Oct 2024 22:44:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736ea7f89ac990eb370b2c10073c9c5eb18902de47ba54ef84968f23f3c8590`  
		Last Modified: Mon, 28 Oct 2024 22:44:14 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc290ecaf16a00ff2acdee997037beaee7906ee1cb03122f5ad4e7f1d2662e06`  
		Last Modified: Tue, 29 Oct 2024 00:40:30 GMT  
		Size: 27.3 MB (27336924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa530a576ae9b5db111915e5d84012a1985750899ad2f6bebaba9787a2aab4`  
		Last Modified: Tue, 29 Oct 2024 00:40:30 GMT  
		Size: 15.6 MB (15630343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9b7e58f1a8e60996a4108bc3f3cc8ef7e3944082e506f53199eabd863c6284`  
		Last Modified: Tue, 29 Oct 2024 00:40:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1901383521d9c51b9632788c680e7346512876be96bd5f1dd4ac68fcada693`  
		Last Modified: Tue, 29 Oct 2024 00:40:29 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee41e8d8e05808a988530bb610dd8eee0274ec07979644dfe30dc30ff8ff18c9`  
		Last Modified: Tue, 05 Nov 2024 20:43:30 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7575fdf7e4dac8ca7cfc2d6886cade011a8d090bd03c8cabc605020e81b842b`  
		Last Modified: Tue, 05 Nov 2024 20:43:32 GMT  
		Size: 32.7 MB (32651968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0ac18831de240bcd88146f937068b3741e8d777b15d969303571a3a52ce0c1`  
		Last Modified: Tue, 05 Nov 2024 20:43:30 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b9d241d3546123c8756ac0bf1c7589ab83ff4a6dbb25c4ad2d610b1226045`  
		Last Modified: Tue, 05 Nov 2024 20:43:30 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:4190ec9e6f122986c973ce13e94962783a23b65c1a0626394b28e686aaacac85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8162930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fad76d3f0f6362b4b006323543b349c68b7fd4747645ac3bdc5992b09d1829b`

```dockerfile
```

-	Layers:
	-	`sha256:bce096226a3e8f7577eba6e8e5f06af3afbf7c73de2cc485953b004108dd54de`  
		Last Modified: Tue, 05 Nov 2024 20:43:30 GMT  
		Size: 8.1 MB (8102009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25df325fc38ee6221ec7f4b537abd79301ad5c734b9fad7505a9cad8c1fca58c`  
		Last Modified: Tue, 05 Nov 2024 20:43:30 GMT  
		Size: 60.9 KB (60921 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.3` - linux; s390x

```console
$ docker pull wordpress@sha256:f71aa411b27881db2075319af89b71d3da59b072e293210516b72f03a33b5038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223719607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349868702abeb8dbaf4b2d92cf2482d61f38836d94e3dbf391bfffa2dad9ccf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 24 Oct 2024 16:31:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 24 Oct 2024 16:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_VERSION=8.3.13
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 24 Oct 2024 16:31:40 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 24 Oct 2024 16:31:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 24 Oct 2024 16:31:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 24 Oct 2024 16:31:40 GMT
WORKDIR /var/www/html
# Thu, 24 Oct 2024 16:31:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 24 Oct 2024 16:31:40 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef30fd559c6ef2ac6477f19c70672a7ee15e6df0955b9418d7d99e635fa1bf0`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4284cccc34f4d86bd5b1ffc10f277aa5cc0d4e8e4bf9be585b727389498bc65`  
		Last Modified: Mon, 28 Oct 2024 22:04:13 GMT  
		Size: 80.8 MB (80817298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b072383a75b21caa7c43d077f84a4e9c721b6f8b19ab0e9df353f53ab84ca`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca23539a560ecbc74c5143d2cafda70db6eb98973a13e443b451e0c9c2995f`  
		Last Modified: Mon, 28 Oct 2024 22:09:43 GMT  
		Size: 19.9 MB (19895121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a45ddf6b46c9a6c7f526ae595797099a5fc579b55abcfd3898676b4d492cd2b`  
		Last Modified: Mon, 28 Oct 2024 22:09:42 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251a13b927d3a64cfbffb8b90c4c32f8b6e265b8d38173390a57a3b727aad43`  
		Last Modified: Mon, 28 Oct 2024 22:09:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b1bda4c44d2e98fb7018115294dc73322a28b9af83874543ca5c63de4abc3d`  
		Last Modified: Mon, 28 Oct 2024 22:58:40 GMT  
		Size: 12.6 MB (12610824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785bf64522e1b32c4cee86819777e62c531123c4d13512f91db7511cbd90a3f4`  
		Last Modified: Mon, 28 Oct 2024 22:58:40 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0f20dcc891cb68594afa6d0175c48a37242b3e963b6be4381227223214d70d`  
		Last Modified: Mon, 28 Oct 2024 22:58:41 GMT  
		Size: 10.9 MB (10860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8912b1ef07621283266d8e2841560b10d404adb263a44572cbe12310802f32`  
		Last Modified: Mon, 28 Oct 2024 22:58:40 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143410cb78ed7da42646370a15b2c736c720ea571758e8e238028bb832befe21`  
		Last Modified: Mon, 28 Oct 2024 22:58:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6cd9cc7ec59b6ceaa395f922720016c9035a7e78ea27ef4d7c1a93f08966c1`  
		Last Modified: Mon, 28 Oct 2024 22:58:40 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d554be4921123db0b485d3ad1278bf493300981da1be22bfefb9076a8728ff3c`  
		Last Modified: Tue, 29 Oct 2024 02:27:56 GMT  
		Size: 25.9 MB (25898824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f032786baaa038fdaa7a482c427a2cdbd3a6ef81bd8ce2e84799b49532bb474`  
		Last Modified: Tue, 29 Oct 2024 02:27:57 GMT  
		Size: 13.5 MB (13465205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209169fd4f2595d1f41d6911178f86ed4528353dd1a9be8be45059bc83f58952`  
		Last Modified: Tue, 29 Oct 2024 02:27:55 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a561d0d4a0bdfba3f88e71c439c25f85cbf2034a611d5a4458cb8ecc03c447e5`  
		Last Modified: Tue, 29 Oct 2024 02:27:55 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aa1d4db744581fc49aeeae70c5664d1bb09b92003878a1c543b5f89fb01b9`  
		Last Modified: Tue, 05 Nov 2024 20:48:25 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03879815d94128ac5ded08e6f7951b26335c7274ba7bee7a223808e33964854f`  
		Last Modified: Tue, 05 Nov 2024 20:48:26 GMT  
		Size: 32.7 MB (32651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801f24bb5ce97af1ab771f0cac1bbd2336141294b6b8b24b82adc60887165838`  
		Last Modified: Tue, 05 Nov 2024 20:48:25 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee1cb3a178335510b6e940c936c95d289f50147c49bcad0f89596a3563cc22`  
		Last Modified: Tue, 05 Nov 2024 20:48:25 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.3` - unknown; unknown

```console
$ docker pull wordpress@sha256:365f1ce7c9578d58e196015b1168640549db6be696493db3f0f73830b60c9d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8013879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69579a2c0a50f4e653bb7da3231ff9dbe3923c463c7ae627fd6e57576952551a`

```dockerfile
```

-	Layers:
	-	`sha256:84d756ca0e42b09ff89279995d52351b85ed1024a3d9e3e5b789bf68f1d75d51`  
		Last Modified: Tue, 05 Nov 2024 20:48:26 GMT  
		Size: 8.0 MB (7953045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da88b03ad57875009464cdb322c7a5e8d65b23eee37bd142801ea11e0056a24a`  
		Last Modified: Tue, 05 Nov 2024 20:48:25 GMT  
		Size: 60.8 KB (60834 bytes)  
		MIME: application/vnd.in-toto+json
