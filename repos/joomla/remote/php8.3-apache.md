## `joomla:php8.3-apache`

```console
$ docker pull joomla@sha256:e97494af904bcf66268cfbebf6d56dc467db07b6f43d50cea10a9cd9dd0ccb7d
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

### `joomla:php8.3-apache` - linux; amd64

```console
$ docker pull joomla@sha256:9270f3585a33d5c4e7ecb93052d2104c325c3b6d6dea7cf22307223ff10db017
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260865024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897fcf2b926c292bc1c8534515c1b072b13d90fababe5e931898a03e294cf0d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:23:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 23:24:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:24:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 23:24:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 23:27:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 23:27:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 23:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 23:28:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 23:28:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 23:28:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:28:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:28:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 23:58:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 23:58:06 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 23:58:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 23:58:06 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 23:58:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 23:58:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 00:01:52 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:01:52 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 00:01:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 00:01:52 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Sep 2024 00:01:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:01:53 GMT
WORKDIR /var/www/html
# Thu, 05 Sep 2024 00:01:53 GMT
EXPOSE 80
# Thu, 05 Sep 2024 00:01:53 GMT
CMD ["apache2-foreground"]
# Thu, 05 Sep 2024 03:33:17 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 05 Sep 2024 03:33:17 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 05 Sep 2024 03:33:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 03:35:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 05 Sep 2024 03:36:00 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 05 Sep 2024 03:36:00 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 05 Sep 2024 03:36:01 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 05 Sep 2024 03:36:01 GMT
VOLUME [/var/www/html]
# Thu, 05 Sep 2024 03:39:43 GMT
ENV JOOMLA_VERSION=5.1.4
# Thu, 05 Sep 2024 03:39:43 GMT
ENV JOOMLA_SHA512=84111f652a4e52029b2d12ab4621203f28dd68cffe67febaa73a562778af559e3b954c7aedc6a0e1579177321a95eee77e0596c395f2e54e8c226690960bd260
# Thu, 05 Sep 2024 03:39:46 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.4/Joomla_5.1.4-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 05 Sep 2024 03:39:47 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 05 Sep 2024 03:39:47 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 05 Sep 2024 03:39:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Sep 2024 03:39:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c335a1cecf2042cefb300d0412e6cacdaac64e802f084333a622684cb1d64e82`  
		Last Modified: Thu, 05 Sep 2024 01:23:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1356d24f266ec64743f0c51c295266004d42e8335b1038c4f14438de5cd516`  
		Last Modified: Thu, 05 Sep 2024 01:23:59 GMT  
		Size: 104.3 MB (104345555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a67f8d1dfc40864edde3a2f41418653b120eb088d5ffcd3fc1e67832260c4c`  
		Last Modified: Thu, 05 Sep 2024 01:23:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773d8e2be6c609f5234e63bf19ce8738505700b3f1f261403385be179e07ea91`  
		Last Modified: Thu, 05 Sep 2024 01:24:23 GMT  
		Size: 20.3 MB (20326804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b874a8bbb5229433272e54f3c4b82729caee22bef31d6c358d1c985f774934f9`  
		Last Modified: Thu, 05 Sep 2024 01:24:21 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395851b4c00bb078bf7bdc54b5776fd2926a5002eb8557ea474161621d214e5d`  
		Last Modified: Thu, 05 Sep 2024 01:24:21 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8ceff0049107f747ce4a814116791a2b88ab20d297d37b738e3b38483c8d4b`  
		Last Modified: Thu, 05 Sep 2024 01:27:05 GMT  
		Size: 12.8 MB (12814188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a536a22fc4b970d8beb2f29886cc207795f7e649cdb1b0059eb36304bb00e895`  
		Last Modified: Thu, 05 Sep 2024 01:27:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5391caed04b1e837e3c4925e4c77209742752ea380c0adf903821a47462b47dd`  
		Last Modified: Thu, 05 Sep 2024 01:27:04 GMT  
		Size: 11.6 MB (11642344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676960564254576e4c9bf9b0eef45efb5710f55d8a27b71c6cb8f490e6e3048`  
		Last Modified: Thu, 05 Sep 2024 01:27:02 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8945584c4c081a96612aebd632290cc76d1c648f8129425cd3eacecd640505d`  
		Last Modified: Thu, 05 Sep 2024 01:27:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7b1f3f46385f783be5a7fca7ea801884f5c9e1ee417350b6d5cc0e1182cf6c`  
		Last Modified: Thu, 05 Sep 2024 01:27:02 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9f073e71cee96e05f494017e3238e40b2187294a486ba64b1f5452a8018054`  
		Last Modified: Thu, 05 Sep 2024 03:54:25 GMT  
		Size: 27.2 MB (27156840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f64ca6297f7d4e3df7cb19a7004ef9b2b6b109199f6fefe6dae97da47dbd62e`  
		Last Modified: Thu, 05 Sep 2024 03:54:26 GMT  
		Size: 31.5 MB (31503991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127332fafacf44a713640b9676180f5fd7b745858ff26cea1ea9241a97cbcb1c`  
		Last Modified: Thu, 05 Sep 2024 03:54:21 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e07709bde42185e8eb38606d92fbbdf506d5fa1a75d4a52ab4ca0fb373d922`  
		Last Modified: Thu, 05 Sep 2024 03:54:19 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8def6ff9fc77084737b75e0a3612346bd97328511b66e119bdf547c6bb011a82`  
		Last Modified: Thu, 05 Sep 2024 03:54:19 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae71467bd3e2b354e7b287a5bc0e453ba39d4049c81b94bc2fdedf60610b538e`  
		Last Modified: Thu, 05 Sep 2024 03:56:46 GMT  
		Size: 23.9 MB (23918716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668dd7b8cc7d0d728d1877a5e7618bd20b8ddf2fd106f95d1c4f07ea79da5c74`  
		Last Modified: Thu, 05 Sep 2024 03:56:42 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c829e591e8bb8ea576b948469065fedc463e1fedd8964d211f49652c7e6af9a6`  
		Last Modified: Thu, 05 Sep 2024 03:56:42 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:d5249fcd64cd9d73954b69baded8f61c7e6b3b4e3f8d610964ff28ee130e343c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230700718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33537f72dc9a63f7f8802b5b775e3d27f383fa6fc589fcf88a7e70fae1251d8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:18:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 22:18:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 22:19:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:19:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 22:19:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 22:22:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 22:22:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 22:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 22:23:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 22:23:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 22:23:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:23:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:23:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 22:51:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 22:51:03 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 22:51:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 22:51:03 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 22:51:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 22:51:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:54:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 22:54:36 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:54:37 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 22:54:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 22:54:37 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 22:54:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:54:38 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 22:54:38 GMT
EXPOSE 80
# Wed, 04 Sep 2024 22:54:38 GMT
CMD ["apache2-foreground"]
# Thu, 05 Sep 2024 02:15:36 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 05 Sep 2024 02:15:36 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 05 Sep 2024 02:15:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 02:18:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 05 Sep 2024 02:18:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 05 Sep 2024 02:18:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 05 Sep 2024 02:18:34 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 05 Sep 2024 02:18:34 GMT
VOLUME [/var/www/html]
# Thu, 05 Sep 2024 02:22:25 GMT
ENV JOOMLA_VERSION=5.1.4
# Thu, 05 Sep 2024 02:22:25 GMT
ENV JOOMLA_SHA512=84111f652a4e52029b2d12ab4621203f28dd68cffe67febaa73a562778af559e3b954c7aedc6a0e1579177321a95eee77e0596c395f2e54e8c226690960bd260
# Thu, 05 Sep 2024 02:22:30 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.4/Joomla_5.1.4-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 05 Sep 2024 02:22:30 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 05 Sep 2024 02:22:31 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 05 Sep 2024 02:22:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Sep 2024 02:22:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cf852a9ba86e2887cb6ae81a22fd3cf861010abcf57ae1066ec0b59a523a8a`  
		Last Modified: Thu, 05 Sep 2024 00:04:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc51225fc9b9e1a6df96d433497faacd05a9849b6e148315b9b6ea2063d55e9b`  
		Last Modified: Thu, 05 Sep 2024 00:04:17 GMT  
		Size: 82.0 MB (81995015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ac14ff273c17e96586bdbeac20331d8b9eff59891a0eed04365468f870f6d2`  
		Last Modified: Thu, 05 Sep 2024 00:04:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9f893b68a8981adcc2767d3840423a4802a7813caf48973a2938f928bca3a`  
		Last Modified: Thu, 05 Sep 2024 00:04:43 GMT  
		Size: 19.6 MB (19628100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3e4a76b069f6b8c4241cbc0d1544bf30edc0beee53391fb217fb70cff90839`  
		Last Modified: Thu, 05 Sep 2024 00:04:39 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597b60cacfe34030f88f587bddd4f77578f7bfaa6324ad46e45f98319b0642e7`  
		Last Modified: Thu, 05 Sep 2024 00:04:39 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831cfed411db0b6ccc06085150c83a3954e87dfcb598cb14e6d13473d61f4281`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 12.8 MB (12812227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ceeb17287ee175a1c6454fd82c79c363343cab66b83e6a582172db8fe82791b`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e66bcce13da47e74bdcf34de1316f5181b4bfd9116ca58a462cdea89cad57c5`  
		Last Modified: Thu, 05 Sep 2024 00:07:29 GMT  
		Size: 10.6 MB (10609883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68439cc55eb19f7294627a97f14c0987a3e8d4e09221ed788b40b8771477d9ec`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08007609be5c1224f9d21fe5ff6943ad13989f6cbdec3d05839e437cf1eabe9c`  
		Last Modified: Thu, 05 Sep 2024 00:07:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40530019e68f0f4803976426cf756d1605e39cefe62a2ea68f4cb0e2b686504a`  
		Last Modified: Thu, 05 Sep 2024 00:07:26 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff216e2ec7b0d3ddf81b76716a0a0c11ee518dde694ed321b246eabc72fcebf`  
		Last Modified: Thu, 05 Sep 2024 02:38:59 GMT  
		Size: 26.6 MB (26614680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb3ad0de45a90020b37ce6fc2d8c314faff86a8a3281179f1fa29ddf9bf53ad`  
		Last Modified: Thu, 05 Sep 2024 02:39:00 GMT  
		Size: 28.2 MB (28204595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf820f577569ede7ab422bbf31ee4df1568a11be08eadc88c61ea57b6f37946`  
		Last Modified: Thu, 05 Sep 2024 02:38:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e51cb25172601caea2f826748dffb8d371c9d78f87ebd79447f16a90ffab5ca`  
		Last Modified: Thu, 05 Sep 2024 02:38:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfd9c73f3ca7a4e3075d348fd253eded123db95cee079d7a5d034fc5fd5b49d`  
		Last Modified: Thu, 05 Sep 2024 02:38:52 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50921460dbbbbedaec16a4e59ff41917eaabd5045f1b1235aa6b490e60d5609`  
		Last Modified: Thu, 05 Sep 2024 02:41:25 GMT  
		Size: 23.9 MB (23918712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fbf0e082e139f5a0ec284cecbf4d77ed4a03cb91d5bdcfba5633325de5de65`  
		Last Modified: Thu, 05 Sep 2024 02:41:20 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ff537f19c9542f5a5e3ac92f3bf6b6198ee76df2f7e6b778f448bfc070a301`  
		Last Modified: Thu, 05 Sep 2024 02:41:20 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:b9ba7cf7aa35b789380db8c2b0bb58376d93d60ecd8c519b95cf83824e5af012
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219202897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b677f2d8505020803e354c8b7899b56998753dca79f94af241b677b611ba3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:46:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 22:46:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 22:47:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:47:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 22:47:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 22:51:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 22:51:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 22:51:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 22:51:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 22:51:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 22:51:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:51:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:51:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 23:18:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 23:18:45 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 23:18:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 23:18:46 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 23:18:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 23:18:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:21:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 23:21:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:21:45 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 23:21:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 23:21:45 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 23:21:45 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:21:46 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 23:21:46 GMT
EXPOSE 80
# Wed, 04 Sep 2024 23:21:46 GMT
CMD ["apache2-foreground"]
# Thu, 05 Sep 2024 03:19:37 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 05 Sep 2024 03:19:37 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 05 Sep 2024 03:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 03:22:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 05 Sep 2024 03:22:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 05 Sep 2024 03:22:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 05 Sep 2024 03:22:30 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 05 Sep 2024 03:22:31 GMT
VOLUME [/var/www/html]
# Thu, 05 Sep 2024 03:26:31 GMT
ENV JOOMLA_VERSION=5.1.4
# Thu, 05 Sep 2024 03:26:31 GMT
ENV JOOMLA_SHA512=84111f652a4e52029b2d12ab4621203f28dd68cffe67febaa73a562778af559e3b954c7aedc6a0e1579177321a95eee77e0596c395f2e54e8c226690960bd260
# Thu, 05 Sep 2024 03:26:35 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.4/Joomla_5.1.4-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 05 Sep 2024 03:26:36 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 05 Sep 2024 03:26:36 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 05 Sep 2024 03:26:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Sep 2024 03:26:37 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52af8d0fa86c9b158af0ab781cb65e065749146b3fe2c329cb4e9d0af8b14067`  
		Last Modified: Thu, 05 Sep 2024 00:26:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ecdfb85b1e01962d1365bfe3926bbbfe42185d9c8b60d0930000a9db914c4f`  
		Last Modified: Thu, 05 Sep 2024 00:26:57 GMT  
		Size: 76.2 MB (76163311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860c94c7af381cee44c718f3a335927de4a439a9ae12847fc214772a3860cd10`  
		Last Modified: Thu, 05 Sep 2024 00:26:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae1097b4dec4fa4f7c19f8af46ce5d5a11f166910ab19a3f03481dcbf2c05d1`  
		Last Modified: Thu, 05 Sep 2024 00:27:21 GMT  
		Size: 19.1 MB (19065552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058c6166ff928aaba746c5eed7f88c59d3291587055d2c72a797d2822575c866`  
		Last Modified: Thu, 05 Sep 2024 00:27:18 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5148041e15e73d623fd28b30026d084e8ab19285799c3ea4739efeabdbb429c4`  
		Last Modified: Thu, 05 Sep 2024 00:27:18 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f84167ed3529657d7b37b9d0341f1a2726314c86a052aa41549c2f2bbbf6267`  
		Last Modified: Thu, 05 Sep 2024 00:30:03 GMT  
		Size: 12.8 MB (12812193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e0b97a04c478a48237b637d138d115d344a30e54ca168942af36935a8e3b12`  
		Last Modified: Thu, 05 Sep 2024 00:30:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26ac4a44bb6b1e6e0060af66a57ea200f5fe9945b49cc167964b62a75951df3`  
		Last Modified: Thu, 05 Sep 2024 00:30:03 GMT  
		Size: 10.0 MB (10033627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c635645075365be26ef61cbd976a56d74a8e94f7b94e26f4bd453bfdbf589082`  
		Last Modified: Thu, 05 Sep 2024 00:30:00 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb28f41dec1777e5da9f75777a2e25532ef896cbbd03750fb92b5dac7cb07e8`  
		Last Modified: Thu, 05 Sep 2024 00:30:00 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1f083b6001c37ef8d23c0a34da908ed9e155eba875a24c262af33fb41bc54b`  
		Last Modified: Thu, 05 Sep 2024 00:30:00 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fdf4d45c7e641b0c53f69de0187581d4e9b7b152c8b99c67bdf0205a53c21f`  
		Last Modified: Thu, 05 Sep 2024 03:43:01 GMT  
		Size: 25.8 MB (25849312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36bc7fb1daaac71a345dbfc85a4243aab140479b649bcf5a8edd7c3c24de913`  
		Last Modified: Thu, 05 Sep 2024 03:43:01 GMT  
		Size: 26.6 MB (26611819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d742c351a9ac582fcee624581855c740e4d2e51c5d2d4a6ef2f06d4350dfd3ae`  
		Last Modified: Thu, 05 Sep 2024 03:42:56 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad809b30290524f672b56f9a070a39aa8bebdf7adc99e926e0e2b9fb9b95844`  
		Last Modified: Thu, 05 Sep 2024 03:42:55 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22339ff223e510c3f2f5b590829f98b79ad0fb9418d72639b99cd4681b0ab98`  
		Last Modified: Thu, 05 Sep 2024 03:42:55 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a47e71bda5389e58e6e74dac8e50a2c320c6bf9346810f8f292fd3b5a53b0f`  
		Last Modified: Thu, 05 Sep 2024 03:45:48 GMT  
		Size: 23.9 MB (23918719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f91b8c703f388d7f964bbe9f4169de1c577438c1a0ef33146af26d53bf24e4`  
		Last Modified: Thu, 05 Sep 2024 03:45:43 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbafa61c1797173b16e67f4a6eb4667e2d8ba702e0cbbc9bc9274c6c0d6d0d6`  
		Last Modified: Thu, 05 Sep 2024 03:45:43 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:9aefc34ffd25d21561da3ec96e5ffe31d55456d2a1dad58a8dbcf3921e387751
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252091548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9745cd3072eb0c24a02b6e3a0548949f4a99d457190130251d26e17ec94e9bb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 22:30:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 22:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 22:30:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 22:34:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 22:34:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 22:34:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 22:34:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 22:34:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 22:34:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:34:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:34:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 22:59:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 22:59:17 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 22:59:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 22:59:17 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 22:59:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 22:59:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:03:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 23:03:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:03:03 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 23:03:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 23:03:03 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 23:03:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:03:03 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 23:03:03 GMT
EXPOSE 80
# Wed, 04 Sep 2024 23:03:03 GMT
CMD ["apache2-foreground"]
# Thu, 05 Sep 2024 02:05:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 05 Sep 2024 02:05:28 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 05 Sep 2024 02:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 02:07:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 05 Sep 2024 02:08:00 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 05 Sep 2024 02:08:00 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 05 Sep 2024 02:08:01 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 05 Sep 2024 02:08:01 GMT
VOLUME [/var/www/html]
# Thu, 05 Sep 2024 02:11:46 GMT
ENV JOOMLA_VERSION=5.1.4
# Thu, 05 Sep 2024 02:11:46 GMT
ENV JOOMLA_SHA512=84111f652a4e52029b2d12ab4621203f28dd68cffe67febaa73a562778af559e3b954c7aedc6a0e1579177321a95eee77e0596c395f2e54e8c226690960bd260
# Thu, 05 Sep 2024 02:11:49 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.4/Joomla_5.1.4-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 05 Sep 2024 02:11:49 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 05 Sep 2024 02:11:50 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 05 Sep 2024 02:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Sep 2024 02:11:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125f50077837c519800d65edc67294c009e30fcc820455fbefc671b63081421`  
		Last Modified: Thu, 05 Sep 2024 00:18:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c15c4686903cb5bbd6cabc5447788b26574756d94e02c0952258c66bb2b4379`  
		Last Modified: Thu, 05 Sep 2024 00:18:40 GMT  
		Size: 98.1 MB (98131394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8893eb8a52e8af8365ae670e2549bcff74923def7137abb8dbd4657905297f01`  
		Last Modified: Thu, 05 Sep 2024 00:18:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa55da0753dad27fbf674997a6a04397736c543162afcaccd636738da352c108`  
		Last Modified: Thu, 05 Sep 2024 00:19:05 GMT  
		Size: 20.3 MB (20325421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a3e15a12625719622136bcd7ea9d8c614ad174f11b4e5d64ee1a0e103a7c94`  
		Last Modified: Thu, 05 Sep 2024 00:19:02 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70c9882f3f52155ce9e7d769b5539a7fdb5eeab8c65342778b58511aabe9dd3`  
		Last Modified: Thu, 05 Sep 2024 00:19:02 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba515f9576300eaf3ab3807d9f575b5a37932308924bcad90b5fa9dc4d5fe18`  
		Last Modified: Thu, 05 Sep 2024 00:21:49 GMT  
		Size: 12.8 MB (12813798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8cf82d18af5745d7125d9799b63374307222dce1866823dcc9c055825de55b`  
		Last Modified: Thu, 05 Sep 2024 00:21:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec00a87d837e93ec7784b7e01cf5d7519fac7f9317ba4ffd3ce4333ee2bf62da`  
		Last Modified: Thu, 05 Sep 2024 00:21:48 GMT  
		Size: 11.6 MB (11633427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b784617d5814d8167a599772fbe9f3850b80c2d7512a25ebdc34f82e45544d`  
		Last Modified: Thu, 05 Sep 2024 00:21:47 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b03b21a80077ef71027aa4e3e7bfb1125e89f42f5b722556231d5260895050`  
		Last Modified: Thu, 05 Sep 2024 00:21:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b12a1a15757ce508f60e484f6d1226675fa9ecd06a53e54e7bfc0f0f6babccc`  
		Last Modified: Thu, 05 Sep 2024 00:21:47 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4325e0cdf8a450082e7387b3d895716d846c60fe19068414ee5977fe31d559c5`  
		Last Modified: Thu, 05 Sep 2024 02:25:10 GMT  
		Size: 27.0 MB (26985580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f7a6b3b9ccdf2693e3b62c2965b0c617c62e2de56f7d16c568fa51bbe484f2`  
		Last Modified: Thu, 05 Sep 2024 02:25:11 GMT  
		Size: 29.1 MB (29096570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cb6d6ef844017931df93c495cf41e9270f9c3461cebee0860c9e078c5cad4a`  
		Last Modified: Thu, 05 Sep 2024 02:25:07 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9bf79e061521bcf668ba07bbcb7687ea38f682cf7ad166ffe1ebf98cbe259c`  
		Last Modified: Thu, 05 Sep 2024 02:25:05 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621736ec450bdd4e4bdb7c9781156cd481141a31f8ba45f260fcbcd59c85cdd0`  
		Last Modified: Thu, 05 Sep 2024 02:25:05 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9103bf8f0e3b6ef62d43384687525325b8fbc0735ef4844650fd3dcbd490ec0e`  
		Last Modified: Thu, 05 Sep 2024 02:27:25 GMT  
		Size: 23.9 MB (23918712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc6035f2645a27d99ee7a0c3d5b44a75dafb1f9881b10867622a06149513e53`  
		Last Modified: Thu, 05 Sep 2024 02:27:22 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ffd77b88ac8101f2cbd509d61e1d81b65262a7b063291d1fdc76d505541163`  
		Last Modified: Thu, 05 Sep 2024 02:27:22 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; 386

```console
$ docker pull joomla@sha256:b8c9b2a8a89073dbcc4c4530c9d2d73fc11cd1985143dac34e6c84dff347dc5e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259451023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625c9aae95bc5cbb8894decfb66fe3b28ddea4c99375f840f6b2fc45f7436ecd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:46:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 23:46:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 23:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:46:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 23:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 23:53:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 23:53:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 23:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 23:53:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 23:53:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 23:53:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:53:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:53:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 00:45:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 00:45:23 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 00:45:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 00:45:24 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 00:45:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 05 Sep 2024 00:45:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:51:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 00:51:42 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:51:43 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 00:51:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 00:51:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 05 Sep 2024 00:51:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 05 Sep 2024 00:51:43 GMT
WORKDIR /var/www/html
# Thu, 05 Sep 2024 00:51:44 GMT
EXPOSE 80
# Thu, 05 Sep 2024 00:51:44 GMT
CMD ["apache2-foreground"]
# Thu, 05 Sep 2024 04:29:57 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 05 Sep 2024 04:29:57 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 05 Sep 2024 04:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 04:33:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 05 Sep 2024 04:33:05 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 05 Sep 2024 04:33:05 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 05 Sep 2024 04:33:06 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 05 Sep 2024 04:33:06 GMT
VOLUME [/var/www/html]
# Thu, 05 Sep 2024 04:37:25 GMT
ENV JOOMLA_VERSION=5.1.4
# Thu, 05 Sep 2024 04:37:25 GMT
ENV JOOMLA_SHA512=84111f652a4e52029b2d12ab4621203f28dd68cffe67febaa73a562778af559e3b954c7aedc6a0e1579177321a95eee77e0596c395f2e54e8c226690960bd260
# Thu, 05 Sep 2024 04:37:30 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.4/Joomla_5.1.4-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 05 Sep 2024 04:37:31 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 05 Sep 2024 04:37:31 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 05 Sep 2024 04:37:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Sep 2024 04:37:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d31e4426139e19c94ca0942df7023cf26932c267261b263dbd848554444817`  
		Last Modified: Thu, 05 Sep 2024 03:02:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c70cae078252759f892081775f43cfce9b4bca811fa4ee5046fc050063c4cf`  
		Last Modified: Thu, 05 Sep 2024 03:02:34 GMT  
		Size: 101.5 MB (101514423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5066486db10391a0fdfecfd181c1c0ac73eefce83f0210b43e3ba3f66cc2c0`  
		Last Modified: Thu, 05 Sep 2024 03:02:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2676b77310bf32695326d895410b9443408ad96744b377fe197360e0f7d6956`  
		Last Modified: Thu, 05 Sep 2024 03:03:00 GMT  
		Size: 20.8 MB (20843985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912fe8524961caad6c13e9f835014cb80b3fead26e3a772d64634a245f8479b6`  
		Last Modified: Thu, 05 Sep 2024 03:02:56 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e5c9b5f4f66032631cb84b8caa4dd8cdbd247ce2dcb95b2f48718b889832b0`  
		Last Modified: Thu, 05 Sep 2024 03:02:56 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6092b88c0108ba7012446a715c547df6cfe9d058cab11e12c414fca08565453`  
		Last Modified: Thu, 05 Sep 2024 03:06:07 GMT  
		Size: 12.8 MB (12813228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688a02d0c750118c06cf8125f23b17d389a37fc16e7798e9f5cf1d11a04fad3d`  
		Last Modified: Thu, 05 Sep 2024 03:06:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd56c8575c3547676a80c8041da4a4af5ffaff5761889d59c38a31ae4984f45`  
		Last Modified: Thu, 05 Sep 2024 03:06:07 GMT  
		Size: 11.9 MB (11863252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07484fee9aeafbdd5fd09de9dce7c6f70ced2c8213f14318209cb8c4e720a330`  
		Last Modified: Thu, 05 Sep 2024 03:06:04 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62008ae7ad7568255145f7ada5677a6ae33800e66484c3b41338a7d06febc527`  
		Last Modified: Thu, 05 Sep 2024 03:06:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f75086e777043b5d24fe05b3a6e2fe36154e0fdef6e04431e745c843f5b8d6`  
		Last Modified: Thu, 05 Sep 2024 03:06:04 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbbf156765a728ea6db3348b37d813157ec6797a83cd178db7d57f168f5ff28`  
		Last Modified: Thu, 05 Sep 2024 04:54:29 GMT  
		Size: 27.5 MB (27522949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9efbc37a10aae526215a1ca6b0af4e2660c29742033d824da235d66a202f9b`  
		Last Modified: Thu, 05 Sep 2024 04:54:30 GMT  
		Size: 30.8 MB (30800067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecdc1285934bf07a13954c090d5259afc24bf80024ab8e7186f32dba04e9dae`  
		Last Modified: Thu, 05 Sep 2024 04:54:21 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadc0d1fd6ea647d9849652ee94bc7f40b69cca2fa25ee402527172fc0be5477`  
		Last Modified: Thu, 05 Sep 2024 04:54:19 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b8e4ed706ca7f569ed6df085dc039d215c24b7e7447ee72ff5ea115047ef32`  
		Last Modified: Thu, 05 Sep 2024 04:54:19 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c04fb4a15af05f91ff8f2299de8112ae484dff9ad7fe96dbf98458178f2feb`  
		Last Modified: Thu, 05 Sep 2024 04:57:05 GMT  
		Size: 23.9 MB (23918716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49b15218683b4aeec3960fd74bb11a34a38a9041e2b2d9f6937825b586cb256`  
		Last Modified: Thu, 05 Sep 2024 04:56:59 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556b1f4ca51c9069ae1808f66828551ca9cb5bb481d2615f3d9c3c5f1562e661`  
		Last Modified: Thu, 05 Sep 2024 04:56:59 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; mips64le

```console
$ docker pull joomla@sha256:08cf342e1c3f7d803499b12277289df62d7378f52c89b5252db49c3856a1662b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232613661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01714149a37fe68dd8572b182ddad7a334bff4f36887f7a56641e35d1e8bdc4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:09 GMT
ADD file:2fad80cfc89f7b624d81eb445f9c64e4cd3f190b85d89f40c33eb7e4bc562c6d in / 
# Tue, 13 Aug 2024 00:11:14 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:45:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Aug 2024 01:45:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Aug 2024 01:46:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:47:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Aug 2024 01:47:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Aug 2024 02:04:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Aug 2024 02:04:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Aug 2024 02:05:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Aug 2024 02:05:53 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Aug 2024 02:05:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Aug 2024 02:06:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Aug 2024 02:06:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Aug 2024 02:06:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Aug 2024 04:21:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 22:09:48 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 22:09:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 22:09:56 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 22:10:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 30 Aug 2024 22:10:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 22:26:35 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:26:41 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 22:26:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 22:26:49 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 Aug 2024 22:26:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 30 Aug 2024 22:26:56 GMT
WORKDIR /var/www/html
# Fri, 30 Aug 2024 22:27:00 GMT
EXPOSE 80
# Fri, 30 Aug 2024 22:27:04 GMT
CMD ["apache2-foreground"]
# Sat, 31 Aug 2024 04:02:07 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 31 Aug 2024 04:02:10 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 31 Aug 2024 04:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 31 Aug 2024 04:15:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 31 Aug 2024 04:15:20 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 31 Aug 2024 04:15:28 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 31 Aug 2024 04:15:35 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sat, 31 Aug 2024 04:15:40 GMT
VOLUME [/var/www/html]
# Sat, 31 Aug 2024 04:34:45 GMT
ENV JOOMLA_VERSION=5.1.4
# Sat, 31 Aug 2024 04:34:50 GMT
ENV JOOMLA_SHA512=84111f652a4e52029b2d12ab4621203f28dd68cffe67febaa73a562778af559e3b954c7aedc6a0e1579177321a95eee77e0596c395f2e54e8c226690960bd260
# Sat, 31 Aug 2024 04:35:19 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.4/Joomla_5.1.4-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Sat, 31 Aug 2024 04:35:28 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Sat, 31 Aug 2024 04:35:35 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Sat, 31 Aug 2024 04:35:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 31 Aug 2024 04:35:49 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e8ebfef8c6b7f6250b54eec0d5d1ae5d66f60f418704f4094cb9291dc214be0f`  
		Last Modified: Tue, 13 Aug 2024 00:22:29 GMT  
		Size: 29.1 MB (29124941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d7d78570066866696cb14db360126368e3a0a1ee89f4b948cf37f55468a007`  
		Last Modified: Tue, 13 Aug 2024 10:16:18 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75969db7a22120ea9a13334170b5e020b905ffb564622c2264ecc4c72cf7f912`  
		Last Modified: Tue, 13 Aug 2024 10:17:16 GMT  
		Size: 80.7 MB (80665961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870b24ca94cd81106d9524ded9f3c504726131fedd763b132f724e99c3a5a27d`  
		Last Modified: Tue, 13 Aug 2024 10:16:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1900c5962378cbee36d45798d48b31cc2f12a1b487bddbb20e11300ce81fc6f`  
		Last Modified: Tue, 13 Aug 2024 10:17:55 GMT  
		Size: 20.1 MB (20069503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e7f77fc1c43a8f9fd309513c4b41c4603af1013f76d4dd47a984e925d637e5`  
		Last Modified: Tue, 13 Aug 2024 10:17:42 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473492975355585b376b804dfaf61621e8854ba37e2913018cd3b00d908c61ac`  
		Last Modified: Tue, 13 Aug 2024 10:17:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb70ff3fdb272bcec24ba7796c83d987f589b8529cda187dbf3c0b95de77266`  
		Last Modified: Sat, 31 Aug 2024 02:08:20 GMT  
		Size: 12.6 MB (12607038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e11fd3dd2e98b1f889a6140f00be15b10177d869ac1fb1d32f235f65badc69b`  
		Last Modified: Sat, 31 Aug 2024 02:08:15 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d280210d9caa37ad0168f6cda997d66b55e7a5b0bdf42f8c6035ad9c4da5bd`  
		Last Modified: Sat, 31 Aug 2024 02:08:24 GMT  
		Size: 10.7 MB (10713211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b1a85cc52446e2f528f6d871a1bd0d016e5aeaf226a5f356f3638347e10e4f`  
		Last Modified: Sat, 31 Aug 2024 02:08:15 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bb434c40a91ff7869bd051d095b36b0419d89a9acb1e8386f9b6ed2b6e8a40`  
		Last Modified: Sat, 31 Aug 2024 02:08:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a00e2ae42484398ecd9cd29bb650296a6028e21e095c025084cc41d3e1ea59`  
		Last Modified: Sat, 31 Aug 2024 02:08:15 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc35cb560dbaef3b4dba7ad486d61e47462841d28e8d063a07daebd430ef4c32`  
		Last Modified: Sat, 31 Aug 2024 05:11:35 GMT  
		Size: 26.9 MB (26911646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0fbe00292ef49b20488f540db6b1d2622595cd8751cb3bae1fff6120508dd4`  
		Last Modified: Sat, 31 Aug 2024 05:11:41 GMT  
		Size: 28.6 MB (28573650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba5bc880188ea06da1cc371c55b931de04aefd845441253cde1d5a978eaa062`  
		Last Modified: Sat, 31 Aug 2024 05:11:12 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23cf16aa6e2e56d85706cdbc3d5208a83eab04e20611421476982e75b719767`  
		Last Modified: Sat, 31 Aug 2024 05:11:09 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffcdfb72b715089a3794d1edec1d0e4be92835045d02f5381867a85af6a0cf6`  
		Last Modified: Sat, 31 Aug 2024 05:11:10 GMT  
		Size: 19.2 KB (19170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58664e91e8e24da5ebaff0342a4100fb15e2634e6774b9d500c21dce4ce499fc`  
		Last Modified: Sat, 31 Aug 2024 05:15:00 GMT  
		Size: 23.9 MB (23917574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807c08181b02d64901de39320662376ce9270989fe75feeee4755b942330e93`  
		Last Modified: Sat, 31 Aug 2024 05:14:39 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368b928b778e16ca47052929be9a27053747995a7343ffa7b388111a0ffa32a4`  
		Last Modified: Sat, 31 Aug 2024 05:14:40 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:d9aa3d2bda3be7de3eeb7c010ce939dd59c8b21f4359f8354a5848dc73d6df06
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266712510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f596a43a7eea4c8445bf6c6a2a1df33281b2b07d1c28a81794c69e48802fe540`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:03 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 13 Aug 2024 00:22:05 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:39:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Aug 2024 01:39:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Aug 2024 01:40:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Aug 2024 01:40:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Aug 2024 01:44:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Aug 2024 01:44:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Aug 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Aug 2024 01:44:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Aug 2024 01:44:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Aug 2024 01:44:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Aug 2024 01:44:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Aug 2024 01:44:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Aug 2024 02:11:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Aug 2024 20:10:46 GMT
ENV PHP_VERSION=8.3.11
# Fri, 30 Aug 2024 20:10:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 30 Aug 2024 20:10:46 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 30 Aug 2024 20:11:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 30 Aug 2024 20:11:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:14:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Aug 2024 20:14:04 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:14:05 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Aug 2024 20:14:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Aug 2024 20:14:06 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 Aug 2024 20:14:06 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 30 Aug 2024 20:14:07 GMT
WORKDIR /var/www/html
# Fri, 30 Aug 2024 20:14:07 GMT
EXPOSE 80
# Fri, 30 Aug 2024 20:14:08 GMT
CMD ["apache2-foreground"]
# Fri, 30 Aug 2024 22:17:10 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 30 Aug 2024 22:17:11 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 30 Aug 2024 22:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Aug 2024 22:21:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 30 Aug 2024 22:21:36 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 30 Aug 2024 22:21:38 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 30 Aug 2024 22:21:39 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Fri, 30 Aug 2024 22:21:40 GMT
VOLUME [/var/www/html]
# Fri, 30 Aug 2024 22:31:20 GMT
ENV JOOMLA_VERSION=5.1.4
# Fri, 30 Aug 2024 22:31:21 GMT
ENV JOOMLA_SHA512=84111f652a4e52029b2d12ab4621203f28dd68cffe67febaa73a562778af559e3b954c7aedc6a0e1579177321a95eee77e0596c395f2e54e8c226690960bd260
# Fri, 30 Aug 2024 22:31:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.4/Joomla_5.1.4-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 30 Aug 2024 22:31:30 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Fri, 30 Aug 2024 22:31:30 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Fri, 30 Aug 2024 22:31:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 22:31:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06653ef71f82635296232203a5165c5573c2ead3963166842f72ee2a3b2ef4e`  
		Last Modified: Tue, 13 Aug 2024 03:23:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e565883e2d514a28111a5bb532a2c842a23c71a73d5a88f1d87566e472a04b`  
		Last Modified: Tue, 13 Aug 2024 03:23:39 GMT  
		Size: 103.3 MB (103319337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2dd094f1396f39e170f27f825f146fac685f7f6c98e96dc3af4a9675ed1de0f`  
		Last Modified: Tue, 13 Aug 2024 03:23:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffa3ca15eb05617f3fb56f26b2011e9c3e3930d65e0fba916ba735a144470e5`  
		Last Modified: Tue, 13 Aug 2024 03:24:04 GMT  
		Size: 21.5 MB (21511456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78475374afd50b36b1d50d7e76b0013a5b44451e299b7322c2a44d1e1142ddd`  
		Last Modified: Tue, 13 Aug 2024 03:24:01 GMT  
		Size: 440.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dbc90c71b4b31ceaaca56bb2014a554dfa1b01129d862cc2c94ed38e3d0c5c`  
		Last Modified: Tue, 13 Aug 2024 03:24:00 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f5022c9021fd50d9c7790fad7e38f7ace502a7606e6d235b58c4289c4066c8`  
		Last Modified: Fri, 30 Aug 2024 21:36:39 GMT  
		Size: 12.8 MB (12813571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9047bcd597670bb8b1f7351addfb19ae680f1999988438d7d1c4c8ee500a0aec`  
		Last Modified: Fri, 30 Aug 2024 21:36:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fd1f66c98d33d43a87e0171876f9a728cf0896b66285e40466862acaaf18e6`  
		Last Modified: Fri, 30 Aug 2024 21:36:39 GMT  
		Size: 12.1 MB (12060044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ae14b5619680127f47eee9c07d31d45eae3ea613297ff60ca050cdccc72736`  
		Last Modified: Fri, 30 Aug 2024 21:36:36 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c031efbb9a047165f3feb7c240ebd9e9fe9d5f69bc6e97f275b429ed5fda3a`  
		Last Modified: Fri, 30 Aug 2024 21:36:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85809fd0a96ec4bf7800122645dcb38d08b1d1edfc9a26359d51e0a3b83c910`  
		Last Modified: Fri, 30 Aug 2024 21:36:36 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f1a07a1bb26442ea965cffbc4f3a46f6777cce9e263b6f7c50983315a4c15d`  
		Last Modified: Fri, 30 Aug 2024 22:47:40 GMT  
		Size: 28.3 MB (28322933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df4fc352c7203c50bca0eb70aab061ad40d60dddae3f21d53190cbac8d64a24`  
		Last Modified: Fri, 30 Aug 2024 22:47:43 GMT  
		Size: 31.6 MB (31614025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d155c819819c9e67b0db37853857635426924ed45f441b3299c8ed9f165319b1`  
		Last Modified: Fri, 30 Aug 2024 22:47:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed01b3c73e5bf2c3f823fef8913bfc4206beec78b0c9e549060a26eba9d92bc`  
		Last Modified: Fri, 30 Aug 2024 22:47:33 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb15d59e6133ae9d4fb55c50796129ff6e4047c446dd990de481d83fb8ba6be`  
		Last Modified: Fri, 30 Aug 2024 22:47:33 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451023772a7f980458e4805004ec72d945df19d3307c9f3a94ea779e16426e7a`  
		Last Modified: Fri, 30 Aug 2024 22:50:36 GMT  
		Size: 23.9 MB (23918719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0c0640160da8ade1f3464e32e7a47ba0009d987dfe7246982967714f2f0ced`  
		Last Modified: Fri, 30 Aug 2024 22:50:26 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6171c9b8d0504e16ac4e5fc6dbbcda87e54e1409c1cf5ab9fa26c43e9df0ed18`  
		Last Modified: Fri, 30 Aug 2024 22:50:26 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; s390x

```console
$ docker pull joomla@sha256:8b5a04f9b95679dc84db19f6c2d9a679a25f343e274aa86d7103e057722ad967
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230937489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843138398c97b9d863c2a2755e640e12a111dc8ae54b2a92791e3ddf970a581b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:12:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 22:12:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 22:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:12:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 22:12:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 22:15:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 22:15:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 22:15:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 22:15:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 22:16:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 22:16:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:16:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:16:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 22:40:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 22:40:00 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 22:40:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 22:40:00 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 22:40:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 22:40:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:42:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 22:42:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:42:44 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 22:42:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 22:42:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 22:42:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:42:44 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 22:42:44 GMT
EXPOSE 80
# Wed, 04 Sep 2024 22:42:44 GMT
CMD ["apache2-foreground"]
# Thu, 05 Sep 2024 00:51:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 05 Sep 2024 00:51:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 05 Sep 2024 00:51:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 05 Sep 2024 00:53:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 05 Sep 2024 00:53:46 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 05 Sep 2024 00:53:47 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 05 Sep 2024 00:53:47 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 05 Sep 2024 00:53:48 GMT
VOLUME [/var/www/html]
# Thu, 05 Sep 2024 00:57:51 GMT
ENV JOOMLA_VERSION=5.1.4
# Thu, 05 Sep 2024 00:57:51 GMT
ENV JOOMLA_SHA512=84111f652a4e52029b2d12ab4621203f28dd68cffe67febaa73a562778af559e3b954c7aedc6a0e1579177321a95eee77e0596c395f2e54e8c226690960bd260
# Thu, 05 Sep 2024 00:57:55 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.4/Joomla_5.1.4-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 05 Sep 2024 00:57:56 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 05 Sep 2024 00:57:57 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 05 Sep 2024 00:57:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Sep 2024 00:57:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9c3e85da8b09b5b347e0de23df0ba14b87db8c71b84ff72bafeff05ac4c45d`  
		Last Modified: Wed, 04 Sep 2024 23:43:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d162a779ea2f70207f50c43a8ea8a2afc36c812e56c03883aef22591b1fadd`  
		Last Modified: Wed, 04 Sep 2024 23:43:27 GMT  
		Size: 80.8 MB (80817858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d512ffc352f972eede4ede7944fbab31c430f84671da665932f51478717b92e0`  
		Last Modified: Wed, 04 Sep 2024 23:43:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da7cad6f7a39f230d1e8de14363803877b8b1c89328c737be2154969bd6f8c`  
		Last Modified: Wed, 04 Sep 2024 23:43:43 GMT  
		Size: 20.1 MB (20099476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e25d89a6f279f62c6f2c2b233479dea22c0d2c23888634ff212bbda2c33066c`  
		Last Modified: Wed, 04 Sep 2024 23:43:40 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1efd0f24c30aa86b4c75e8ddb0e50a36663b9a80a3d8339de48eded5ecf46ef`  
		Last Modified: Wed, 04 Sep 2024 23:43:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668e8ab13d7b69aed4d85fa035d08720d652e70efdc8698fc25b09cae6b61eb7`  
		Last Modified: Wed, 04 Sep 2024 23:45:35 GMT  
		Size: 12.8 MB (12812554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05f1fc8564784e860e06e7ad2b58532a931f6ccf7304de77303cbca916c8405`  
		Last Modified: Wed, 04 Sep 2024 23:45:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ae40c868453e0058c5856d1e3401015e4bccd76cd1c0c382e71c32c44ee029`  
		Last Modified: Wed, 04 Sep 2024 23:45:35 GMT  
		Size: 10.9 MB (10860723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a4976e91d087b77af9309bd1cbf136a2abc35450849ed81f8ef79d11f4422e`  
		Last Modified: Wed, 04 Sep 2024 23:45:33 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b653765846e03ecd316ad84f8460d3e6561690199bff738f9188d214654f0644`  
		Last Modified: Wed, 04 Sep 2024 23:45:34 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c8ac17c0eb33a5a9d73b3972555059b57ae61d7e3af533a7c99aba8b333a40`  
		Last Modified: Wed, 04 Sep 2024 23:45:33 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619f8106703f0e20201f973f5c38a7988186e10e8c48b821c1309827747a0b95`  
		Last Modified: Thu, 05 Sep 2024 01:10:27 GMT  
		Size: 26.7 MB (26700157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5e5391cf3fb99fbcf7d919abdd3a7dd9490f833926b284f59dce6dc321a8f8`  
		Last Modified: Thu, 05 Sep 2024 01:10:27 GMT  
		Size: 28.2 MB (28207588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ca445f967d1dd80e4dd367832f175b6ae2b87819ace952662bc773aaeda96e`  
		Last Modified: Thu, 05 Sep 2024 01:10:21 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af6e187aaf33caa44ebf4a5ab32eeb643bec0688f34c5fe7baeed0eae0b2b1e`  
		Last Modified: Thu, 05 Sep 2024 01:10:20 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa5b0b622fe0a6dbf2f2575ae1fb8b534af27cf6fe6d9d31a102fc789b27601`  
		Last Modified: Thu, 05 Sep 2024 01:10:20 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91c3473de993bd8735adbfc4e5bb87f7b9b69b67de0836fbdc33cedc68340a0`  
		Last Modified: Thu, 05 Sep 2024 01:12:30 GMT  
		Size: 23.9 MB (23918725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ee9f8b36fde1038397c3b9f8bcc170ca8ae33cda28d98ac6a7c48af39edcd6`  
		Last Modified: Thu, 05 Sep 2024 01:12:25 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaca96a187d8f747bf27b52cf10d12e698725a933830de0bb5905a43c103637b`  
		Last Modified: Thu, 05 Sep 2024 01:12:25 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
