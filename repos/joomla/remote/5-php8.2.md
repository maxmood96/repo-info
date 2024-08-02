## `joomla:5-php8.2`

```console
$ docker pull joomla@sha256:1a40c1b62aa888f2edf43289a2dd853d465c681d2993fca3db0fd08e0cda0078
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

### `joomla:5-php8.2` - linux; amd64

```console
$ docker pull joomla@sha256:26633d62666e050c6ffe63d5703bdcaf216ea170819f0b62185ede3e630743de
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260083598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833e833bf23f97d2e6901dc2bde63cdc4f5f53cb6ef5958ea4d1cae00e3a450d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:39:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 06:39:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 06:39:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:39:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 06:39:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 06:43:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 06:43:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 06:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 06:43:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 06:43:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 06:43:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 06:43:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 06:43:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 08:11:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 21:31:50 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 21:31:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 21:31:50 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 21:32:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 21:32:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:35:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 21:35:35 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:35:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 21:35:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 21:35:36 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Aug 2024 21:35:36 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:35:36 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 21:35:36 GMT
EXPOSE 80
# Thu, 01 Aug 2024 21:35:37 GMT
CMD ["apache2-foreground"]
# Thu, 01 Aug 2024 22:43:41 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 01 Aug 2024 22:43:41 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 01 Aug 2024 22:43:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Aug 2024 22:46:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 01 Aug 2024 22:46:28 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 01 Aug 2024 22:46:28 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 01 Aug 2024 22:46:29 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 01 Aug 2024 22:46:29 GMT
VOLUME [/var/www/html]
# Thu, 01 Aug 2024 22:52:53 GMT
ENV JOOMLA_VERSION=5.1.2
# Thu, 01 Aug 2024 22:52:53 GMT
ENV JOOMLA_SHA512=d344506443b403fa662aa4e626e11a76d8666c938f52e497030d4b422205a1cdf21d4457d5943f68eea47e904067f8005b49a6d95432255e772809a3a471d1b0
# Thu, 01 Aug 2024 22:52:57 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.2/Joomla_5.1.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 01 Aug 2024 22:52:57 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 01 Aug 2024 22:52:57 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 01 Aug 2024 22:52:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Aug 2024 22:52:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a83fa76a2b6c79f2ceb6a3ac1d705844e9f1b13544b372353738d852317d8a`  
		Last Modified: Tue, 23 Jul 2024 09:35:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb3cd9e6b429af5419fe7f9a9d1ebd1b80eec307fb1eb50d85e9ce901775300`  
		Last Modified: Tue, 23 Jul 2024 09:35:51 GMT  
		Size: 104.3 MB (104349191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41714dd6e6a02a12b553a69607d296b4acfe06ebfd34170e47f89ce43f2fd09`  
		Last Modified: Tue, 23 Jul 2024 09:35:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e362d14d0b88a76a0df065fd31bfc25b16f4f2afc88ecb30273c08bd21d1ab60`  
		Last Modified: Tue, 23 Jul 2024 09:36:16 GMT  
		Size: 20.3 MB (20327898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b475c73fa4cd4c57941308b5448392792620bdb6654ebde07c1856ea462830`  
		Last Modified: Tue, 23 Jul 2024 09:36:12 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1c872d3db8284d29f89158d5ecb0ff14ebbc08e78834d499468496a1232bd9`  
		Last Modified: Tue, 23 Jul 2024 09:36:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97876285719a3926791dae6daf617f442ad6ebd72bb6aadcd6e75a057763ceb4`  
		Last Modified: Thu, 01 Aug 2024 22:24:35 GMT  
		Size: 12.4 MB (12433177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fb4d37a6c21f19658c9b8cc1982937978535910681835832fbaaf18b589681`  
		Last Modified: Thu, 01 Aug 2024 22:24:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35e4747e8da8a8a230df17fac175b1ca1e8fb00ee40e7bd2f15b2e22788bd72`  
		Last Modified: Thu, 01 Aug 2024 22:24:34 GMT  
		Size: 11.4 MB (11404388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdab7abc93847315c1bae86b3fff17e155d13c34e0bf39d8a2ae70fbcd7ac4d6`  
		Last Modified: Thu, 01 Aug 2024 22:24:32 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d1509706696990e5b9e9a56a46b6b6271be377112ec6f5a2a31d0c46f60c11`  
		Last Modified: Thu, 01 Aug 2024 22:24:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096b0161e32fdfd3684d3735197d451eac28ea855cde552dbafe1f1167c97d1e`  
		Last Modified: Thu, 01 Aug 2024 22:24:32 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcc823a38786df8d1425d1268659d632c60749b445089472b4d2f4050c652ea`  
		Last Modified: Thu, 01 Aug 2024 23:03:21 GMT  
		Size: 27.2 MB (27160706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbe1b4a800e2faafbed4026c040c4fae1201b8b4b74c74fc0a9633b1636e9eb`  
		Last Modified: Thu, 01 Aug 2024 23:03:22 GMT  
		Size: 31.5 MB (31485893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7436069e43c83bc90ce35857e60023be2f77933c23b7d47b82037c7b503b9d`  
		Last Modified: Thu, 01 Aug 2024 23:03:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c15b2305220e20c9e0765f26d89bb61c5e67ed891bd6ca31e8f47693b4cf81`  
		Last Modified: Thu, 01 Aug 2024 23:03:15 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f3aa15e49b2357d8fbc43a3c7c044cb3f5aa8127ece248a4456012acfcee66`  
		Last Modified: Thu, 01 Aug 2024 23:03:15 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3dc0035bb6483b9bfc179ba489e36aac8b079508eb6840108d1e30197941c3d`  
		Last Modified: Thu, 01 Aug 2024 23:05:00 GMT  
		Size: 23.8 MB (23765960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37fa13bd206862c9324d492599da961dc95a88ba7436318d556533e496c94f7`  
		Last Modified: Thu, 01 Aug 2024 23:04:56 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30d12c288adc69a78af83450333b42082240a5eaac2a99f97c45a2b5902f365`  
		Last Modified: Thu, 01 Aug 2024 23:04:56 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.2` - linux; arm variant v5

```console
$ docker pull joomla@sha256:9ca631659897d8ead0bfaf070c64cc3284b7c20f5451a92473c7a4528d9b7da1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229939423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31c6e64a1aaed891ccfe2609e5c686d2fe901e6e6f835e5fc51c065eaadef1f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:01 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Mon, 22 Jul 2024 23:57:01 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:27:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 00:27:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 00:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:27:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 00:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 00:33:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 00:33:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 00:33:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 00:33:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 00:33:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 00:33:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 00:33:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 00:33:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 02:01:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 22:41:52 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 22:41:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 22:41:52 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 22:42:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 22:42:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:44:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 22:44:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:44:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 22:44:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 22:44:44 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Aug 2024 22:44:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:44:44 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 22:44:44 GMT
EXPOSE 80
# Thu, 01 Aug 2024 22:44:44 GMT
CMD ["apache2-foreground"]
# Thu, 01 Aug 2024 23:21:55 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 01 Aug 2024 23:21:55 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 01 Aug 2024 23:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Aug 2024 23:24:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 01 Aug 2024 23:24:52 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 01 Aug 2024 23:24:53 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 01 Aug 2024 23:24:53 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 01 Aug 2024 23:24:54 GMT
VOLUME [/var/www/html]
# Thu, 01 Aug 2024 23:28:33 GMT
ENV JOOMLA_VERSION=5.1.2
# Thu, 01 Aug 2024 23:28:33 GMT
ENV JOOMLA_SHA512=d344506443b403fa662aa4e626e11a76d8666c938f52e497030d4b422205a1cdf21d4457d5943f68eea47e904067f8005b49a6d95432255e772809a3a471d1b0
# Thu, 01 Aug 2024 23:28:39 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.2/Joomla_5.1.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 01 Aug 2024 23:28:39 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 01 Aug 2024 23:28:39 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 01 Aug 2024 23:28:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Aug 2024 23:28:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1060bd7a17f68edf46abfd7f2bbe196a13150748c143722804f62e6decb61a4`  
		Last Modified: Tue, 23 Jul 2024 03:19:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abab82a130067dcceb069a9535c56733df616e1c839b216cd8148a9b312c91e9`  
		Last Modified: Tue, 23 Jul 2024 03:20:22 GMT  
		Size: 82.0 MB (81997235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e53f141e71951b20be7495d56543c4bfd6d8429bca31b80d3401fee7f306b3`  
		Last Modified: Tue, 23 Jul 2024 03:19:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c60a3731902b294c49dd82a016f333a1ed13a06bb5d76e6cfd1c61bec0eef6e`  
		Last Modified: Tue, 23 Jul 2024 03:20:52 GMT  
		Size: 19.6 MB (19627696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd6afb49323fe743b6982ce9411e316d8907dff9f77b5cef2f2c4a1492f9e8b`  
		Last Modified: Tue, 23 Jul 2024 03:20:46 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffeadfa956a312fbd3125874d59e26df75ae32e29f973101bfa17f48c84c886`  
		Last Modified: Tue, 23 Jul 2024 03:20:46 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e9e34f908f1a653d70347b2025f13c0cf7015ec5aa74460ce5fa9020173042`  
		Last Modified: Thu, 01 Aug 2024 23:04:37 GMT  
		Size: 12.4 MB (12431012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bae8f15bd5c3617e7f7aa09355c2f05dfeb509720dc239e8cd20bc182dc46fb`  
		Last Modified: Thu, 01 Aug 2024 23:04:34 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20b53d014914fe6275e0178033fa79ad02e9ffdc7f5bc7354e28e57b278f90b`  
		Last Modified: Thu, 01 Aug 2024 23:04:37 GMT  
		Size: 10.4 MB (10390634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedcf465509a8a31d8dc3290cacaed463f6aab2c1cafb913c59b2f55917d3762`  
		Last Modified: Thu, 01 Aug 2024 23:04:34 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be5c9b09e3f8422e245c6d7618522018fec75cd7f826680056393e63e5ab0c8`  
		Last Modified: Thu, 01 Aug 2024 23:04:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2367022bb6453cf29a67624d4ec7eb45bb08c5ad55929eb95a773a3928b732ca`  
		Last Modified: Thu, 01 Aug 2024 23:04:34 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233ad8c370b444d95df0986a65d918cb92fd02d7679e982653c3b4e9f5b8bd4`  
		Last Modified: Thu, 01 Aug 2024 23:35:57 GMT  
		Size: 26.6 MB (26614313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc5416ed6fb2896c51eec647a42cf21596990a1e5392398885b3311d3000fa5`  
		Last Modified: Thu, 01 Aug 2024 23:35:59 GMT  
		Size: 28.2 MB (28195232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c5e47ba2fddfae23c7cb692d807779885aa0e2c4ce3773800201f51a3d2e62`  
		Last Modified: Thu, 01 Aug 2024 23:35:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515b202430a57abb13c57c0bf9465452e6d4cb11a87bf8db9518c793a319d7b1`  
		Last Modified: Thu, 01 Aug 2024 23:35:50 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9d389e6bf09e996f4d67c606a503a945a6271f87fc3269085f98e550befde`  
		Last Modified: Thu, 01 Aug 2024 23:35:50 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7196d6711b6b887afa3cf89a23a279f4e767305e9548a59d1cf09f10c3871319`  
		Last Modified: Thu, 01 Aug 2024 23:37:14 GMT  
		Size: 23.8 MB (23765913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2048fddb1199bcf6e07292b8f7b871e86c6c5b4a21bbdd6142f306da04cf1e1`  
		Last Modified: Thu, 01 Aug 2024 23:37:10 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7584bf2811d316e8ef1dbaf3a2540a345587ec40cd63e4895c4e6b2e9f4cadd`  
		Last Modified: Thu, 01 Aug 2024 23:37:10 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.2` - linux; arm variant v7

```console
$ docker pull joomla@sha256:4c80f46c99e728a08ff27b1cc8617b0a25b96123ac7a1c346963f9287164f7dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218440414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ef67b4b588a874e5b14e2b45e6ea6ca57291a1574b46d72e2db3a0e643f300`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:24:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 04:24:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 04:25:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:25:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 04:25:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 04:32:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 04:32:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 04:32:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 04:32:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 04:33:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 04:33:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 04:33:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 04:33:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 06:50:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 21:50:10 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 21:50:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 21:50:10 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 21:50:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 21:50:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:53:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 21:53:48 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:53:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 21:53:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 21:53:49 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Aug 2024 21:53:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:53:50 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 21:53:50 GMT
EXPOSE 80
# Thu, 01 Aug 2024 21:53:50 GMT
CMD ["apache2-foreground"]
# Thu, 01 Aug 2024 23:13:02 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 01 Aug 2024 23:13:02 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 01 Aug 2024 23:13:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Aug 2024 23:15:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 01 Aug 2024 23:15:50 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 01 Aug 2024 23:15:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 01 Aug 2024 23:15:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 01 Aug 2024 23:15:52 GMT
VOLUME [/var/www/html]
# Thu, 01 Aug 2024 23:22:06 GMT
ENV JOOMLA_VERSION=5.1.2
# Thu, 01 Aug 2024 23:22:07 GMT
ENV JOOMLA_SHA512=d344506443b403fa662aa4e626e11a76d8666c938f52e497030d4b422205a1cdf21d4457d5943f68eea47e904067f8005b49a6d95432255e772809a3a471d1b0
# Thu, 01 Aug 2024 23:22:11 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.2/Joomla_5.1.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 01 Aug 2024 23:22:12 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 01 Aug 2024 23:22:12 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 01 Aug 2024 23:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Aug 2024 23:22:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d3ec06c5e0e90071038fdee9232ba4133360411125844bff1e22a52304e3c5`  
		Last Modified: Tue, 23 Jul 2024 08:33:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd846de240ae9bfefaac5899b068df5455a7f31a27e33777e570ad4672b5f483`  
		Last Modified: Tue, 23 Jul 2024 08:33:38 GMT  
		Size: 76.2 MB (76166096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ba38eb3f2eb6eb3d8dc7fb73ec6839277b5fa128f0e76530300b9b2c7ea11b`  
		Last Modified: Tue, 23 Jul 2024 08:33:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d3a944b3fc7ab92bd394ccbe902f5a1849f8040bc6b87bb71c55a597806ad4`  
		Last Modified: Tue, 23 Jul 2024 08:34:04 GMT  
		Size: 19.1 MB (19062695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074c49465f19a38077840c8da574714fb625678c76cd49a611c4baf44c5b8da2`  
		Last Modified: Tue, 23 Jul 2024 08:33:59 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563d18616929af33d314b6f921c8aebd71dcf275575b6ac1bf44317795ff3d83`  
		Last Modified: Tue, 23 Jul 2024 08:33:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6974b4d6b3ce5aa536ab97f47b866d6236919d6e14d700c04948aeb92ab3a49d`  
		Last Modified: Thu, 01 Aug 2024 22:45:36 GMT  
		Size: 12.4 MB (12430923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd695692fb928af41d52b8d10a1c7db2ebd2b91ee498f2f528ab20615e5b87a`  
		Last Modified: Thu, 01 Aug 2024 22:45:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00b386f4be24366cac12f857922bda09e317afc726794d08751ae34ab7f6cc3`  
		Last Modified: Thu, 01 Aug 2024 22:45:36 GMT  
		Size: 9.8 MB (9821208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca50f3abd5887bf2342b87de8e5f972208175961d9ebd3f158857481caa94dd8`  
		Last Modified: Thu, 01 Aug 2024 22:45:33 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd37c8754f0cc3db455ee6cc34ae9b0bc46167ea392edfd0d6889b0139484503`  
		Last Modified: Thu, 01 Aug 2024 22:45:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf67375f400392804df9d50f3b046491c521731b84233bb2349e1ae45dc8139`  
		Last Modified: Thu, 01 Aug 2024 22:45:33 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bc7e7cf5b482e102bd9161cf5e190f54e7b3d00d7f5d3e4bdcec46dcb5731c`  
		Last Modified: Thu, 01 Aug 2024 23:32:24 GMT  
		Size: 25.9 MB (25850419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c10fb8d7910d77be910d19b30f10bbc2891f0fed798a2539f49bb6c0884bd1a`  
		Last Modified: Thu, 01 Aug 2024 23:32:24 GMT  
		Size: 26.6 MB (26594851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdc9bf38c1cc95cd6f8e7b1f8375d896ca5bdb8e1b76cdcd4c1b88e7f8c6e87`  
		Last Modified: Thu, 01 Aug 2024 23:32:19 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be5cbb8c9a36f9eb62751bdc696e3ff306b9d9e88cfa59dc001a64d57157024`  
		Last Modified: Thu, 01 Aug 2024 23:32:17 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cc8f5f436fcc2431cf991f84e25a54c614910b406def21e181861308f6cbb1`  
		Last Modified: Thu, 01 Aug 2024 23:32:17 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49aeaff21368d898b5e67d945207cbc5fde5b80ebb6cb4b15002878b9cda1983`  
		Last Modified: Thu, 01 Aug 2024 23:34:12 GMT  
		Size: 23.8 MB (23765919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd29c2ec2bff81edb6571c0107fbb899fd1eb0e325a5d5ab4b79965a03d5dd8`  
		Last Modified: Thu, 01 Aug 2024 23:34:06 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1702a26501e746e31ef91cddde7f45b9241a04a438d3a8721884fbcbed88bd64`  
		Last Modified: Thu, 01 Aug 2024 23:34:06 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.2` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:a496646b81ac378ca8bd2993ceeb6815efb6a616c0c8dee65098aec3e53ea24a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251332763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7912dd64c14840c3ef0b6bd6ba62d4e34dd95014fb6c00e7ce5ca6eb3cf2d211`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 05:09:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 05:09:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 05:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 05:09:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 05:09:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 05:12:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 05:12:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 05:12:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 05:12:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 05:12:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 05:12:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 05:12:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 05:12:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 06:31:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 21:56:08 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 21:56:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 21:56:08 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 21:56:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 21:56:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:59:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 21:59:30 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:59:31 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 21:59:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 21:59:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Aug 2024 21:59:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:59:31 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 21:59:31 GMT
EXPOSE 80
# Thu, 01 Aug 2024 21:59:31 GMT
CMD ["apache2-foreground"]
# Thu, 01 Aug 2024 23:06:41 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 01 Aug 2024 23:06:41 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 01 Aug 2024 23:06:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Aug 2024 23:09:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 01 Aug 2024 23:09:05 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 01 Aug 2024 23:09:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 01 Aug 2024 23:09:06 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 01 Aug 2024 23:09:06 GMT
VOLUME [/var/www/html]
# Thu, 01 Aug 2024 23:14:15 GMT
ENV JOOMLA_VERSION=5.1.2
# Thu, 01 Aug 2024 23:14:15 GMT
ENV JOOMLA_SHA512=d344506443b403fa662aa4e626e11a76d8666c938f52e497030d4b422205a1cdf21d4457d5943f68eea47e904067f8005b49a6d95432255e772809a3a471d1b0
# Thu, 01 Aug 2024 23:14:18 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.2/Joomla_5.1.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 01 Aug 2024 23:14:19 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 01 Aug 2024 23:14:19 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 01 Aug 2024 23:14:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Aug 2024 23:14:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb57d14375011cadb1425f6530fb6a23e2f97cc0ccd6ce600b387796d09b6b4`  
		Last Modified: Thu, 01 Aug 2024 22:46:06 GMT  
		Size: 12.4 MB (12432709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39b2ab2d4dbeb01af65f4e26ea8b6dc08c42116a32407d9d5dde0ffb9d19d3d`  
		Last Modified: Thu, 01 Aug 2024 22:46:03 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ed9c0d97624457fea31353db9846e1bfcc6db53724052a83f379142a61a0f`  
		Last Modified: Thu, 01 Aug 2024 22:46:05 GMT  
		Size: 11.4 MB (11415586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f772d30c25f084365844471f325a8725e11c8a4b82ccc5ab18c719d6a41ffbd5`  
		Last Modified: Thu, 01 Aug 2024 22:46:03 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30ff2b3ecb6636d36b21fd2bf898bae0846d228aa26af91fd4a482bc3267b67`  
		Last Modified: Thu, 01 Aug 2024 22:46:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ed996fa9043a7271019d19116f9c491c392c55ba17f631ddd472bfdd0d973f`  
		Last Modified: Thu, 01 Aug 2024 22:46:03 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480acef61bcbe552bf1d64479b1d4122522a28dd45b123b8111ea42be4a84900`  
		Last Modified: Thu, 01 Aug 2024 23:22:49 GMT  
		Size: 27.0 MB (26996945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bd700bf2e92b8b3ad27e1d763bd2f28ea87af00a1d15dc53ee6a56478bd069`  
		Last Modified: Thu, 01 Aug 2024 23:22:49 GMT  
		Size: 29.1 MB (29078688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02122ed79619b0746dd41a7984961bcd0464e07aef5a912e92c6df03cb24cbab`  
		Last Modified: Thu, 01 Aug 2024 23:22:46 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400bd04d9538c39db5e1f2195fd1985ce4ec14aa85a69573ff956a5d14a0729e`  
		Last Modified: Thu, 01 Aug 2024 23:22:44 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa5729e36da2876a643082e6bc004ca7bb50776bb0f2c0c42113aa9532ae35a`  
		Last Modified: Thu, 01 Aug 2024 23:22:44 GMT  
		Size: 19.1 KB (19149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f30a8b1c56ac5affd94dabf4ba0f30ef82bc8e9352d9564a0eb735fcf0a4abe`  
		Last Modified: Thu, 01 Aug 2024 23:24:19 GMT  
		Size: 23.8 MB (23765949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2888a090fe36f1edebd076b4e1e576cacd999d8599ea982f70399d527f158fe`  
		Last Modified: Thu, 01 Aug 2024 23:24:16 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e71e79b6b5ae681ba6176447767dc64d55ea3a6ac489dcbb1eccf7fa411997`  
		Last Modified: Thu, 01 Aug 2024 23:24:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.2` - linux; 386

```console
$ docker pull joomla@sha256:08b7e707c8fb953ce944afa2366cee0c14ea7924143ebcee97ac95ed571b9fde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258691236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0ae7dde20b8a1a0bc044781ae016ecee5f058985d5962199054416f95416df`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:13 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Tue, 23 Jul 2024 03:54:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:54:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 04:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 04:54:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:54:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 04:54:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 05:01:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 05:01:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 05:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 05:01:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 05:01:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 05:01:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 05:01:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 05:01:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 07:25:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 23 Jul 2024 08:11:50 GMT
ENV PHP_VERSION=8.2.21
# Tue, 23 Jul 2024 08:11:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Tue, 23 Jul 2024 08:11:50 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Tue, 23 Jul 2024 08:12:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Jul 2024 08:12:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 08:17:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 08:17:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 Jul 2024 08:17:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 08:17:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 08:17:51 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 Jul 2024 08:17:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 Jul 2024 08:17:51 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 08:17:51 GMT
EXPOSE 80
# Tue, 23 Jul 2024 08:17:51 GMT
CMD ["apache2-foreground"]
# Tue, 23 Jul 2024 11:20:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 23 Jul 2024 11:20:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 23 Jul 2024 11:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 11:23:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 23 Jul 2024 11:23:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 23 Jul 2024 11:23:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 23 Jul 2024 11:23:30 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 23 Jul 2024 11:23:30 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 11:35:24 GMT
ENV JOOMLA_VERSION=5.1.2
# Tue, 23 Jul 2024 11:35:24 GMT
ENV JOOMLA_SHA512=d344506443b403fa662aa4e626e11a76d8666c938f52e497030d4b422205a1cdf21d4457d5943f68eea47e904067f8005b49a6d95432255e772809a3a471d1b0
# Tue, 23 Jul 2024 11:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.2/Joomla_5.1.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 23 Jul 2024 11:35:30 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Mon, 29 Jul 2024 17:39:57 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Mon, 29 Jul 2024 17:39:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jul 2024 17:39:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34caeeb2ec9b0a871c2808cc5cad03c85e3775d863522099238ac68eda5e4073`  
		Last Modified: Tue, 23 Jul 2024 09:41:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ee053233ee4b919aa7cfb9d47b5f6760be8d3ec7f62e66dd4fe9e6c60e99a7`  
		Last Modified: Tue, 23 Jul 2024 09:41:49 GMT  
		Size: 101.5 MB (101517599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbc19e49f8d18ecebf1bf4f346d396cf87df4d75ee7b99b43a0f051717b7a5a`  
		Last Modified: Tue, 23 Jul 2024 09:41:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fda610fbfb0250b0d7e6b2430595f61c3dad96ed4a2536f3469b9de80d5f57`  
		Last Modified: Tue, 23 Jul 2024 09:42:15 GMT  
		Size: 20.8 MB (20843275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa63e9eb0f2b2ad20ff051c8efa62397470384f5c75a9dbd4d774b6028e8647`  
		Last Modified: Tue, 23 Jul 2024 09:42:11 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1608ceaa879e01156cb06283c35d1871d0cb91db35e47cc469b3da6547a360f`  
		Last Modified: Tue, 23 Jul 2024 09:42:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021fbecd8ebc31f4a1e2cac6275323afb05320f41a4f10939cfbd9a1f6761400`  
		Last Modified: Tue, 23 Jul 2024 09:53:23 GMT  
		Size: 12.4 MB (12439249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5154afd68c480849ced23fe28c8fd3c8c43cf8e7c9e811ff24c251b65f449a`  
		Last Modified: Tue, 23 Jul 2024 09:53:20 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacbae462c9afd3215eedb5d5db0b8577d89c94b2ca6f377d679caf4a0071d6f`  
		Last Modified: Tue, 23 Jul 2024 09:53:24 GMT  
		Size: 11.6 MB (11638507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a884839ad0a54538338675e5ca047bd8369fea8a2cd626e1b48d994e2e647c`  
		Last Modified: Tue, 23 Jul 2024 09:53:20 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec6b1e4c90557afd72214653bdbe14976e80c76302090988c6beb1739497e93`  
		Last Modified: Tue, 23 Jul 2024 09:53:20 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c181733ff49ce9a5c2f5ff4387995dd08348bd7a36cf0f64ed13c85edc1d0395`  
		Last Modified: Tue, 23 Jul 2024 09:53:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640a931dedb99e709253346444bfd16b13699334d332517c7a9f9ad137386ed4`  
		Last Modified: Tue, 23 Jul 2024 11:53:58 GMT  
		Size: 27.5 MB (27526017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea96baa0b21bd1793c0e5031f89c06d501436baff857b3a8eeef56e6bf21a30`  
		Last Modified: Tue, 23 Jul 2024 11:53:58 GMT  
		Size: 30.8 MB (30786277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d90950297339cd58c3d1937ffdc7855063c37067ac66a44379e1b7fa411971a`  
		Last Modified: Tue, 23 Jul 2024 11:53:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f875f34785f0ac7f191b45c7f68eabc8f5e604254d1ab7f284f58b6804765875`  
		Last Modified: Tue, 23 Jul 2024 11:53:47 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149805f6016de56df16e29f6a4e8ea5db606a8edf1c366d8b19b44f31090cf7c`  
		Last Modified: Tue, 23 Jul 2024 11:53:47 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9c6553de6c6d30ac5d881cab3edc82eff6d6473638d62fc6e2501127e269e7`  
		Last Modified: Tue, 23 Jul 2024 11:56:50 GMT  
		Size: 23.8 MB (23765918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b628463bde237895205dffea3650ccd0db8b624e7cfb2f144f8d013a4d977a07`  
		Last Modified: Tue, 23 Jul 2024 11:56:44 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455429732ae8938be2772fe90346fb07210b3a38c615e1ee3fcf2d4592ece272`  
		Last Modified: Mon, 29 Jul 2024 17:45:24 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.2` - linux; mips64le

```console
$ docker pull joomla@sha256:e0afc1032c3f50d1a1168f725250562df16b99488db64f1f61cf2e7ed946c8c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231856124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cd77f3218f82191be0bf060835c11e75a27b8fab94db231fd37bbebdd01e4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 00:37:51 GMT
ADD file:6b0de87e15c6880fed3a8430d23a511322519e32c50677c24f4597141e3a85ff in / 
# Tue, 23 Jul 2024 00:37:56 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:19:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 02:19:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 02:21:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:21:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 02:21:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 02:39:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 02:39:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 02:40:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 02:40:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 02:40:32 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 02:40:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 02:40:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 02:40:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 09:06:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 23 Jul 2024 11:09:41 GMT
ENV PHP_VERSION=8.2.21
# Tue, 23 Jul 2024 11:09:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Tue, 23 Jul 2024 11:09:49 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Tue, 23 Jul 2024 11:10:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Jul 2024 11:10:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 11:25:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 11:26:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 Jul 2024 11:26:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 11:26:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 11:26:16 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 Jul 2024 11:26:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 Jul 2024 11:26:24 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 11:26:28 GMT
EXPOSE 80
# Tue, 23 Jul 2024 11:26:32 GMT
CMD ["apache2-foreground"]
# Tue, 23 Jul 2024 16:55:57 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 23 Jul 2024 16:56:01 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 23 Jul 2024 16:57:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 17:09:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 23 Jul 2024 17:09:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 23 Jul 2024 17:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 23 Jul 2024 17:09:38 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 23 Jul 2024 17:09:43 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 17:59:41 GMT
ENV JOOMLA_VERSION=5.1.2
# Tue, 23 Jul 2024 17:59:46 GMT
ENV JOOMLA_SHA512=d344506443b403fa662aa4e626e11a76d8666c938f52e497030d4b422205a1cdf21d4457d5943f68eea47e904067f8005b49a6d95432255e772809a3a471d1b0
# Tue, 23 Jul 2024 18:00:19 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.2/Joomla_5.1.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 23 Jul 2024 18:00:28 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Mon, 29 Jul 2024 17:18:23 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Mon, 29 Jul 2024 17:18:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jul 2024 17:18:37 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f8de7af9de8596141237ef7c589f08f773ca8ce07671b2bd7e192055d5165f74`  
		Last Modified: Tue, 23 Jul 2024 00:49:06 GMT  
		Size: 29.1 MB (29124926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c291bad035220479aa755b3760aafa2f0c35b3630221446a2a23560ae57dcde`  
		Last Modified: Tue, 23 Jul 2024 15:01:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef84f4d9e1061839dd0c2a34ac2cc878fc5ed53d24b7a4ee365a691ff820797`  
		Last Modified: Tue, 23 Jul 2024 15:02:25 GMT  
		Size: 80.7 MB (80666170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6ff158946a50e927e4a8d94ae605cf7b5150056822a73dd77732f66174bc55`  
		Last Modified: Tue, 23 Jul 2024 15:01:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dffd4a590a8ca7454b24dced962a920734a2d6e96f361c6d65d00d45fdd9468`  
		Last Modified: Tue, 23 Jul 2024 15:03:07 GMT  
		Size: 20.1 MB (20069509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9c13823200c80add69ff1448c78da4340995a04d656e8038a04ce6f32ab2f7`  
		Last Modified: Tue, 23 Jul 2024 15:02:53 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb0aa679528670d613e2331dd23c425c19bdd0c3594d88b82c996b88f5d2847`  
		Last Modified: Tue, 23 Jul 2024 15:02:53 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a67dd9d4f0c9b3c6778a2a834f8d8dd2d02593f93bccfe6329432915847869`  
		Last Modified: Tue, 23 Jul 2024 15:22:24 GMT  
		Size: 12.2 MB (12233407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfc293e86bcf9e39f8ae3261b60afc3061ace4313602f2b71f98623d7669e5e`  
		Last Modified: Tue, 23 Jul 2024 15:22:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54372a80f57114f0b3819d59555487788fac994228b2b96fe963f3586bbc817e`  
		Last Modified: Tue, 23 Jul 2024 15:22:27 GMT  
		Size: 10.5 MB (10485285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adb9073ac4bea54cf2e38badd662b860636d14241fddbacfbdeb32686ed3379`  
		Last Modified: Tue, 23 Jul 2024 15:22:19 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cea49f6c3e818c19484ec8c9ed7b854e1bb4f49b5d1c2e43a37575d3f23f89`  
		Last Modified: Tue, 23 Jul 2024 15:22:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a023ad4014d801db852e1e4d6ee1547ce121745a6575c7dcd885b1f6c408b7`  
		Last Modified: Tue, 23 Jul 2024 15:22:19 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e03520e669aa2ab9488c897d53972e55b7b2bf37e6db5d4ba8b080f81140925`  
		Last Modified: Tue, 23 Jul 2024 19:10:21 GMT  
		Size: 26.9 MB (26912027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dabae0413d410e7b32b7342dcd07d0ea1d8e1c1f3a796d27ed3417dca63cbb5`  
		Last Modified: Tue, 23 Jul 2024 19:10:29 GMT  
		Size: 28.6 MB (28567018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b27029b4d825b9a24d89e799da395dd852cec5cfd010baf07b07afde01de91`  
		Last Modified: Tue, 23 Jul 2024 19:09:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6d4bf9b3efdf6b51c6f08112a9f56191357510555923a54e2342e0b6176bd4`  
		Last Modified: Tue, 23 Jul 2024 19:09:55 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d8a36d3561a98cdc2248940a1fa39c6829b977c57f2c0c2db895de44021c6d`  
		Last Modified: Tue, 23 Jul 2024 19:09:55 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b241f990fdd55885be9a4cfe4d06158b0f5b11765cff2840a6b21fc98dff99`  
		Last Modified: Tue, 23 Jul 2024 19:16:02 GMT  
		Size: 23.8 MB (23767662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b09367bcbc680be542ee303f990713ce551a9bf5770095eab36e726e7d101a`  
		Last Modified: Tue, 23 Jul 2024 19:15:39 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50efbe3dd654a61394e5845aad97b8a8227f612f80a3e815ff9f5d6a573de6ac`  
		Last Modified: Mon, 29 Jul 2024 17:28:27 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.2` - linux; ppc64le

```console
$ docker pull joomla@sha256:61464c287c55afd700e72af9e38278753696ba72378c297771c8526edda44028
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265938695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d86d0d89d5895d22833f599cae0ef20f469f44b34117ecd913ed5af47f90c84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:46:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 02:47:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 02:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:47:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 02:47:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 02:51:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 02:51:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 02:51:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 02:51:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 02:51:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 02:51:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 02:51:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 02:51:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 04:06:52 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 23 Jul 2024 04:31:13 GMT
ENV PHP_VERSION=8.2.21
# Tue, 23 Jul 2024 04:31:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Tue, 23 Jul 2024 04:31:14 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Tue, 23 Jul 2024 04:31:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Jul 2024 04:31:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 04:34:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 04:34:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 Jul 2024 04:34:28 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 04:34:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 04:34:29 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 Jul 2024 04:34:30 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 Jul 2024 04:34:30 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 04:34:30 GMT
EXPOSE 80
# Tue, 23 Jul 2024 04:34:31 GMT
CMD ["apache2-foreground"]
# Tue, 23 Jul 2024 06:02:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 23 Jul 2024 06:02:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 23 Jul 2024 06:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 23 Jul 2024 06:06:52 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 23 Jul 2024 06:06:53 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 23 Jul 2024 06:06:55 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 23 Jul 2024 06:06:55 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 06:21:23 GMT
ENV JOOMLA_VERSION=5.1.2
# Tue, 23 Jul 2024 06:21:24 GMT
ENV JOOMLA_SHA512=d344506443b403fa662aa4e626e11a76d8666c938f52e497030d4b422205a1cdf21d4457d5943f68eea47e904067f8005b49a6d95432255e772809a3a471d1b0
# Tue, 23 Jul 2024 06:21:32 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.2/Joomla_5.1.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 23 Jul 2024 06:21:34 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Mon, 29 Jul 2024 17:20:50 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Mon, 29 Jul 2024 17:20:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jul 2024 17:20:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679744addd25c44b49c10b6d0881679a0285af40dabbd99b4006332b338823e3`  
		Last Modified: Tue, 23 Jul 2024 05:17:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0c4608463aeeae784b14fc3e81ca8b4b81bd60e1b7a34823399adca9b770d5`  
		Last Modified: Tue, 23 Jul 2024 05:18:13 GMT  
		Size: 103.3 MB (103319086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f792a79caaf61b5ad5c6975df0f029f85e03b8e4560339110102763bde450248`  
		Last Modified: Tue, 23 Jul 2024 05:17:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbcbd591db67cc93879717462625294983b0ea984ec7daeb3ce7a2f84b49a60`  
		Last Modified: Tue, 23 Jul 2024 05:18:38 GMT  
		Size: 21.5 MB (21511417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe64cbce59d87195b9dab5e2f77c18dd42c43726b1d403e26b4aae6195ecdb7`  
		Last Modified: Tue, 23 Jul 2024 05:18:34 GMT  
		Size: 442.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b032e6ddf45fcdb0a5bcb1a93b94de425b9b38e0283696ffca9b79b528f7bbca`  
		Last Modified: Tue, 23 Jul 2024 05:18:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb04ab356a9cbf43bb5cae924cb21b65bcb872255f05ddfb0498dc302d77c78`  
		Last Modified: Tue, 23 Jul 2024 05:28:44 GMT  
		Size: 12.4 MB (12439479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9deadc2f0947522843c0db43b8a4eb62444195ac333fc460b8c3490fdd11f047`  
		Last Modified: Tue, 23 Jul 2024 05:28:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7901e2964f1a5ff1439d30a37e1aa375cd500e7fa5c58288daf7dfe0ca078b`  
		Last Modified: Tue, 23 Jul 2024 05:28:43 GMT  
		Size: 11.8 MB (11819426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696f569d5bb5396488646a76b13c9129a720e5721059c3e2a7c0f35bb8cb7345`  
		Last Modified: Tue, 23 Jul 2024 05:28:41 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb2fc48d2b2ec1e727ade89c70d20b49837fa895e31fc8f69b5d861b77e7a96`  
		Last Modified: Tue, 23 Jul 2024 05:28:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82caf1c6b06f7c22c75e0f9a203b324b948aeb0260334cce4dfed3e83d9058ca`  
		Last Modified: Tue, 23 Jul 2024 05:28:41 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9482e616aa4eb2bda65532cea0905386a8f566058bc9900348a0235ac1b861b9`  
		Last Modified: Tue, 23 Jul 2024 06:41:50 GMT  
		Size: 28.3 MB (28323223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ff4c3b052e75ec72ca291901ea6920074aecf909ff57c5e48480f283e6c07f`  
		Last Modified: Tue, 23 Jul 2024 06:41:52 GMT  
		Size: 31.6 MB (31607761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6a981942ef092c011a3d9170b7892a5c99a7aba6472db08cee49e8e20f699b`  
		Last Modified: Tue, 23 Jul 2024 06:41:45 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018024b06f6c3bdb844a99e84434a5e9b36923395a10d500f912dd2f2e7b1677`  
		Last Modified: Tue, 23 Jul 2024 06:41:43 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9d98769aba31ce86ae5526622da9543337bc14ec62a7fbdb01b82ffb2ff112`  
		Last Modified: Tue, 23 Jul 2024 06:41:43 GMT  
		Size: 19.2 KB (19161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96c299247e7ad1dfc669ee692c17b6d0746e38e306e6121d46651481145374b`  
		Last Modified: Tue, 23 Jul 2024 06:44:38 GMT  
		Size: 23.8 MB (23765915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4c6e6ae5ae053c8eca00fb56afce27a566317807e4518111e2ddf7826984bc`  
		Last Modified: Tue, 23 Jul 2024 06:44:30 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b665c84612ad4d3fe6ffb9dbf49c994a885649c3483d85f6fd05194e0bcf1c32`  
		Last Modified: Mon, 29 Jul 2024 17:26:13 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.2` - linux; s390x

```console
$ docker pull joomla@sha256:68ca08992ca44aea70e93b959bee3dfdfdcb4014cccae6d01ecffe73dc844b7e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230165099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c071936126ca1fd24eee1cb54d54d6ad1865b20c24eb17e4ebc8d4abdec870bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:49 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Tue, 23 Jul 2024 02:27:50 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:42:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 03:42:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 03:42:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:42:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 03:42:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 03:45:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 03:45:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 03:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 03:45:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 03:45:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 03:45:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 03:45:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 03:45:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 05:01:39 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 23 Jul 2024 05:25:04 GMT
ENV PHP_VERSION=8.2.21
# Tue, 23 Jul 2024 05:25:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Tue, 23 Jul 2024 05:25:04 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Tue, 23 Jul 2024 05:25:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Jul 2024 05:25:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 05:27:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 05:27:45 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 Jul 2024 05:27:46 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 05:27:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 05:27:46 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 Jul 2024 05:27:46 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 Jul 2024 05:27:46 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 05:27:46 GMT
EXPOSE 80
# Tue, 23 Jul 2024 05:27:47 GMT
CMD ["apache2-foreground"]
# Tue, 23 Jul 2024 07:29:42 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 23 Jul 2024 07:29:42 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 23 Jul 2024 07:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 07:32:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 23 Jul 2024 07:32:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 23 Jul 2024 07:32:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 23 Jul 2024 07:32:12 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 23 Jul 2024 07:32:12 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 07:42:53 GMT
ENV JOOMLA_VERSION=5.1.2
# Tue, 23 Jul 2024 07:42:53 GMT
ENV JOOMLA_SHA512=d344506443b403fa662aa4e626e11a76d8666c938f52e497030d4b422205a1cdf21d4457d5943f68eea47e904067f8005b49a6d95432255e772809a3a471d1b0
# Tue, 23 Jul 2024 07:42:58 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.2/Joomla_5.1.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 23 Jul 2024 07:43:01 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Mon, 29 Jul 2024 17:44:45 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Mon, 29 Jul 2024 17:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jul 2024 17:44:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cfba21730315054a9974bd81d57f4a0af83b3bce0ec602a8f39389526bc2a1`  
		Last Modified: Tue, 23 Jul 2024 06:11:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd83f19e63f8d7e6b0b418799c2fb3484a9b57681a15bb5c58dce953d894962`  
		Last Modified: Tue, 23 Jul 2024 06:11:47 GMT  
		Size: 80.8 MB (80816895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be2e88b5706d13997a405886ca83d6ee622ee824201de072a4e20126cf86513`  
		Last Modified: Tue, 23 Jul 2024 06:11:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb79cf9c2bd490848a9ac73af98b8cefb3d122a50b2cbb486d0fb3ae2a8db97f`  
		Last Modified: Tue, 23 Jul 2024 06:12:04 GMT  
		Size: 20.1 MB (20100185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4025c7bae49c61bc1bff1636e41c0224459752e9c72ebe99611290e1666f6e46`  
		Last Modified: Tue, 23 Jul 2024 06:12:01 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86355c71c575018477f6144acf0b48c2c5ab63f1264d4aeaa532f87ef04b7b08`  
		Last Modified: Tue, 23 Jul 2024 06:12:02 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061f84dd80b1feb7eb73ab08093900e12c30566afc03c54416082a8379efb56f`  
		Last Modified: Tue, 23 Jul 2024 06:19:36 GMT  
		Size: 12.4 MB (12438611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bbca816bc846117ddd76ea0db88deee30f219514f268e7458e7c4489e61d9c`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e00239342e2e2d95cd4a2a1fd94a3aaaccaaa8e5ea86c40a32f4d2514430ab6`  
		Last Modified: Tue, 23 Jul 2024 06:19:36 GMT  
		Size: 10.6 MB (10639853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e0e80beddd1b6cc0f0d3021338d8a05ce0ffaaa003754b62683ab4903690c7`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af6b58d4a7c6dc9f0d3c45e50f102d26d519e8eee83ae22ff07a379fc05867e`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa2189971768087d257369eaf7c8f4422424b497302bf1a537f4e8d672314f0`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3a3784c1000dfcc26126fbff00aae5b43bedbb1b00669f535c4b84e165f901`  
		Last Modified: Tue, 23 Jul 2024 07:55:32 GMT  
		Size: 26.7 MB (26701073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ef6442f4e7057385cb2eebd00dd66574f343c882685620799db38513dee10`  
		Last Modified: Tue, 23 Jul 2024 07:55:33 GMT  
		Size: 28.2 MB (28182395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0848cbc71d41bcda1f30889967d0ebffe466d420f5c517604451243aae6567`  
		Last Modified: Tue, 23 Jul 2024 07:55:28 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb51dbab456adad503e5e1a22c70e9a8a82abcef7cded37e9a61fccb8d44c07`  
		Last Modified: Tue, 23 Jul 2024 07:55:27 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf715019151ebd04480f226f79bccf13deca41f14b3b5f23e357e3b6aa057e`  
		Last Modified: Tue, 23 Jul 2024 07:55:27 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc44a1b6dec0f7e9961772f6563b0238d96d9577caae7441bbf403d57ba11d`  
		Last Modified: Tue, 23 Jul 2024 07:57:20 GMT  
		Size: 23.8 MB (23765919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8876d9eaf3e35377b4a847a356358870878791c06fd2ff05823e9025d36bc2`  
		Last Modified: Tue, 23 Jul 2024 07:57:14 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84109e6e895b217b41af183e4c8dd5360e16ca351ad4d63d8c18383535adc3c9`  
		Last Modified: Mon, 29 Jul 2024 17:49:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
