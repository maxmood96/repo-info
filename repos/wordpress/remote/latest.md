## `wordpress:latest`

```console
$ docker pull wordpress@sha256:022c7d4c14b8af7ddd7c1a7c3b8ea633d2db42219913eb1e79ef89484ae26375
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

### `wordpress:latest` - linux; amd64

```console
$ docker pull wordpress@sha256:5a66aeadeeaa9f063daeea0404ce183c7643763a37ec6a0f4260eb5420b24497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240815159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d653f5f8a60226be8830c1467fd39e67fdcc4882aeb224ff30fffdb225bf8fb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 02:30:59 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 02:30:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 02:30:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_VERSION=8.2.18
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 02:30:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 02:30:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	version='6.5.2'; 	sha1='b70701b5426891ca1f8ff9b3cd96653e2b60d7e9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 02:30:59 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:cfeec87621aeb5b3bf8907398acc95a5e9b85a5f3faa6a68e0640e7d6653f850`  
		Last Modified: Wed, 24 Apr 2024 10:13:58 GMT  
		Size: 20.3 MB (20329716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1badcd002c0a773002eaf87724b5a303e17873ae752e7e69dfd6b22c05a7dea`  
		Last Modified: Wed, 24 Apr 2024 10:13:56 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d463a60cb62b1b64dd43c0defef018c6ab557e474c029d17824cc9d1b5d103`  
		Last Modified: Wed, 24 Apr 2024 10:13:55 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ad50b335f5e9274621b9982b7f1ddacfbac8e0dbd961b7e0a69d1300057737`  
		Last Modified: Wed, 24 Apr 2024 10:17:14 GMT  
		Size: 12.4 MB (12423961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c64971444ad785bf5c2d171c0171998b098d4be35dfbfae2afd745b175f35c`  
		Last Modified: Wed, 24 Apr 2024 10:17:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7d8962b7e146fccfa8aaca820ce5d5f23f5fb75549fc25406d319959050182`  
		Last Modified: Wed, 24 Apr 2024 10:17:14 GMT  
		Size: 11.4 MB (11406758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e620d8fafd56bafa939a722214a1558f921012bd8e1933d18a7db080929926c7`  
		Last Modified: Wed, 24 Apr 2024 10:17:12 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038239aa3e19625ee0a3db07cb151f551e4600aa3b269ffecde0e1841d7c1bb`  
		Last Modified: Wed, 24 Apr 2024 10:17:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99eaff68704dc9c5ed85b9c1ad7cabb97f8a4da932d033b50ae7f9f507818f`  
		Last Modified: Wed, 24 Apr 2024 10:17:12 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ef72901a7f4dce272b9ce87827ee990348cb6ead81b0f4d3c65785d80aa4e`  
		Last Modified: Wed, 24 Apr 2024 10:57:55 GMT  
		Size: 26.3 MB (26256767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7acd866c76c9ba95245fceffd188f17bdf66f189a5644b97f8539c1869f956f`  
		Last Modified: Wed, 24 Apr 2024 10:57:55 GMT  
		Size: 12.3 MB (12334204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666e528f269a1c56b4f5b8702ab8451bfb2f0d5756e96e864eb8059a818a0e9e`  
		Last Modified: Wed, 24 Apr 2024 10:57:54 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0312bea7a4516d83c4066201163ee992a4bbb5f5739fe2d6514af067942e365b`  
		Last Modified: Wed, 24 Apr 2024 10:57:55 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8477b729f124bee78d11f84a1474f2197bf86f0d37a9034141b41c584385b36b`  
		Last Modified: Wed, 24 Apr 2024 10:57:54 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e06c94867eb579ecf22c153d7e64fe6ba94073786c4690dd7d1017c73a29d3`  
		Last Modified: Wed, 24 Apr 2024 10:57:56 GMT  
		Size: 24.5 MB (24526010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baa1fda38e738f98cfcf48517bb17e4b445cc85a3762479c9ed61c94fdb5ce3`  
		Last Modified: Wed, 24 Apr 2024 10:57:56 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fe2989bce13bb759f3e5018141cafbec17063c66de28592dcb0b0f17dedcc4`  
		Last Modified: Wed, 24 Apr 2024 10:57:56 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:latest` - unknown; unknown

```console
$ docker pull wordpress@sha256:1e2d76b439c5fdd3ef6100ab5e37e5b5ba5115b1341514cf7937f32320e7dcfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8023208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb586ab2cd20df30edc8c2d01beb0e02c8b89ab53fc15c333acab86b373232e`

```dockerfile
```

-	Layers:
	-	`sha256:285462f5da1d7c39f63d3a8b804824f24b34ad36f435913e23bd2a15454d7009`  
		Last Modified: Wed, 24 Apr 2024 10:57:55 GMT  
		Size: 8.0 MB (7959086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe7f86f0abdd74d8441de8520387fb0f04fe2da1375900409180975c9385d24`  
		Last Modified: Wed, 24 Apr 2024 10:57:54 GMT  
		Size: 64.1 KB (64122 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:latest` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:28cbd98315c82241e64912ff3e95f4d41e0046a0e7142254302a33630e056f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.6 MB (211555163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e96195d0002adb7f9146e7a739bb69f1ebfcf2cbc70b2aa8a8ece9a517aa922`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 02:30:59 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 02:30:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 02:30:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_VERSION=8.2.18
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 02:30:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 02:30:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	version='6.5.2'; 	sha1='b70701b5426891ca1f8ff9b3cd96653e2b60d7e9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 02:30:59 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:d36427a405cf177054e947e9baeef56feb7b30b66554c246dcccef90034e5da1`  
		Last Modified: Wed, 24 Apr 2024 06:55:16 GMT  
		Size: 19.6 MB (19622260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db7c5fc4b717b1579e929d568bd1d9b410ef5222d871df15efa9f166014bb50`  
		Last Modified: Wed, 24 Apr 2024 06:55:13 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3465262ec0d939d77c76a7bd4c02dc1d98b254c2540b9ea1adbeb7f783d4079f`  
		Last Modified: Wed, 24 Apr 2024 06:55:13 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1fdfdc14e83b5e545bdc91096101a7c8c7166adfa508e376f1810d1f5eeba4`  
		Last Modified: Wed, 24 Apr 2024 06:58:31 GMT  
		Size: 12.4 MB (12422250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f33e220e67a6d7fa4ae9b87ca1604ed99156c989fbb67746bdf39a6b11070f`  
		Last Modified: Wed, 24 Apr 2024 06:58:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6035006342f0f9e9b50e244ac54287466d95e8fb3c7e2953ffb1d2fcf24e1d`  
		Last Modified: Wed, 24 Apr 2024 06:58:30 GMT  
		Size: 10.4 MB (10389981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e01ebe6f0f6d85b3b6e7e08ede0f0f325354ce5f50fcf149d86f490e32e0fd`  
		Last Modified: Wed, 24 Apr 2024 06:58:28 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab86caeaf4676b04e623a882ba79c082dcf3b3e195c9e860e0d2beb67c1c19f9`  
		Last Modified: Wed, 24 Apr 2024 06:58:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87804eae9b7254929229465a02cef3e98fed1ac8d5fce328fa57aa7fbbeb8782`  
		Last Modified: Wed, 24 Apr 2024 06:58:28 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c25c1a34b2fd6a478f23214ea27b6bab841b6c306c80919185ce3496735875e`  
		Last Modified: Thu, 25 Apr 2024 01:05:30 GMT  
		Size: 25.7 MB (25707709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8eca3931c85fd84e7bc546adb508db740986772f78285edc0a60d22c2760f7`  
		Last Modified: Thu, 25 Apr 2024 01:05:30 GMT  
		Size: 9.9 MB (9944941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f6121918ba4925d81a74a486dab53586922bfff7facb23032596418a4702b`  
		Last Modified: Thu, 25 Apr 2024 01:05:28 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2554ae68a4c5384950fae8e6daa2a2b892548fb5298e18cf282a7b1e343115`  
		Last Modified: Thu, 25 Apr 2024 01:05:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8397ca46c49a8f2e12da5f2b1b7e170bd049350ae04a11649a2352841b4d911d`  
		Last Modified: Thu, 25 Apr 2024 01:05:30 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5260177ff138c3aaa58a0d82522d54d34f063d43f171d2b6b2ce8c3297c227`  
		Last Modified: Thu, 25 Apr 2024 01:05:31 GMT  
		Size: 24.5 MB (24526009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a6b390eeb0e15a0774ff308b3539643bc5fc03d8ea49060e337ab6c1ec5096`  
		Last Modified: Thu, 25 Apr 2024 01:05:31 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b4450b2bb716be40cd9d952a146a7dac8aa095981e1ba67f7bf4324634c3d6`  
		Last Modified: Thu, 25 Apr 2024 01:05:31 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:latest` - unknown; unknown

```console
$ docker pull wordpress@sha256:a19b39f674308305f060c8208e3d9b9081de052a62e67e41879450237ec3d96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7828934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a462fa78058c2483bb9adfbc1f92f7adf8fcf671e0582a58db6873af6f3c4`

```dockerfile
```

-	Layers:
	-	`sha256:3f29a8eb6a9abd6756de2d64503454ea0cb6e1ef3cdda13b2b0f01ea45a629d4`  
		Last Modified: Thu, 25 Apr 2024 01:05:29 GMT  
		Size: 7.8 MB (7766706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c67fbc7f69f3bccab1c776dbd4bb00f85f8829eab617e8f2a4d9eda9fbe30c`  
		Last Modified: Thu, 25 Apr 2024 01:05:28 GMT  
		Size: 62.2 KB (62228 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:latest` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:dd5cba1439b31fe20cb99658b5dbc5b7efe0bc73fd24b08f0e76ba46669341fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200823390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b634e0fcd4a6340a551b5c55b3695344c2a0f11ee243e5b2a023f2d87793f76c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 02:30:59 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 02:30:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 02:30:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_VERSION=8.2.18
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 02:30:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 02:30:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	version='6.5.2'; 	sha1='b70701b5426891ca1f8ff9b3cd96653e2b60d7e9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 02:30:59 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:bd0e892a65683abb56ae3c750f0cc4d6e9bd9a4e3f597041edffe56d8f7e9df7`  
		Last Modified: Wed, 24 Apr 2024 08:24:58 GMT  
		Size: 19.1 MB (19059142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f908c1d59ecca5b5dbdc422e2d1a2aaa4511430ac6cddb0bb15ad42960c8a4`  
		Last Modified: Wed, 24 Apr 2024 08:24:54 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50ac67d48d9bf873d068e3de7e967a93e4b35d3d8d91ccf92cb1211eed0aa28`  
		Last Modified: Wed, 24 Apr 2024 08:24:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115becd5f8d7c4f2ca90e0fbd9db9bb12cff1cac0770fbc242cf17c28510655e`  
		Last Modified: Wed, 24 Apr 2024 08:28:26 GMT  
		Size: 12.4 MB (12422190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04fc4d7c0335f3691e82cdbf2f9e9c4de1e1542360b63052b6d43d6c739f04`  
		Last Modified: Wed, 24 Apr 2024 08:28:23 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a17e70abb76c96eee4ce55c754ca9557473fc0a391866e5b6f49d6aed8e877`  
		Last Modified: Wed, 24 Apr 2024 08:28:26 GMT  
		Size: 9.8 MB (9820768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2f02db06698adfad92c26760a82abe582c588bc20a1c6ec6c75bfc52323a77`  
		Last Modified: Wed, 24 Apr 2024 08:28:23 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840da0018b1c4c4726f799b0d1596dc93cfb8dc7c0597d7c58293554a1a9b07e`  
		Last Modified: Wed, 24 Apr 2024 08:28:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8464ae52b9496079236631e90486158cbb7d58fd6a83df2f66336bf463b477c`  
		Last Modified: Wed, 24 Apr 2024 08:28:23 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16441b6f41aa79ab57d29fa759e927242672c30386e51ccefc8ef9384b0db19f`  
		Last Modified: Thu, 25 Apr 2024 11:51:05 GMT  
		Size: 25.1 MB (25079007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483e543fc83e5e67a8948986d1624122c0a8f3819f4863b7018471aea9081e4f`  
		Last Modified: Thu, 25 Apr 2024 11:51:04 GMT  
		Size: 9.0 MB (8973424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0e7fd113e6c2ea946be5c1df850767b0dd80dfdf41c326fb48e772b57c7324`  
		Last Modified: Thu, 25 Apr 2024 11:51:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bd7cbf656e8848aa33e384de101be623705aa8af8a0d5433cff06a6500eaf8`  
		Last Modified: Thu, 25 Apr 2024 11:51:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfadb71df9d1fc54155f84e443a101936bb07f6b56d000cdccd0ca626dd56890`  
		Last Modified: Thu, 25 Apr 2024 11:51:05 GMT  
		Size: 19.1 KB (19147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df8a6bdaadf7110c8a21ba1fe8c2c9e1e2a7b7257ade1cd6a7a9cb72df12291`  
		Last Modified: Thu, 25 Apr 2024 11:51:06 GMT  
		Size: 24.5 MB (24526012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4485cdf1a93aca326d2ff478cb415dc9f68c29d65c4004d05dbdd620be24c9`  
		Last Modified: Thu, 25 Apr 2024 11:51:05 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d42467dbeb7fc3bc5fc20d4c8abd7d202012598afe7945cc21cb98e5bf6472`  
		Last Modified: Thu, 25 Apr 2024 11:51:05 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:latest` - unknown; unknown

```console
$ docker pull wordpress@sha256:5616b3ac2cb63af82e2f07ab2057e14a5c92e2890dcb2ffc25fcbf1b94e62473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7833481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5cddb396820b5b2710c946f20fe6ce64f974c6727fc8eea3b966506e6f4aa8`

```dockerfile
```

-	Layers:
	-	`sha256:16f1e34565e4d9923286a8e9f8ba69b3d5997c85374bd649bf6b9cae3a04d386`  
		Last Modified: Thu, 25 Apr 2024 11:51:04 GMT  
		Size: 7.8 MB (7771262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d156037c02c0406d1935b4ee9ff78aa6975a4149c4aee29bfd9b242d8e244f4`  
		Last Modified: Thu, 25 Apr 2024 11:51:03 GMT  
		Size: 62.2 KB (62219 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:latest` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:273e24a39e4401c8e99051ab970d8879175be9be69595c81f627fa46c4fbeae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232170570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aad928bd1ca5324278488a375d3b914fbd7bf8dae84ef7e3b060b0df6d8edf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 02:30:59 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 02:30:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 02:30:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_VERSION=8.2.18
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 02:30:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 02:30:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	version='6.5.2'; 	sha1='b70701b5426891ca1f8ff9b3cd96653e2b60d7e9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 02:30:59 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4246bb70e866bd7dd3dccad886145a828fb1a1323f17ef26ec181465dbcb0b28`  
		Last Modified: Wed, 24 Apr 2024 06:35:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9cbc94d9e79c445b63152194f2f71247fc73f539ba2b78046fd04c59ff44b`  
		Last Modified: Wed, 24 Apr 2024 06:35:43 GMT  
		Size: 98.1 MB (98132015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760f776f4854c09ee785a8e7e0b102fbcd2483de52db872f8a92ce21e43cac04`  
		Last Modified: Wed, 24 Apr 2024 06:35:31 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a0ec8ef6bc2cde02f58dc81eeee21fde397e0ad51d4ab138f21b67b77c89c4`  
		Last Modified: Wed, 24 Apr 2024 06:36:24 GMT  
		Size: 20.3 MB (20322298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d170b72693bbaede3e95c7b3f669df38b31b21d3d1a25458e4153823999ceb1`  
		Last Modified: Wed, 24 Apr 2024 06:36:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dda424ab92b122f202ae6b960aa32dd30bc2da243480399c10b1bb870e3342`  
		Last Modified: Wed, 24 Apr 2024 06:36:21 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c34f6d7a5a9954f2ddc871335318219462465c612889fd4a16ef3df5738c5e`  
		Last Modified: Wed, 24 Apr 2024 06:39:31 GMT  
		Size: 12.4 MB (12423551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f575ea9fba7b900b250d4b0c8b747eedf9ebb115b0a384149d59d92aa7c9de`  
		Last Modified: Wed, 24 Apr 2024 06:39:28 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbedf94277fe1a55fc60627e000d28810d98db1a62910d8c8c3105d2dcb29462`  
		Last Modified: Wed, 24 Apr 2024 06:39:30 GMT  
		Size: 11.4 MB (11413986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295c83d53de584c1886aeae781204ee0999c61653e5810a131e62c0ac8ea1a54`  
		Last Modified: Wed, 24 Apr 2024 06:39:28 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36945fedbfdc0e332d181a834e2dbcec086ea3e2e3282ccdb71ce0480026ef62`  
		Last Modified: Wed, 24 Apr 2024 06:39:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63c608cba6fd158ba03c04ff24c3c40789770e0216cb6454a76d4f66a96f179`  
		Last Modified: Wed, 24 Apr 2024 06:39:28 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a045d1c7969fed7e981b4818b42feb0711c9ee9526b99e23fb00be96dc83324b`  
		Last Modified: Fri, 26 Apr 2024 06:29:50 GMT  
		Size: 26.2 MB (26178707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b77ccce484c36b0ca8996e08c620d1b92ffa0ab81f08c499c7972dda4e28f`  
		Last Modified: Fri, 26 Apr 2024 06:29:49 GMT  
		Size: 10.0 MB (9964498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a818f316f1204d65fc1244d8fcc4ea7dcd59966ff2d9f72de60bbda98303f9f`  
		Last Modified: Fri, 26 Apr 2024 06:29:48 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf66fdfeb4fa01031a31f32b12c4cd7bbbd8f932f9c6e39e6b0e34b90db21f7`  
		Last Modified: Fri, 26 Apr 2024 06:29:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc4cab546c7cd2695a3bb3ee160eae50db94acf5ac0640bd99474f4ddafd148`  
		Last Modified: Fri, 26 Apr 2024 06:29:50 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8408aa10561387128b43338abb8db583c514f56b421cf48d2d7be9d08f3dbc42`  
		Last Modified: Fri, 26 Apr 2024 06:29:51 GMT  
		Size: 24.5 MB (24526001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175008a68d2f97e0db799a2a3ecdc15c08d035317084fd1895e7a264bc65df84`  
		Last Modified: Fri, 26 Apr 2024 06:29:50 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8190eb03d8dd3505c047f57bbd708a36ad661171dd2724183c4a547b23eaca`  
		Last Modified: Fri, 26 Apr 2024 06:29:51 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:latest` - unknown; unknown

```console
$ docker pull wordpress@sha256:0eef6162afcfe4be19244e1dc280daeaba7e1ef866ccb2c41f30df01469c0dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8049826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8baa389aa2508899451c9a0f55d410c71b2de63b1329cc22ee0bb6c8e2ce1784`

```dockerfile
```

-	Layers:
	-	`sha256:a5855714cc4f57a65f7f4089ff121fb75e7145247ea4ed87599d90a2f678b0c1`  
		Last Modified: Fri, 26 Apr 2024 06:29:49 GMT  
		Size: 8.0 MB (7987795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845b35a800895402954edd539fd51d07836c8661bae482f27bb3f5d29ad5cfb8`  
		Last Modified: Fri, 26 Apr 2024 06:29:49 GMT  
		Size: 62.0 KB (62031 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:latest` - linux; 386

```console
$ docker pull wordpress@sha256:18a1275285aab3a96cb24e68e896729fe3d0f219a55d191ce35558879089b50a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239271340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cdecc336c9661886407daac66a3b5946c29efec308b5272b538fbab2a2980c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 02:30:59 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 02:30:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 02:30:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_VERSION=8.2.18
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 02:30:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 02:30:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	version='6.5.2'; 	sha1='b70701b5426891ca1f8ff9b3cd96653e2b60d7e9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 02:30:59 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:0fa961eb09ca3c9b99fc06b865a7a6fd8608a50684db856f6da97733cecb9c0e`  
		Last Modified: Wed, 24 Apr 2024 07:37:11 GMT  
		Size: 20.8 MB (20844719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8105c623b5e86209dc2d11e7aff7ae42685ea6efbd232f64750a7d2d42e817`  
		Last Modified: Wed, 24 Apr 2024 07:37:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c7989bc9f4db0aeee6f780bdfd90643adebf6585c505c8ba1cb7fdee8b4b7b`  
		Last Modified: Wed, 24 Apr 2024 07:37:06 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae78e6e41bc21efdc88de91719fac55396470327c7218631dfb23aaeb6b65cb`  
		Last Modified: Wed, 24 Apr 2024 07:41:09 GMT  
		Size: 12.4 MB (12423087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6415972c81c1aeec0002afcc286c0fed7891f7462f526e47f1938b437d9bca`  
		Last Modified: Wed, 24 Apr 2024 07:41:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2debc20cfbc1ff1202267263ed56653d4a8873b0fa3fc21f0baf4af6cdd5f5da`  
		Last Modified: Wed, 24 Apr 2024 07:41:09 GMT  
		Size: 11.6 MB (11640594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c3d8746d1daa18ba21dbcd7a40e9b77af0cc5e64f1fbcd69c6e9098d81ea73`  
		Last Modified: Wed, 24 Apr 2024 07:41:06 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128a1d44d4a302f06357ed62cb5bea1ef7428a4163d88f15721c73f12ee7df42`  
		Last Modified: Wed, 24 Apr 2024 07:41:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8200a279684d72799021e24a64aeecac9b21f368dac5b3591d3861cc16692f14`  
		Last Modified: Wed, 24 Apr 2024 07:41:06 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539928a5024e5964b1caff8a1d0a64f2eb4afc37a68884f9f7f0222c7e8a9584`  
		Last Modified: Wed, 24 Apr 2024 08:59:07 GMT  
		Size: 26.7 MB (26702780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c7a86ccab71cd0cc55ab9a4520268cfc9dffb25df4729fa83a14b655f777a0`  
		Last Modified: Wed, 24 Apr 2024 08:59:07 GMT  
		Size: 11.4 MB (11419297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2520e0ded251ac7155567e473490534dd3a3d7ce9439986b529533f217e68fa0`  
		Last Modified: Wed, 24 Apr 2024 08:59:06 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c426a734865285064f179ca6cc6a800df03add9786ee163fdd2d6d0b7a439be4`  
		Last Modified: Wed, 24 Apr 2024 08:59:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb97fc4b968fb881c14ceeb682e13fe76657651de868a2db67c3ab745a5aa9b`  
		Last Modified: Wed, 24 Apr 2024 08:59:07 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9e2a7acc2b36eec04e77298c319563c25256b7c72e46ea89a515fc8506f180`  
		Last Modified: Wed, 24 Apr 2024 08:59:08 GMT  
		Size: 24.5 MB (24526017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19faec5557044e898fecfcb0072d1d9ef54a51053a1340360438cbb2609bb79`  
		Last Modified: Wed, 24 Apr 2024 08:59:08 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e402df8532ce4ea2b2de4403af7083bfd91b8a43e9682e8e007ce89f657bbb`  
		Last Modified: Wed, 24 Apr 2024 08:59:08 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:latest` - unknown; unknown

```console
$ docker pull wordpress@sha256:1a4a08d45ff36c5fad70108b2d26aca8b1e4c6ab60eb041cb3cef7e30951c29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8003195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c9c2bef13d2424f03d43cc3731755727c6864248454a3ca6b283b90d3dada1`

```dockerfile
```

-	Layers:
	-	`sha256:0c3176d327f922cdd9610d88f97db4c394daa51bed620febee0e34b96c9268bc`  
		Last Modified: Wed, 24 Apr 2024 08:59:07 GMT  
		Size: 7.9 MB (7939172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361a870075491a6a7a24221fb8d49e5da4f74120305fd21b8220b0e0c7f6180c`  
		Last Modified: Wed, 24 Apr 2024 08:59:07 GMT  
		Size: 64.0 KB (64023 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:latest` - linux; mips64le

```console
$ docker pull wordpress@sha256:adc3319781a05f1ffea3595acae0049e328eb462f8cfa853b0b48afca8f43338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212428469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea103880511f0260a1c54928953e16f5b806a44fc668fbc92e13b87775c1d1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 02:30:59 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 02:30:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 02:30:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_VERSION=8.2.18
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 02:30:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 02:30:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	version='6.5.2'; 	sha1='b70701b5426891ca1f8ff9b3cd96653e2b60d7e9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 02:30:59 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:796fa395fb05e5a39254d0d9582b02b4121109eda21399913880a92cf308465f`  
		Last Modified: Wed, 24 Apr 2024 17:10:14 GMT  
		Size: 20.1 MB (20064275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a013e8397474ca02386b15a3f4275dd3bafea255c7d4a0473efdade3a7a35305`  
		Last Modified: Wed, 24 Apr 2024 17:10:01 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c13a0066263138d3939a9dbee014c328c5cff619f5a5e211581815e00aac8ae`  
		Last Modified: Wed, 24 Apr 2024 17:10:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56f82741ba336541a009606fd5f8c948ba5846c84dd2acdaf9838c214393a21`  
		Last Modified: Wed, 24 Apr 2024 17:15:57 GMT  
		Size: 12.2 MB (12215805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69702d366a75baebd219f9389865733b70636bf39ef424ed62f3d088a6e1156`  
		Last Modified: Wed, 24 Apr 2024 17:15:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829c6354f460c2625d47662f73e9611dcdad5d6525cbc2d3fa501d4346ca19c`  
		Last Modified: Wed, 24 Apr 2024 17:16:00 GMT  
		Size: 10.5 MB (10485710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ec6b9d9ed7d530a0c726e13800e6e107b552148a9c41384dfd74052f14e368`  
		Last Modified: Wed, 24 Apr 2024 17:15:52 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9232f9cdbe14415839ced88c7dd01e7849cbc4e74e2fedb6117fc0ce51745d6`  
		Last Modified: Wed, 24 Apr 2024 17:15:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a541ad241c3f4c92973cedc9ad552e4622b0e43b86152d852bc994e54bcc161d`  
		Last Modified: Wed, 24 Apr 2024 17:15:52 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbb5efa1bb8833acfad628c0d470c24e4ba07c485309cd18caeb054fecf345d`  
		Last Modified: Fri, 26 Apr 2024 06:06:17 GMT  
		Size: 26.0 MB (26024726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9f70ef7ad54ae2a81774bff38ee29c40d2116e01805b3a16e923872b6f969`  
		Last Modified: Fri, 26 Apr 2024 06:06:15 GMT  
		Size: 9.5 MB (9463539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0754cd97852d1d286869aa63e202325cb0f90c4e52935044d6c7a78327a6183`  
		Last Modified: Fri, 26 Apr 2024 06:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32582e8a44dd77459fd97288f336bd40e8297873471a6588f711f8f3bfbc2fcd`  
		Last Modified: Fri, 26 Apr 2024 06:06:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343c6849730fce7fa9822e13aff08478b2c122e1ebd301794896a82cae7cec37`  
		Last Modified: Fri, 26 Apr 2024 06:06:15 GMT  
		Size: 19.2 KB (19176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3336018f95dd9c0d80f14c078a0e0fa7e7adcb3b1cd2d9f1a25cbedd90a30ddf`  
		Last Modified: Fri, 26 Apr 2024 06:06:18 GMT  
		Size: 24.5 MB (24526006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eeea0954f6afe3d25c9a9f2b5c39fd39bdb4b00535e6e3c1fa8083ce7f7c4f`  
		Last Modified: Fri, 26 Apr 2024 06:06:16 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f934c20e71dd04fe5cfa5500865e10799b442abc52338d23909e3fb369b6ea9a`  
		Last Modified: Fri, 26 Apr 2024 06:06:16 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:latest` - unknown; unknown

```console
$ docker pull wordpress@sha256:0b808082320881d68d6761607cf501403b75b4ff91c586e37830fcb8266d4cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 KB (61958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe6695966ec4de0baa1a8345e1e6b241ff743b24caa9f6b3e1c28e0bab31ddc`

```dockerfile
```

-	Layers:
	-	`sha256:23128381795a24f54c7aba87c2a8b80d83e9dd35225033bac7570a4185d860e0`  
		Last Modified: Fri, 26 Apr 2024 06:06:13 GMT  
		Size: 62.0 KB (61958 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:latest` - linux; ppc64le

```console
$ docker pull wordpress@sha256:41d9ea7ee97876b905ad6710b3dbb34196171805308d1b01e7866b9f04742659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245364753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385d16d291fb3ca5518fa7efaf44fa6a79740eaf0a14f53065ea19cfc2c54e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 02:30:59 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 02:30:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 02:30:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_VERSION=8.2.18
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 02:30:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 02:30:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	version='6.5.2'; 	sha1='b70701b5426891ca1f8ff9b3cd96653e2b60d7e9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 02:30:59 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0691face80da0cd3cc797ec4a2ebc8b8db4a2220cd3512317f2a7482987d6c`  
		Last Modified: Wed, 24 Apr 2024 08:07:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b402bfece7b36278991277cb8b969b21bc0826c9f39c9a280b58069053d3cec`  
		Last Modified: Wed, 24 Apr 2024 08:07:24 GMT  
		Size: 103.3 MB (103317105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c476f59d918d2f80058be2efb33e35fd07d1eb9041c856545feea018b2dd7f`  
		Last Modified: Wed, 24 Apr 2024 08:07:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803028d2487c30e28b2758457f5e9a3a47ac99023399a4633ee3f3ac7a5c4f20`  
		Last Modified: Wed, 24 Apr 2024 08:08:13 GMT  
		Size: 21.5 MB (21512987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5acf4731e76e597efa1ab916917c0e56f03dedadd6732441a8d2d7dc4902a8`  
		Last Modified: Wed, 24 Apr 2024 08:08:09 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ef4f8146013e8c50b7057af1996d1297cd096d1cfe4231dc778e85e371bae8`  
		Last Modified: Wed, 24 Apr 2024 08:08:09 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1fc9f33d5ef80df8eddee4eeddb72609d7d6c4103bf4c3982337fbc708e2cf`  
		Last Modified: Wed, 24 Apr 2024 08:11:58 GMT  
		Size: 12.4 MB (12423530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dedb7e6b0cda207a79164d23cdc796817543399868ee1c3eea189d1c5f78f7`  
		Last Modified: Wed, 24 Apr 2024 08:11:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e316fdeaeb0218e09746d4bc015689b89866c7db6fa3cc2aa48fa80f0c0aa8e`  
		Last Modified: Wed, 24 Apr 2024 08:11:57 GMT  
		Size: 11.8 MB (11817725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53110a78646d022012ece64c44a90e7bab43cbebef371567dec12a8e9d5045a`  
		Last Modified: Wed, 24 Apr 2024 08:11:55 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940e7bf60a722a211378e1555f76ca5cb98bb5b5af034747bd15ad5e3ed22061`  
		Last Modified: Wed, 24 Apr 2024 08:11:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a842c4fd778371a561c58b7b51aff1d6f534985cfd4ffaf4d1b81185006d82`  
		Last Modified: Wed, 24 Apr 2024 08:11:55 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfe6baa213638a3c2f4418b029dd48579b632ef6b76bffd27c998eec6aa775f`  
		Last Modified: Thu, 25 Apr 2024 09:52:24 GMT  
		Size: 27.3 MB (27345339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817bc709de7d4484fe17d27b2834ddf1e44d668cdeddb44bf57fcdf77d336512`  
		Last Modified: Thu, 25 Apr 2024 09:52:24 GMT  
		Size: 11.3 MB (11251287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fa834bd84ce448e987a52919e6c3386c82ed55d6273525a4b64b82b000aecc`  
		Last Modified: Thu, 25 Apr 2024 09:52:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04601809f471f5522523a0cee1b0c7c108f4eb1f338249be2faa2ebd24d6de86`  
		Last Modified: Thu, 25 Apr 2024 09:52:23 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26987b3610ec6e616186bd769d5e629b245f927ae3e4232246952455100d7678`  
		Last Modified: Thu, 25 Apr 2024 09:52:24 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fdcf571d4789285c4466b73ef72bc5b52754ede240704bbedf845175dc693a`  
		Last Modified: Thu, 25 Apr 2024 09:52:25 GMT  
		Size: 24.5 MB (24526008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5a15e8d857f70619631c9f0d5951f68f1e28a78f2f65a496a152166dd5c4a0`  
		Last Modified: Thu, 25 Apr 2024 09:52:25 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66641d879788678b5df476fa1049f97f76a174a25bd618406e29a1a573fdf8c`  
		Last Modified: Thu, 25 Apr 2024 09:52:25 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:latest` - unknown; unknown

```console
$ docker pull wordpress@sha256:a45130f400fb52a52ac6c91839fd911ae25c4e80a4269382a4e40d8c1f4dd9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8000100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afa565389e67f9cfeaddd6288fa359dc3dacaa19d9fca99a9c9fcc6a7855031`

```dockerfile
```

-	Layers:
	-	`sha256:265d8a594388248db1881be05cb03e2776339bfcf9ad8692d7164dbde360473e`  
		Last Modified: Thu, 25 Apr 2024 09:52:23 GMT  
		Size: 7.9 MB (7937967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:867e7f2b0adca0830460f694d93959c0ba1e620ffe995c6b4f5aa7040b4b403f`  
		Last Modified: Thu, 25 Apr 2024 09:52:22 GMT  
		Size: 62.1 KB (62133 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:latest` - linux; s390x

```console
$ docker pull wordpress@sha256:e5f9dd492987c5ce91e362af51c1e031b112c3d6ec4626b76aacc2ca1d6c4a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211222988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef01d6092f53ab776bf9a974352ae53f2e2acb04e58c1f5c998b6c6b726a515`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 02:30:59 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 02:30:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 02:30:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 02:30:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_VERSION=8.2.18
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 10 Apr 2024 02:30:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 10 Apr 2024 02:30:59 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
RUN docker-php-ext-enable sodium
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Apr 2024 02:30:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 10 Apr 2024 02:30:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:30:59 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:30:59 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
RUN set -eux; 	version='6.5.2'; 	sha1='b70701b5426891ca1f8ff9b3cd96653e2b60d7e9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
VOLUME [/var/www/html]
# Wed, 10 Apr 2024 02:30:59 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 02:30:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 02:30:59 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:8f65d9c7a3c7fbabbee65db4bc3f6b89c6e4658ebd4c4f4bc8d22072c120e8b2`  
		Last Modified: Wed, 24 Apr 2024 06:53:56 GMT  
		Size: 20.1 MB (20103206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09fa0ce42167bd609392aa4caec40de5fb1ac54bae4ddd67c1b30f41a457a9b`  
		Last Modified: Wed, 24 Apr 2024 06:53:54 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36c8a20b0c6f1b50c385757e29f5d1653bb89fac62ab9c56f01d8799873f23`  
		Last Modified: Wed, 24 Apr 2024 06:53:54 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6831d3c27679a33b860e3e7d471d919379faa1aafe978e9449397e4a11e799`  
		Last Modified: Wed, 24 Apr 2024 06:56:44 GMT  
		Size: 12.4 MB (12422598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fa4ed2be9c2df3daf746416561a56a74e4089bec9e1a0fbfe80321e843eba`  
		Last Modified: Wed, 24 Apr 2024 06:56:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5a62fce44437d5a6ead6f8286cd5c32bed1233feb054e0888df9b0cca7e357`  
		Last Modified: Wed, 24 Apr 2024 06:56:44 GMT  
		Size: 10.5 MB (10451875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1340197e25cac1fc9ce83b044ed2883a2e78ed4fddb7147bb06984f59f5505cc`  
		Last Modified: Wed, 24 Apr 2024 06:56:42 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b5a4fe0b3eab1f9d3e7bb2def5cf41f00f4c93560f90203f67e4f24572c10f`  
		Last Modified: Wed, 24 Apr 2024 06:56:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72f7dbafae26ad1a8c69baf99a314aca581c64a76183e6356f442ce80d18ef8`  
		Last Modified: Wed, 24 Apr 2024 06:56:42 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b988cee84387cc92a8ef69f1a1ad7f0a91e35c82d3f15407677ff500e504f70`  
		Last Modified: Thu, 25 Apr 2024 11:45:40 GMT  
		Size: 25.9 MB (25902670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92697b902f06d367e884e76ed77d7050df839280424fb9c8879c3daf984b9614`  
		Last Modified: Thu, 25 Apr 2024 11:45:40 GMT  
		Size: 9.5 MB (9460837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce3793105316fc82f31ab1a0d1ca1ec13edb0b20a295f0823cd5923da8954fd`  
		Last Modified: Thu, 25 Apr 2024 11:45:40 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8c26fba0d5adcb33ec2828631f23f21e3446228a4522c85f462cb4c9fa9a06`  
		Last Modified: Thu, 25 Apr 2024 11:45:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c8a59782cc02c35edc53e7d18b32dd383cb4b7572c8860dba34367117d195d`  
		Last Modified: Thu, 25 Apr 2024 11:45:40 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b5e0557a905204fb297c369e6617a2677458d05fbda854034de75c5818a897`  
		Last Modified: Thu, 25 Apr 2024 11:45:41 GMT  
		Size: 24.5 MB (24526006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973dea15b723d29135dcd20c5a4d9fcef1c69df2706e0c3c5f3cc70fb221c86`  
		Last Modified: Thu, 25 Apr 2024 11:45:41 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc1a3c205dd2ab2068667fd7ef032e6d488fdf9210f903883bbf0aeb40b039f`  
		Last Modified: Thu, 25 Apr 2024 11:45:41 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:latest` - unknown; unknown

```console
$ docker pull wordpress@sha256:7ab5078c11e2aefa4ff6c37eb28697385e77c0aa5493851614074e92a2b232fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7853015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41e5c4124d2bef70751c62163eed195a6258637f477df882790eeb6f2feeca1`

```dockerfile
```

-	Layers:
	-	`sha256:2a9770dd69d5749ab6550862db595a12da2a4d7f5217f108e4c465dc4c822931`  
		Last Modified: Thu, 25 Apr 2024 11:45:39 GMT  
		Size: 7.8 MB (7791018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da2d8113aa3f7fe315964399cf94f96b85f24a26f4008b5897e7acc80fb1460`  
		Last Modified: Thu, 25 Apr 2024 11:45:39 GMT  
		Size: 62.0 KB (61997 bytes)  
		MIME: application/vnd.in-toto+json
