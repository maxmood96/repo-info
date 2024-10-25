## `drupal:11-apache-bullseye`

```console
$ docker pull drupal@sha256:7cc65ea75057a6bfad7b217f009f1462a11356258027724707fa3b27681b2b5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `drupal:11-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:7b1b97a6a666d34efbaa8a3062317f2e609da924a4e1593d0de34557028cc7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188685268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912b1463867eeadbece9c77b15bcdbf8e76f6a6ec93bbbd80bb028dcbb41bd87`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Oct 2024 09:27:25 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Oct 2024 09:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 03 Oct 2024 09:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 09:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 80
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["apache2-foreground"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbbd15f347bcdafcf64d35ef1d5188d26e93dbd1a9f6c597aadb9d73c5e4bf1`  
		Last Modified: Thu, 17 Oct 2024 04:20:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf5a80d2887f3525d056883d0933bb421e308d260def97abcc7866e92b74fef`  
		Last Modified: Thu, 17 Oct 2024 04:20:33 GMT  
		Size: 91.6 MB (91648779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e1925177bb647010bddc6c584e5d4a7ff00063fdc8b64ed1bb82c45aa4fc74`  
		Last Modified: Thu, 17 Oct 2024 04:20:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d49eea953465a4ecc3add99a641e83024465f0e22bd7b3d7500a3ba920a8a04`  
		Last Modified: Thu, 17 Oct 2024 04:20:48 GMT  
		Size: 19.3 MB (19279196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eca754d321489b60cd9eeffb40e7621572eb275775ee43e67e763b79ab18a4a`  
		Last Modified: Thu, 17 Oct 2024 04:20:46 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b2f8e837025a04ecea9a5ed7eb84a58dc64c8e4285b73b4e75aad4ec86ee29`  
		Last Modified: Thu, 17 Oct 2024 04:20:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeb12faac3607fe666aa21fa4df563551e535cf3b4d1a5447b08079eb11067d`  
		Last Modified: Fri, 25 Oct 2024 02:15:52 GMT  
		Size: 12.8 MB (12824056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f639d64723d9b7e1d67952f08a188cecee37ed55151f0bb12bcf3127cd7898e`  
		Last Modified: Fri, 25 Oct 2024 02:15:49 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0cc163bbe6de4f435ca7733f97ad3565479c9b53125af87187b5188c397242`  
		Last Modified: Fri, 25 Oct 2024 02:15:52 GMT  
		Size: 11.6 MB (11580597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da5823bee73516b2d84e9edaf979229ef12a4b44776b76923a0d93de07e556e`  
		Last Modified: Fri, 25 Oct 2024 02:15:50 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a210b227222176e1aeee30e016e180331987e64de667ea69c43750e222f58`  
		Last Modified: Fri, 25 Oct 2024 02:15:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dce5e9041468d6293a63a6e5c86c100e783e0e052c252f9c020358b1b173d7`  
		Last Modified: Fri, 25 Oct 2024 02:15:50 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcbbaea8bbdd889151731b85a77dda176e4b18a79e40119830371b8c9917665`  
		Last Modified: Fri, 25 Oct 2024 03:51:00 GMT  
		Size: 1.9 MB (1932517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b8b546c640f52fe5306e9db3577506308ea58a194bc5a92bfb7880c2abe905`  
		Last Modified: Fri, 25 Oct 2024 03:51:00 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511e09ce8193865206bebfb4ca4bd22ae80400cca102405bf8fb6f4c8b6a40d1`  
		Last Modified: Fri, 25 Oct 2024 03:51:00 GMT  
		Size: 738.7 KB (738720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917410ac973fcb877cff857db1a8406010e8d9c90500308442b2e2596aaaea16`  
		Last Modified: Fri, 25 Oct 2024 03:50:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5508c3246afbdccfc33a2894f930ffadb6035037c6cf281241f33a04e2db9c6a`  
		Last Modified: Fri, 25 Oct 2024 03:51:01 GMT  
		Size: 19.2 MB (19246717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:25ac7d82615855c09f024a53d9524597c10d533e69ca44d3c51eff995552abb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d5a59c7a2e984240497de02d3b352e119a23fc673ffa434658b2453945868a`

```dockerfile
```

-	Layers:
	-	`sha256:9fa66d37712b3803a019613417b3937f731302646563fdd87f7fd21d98bee362`  
		Last Modified: Fri, 25 Oct 2024 03:51:00 GMT  
		Size: 7.0 MB (7041871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf1420441285c4a44d270a9b10b03396d8955dda27b26b75818b4c70e7e0ee21`  
		Last Modified: Fri, 25 Oct 2024 03:50:59 GMT  
		Size: 37.4 KB (37350 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:a6ab5143734c4b303753014383f1d594b9e9af134a772b0f0c9ff48111462bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158088920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfa327c5fca5486c9aa94a5a1d7156fcfd431005415c3beaf11cb845f6e0433`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Oct 2024 09:27:25 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Oct 2024 09:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 03 Oct 2024 09:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 09:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 80
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["apache2-foreground"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0606d2c81db30773bad8bfc0fe9de13c273ca378969df520e2bcc097e2b1c968`  
		Last Modified: Thu, 17 Oct 2024 06:01:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0bc221353bad7dcb9a35d25b7e0366d8b7ad0b5800ee681486a49f010ab9b6`  
		Last Modified: Thu, 17 Oct 2024 06:02:00 GMT  
		Size: 69.3 MB (69327127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3ec6f0f820288d353259f98dd4661bcfda8c6acdfb31275dde353487d6e9e3`  
		Last Modified: Thu, 17 Oct 2024 06:01:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7279221aca8b55f43e6443be212b1657f9c1eb0166b21a5cff7c0dedb83c4987`  
		Last Modified: Thu, 17 Oct 2024 06:02:17 GMT  
		Size: 18.0 MB (18033763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7e67eec042806807953e626da02d18115bfb78f0edd01c3998bc24c88c81d4`  
		Last Modified: Thu, 17 Oct 2024 06:02:13 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3cdc9341b31526e89809c4f7c7bc428ebf26dd65f69c5f3e71903660f744e1`  
		Last Modified: Thu, 17 Oct 2024 06:02:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acdb55c92029d82f04369d78e33e76323489657ac0ebb4b0d489300aaeb413d`  
		Last Modified: Fri, 25 Oct 2024 02:36:39 GMT  
		Size: 12.8 MB (12822517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0f0c1a8d06c509e032226abb1e7bed4d8f5acb6ee622294818fc5bdf418620`  
		Last Modified: Fri, 25 Oct 2024 02:36:36 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dad2b81f61780d5e2ea859cbfa653da3e593074d47b494e424d98bd2716217`  
		Last Modified: Fri, 25 Oct 2024 02:36:38 GMT  
		Size: 10.0 MB (10011573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4ab26dac59efdb09038e9e49488c2f336c899afb81251bbaeb74ff854f551`  
		Last Modified: Fri, 25 Oct 2024 02:36:36 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33df68c3da06a4f6190d583863a8d8ce4b7ffc5032f7e0ba8b1aa8e9f1c4144f`  
		Last Modified: Fri, 25 Oct 2024 02:36:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cf9428775845ebfcd67feb189b76495fd96af19f88675249d37a188fe67409`  
		Last Modified: Fri, 25 Oct 2024 02:36:36 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a949561a458a9f7391af4efacabbd53418c8ba4adf74a402531f8df213d4cf41`  
		Last Modified: Fri, 25 Oct 2024 04:59:14 GMT  
		Size: 1.3 MB (1311795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9358ec09df6b942d6aa6b2aee537ca06b71c0f26368618ea0e46aa823cce78`  
		Last Modified: Fri, 25 Oct 2024 04:59:14 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d497ea284cfb93ce0422bbfaeff0c307cf49478a9653ebb01e7e616645be16`  
		Last Modified: Fri, 25 Oct 2024 04:59:14 GMT  
		Size: 738.7 KB (738716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9605031175e2d846d9c22193ef8076e2c80fad4e6de01229171bc13b77e218`  
		Last Modified: Fri, 25 Oct 2024 04:59:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dae7346cadc9165144817728388fc3ecdb0a1c0225eef5e1749ec24b9f6a80`  
		Last Modified: Fri, 25 Oct 2024 04:59:16 GMT  
		Size: 19.2 MB (19247991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:ca54f9bef255c2bd80994377aca4e7d8cd4d8b4b1c406bce630af9412e825344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6888123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a54f67b72ad86a8fdea0d1cf159020e09d90dad479cb667efba5b06cab3467`

```dockerfile
```

-	Layers:
	-	`sha256:dcf7861769b8ee088fcf77490db9b225e1fe8a8e0d56a2602cef3f77bb811029`  
		Last Modified: Fri, 25 Oct 2024 04:59:13 GMT  
		Size: 6.9 MB (6850569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd8d903f9df3a3286336b544e8e7dca88c16e151404d41931f9ebbd7001030b`  
		Last Modified: Fri, 25 Oct 2024 04:59:12 GMT  
		Size: 37.6 KB (37554 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:dfe28d97068a8a592fb92ca0c49cd5c88081d5d69fa91690d81eb092c2eb3c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182866618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e2cf2b56ec0c7ebd8629e43c8fcb4af0f0cfe57c72defeac9dda4d9d7ae848`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Oct 2024 09:27:25 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Oct 2024 09:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 03 Oct 2024 09:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 09:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 80
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["apache2-foreground"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace9636e6938c06012e872f575501cde8bf2eca9acb98f854f4751aa1514dd9`  
		Last Modified: Thu, 17 Oct 2024 04:18:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7171c8bb99efea9002d518bf04cebb687c75638eefbe3666e14777dc886ef464`  
		Last Modified: Thu, 17 Oct 2024 04:18:41 GMT  
		Size: 86.9 MB (86938384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b149e2ef200eac8e6802701c011653731e4d39d82222744d140dc44a7887836e`  
		Last Modified: Thu, 17 Oct 2024 04:18:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b980c2cf5f1d5985e5fd448ff6d061569c78dab491fdd6cf426d17ed80f5ed`  
		Last Modified: Thu, 17 Oct 2024 04:18:56 GMT  
		Size: 19.2 MB (19196724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8358973d1388c71d67de1b48dfb30463a5b98d0cb1ee434e6e4ed428cd185551`  
		Last Modified: Thu, 17 Oct 2024 04:18:54 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c5eb242c4d60a34a586a26ff5f3a53147c64f2f028014b29c6a95cc21d5d9`  
		Last Modified: Thu, 17 Oct 2024 04:18:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b53fa98c464849465f6f0aa3b57763114c6189575d6fe1069d665a0dda409`  
		Last Modified: Fri, 25 Oct 2024 02:18:53 GMT  
		Size: 12.8 MB (12823300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5ffc382e81909e6bc6321ee1d3ccb03ba79c406c56c3a11803cd727dc84fa1`  
		Last Modified: Fri, 25 Oct 2024 02:18:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c448012f50f60472b597f43c52300154d6dbf3e91f07014a9d278937c3fd4db7`  
		Last Modified: Fri, 25 Oct 2024 02:18:52 GMT  
		Size: 11.6 MB (11644823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fcc0ba4458d456f8513caa3d99243b07b8bdac8b0d356ffce7508db3ba52c3`  
		Last Modified: Fri, 25 Oct 2024 02:18:50 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38eb1c89b619ed5d9db0395d66819a85e1659f2f71902d41f09329eab5f417a`  
		Last Modified: Fri, 25 Oct 2024 02:18:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7d7463932141e8371746f5a4ec50997bdff3ab1617d5c7d770d753dfa67937`  
		Last Modified: Fri, 25 Oct 2024 02:18:50 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d714cd9ffd371149735b149ea27fdb6ba39daa2db9c783670f8f3b56fb4b26`  
		Last Modified: Fri, 25 Oct 2024 05:04:48 GMT  
		Size: 2.2 MB (2195047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819295e0c79156c2682e87834a6898cd7e76e598ec7420a97846caff1890bb9c`  
		Last Modified: Fri, 25 Oct 2024 05:04:48 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abec547e192f45ee31cffc680cb42ce0640d7b7b23d2cddb232e7779409c55b5`  
		Last Modified: Fri, 25 Oct 2024 05:04:49 GMT  
		Size: 738.7 KB (738721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d11a4a7333d0dff56e5b9dbba4df7c0ed1213e1f869e9f0ad14494c9d4aab8`  
		Last Modified: Fri, 25 Oct 2024 05:04:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f2dab05ca88781a8a88e5213df2634feac4e7e5a4f78b065ad38da51989509`  
		Last Modified: Fri, 25 Oct 2024 05:04:50 GMT  
		Size: 19.2 MB (19247975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:e34c94019a90b9d7d3c31774766c4f84143b4b72fcdc49a9e03c6a420b5285ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7082325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf0368b712320ad89ea7802d0b6f7c3155c277dcf31eef9285047d3f8d6d16d`

```dockerfile
```

-	Layers:
	-	`sha256:225887908363cde1830e2a908acdeb25b96511b72fbc1694b70c28f58546d9b1`  
		Last Modified: Fri, 25 Oct 2024 05:04:47 GMT  
		Size: 7.0 MB (7044719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21de97f065a012245ebb00fe6cb5698e81b3c7fe264181770ca2939b3897699`  
		Last Modified: Fri, 25 Oct 2024 05:04:46 GMT  
		Size: 37.6 KB (37606 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:7b88b98eafa66807698a0ef55e7839e5bb69f688af96ba941579ecc1562e53a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191513606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354d0f3b86e222a4cdccdd6188ecea8e5bcd9426f34b7de4c54493f30790a8cd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Oct 2024 09:27:25 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Oct 2024 09:27:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 03 Oct 2024 09:27:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Oct 2024 09:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_VERSION=8.3.13
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 03 Oct 2024 09:27:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 03 Oct 2024 09:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Oct 2024 09:27:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Oct 2024 09:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /var/www/html
# Thu, 03 Oct 2024 09:27:25 GMT
EXPOSE 80
# Thu, 03 Oct 2024 09:27:25 GMT
CMD ["apache2-foreground"]
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV DRUPAL_VERSION=11.0.5
# Thu, 03 Oct 2024 09:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 03 Oct 2024 09:27:25 GMT
WORKDIR /opt/drupal
# Thu, 03 Oct 2024 09:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 03 Oct 2024 09:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43260051671f41da7ac3074533520d1adf3836622787931130d47b36ccc9c71`  
		Last Modified: Thu, 17 Oct 2024 06:08:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c2d6fb54fdb4ca9247c69c301328a0648364b4ce3458fcc483de830da5d8ae`  
		Last Modified: Thu, 17 Oct 2024 06:09:18 GMT  
		Size: 92.7 MB (92720839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f93045a988ea98d726109dd89f4e5a35696e290cd4b976ceb78578f11d12fa`  
		Last Modified: Thu, 17 Oct 2024 06:08:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ddf8ce51c109b7bb83cdc751f321539bb2a49e143c49641e4568e518e78a20`  
		Last Modified: Thu, 17 Oct 2024 06:09:35 GMT  
		Size: 19.8 MB (19767420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dcc3b4a41a7530a5d746216200906369af999165c38a5ff788ec50d3f4115e`  
		Last Modified: Thu, 17 Oct 2024 06:09:31 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ad97ea386e5b7a7e6e2df36ca746b373e1926f47c70d771b709f67e89ba637`  
		Last Modified: Thu, 17 Oct 2024 06:09:31 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5df40a23a828f7f0620cb338b2c65e47c2e5e834fc1d6ce2daa39fdaa7fdd9d`  
		Last Modified: Fri, 25 Oct 2024 04:21:29 GMT  
		Size: 12.8 MB (12823337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efc522d9a55fe4c7f65ad875323f291ac06a3e28bf5196ed6bfaa064c182f8f`  
		Last Modified: Fri, 25 Oct 2024 04:21:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5883eb3844820d4808c959269cff6cbbdd4bff0dc4670907eb3ac89dfa9f2c12`  
		Last Modified: Fri, 25 Oct 2024 04:21:29 GMT  
		Size: 11.8 MB (11799001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da24ece262afb274b6a5729e10e3dbf0a15628c4a57a286c7450d4f0b62d46bd`  
		Last Modified: Fri, 25 Oct 2024 04:21:26 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbbfbfea279fbb6969cb23961b37b143fd4341ebcbefcda2856347358542e26`  
		Last Modified: Fri, 25 Oct 2024 04:21:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb1104c6a2fe324db8df0351ed28ef0d7a39fe8bbdec495be26b5c298a49dd`  
		Last Modified: Fri, 25 Oct 2024 04:21:26 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd0ccd2c5141879a83decb7cbd9cee389073435a238d89106ba6cab60394a7c`  
		Last Modified: Fri, 25 Oct 2024 05:50:04 GMT  
		Size: 2.0 MB (1997937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9539303d4d5ccd52a011117d6936cc636fd5ccc24d7190d4a3e6883c3d72af`  
		Last Modified: Fri, 25 Oct 2024 05:50:04 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c57ddbf1483b9106d03c9dcbd7b6f91bf9ce31bdf0c86dbfe4add6ddfa620`  
		Last Modified: Fri, 25 Oct 2024 05:50:04 GMT  
		Size: 738.7 KB (738718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c97d89cfd5d0e676f24957a64504062156a15b5ca7bb0d7c23ba42919a01bf`  
		Last Modified: Fri, 25 Oct 2024 05:50:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33656eb07201c4ba0519f4c77b1994db1f687ddcb4ccefe51a10f9180888d3ef`  
		Last Modified: Fri, 25 Oct 2024 05:50:04 GMT  
		Size: 19.2 MB (19246639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:22cd4c57e99415970d56cac9a2019b01b1ec4a43ab54289321dabafa29c0896e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7069745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c182e3e7a51d1f2e2aa849191c768f636452d122ae34d76469c99b5973b359`

```dockerfile
```

-	Layers:
	-	`sha256:1a5bfb0edfc1bf929a4f1e82cb890334696677b933b39c895d158fd84d466c8a`  
		Last Modified: Fri, 25 Oct 2024 05:50:03 GMT  
		Size: 7.0 MB (7032455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d74a6f58a09640c1548e4e6b6cd021147aeb2820e8acdaa0af79b04e902f6a7`  
		Last Modified: Fri, 25 Oct 2024 05:50:02 GMT  
		Size: 37.3 KB (37290 bytes)  
		MIME: application/vnd.in-toto+json
