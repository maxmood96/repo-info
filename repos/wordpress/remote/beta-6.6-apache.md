## `wordpress:beta-6.6-apache`

```console
$ docker pull wordpress@sha256:99859e3742907212a59328b4278ad043471573c199a3dc9528acf897e543dc8c
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

### `wordpress:beta-6.6-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:78cbd81f809dca808203cfc0fa3109bbc34e11ad9512fdbcdefb4a5d8b3c1ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240733990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1835f8f266a71f6198791bf7cec087927ca379cf265e0f71cd0c811b191bc711`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Jun 2024 19:03:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["bash"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 25 Jun 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Jun 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Jun 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Jun 2024 19:03:11 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_VERSION=8.2.20
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Jun 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Jun 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Jun 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 25 Jun 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
WORKDIR /var/www/html
# Tue, 25 Jun 2024 19:03:11 GMT
EXPOSE 80
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	version='6.6-RC1'; 	sha1='926c5c62dc58e5c10ffa2a51c508c91f6b7f0c7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Tue, 25 Jun 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c1fd48de30b16f5766e6ac96a6fe3c0b3241c34c93fe82ddc8a8536729dd53`  
		Last Modified: Tue, 02 Jul 2024 04:36:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b3bda7c6d1ae6620633030596609872e7f2b102e3f274f02c71ee92e136cb7`  
		Last Modified: Tue, 02 Jul 2024 04:36:44 GMT  
		Size: 104.3 MB (104349018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a68eb681dd3cc5f145cf854bf049843298d6ee06c3259ddff5bf4793710a80`  
		Last Modified: Tue, 02 Jul 2024 04:36:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35406f9afc7f771a49890b78aa21515eb9a55078c04c935db2eccebfa0ee09e1`  
		Last Modified: Tue, 02 Jul 2024 04:37:07 GMT  
		Size: 20.3 MB (20328149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d29e3575095485f641778e00db76200a84450e66c56ade92952177c80038fd`  
		Last Modified: Tue, 02 Jul 2024 04:37:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d497b137ced83d700feeac177251b0552c63749019adf459aeb89db255825ee2`  
		Last Modified: Tue, 02 Jul 2024 04:37:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199c1373b38a486cf06c37a0d40388436572e26ce5011a494be446265df566a3`  
		Last Modified: Tue, 02 Jul 2024 04:44:37 GMT  
		Size: 12.4 MB (12431056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a087c2a4e19b42decfed96403909b5c3170ff746190eefc41ef9b8e65322fee7`  
		Last Modified: Tue, 02 Jul 2024 04:44:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646a76836d788373977cb6e165941b84336ffbd2fc71d7758ca54b9ceb463f10`  
		Last Modified: Tue, 02 Jul 2024 04:44:37 GMT  
		Size: 11.4 MB (11403950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de207cf6ae353ab7df867583973042be7a2155f857406fea28924d3303a26965`  
		Last Modified: Tue, 02 Jul 2024 04:44:35 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e491b77be4cc5e30bd91c3e27dbc90080ab0a404719f77def3d6282a749757d`  
		Last Modified: Tue, 02 Jul 2024 04:44:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f7afba5a8e6476e2ebab8a7e8a9f764b6da87b5e83fafd6a52f7f979f5a26e`  
		Last Modified: Tue, 02 Jul 2024 04:44:35 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9780c5e21d27e782b17bd33adea1b076d971e31f62ed4644bd3beec829f3ba`  
		Last Modified: Tue, 02 Jul 2024 06:10:05 GMT  
		Size: 26.3 MB (26254285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c66d93fcab1535baa01c660576fd967364b746a786a8ed4d7cd932530cb04a`  
		Last Modified: Tue, 02 Jul 2024 06:10:05 GMT  
		Size: 12.4 MB (12356028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218516df4e83286eb402b8813b411c79f32ecfb994823c9ec087bda8f129cbe1`  
		Last Modified: Tue, 02 Jul 2024 06:10:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b6f4293d800fc4ae1cce309e41efcd8d1df5178fb6616b85f27c47992658a0`  
		Last Modified: Tue, 02 Jul 2024 06:10:05 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccc089fe446c46887b782444dfe92c5b8660d41b51f96922cbf53958bea815b`  
		Last Modified: Tue, 02 Jul 2024 06:10:06 GMT  
		Size: 19.2 KB (19169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3594995e1b4c4400c139d6c733c4ac431e84d8a698682192875bb59d635c99`  
		Last Modified: Tue, 02 Jul 2024 06:10:06 GMT  
		Size: 24.5 MB (24455767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04abf94c3a1250513e0316176efc1f3e2dec000303448fee1d84d0402996ce71`  
		Last Modified: Tue, 02 Jul 2024 06:10:06 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc851e38e85acdecbd290a1a4c1bc4c807263305d6f96cbfccb80c099531dc2d`  
		Last Modified: Tue, 02 Jul 2024 06:10:07 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:c7ff99a4214fabf163f59baf488bfa14da9982c6afad7d57361916742cfea838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8020669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977143b07acf79e8c92bbc1d7b18c2d20f4a88ae12f1af4775dfeb9c6eb61f20`

```dockerfile
```

-	Layers:
	-	`sha256:0ee5e105f6133fc53ce0544fc0429a26f76b312899c1a6c75c07a3d6a20856b7`  
		Last Modified: Tue, 02 Jul 2024 06:10:05 GMT  
		Size: 8.0 MB (7958449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad1e657cd09027d54e1c678b79b7e35cad059c6210a8a9d3a1c6a0e65055f13`  
		Last Modified: Tue, 02 Jul 2024 06:10:05 GMT  
		Size: 62.2 KB (62220 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:c5f14ff9ff6b17699170f595b77ecb10336e83cf8440175abce26bb5820a3e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211502300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1964c47683f3b9d68dfa0e60f211bf55da0721195d812ee7c4572f6769ccae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:32 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Thu, 13 Jun 2024 00:48:33 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:29:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 13 Jun 2024 01:29:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Jun 2024 01:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:29:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Jun 2024 01:29:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 13 Jun 2024 01:32:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Jun 2024 01:32:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Jun 2024 01:33:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 13 Jun 2024 01:33:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 13 Jun 2024 01:33:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 13 Jun 2024 01:33:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 01:33:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 01:33:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Jun 2024 01:58:00 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Jun 2024 01:58:00 GMT
ENV PHP_VERSION=8.2.20
# Thu, 13 Jun 2024 01:58:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 13 Jun 2024 01:58:01 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 13 Jun 2024 01:58:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 13 Jun 2024 01:58:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:00:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 13 Jun 2024 02:00:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:00:59 GMT
RUN docker-php-ext-enable sodium
# Thu, 13 Jun 2024 02:00:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Jun 2024 02:01:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Jun 2024 02:01:00 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:01:00 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 02:01:00 GMT
EXPOSE 80
# Thu, 13 Jun 2024 02:01:00 GMT
CMD ["apache2-foreground"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	version='6.6-RC1'; 	sha1='926c5c62dc58e5c10ffa2a51c508c91f6b7f0c7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Tue, 25 Jun 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fbad6f92fdf1465062c303dd0c7c9130ab6dc529b183c304547da5e8bf2c8f`  
		Last Modified: Thu, 13 Jun 2024 02:44:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5182fbee20e89d105204362e19892b9ca39125b22b43251bc7073713b5708f`  
		Last Modified: Thu, 13 Jun 2024 02:44:48 GMT  
		Size: 82.0 MB (82002197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3717ccaf6d8fcdea2c4dc5dc81fc3f8e4469a1ef8e211f6944bb0b52ec160ae`  
		Last Modified: Thu, 13 Jun 2024 02:44:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2500e80ef231e4d9daf39c4d5330bcae222ae5a6b7055799b23eb256d88af`  
		Last Modified: Thu, 13 Jun 2024 02:45:29 GMT  
		Size: 19.6 MB (19622246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336fc7f090e5cbaa48a4022823b653cdeebd185b48cfbea2daabbd492e2f4727`  
		Last Modified: Thu, 13 Jun 2024 02:45:26 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9aa937b384a12f7963ca6bf90a0113ab25ee44eb6a5929e75d1a21a879a89f`  
		Last Modified: Thu, 13 Jun 2024 02:45:26 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952cceea804040adad0cacf1c8a87888a87c699d2a493ffc1f0e08f3e563bd9`  
		Last Modified: Thu, 13 Jun 2024 02:48:46 GMT  
		Size: 12.4 MB (12430600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6313b99b982ecbfda4ca1204cc13e38e3543a4b7cbed7adca8e231367f851d7`  
		Last Modified: Thu, 13 Jun 2024 02:48:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce74a20633c6486dd22f73094d592a46963c924e3dc5b964d205730a1ad81c9b`  
		Last Modified: Thu, 13 Jun 2024 02:48:46 GMT  
		Size: 10.4 MB (10391791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3c1cce8476a331da5fff287f47f4cbc17df18f1468f630e3a73eb88fb0fa3d`  
		Last Modified: Thu, 13 Jun 2024 02:48:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb9d58827cc42f338f0ff23df4bf4dc47cd253bfc10d9a4805e9539d37c9dc4`  
		Last Modified: Thu, 13 Jun 2024 02:48:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ccb474409931ecc65da2295e4946e8b14bc1e82db2fb704247e554616f5005`  
		Last Modified: Thu, 13 Jun 2024 02:48:43 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e773c060d61db03c115061b8c0f0b52a87b1ccec2fbc642d065edb1852b62f5`  
		Last Modified: Wed, 26 Jun 2024 20:12:01 GMT  
		Size: 25.7 MB (25710807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6080345e502601d612f1189f36adeac73c9d4ea06bde14dae4f91842fbd5f8a`  
		Last Modified: Wed, 26 Jun 2024 20:12:01 GMT  
		Size: 9.9 MB (9949482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e47847d0f04f7cc27adb3bc54bc103b1afdd28d10b4af5704f6c7766dd5b1b`  
		Last Modified: Wed, 26 Jun 2024 20:12:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6609b8b74b601f7cb709f0f0a73ff3000016539a71bbad59426fa613972eabf9`  
		Last Modified: Wed, 26 Jun 2024 20:12:00 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db224983773ee9cf881e93dcf593987f2ee87b1178255e8266fe323429b76e7`  
		Last Modified: Wed, 26 Jun 2024 20:12:01 GMT  
		Size: 19.1 KB (19149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6645eaebe518cd2fed46a0a87d4bd9d24cf8b5364567aae2b6b440cd9a2c15b`  
		Last Modified: Wed, 26 Jun 2024 20:12:02 GMT  
		Size: 24.5 MB (24455770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b955476aad9361609147eb2903980710c62e380c74958526c3a10a47b7df19e`  
		Last Modified: Wed, 26 Jun 2024 20:12:02 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6324e677a3184d4e4332e2aba8d2136ba80ae35bb77ae598a09450c3f84b6da5`  
		Last Modified: Wed, 26 Jun 2024 20:12:02 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:6647e5a43413f2d03e3cb80ea9d567a4e17d0738688eb46f1f8ef1a62050f384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7828408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5e05b2214f5f5a69a236d32838947dab0c2d11ee701b53d54e73855a7e739a`

```dockerfile
```

-	Layers:
	-	`sha256:1e3463721108afcb48e47bb2500bc0fe8363b3885b400ef0748adb5c0d74f9d4`  
		Last Modified: Wed, 26 Jun 2024 20:12:00 GMT  
		Size: 7.8 MB (7765973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b5b212109e564e34372f8f929e413c4e57d5b519849659cdd0b84fbf112f9d9`  
		Last Modified: Wed, 26 Jun 2024 20:11:59 GMT  
		Size: 62.4 KB (62435 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:6cbcbbcff5ddee3eff50fff9c973007b91f2e3872a58162ae71005e1ff82af26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200770148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d82bce42b91b525da7f39634f83d9ded0e8e294c749ef42acf5c1837753148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:04:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 13 Jun 2024 02:04:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Jun 2024 02:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 02:05:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Jun 2024 02:05:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 13 Jun 2024 02:08:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Jun 2024 02:08:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Jun 2024 02:08:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 13 Jun 2024 02:08:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 13 Jun 2024 02:08:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 13 Jun 2024 02:08:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 02:08:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 02:08:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Jun 2024 02:33:08 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Jun 2024 02:33:08 GMT
ENV PHP_VERSION=8.2.20
# Thu, 13 Jun 2024 02:33:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 13 Jun 2024 02:33:09 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 13 Jun 2024 02:33:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 13 Jun 2024 02:33:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:36:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 13 Jun 2024 02:36:10 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:36:11 GMT
RUN docker-php-ext-enable sodium
# Thu, 13 Jun 2024 02:36:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Jun 2024 02:36:11 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Jun 2024 02:36:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:36:12 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 02:36:12 GMT
EXPOSE 80
# Thu, 13 Jun 2024 02:36:12 GMT
CMD ["apache2-foreground"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	version='6.6-RC1'; 	sha1='926c5c62dc58e5c10ffa2a51c508c91f6b7f0c7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Tue, 25 Jun 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be17cb314dcaf53542eada4b57866c469e138ad6901db5c3074dfaba4470199`  
		Last Modified: Thu, 13 Jun 2024 03:17:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cfe0886157848c769e894a6967d6b6b30a419d938b12e47c0096c362d346c6`  
		Last Modified: Thu, 13 Jun 2024 03:17:43 GMT  
		Size: 76.2 MB (76173122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c3730456765699b96ec3f300c53ede2aa43c16f2ba3c6caed3c19e880a4303`  
		Last Modified: Thu, 13 Jun 2024 03:17:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3bf3b8617ae0fb9b5f520230ef2e369d8f806d7ee7f5627758b187720f9670`  
		Last Modified: Thu, 13 Jun 2024 03:18:25 GMT  
		Size: 19.1 MB (19059121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90901435889008b10db748a4631079d89838d067280e97651a64a0e14590215`  
		Last Modified: Thu, 13 Jun 2024 03:18:22 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d7533e1ace3158032a17d51c1f0302e4044ef1f95674a57a7130bddcafae1`  
		Last Modified: Thu, 13 Jun 2024 03:18:22 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f6254f0af6bcdbf22265b5da7f6d51bfc37a77fa3044f0ef482e88e3d29ee`  
		Last Modified: Thu, 13 Jun 2024 03:21:52 GMT  
		Size: 12.4 MB (12430549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6a8cebea489a098d608ce0e770454e890cbc1de65e9bf0c249118305f78a1d`  
		Last Modified: Thu, 13 Jun 2024 03:21:49 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f24d67a2df89820fa7ec7801dac68ed3e0ad2ff002615df5e72c28e4449dd0`  
		Last Modified: Thu, 13 Jun 2024 03:21:51 GMT  
		Size: 9.8 MB (9822167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e62e0dc8be35440e62f5986fb6bfb32d8dfd27d4fe40b79cd73a63cdab0bc56`  
		Last Modified: Thu, 13 Jun 2024 03:21:49 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b847d5b018af5ec0e418153150af065a0740331c9297e2c8804cf432785ccef1`  
		Last Modified: Thu, 13 Jun 2024 03:21:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d10b42b11c014c201d064c30fbd209808cb65616deed1461b66fc977c7602`  
		Last Modified: Thu, 13 Jun 2024 03:21:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb6eb1d8e2d321e0b989ff131a68f7824b35314c2528f4910d310ecea09c3df`  
		Last Modified: Wed, 26 Jun 2024 20:05:03 GMT  
		Size: 25.1 MB (25078320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6113f8ef161d9c24581ebda82637a43447fe770ef96b783af0c51423362c89cb`  
		Last Modified: Wed, 26 Jun 2024 20:05:03 GMT  
		Size: 9.0 MB (8981452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bf3ff61fe1bd563e8449ee2dee315ab47920e5dc5b822f3d01af90280070e2`  
		Last Modified: Wed, 26 Jun 2024 20:05:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1184737df6e61604c30cfbd887c051e127bb2ab163b97e5a46aea5e3b75009`  
		Last Modified: Wed, 26 Jun 2024 20:05:02 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b93f5a4608bd10688b52ec45788c3ddb1ba0c27cf090a054a0921d9007c8b57`  
		Last Modified: Wed, 26 Jun 2024 20:05:04 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbba73cf4723d59a0d1a74d5edb8407749407b9cec3f9166a38ee22c24f57c02`  
		Last Modified: Wed, 26 Jun 2024 20:05:05 GMT  
		Size: 24.5 MB (24455749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d7d948fc424b69416fb9e57c7f00e1fcd1358cc61ca2bf4ba3ad4b9546a3a`  
		Last Modified: Wed, 26 Jun 2024 20:05:04 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c50bd659f7da7e0448e1bf8254fd2e32183c4d7af7a220b0388e9f34303974a`  
		Last Modified: Wed, 26 Jun 2024 20:05:05 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:d750a0b84e5e9d9bd01372186394079d9a5e7fb9aa61483a252b30d87825bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7832955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec24763b21af3ca4501dc7a5cb889a9a649137a8e75e04a4df1942dfb8f0e014`

```dockerfile
```

-	Layers:
	-	`sha256:cf41d62cbfcfa74a8f1c5d7e8f17f7e5d545c81ed1cf4cfc02ef7cd07bd04ea7`  
		Last Modified: Wed, 26 Jun 2024 20:05:02 GMT  
		Size: 7.8 MB (7770529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337477432ff3bb88b554cb4d39ed7cacec9ab9c2c0dc46711f65e97062cec31f`  
		Last Modified: Wed, 26 Jun 2024 20:05:02 GMT  
		Size: 62.4 KB (62426 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:b82de10a923d11f24d5132f2bda2a2e2f3e7e155d5db1fd81271c54dc7309739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232112820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a322144670885000e951f3db77de1befbfaa84f5cb67b9ee2af59fe1961198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 05:31:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 13 Jun 2024 05:31:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Jun 2024 05:31:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 05:31:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Jun 2024 05:31:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 13 Jun 2024 05:35:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Jun 2024 05:35:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Jun 2024 05:35:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 13 Jun 2024 05:35:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 13 Jun 2024 05:35:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 13 Jun 2024 05:35:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 05:35:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 05:35:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Jun 2024 06:03:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Jun 2024 06:03:50 GMT
ENV PHP_VERSION=8.2.20
# Thu, 13 Jun 2024 06:03:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 13 Jun 2024 06:03:50 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 13 Jun 2024 06:03:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 13 Jun 2024 06:03:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 13 Jun 2024 06:07:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 13 Jun 2024 06:07:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 13 Jun 2024 06:07:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 13 Jun 2024 06:07:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Jun 2024 06:07:13 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Jun 2024 06:07:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 13 Jun 2024 06:07:13 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 06:07:13 GMT
EXPOSE 80
# Thu, 13 Jun 2024 06:07:13 GMT
CMD ["apache2-foreground"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	version='6.6-RC1'; 	sha1='926c5c62dc58e5c10ffa2a51c508c91f6b7f0c7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Tue, 25 Jun 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82232c6a91a19c70f422ee832834541dc60f5aa79a0390d1b4f970b78cb94cfe`  
		Last Modified: Thu, 13 Jun 2024 06:54:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10870c6e7c794dbaa9b4485a880b2632188af1c206671a34d1ab297d9dc40b78`  
		Last Modified: Thu, 13 Jun 2024 06:54:15 GMT  
		Size: 98.1 MB (98132894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90df84e2a5d16a1c1192d259caccf2309cdf55df5c7c03d2528eeb67d8dacf5`  
		Last Modified: Thu, 13 Jun 2024 06:54:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41254a93ad1e54e3b0bbddc96f907af7d1c9a0820f37f9c4c73892bee1a431d`  
		Last Modified: Thu, 13 Jun 2024 06:54:55 GMT  
		Size: 20.3 MB (20322191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4977a4edd5a41c53bc46be0a1d3247790e61e1091667f264c3ea3b69c93e776`  
		Last Modified: Thu, 13 Jun 2024 06:54:51 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9f509afecd036b0f11d083b31358779d3f18feff61ea9b152912786cef1290`  
		Last Modified: Thu, 13 Jun 2024 06:54:51 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb0f82d79be40a2acdcefe2287822a729abf6fa99e58b690098cce27dc1ea57`  
		Last Modified: Thu, 13 Jun 2024 06:58:06 GMT  
		Size: 12.4 MB (12432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b79593191e6bd96bc59ff75084da42d43340c44876ab1dd95512021790d333`  
		Last Modified: Thu, 13 Jun 2024 06:58:03 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121f4ddabf3c7e341962e48c4d97f71a72056d6e0fea62f191338d86ee6cd30d`  
		Last Modified: Thu, 13 Jun 2024 06:58:05 GMT  
		Size: 11.4 MB (11415130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b000a062b835783224193f0e017c8e4756e55e9a3c1eaa6367b3b2903a753861`  
		Last Modified: Thu, 13 Jun 2024 06:58:04 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd58c0a30907f103c1761b5925dd0b7816d19c92f7dd7f094896574c3a95618b`  
		Last Modified: Thu, 13 Jun 2024 06:58:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd67eb1e013ed3cd7945793f2d6a9597ea92d1fdb86ade6f707f2695ca6a978`  
		Last Modified: Thu, 13 Jun 2024 06:58:03 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060340efbe7d1bb3e18dbd897fe77fdf7126b42c8901d30133154b8106ca5766`  
		Last Modified: Fri, 14 Jun 2024 04:56:41 GMT  
		Size: 26.2 MB (26179659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f58f3a1874255a86a14880371e49ddd3e05b9246ea6f7267298edad3166cc56`  
		Last Modified: Fri, 14 Jun 2024 04:56:41 GMT  
		Size: 10.0 MB (9965638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cd090cac0b156affe1bd496559db8f9d0cec98e94a59d3ab2f50848c46f85b`  
		Last Modified: Fri, 14 Jun 2024 04:56:40 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5671ee9dbfb75473aa5e0c016dc9dc9b21760858560fe6475690bbd2d625a263`  
		Last Modified: Fri, 14 Jun 2024 04:56:40 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6674957140da4d1ca329b574562e639a5b5651465b967b81c72d06a8d0f48e`  
		Last Modified: Fri, 14 Jun 2024 04:56:41 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab39157d0475746a9f06376377b69840dbc0268d246d8b20d76c8991756ff8`  
		Last Modified: Wed, 26 Jun 2024 19:59:03 GMT  
		Size: 24.5 MB (24455773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd207d366e919924b77f0809b003e35232bec9524f89b3234b7c4ed8073a1cf`  
		Last Modified: Wed, 26 Jun 2024 19:59:02 GMT  
		Size: 2.3 KB (2345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6902664600515c0881ad44038fd20031ecf4ee2024a28e5f91bd0e3fca046715`  
		Last Modified: Wed, 26 Jun 2024 19:59:02 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:d37596b515e70794b23cb229102e8a6ef17e2761dcfeccea9f362244efcc957e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8049878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9b7f0f72d653ee2de0c3c5b5013c1368e19c0d29f3281dbd8deb0366e94ed8`

```dockerfile
```

-	Layers:
	-	`sha256:64fc7a88dfeb9f345ae7eef2e6884a804214602b80f79bcd3ca09897c52df51f`  
		Last Modified: Wed, 26 Jun 2024 19:59:02 GMT  
		Size: 8.0 MB (7987227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc0b3e991f9a369eb4063174004a6c9a5eb2153f96ea32215743bd8badf9c225`  
		Last Modified: Wed, 26 Jun 2024 19:59:01 GMT  
		Size: 62.7 KB (62651 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-apache` - linux; 386

```console
$ docker pull wordpress@sha256:05fa43983a0032ecf44a5d598bbc09f277a0116fa5bbcad90f161e5241bfd411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239185134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87671f92b297f78c13c5addb782c5c2fc726d711fe9a25372eca58fcd5342d70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Jun 2024 19:03:11 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["bash"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 25 Jun 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Jun 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Jun 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Jun 2024 19:03:11 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_VERSION=8.2.20
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Jun 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Jun 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Jun 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 25 Jun 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
WORKDIR /var/www/html
# Tue, 25 Jun 2024 19:03:11 GMT
EXPOSE 80
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	version='6.6-RC1'; 	sha1='926c5c62dc58e5c10ffa2a51c508c91f6b7f0c7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Tue, 25 Jun 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daa048202ff5a552b6eacd27b84297ac780821f0730574f9bb61ed3a6996e20`  
		Last Modified: Tue, 02 Jul 2024 05:39:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d876e28acd3b5f3038bdfb0fb8fe720824179dc347e25e6d745ae512376fa6`  
		Last Modified: Tue, 02 Jul 2024 05:39:40 GMT  
		Size: 101.5 MB (101516977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe24ff1fc83352bac36eafb7daa5d32e7ea2232fe6fef612107fdbd1f81e7c8`  
		Last Modified: Tue, 02 Jul 2024 05:39:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087987d024f8b2145282ca5bfbb784c34ed054bbc454fc96a25334882be4e1fe`  
		Last Modified: Tue, 02 Jul 2024 05:40:06 GMT  
		Size: 20.8 MB (20843476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8723ec10434fcdc00676902f705fe56081a8fb0a774cb1a3a00894a4be83d8bf`  
		Last Modified: Tue, 02 Jul 2024 05:40:01 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f856f33b11561e423f77df5f979a60b6dd4042c3f53df3d21647a29b671248`  
		Last Modified: Tue, 02 Jul 2024 05:40:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efc136d47679de60024fa31f398a276879819cf9194d4166ce4282ecb489021`  
		Last Modified: Tue, 02 Jul 2024 05:48:35 GMT  
		Size: 12.4 MB (12429928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703728e71c128345ee40176b3c3beee54ce886806f2dddaffc3a6b098f17be24`  
		Last Modified: Tue, 02 Jul 2024 05:48:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cdb328ff7054b3308c220775a9b492611a4e6397c84d55cc71d229ce6216f1`  
		Last Modified: Tue, 02 Jul 2024 05:48:35 GMT  
		Size: 11.6 MB (11638091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bcce8afa1836f3a3737b2df3cadae79d896f5a1e476914afc88999e01fcfbb`  
		Last Modified: Tue, 02 Jul 2024 05:48:32 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1426e91a99404dc41bab8db353812443b361498871373559054f8342fc56197`  
		Last Modified: Tue, 02 Jul 2024 05:48:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70889cc9a57ffb091d6c1cadcb190715eb63797636a533e852ddc67d52b86463`  
		Last Modified: Tue, 02 Jul 2024 05:48:32 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a22938726208b09862a0158064fc7b0e4c73f7ee64b3de8b08468da2967621`  
		Last Modified: Tue, 02 Jul 2024 07:12:29 GMT  
		Size: 26.7 MB (26698894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c193d315d3c0754696ecb4eafaa4a340b0f01bb7ec239c7c1c56a65ef601f9`  
		Last Modified: Tue, 02 Jul 2024 07:12:29 GMT  
		Size: 11.4 MB (11428279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd92573a568bd8f996bd642edfea0d09901020e5a9558926e630730f5e04923`  
		Last Modified: Tue, 02 Jul 2024 07:12:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f565b3091621bf763b9a6ebb81173187347609cf0513424bdd6f21b4917c6`  
		Last Modified: Tue, 02 Jul 2024 07:12:29 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30c798f249bf6e58fdb943fb8bdd28a2062a2c6ab8bbcecefb5a57533d7c452`  
		Last Modified: Tue, 02 Jul 2024 07:12:29 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d79580f0649d4c69678740e47141546bd58271a2420fb0c3c9a358a21c3a85`  
		Last Modified: Tue, 02 Jul 2024 07:12:30 GMT  
		Size: 24.5 MB (24455762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd3efcce59d60b84c2b03e7331fc66ff176ff5d503f51c8f97882a96258fec3`  
		Last Modified: Tue, 02 Jul 2024 07:12:30 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81539890dec7d4b246d976015f115c97e25f6d743d31ef552179a967ad6f0119`  
		Last Modified: Tue, 02 Jul 2024 07:12:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:346b8d54b6fe0fddbb02cd4430b6167e8c0f4d9b6642846ab6a197d27d0b9501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4406cc3ef781b2abcc76e8b074769805293f6f3d1094dc793aa45977e5cc0c`

```dockerfile
```

-	Layers:
	-	`sha256:65624656cd12eeee912ae0079080a7d814be3ec550009d33ada9d624c2a0402f`  
		Last Modified: Tue, 02 Jul 2024 07:12:29 GMT  
		Size: 7.9 MB (7938535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c59414542614db79afa222998a6c5d738899b413fe8572aad1b33989b917f338`  
		Last Modified: Tue, 02 Jul 2024 07:12:29 GMT  
		Size: 62.1 KB (62121 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:c730ccdb1172219d40711c2a9a2a017c71f876e615c720969431118bc2ad416f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212364154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766f50b2d4c0a64bb024762cbe48aaa57ba363f6889c32e086fd902ac8bc97b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:10:34 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Thu, 13 Jun 2024 01:10:39 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 04:38:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 13 Jun 2024 04:38:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Jun 2024 04:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 04:40:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Jun 2024 04:40:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 13 Jun 2024 04:56:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Jun 2024 04:57:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Jun 2024 04:57:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 13 Jun 2024 04:58:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 13 Jun 2024 04:58:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 13 Jun 2024 04:58:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 04:58:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 04:58:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Jun 2024 07:06:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Jun 2024 07:06:17 GMT
ENV PHP_VERSION=8.2.20
# Thu, 13 Jun 2024 07:06:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 13 Jun 2024 07:06:25 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 13 Jun 2024 07:07:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 13 Jun 2024 07:07:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 13 Jun 2024 07:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 13 Jun 2024 07:22:39 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 13 Jun 2024 07:22:46 GMT
RUN docker-php-ext-enable sodium
# Thu, 13 Jun 2024 07:22:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Jun 2024 07:22:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Jun 2024 07:22:58 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 13 Jun 2024 07:23:02 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 07:23:06 GMT
EXPOSE 80
# Thu, 13 Jun 2024 07:23:10 GMT
CMD ["apache2-foreground"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	version='6.6-RC1'; 	sha1='926c5c62dc58e5c10ffa2a51c508c91f6b7f0c7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Tue, 25 Jun 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f642d228b7653cb0773a864d5251e0be042ebc63ba123f76a2ee96d99f0cd`  
		Last Modified: Thu, 13 Jun 2024 10:55:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7e656a5f67cd261b9639f19da875eb3bfb3f267ee1019dc4147fc3051f3428`  
		Last Modified: Thu, 13 Jun 2024 10:56:37 GMT  
		Size: 80.5 MB (80474931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85627c8d9ca80056d763e9a846c0a5ad6d1f4d99cbfd5394306de302d3126cf4`  
		Last Modified: Thu, 13 Jun 2024 10:55:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eae8ba09be0609884c62ca9dde575c2b43d5477c438e0c31c248995beceb8e2`  
		Last Modified: Thu, 13 Jun 2024 10:57:38 GMT  
		Size: 20.1 MB (20064190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d04f2bb3a32ce8eb7e8d8b20e7a211525218391a48d0a82d77b91c41850b0a8`  
		Last Modified: Thu, 13 Jun 2024 10:57:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b0d3a6994847794b9a5124e40369c3b1b12455ac518c8ac05b97e7f687bb71`  
		Last Modified: Thu, 13 Jun 2024 10:57:24 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19cc7437f6941e7355c7cb75db6790349e7dddc326398d1997c36057491c5ea`  
		Last Modified: Thu, 13 Jun 2024 11:03:24 GMT  
		Size: 12.2 MB (12224088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07e546badb4e71fe8343a3473047fea1b8bcccbc1752d65562f5b64ffb55a81`  
		Last Modified: Thu, 13 Jun 2024 11:03:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3acc136b2989da4a0ef3a5dceeda959a12a2c13de5fd9a4293b0e4ede50d680`  
		Last Modified: Thu, 13 Jun 2024 11:03:27 GMT  
		Size: 10.5 MB (10485775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44382d3f13621a733b450b69cdb6e4962a43d6bdba33c0822f7dbd17e565af65`  
		Last Modified: Thu, 13 Jun 2024 11:03:19 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b60c9ec31cd07f3a8384f16cb3a8bdb61cc45ef77b4a66f8768bc5afc881327`  
		Last Modified: Thu, 13 Jun 2024 11:03:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b56aa7ff0900e0f48423ac0016fbe9166bf27ee56c2c9f795488be88aaaa2d2`  
		Last Modified: Thu, 13 Jun 2024 11:03:19 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d898afc132e318df047990147cbfe03eaac54660b5d682e5a00e5b9c413d24c6`  
		Last Modified: Wed, 26 Jun 2024 20:27:41 GMT  
		Size: 26.0 MB (26021665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a552fea71c64c0cc22e533a9f75e65e4c7bde8bfa8717d168a66261ce0301e4a`  
		Last Modified: Wed, 26 Jun 2024 20:27:40 GMT  
		Size: 9.5 MB (9464456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d422eb6d68de112547e13cca92782e5a62ec3a80ac7f194f7b50ff8a115c1d9f`  
		Last Modified: Wed, 26 Jun 2024 20:27:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540d8b19cf40055ce0da7f5e86b76c600a79b09bed7a231c6e72d83358a31172`  
		Last Modified: Wed, 26 Jun 2024 20:27:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6b41775d121a61021aade82d682147db43929e75858d63ecdb55bfb7b43e22`  
		Last Modified: Wed, 26 Jun 2024 20:27:39 GMT  
		Size: 19.2 KB (19164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4119b29a15cfb4efd6e551df2ddb3a7d1db010c926eb03533cae5e20812f26a3`  
		Last Modified: Wed, 26 Jun 2024 20:27:42 GMT  
		Size: 24.5 MB (24455740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d05b1e17651e7e0218954dbf25b81802f8fb24f10112eadfc350debb4ed01a5`  
		Last Modified: Wed, 26 Jun 2024 20:27:41 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd948f49c8f213e90dc762a0f0da3ee730d348b0b272065fbd926cf63f99d344`  
		Last Modified: Wed, 26 Jun 2024 20:27:41 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:a383244c47be3d5fb8062bbb72c05249ad53e032a314f159b7fc00bc0caf189e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 KB (62165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da50e4f66ca5bcbb359d0694efd3d0b71a7888b2b8a972aa1f65995ebaf96dc`

```dockerfile
```

-	Layers:
	-	`sha256:822376f6af391b7ed0ba235777e428faec5fb76ec805cc14a62ec40b5cc9a971`  
		Last Modified: Wed, 26 Jun 2024 20:27:38 GMT  
		Size: 62.2 KB (62165 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:6597e51dc31eb8d3eb01d1e069820b25b0c31ae1f5f8bda70a42583e3c7c504c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245309206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbefd0226bf40535b0d72c7832760b513dfa0b5681c50f80e76e285660721b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:04 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Thu, 13 Jun 2024 01:17:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:35:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 13 Jun 2024 02:35:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Jun 2024 02:36:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 02:36:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Jun 2024 02:36:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 13 Jun 2024 02:39:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Jun 2024 02:39:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Jun 2024 02:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 13 Jun 2024 02:39:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 13 Jun 2024 02:39:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 13 Jun 2024 02:39:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 02:39:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 02:39:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Jun 2024 03:05:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 13 Jun 2024 03:05:20 GMT
ENV PHP_VERSION=8.2.20
# Thu, 13 Jun 2024 03:05:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 13 Jun 2024 03:05:20 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 13 Jun 2024 03:05:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 13 Jun 2024 03:05:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 13 Jun 2024 03:08:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 13 Jun 2024 03:08:28 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 13 Jun 2024 03:08:29 GMT
RUN docker-php-ext-enable sodium
# Thu, 13 Jun 2024 03:08:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Jun 2024 03:08:30 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Jun 2024 03:08:30 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 13 Jun 2024 03:08:31 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 03:08:31 GMT
EXPOSE 80
# Thu, 13 Jun 2024 03:08:32 GMT
CMD ["apache2-foreground"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	version='6.6-RC1'; 	sha1='926c5c62dc58e5c10ffa2a51c508c91f6b7f0c7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Tue, 25 Jun 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c59947c2cef9cbf6f5bef5de64e7f960ccdaaed44404fae2a88b64156ca742b`  
		Last Modified: Thu, 13 Jun 2024 03:52:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c47d17b3441713a837f7a04d45fd3e7ff79e4b0ca8c528a3688697f94ea56f0`  
		Last Modified: Thu, 13 Jun 2024 03:52:18 GMT  
		Size: 103.3 MB (103317029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52959e505540a7098f57c8712abd28a8b810af8a655f983f693b19fa1d1efc94`  
		Last Modified: Thu, 13 Jun 2024 03:52:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aed0677b85a68c4b6b29688f759799a1ff82511ac0e242010f3e61333c6a965`  
		Last Modified: Thu, 13 Jun 2024 03:53:00 GMT  
		Size: 21.5 MB (21512870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182c049972fd31a91ebf4c749e3107dadb2d99350df038b4f4fef67a0096ced2`  
		Last Modified: Thu, 13 Jun 2024 03:52:55 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eee5b5c111fa3dee2fcdba623563e99afaa979aa7e3d8538f66309019c1348`  
		Last Modified: Thu, 13 Jun 2024 03:52:55 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff6c0912d5cff80fd8e2cb0e4f81b662256c6aab2218f2fef327f6ef8244f34`  
		Last Modified: Thu, 13 Jun 2024 03:56:24 GMT  
		Size: 12.4 MB (12432119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66a7c4ba29ff7fe18a3bb5c3688a06c495adc86208dc68ad87f98fa645d5ec`  
		Last Modified: Thu, 13 Jun 2024 03:56:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5383b3b76d7fe2bcfb71ad1f04fbbc61d76a1bdbb65c21f9c260152d2ecba93`  
		Last Modified: Thu, 13 Jun 2024 03:56:24 GMT  
		Size: 11.8 MB (11820254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a8a2781ee630c3ce71a4ef39077d32aad28f60c557ccaac3906d07be81ba4a`  
		Last Modified: Thu, 13 Jun 2024 03:56:21 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d44f86d0af98c6897363ee52367df5e55fb03692377babe3555c8367b0fec0`  
		Last Modified: Thu, 13 Jun 2024 03:56:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed565d989b82ef7c69dd8c28073cc99d94abc014d76c97b1c4068e8d0b268cc`  
		Last Modified: Thu, 13 Jun 2024 03:56:21 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d31a3e61f38f753660b1494d24eed1ab7c57a14cf5eed2dd81a611b8241438`  
		Last Modified: Fri, 14 Jun 2024 06:38:25 GMT  
		Size: 27.3 MB (27347176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3977375ebf5d85b18d337e41a91dff60d3f376a7d75f36d6cc34331f345203c`  
		Last Modified: Fri, 14 Jun 2024 06:38:25 GMT  
		Size: 11.3 MB (11253336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c824b8465454ea5a5ef67aa0d2bbdf35c5c5f31e6f9d856955ef361a8ab7e2e`  
		Last Modified: Fri, 14 Jun 2024 06:38:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6480dbeac59ec7cee86e9360953c2b516ff7b1ccae90fa7360169cfc108d53b`  
		Last Modified: Fri, 14 Jun 2024 06:38:24 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efae341a4dd2dab8c92d2ec22e0f4bb9e5940747c71619ca9fdd837ab141a22`  
		Last Modified: Fri, 14 Jun 2024 06:38:25 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4121ba1869f562821538be4c5ed1de58def717d6b1368e5831ab7d550d2c6c`  
		Last Modified: Wed, 26 Jun 2024 20:04:46 GMT  
		Size: 24.5 MB (24455775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277833a12840a5dcc5381ca4b0a0a42cd384164db2bfeff3bb470787463fafa9`  
		Last Modified: Wed, 26 Jun 2024 20:04:44 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a828f4311ba2271f23981a9591f615d740e20d49862bfaafa055fb8dc74f0a0`  
		Last Modified: Wed, 26 Jun 2024 20:04:44 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:f79b810ca18b020e21227de858b0e19cdcbd32c870baa22f5a157987414bba47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7999574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989c0b9668c947be8eeb8df57fd1d0c466fe58e082da32285c984375d2d2fa17`

```dockerfile
```

-	Layers:
	-	`sha256:c68238b8b8744bcde8523f8199cdd838bdfb6560e031c023071c8a077b790e92`  
		Last Modified: Wed, 26 Jun 2024 20:04:44 GMT  
		Size: 7.9 MB (7937234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ce21db253cb63161d71563f27e143a58da8455291060fa2293ee027271d203`  
		Last Modified: Wed, 26 Jun 2024 20:04:44 GMT  
		Size: 62.3 KB (62340 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:260b61ae4b1d54481743c75c382106f0b74a4e64b806719696357bff7e3adf09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211334928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72930e02f34228fc88d2f54d9f41e265bb00ba8643b4fab2bec42d78a108fbf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Jun 2024 19:03:11 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["bash"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 25 Jun 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Jun 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Jun 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Jun 2024 19:03:11 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_VERSION=8.2.20
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Tue, 25 Jun 2024 19:03:11 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Jun 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Jun 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Jun 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 25 Jun 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 25 Jun 2024 19:03:11 GMT
WORKDIR /var/www/html
# Tue, 25 Jun 2024 19:03:11 GMT
EXPOSE 80
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
RUN set -eux; 	version='6.6-RC1'; 	sha1='926c5c62dc58e5c10ffa2a51c508c91f6b7f0c7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Tue, 25 Jun 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Jun 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jun 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9251ecd224e15bee1af8e5d8ed06b4583727d21c25571b0841308fa40637020`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de732a471a32b9581046aa3735f5891fa36c8dc024c7c7a007087dd77b0bd3a`  
		Last Modified: Tue, 02 Jul 2024 03:05:16 GMT  
		Size: 80.8 MB (80817736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f9b6de1c71adae007cab6934b2b7dfe2155be5d6b7fecfea770f4dca1aa159`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac393ffa46cdbdd309e76835caefc39b9a5f28208a5117719850422e50cd1830`  
		Last Modified: Tue, 02 Jul 2024 03:05:34 GMT  
		Size: 20.1 MB (20101995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b9ac198003d25e1ae488b290fbd759f674d87fea5692596dc85177b0ad0014`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe10d7b17a1f1937efded756698b3791c41a781a95ad1f5b3436f29993e08d6`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bacd687d0c0db8c41aeca68d0ef1f6f2f7fbe6dd5e0c6619d0311f5feafc96e`  
		Last Modified: Tue, 02 Jul 2024 03:11:36 GMT  
		Size: 12.4 MB (12429051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fe3a7b26d8013230e7aff3ca621435911c92395d9813a6c67a440f98788836`  
		Last Modified: Tue, 02 Jul 2024 03:11:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f7ef65841bc9b9a5b5312432a3b9aa69197d0b4911604e68fbecd5c60956b`  
		Last Modified: Tue, 02 Jul 2024 03:11:36 GMT  
		Size: 10.6 MB (10638401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81f9dde78217abdaa6805e3733cba662ab36eccf2627e5f0e4b1e97c1fb79c4`  
		Last Modified: Tue, 02 Jul 2024 03:11:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0c1c7da62719ed5a94c7e7f88a37eb883db877d7679e8724bf06e7864e8b02`  
		Last Modified: Tue, 02 Jul 2024 03:11:34 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc89148e465aae7bd41de070a6a2baaaa8577aa1c3c998e7948fc3af6cd60d35`  
		Last Modified: Tue, 02 Jul 2024 03:11:34 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680e3569e7ddefbe8f75c425ed21d6b8eb095a12922ffa9f6a4370b78e1af4ad`  
		Last Modified: Tue, 02 Jul 2024 21:06:33 GMT  
		Size: 25.9 MB (25899140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7aec1adce47d0a7aabfc4d9bc1596cfec893477166be51bcef85c18c266cbe`  
		Last Modified: Tue, 02 Jul 2024 21:06:33 GMT  
		Size: 9.5 MB (9473312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4889d3fee753500f04cdf18163ebafaabd1c539d2e2ddf29bff885daa4b9fe1c`  
		Last Modified: Tue, 02 Jul 2024 21:06:33 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543c46aa6ec6f74c6fa5706e26dad34b323a24d3b14ca65808fd3774b380e08b`  
		Last Modified: Tue, 02 Jul 2024 21:06:33 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8129bbe8ead6fdead7183187f641f2cd8d9d17b12fd2e94a7d2b7f6048edab45`  
		Last Modified: Tue, 02 Jul 2024 21:06:34 GMT  
		Size: 19.2 KB (19155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e64d9121808b2b245a9dfe84f74e276fb6104234fdc2fb9cdaa4be0df6d31`  
		Last Modified: Tue, 02 Jul 2024 21:14:34 GMT  
		Size: 24.5 MB (24455769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e768b152d48067df9c928c2dd3e9923091d2fa02c5991b5a636c6ad9458553a`  
		Last Modified: Tue, 02 Jul 2024 21:14:34 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9f5beeb93275832a21931c64d45af31e38b44c16d62c32b6e3444dbbc65a39`  
		Last Modified: Tue, 02 Jul 2024 21:14:34 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:3dc3684c6fba6eeebdb05a23f32f4cb74301a89afda9b2cb203e03f8f4d575ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7852585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9af0777500a3c93b0ac72ad741e7988770b6aea4c74bffc00b1462ef2def02`

```dockerfile
```

-	Layers:
	-	`sha256:d36866d7cb19d556fd9a03b60ebba003e5e5d0d5a0f5b97b3274d64756f7d646`  
		Last Modified: Tue, 02 Jul 2024 21:14:34 GMT  
		Size: 7.8 MB (7790381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3a1e6276f189869f09a2a1ab6f533ff3b8ab2969aa0ae15027dc90e884440eb`  
		Last Modified: Tue, 02 Jul 2024 21:14:33 GMT  
		Size: 62.2 KB (62204 bytes)  
		MIME: application/vnd.in-toto+json
