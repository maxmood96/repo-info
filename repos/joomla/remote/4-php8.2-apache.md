## `joomla:4-php8.2-apache`

```console
$ docker pull joomla@sha256:4594f9dc554cf9cc8b9727cb61ad1a65e1ded6868b1b737222da48d8e4e468d2
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

### `joomla:4-php8.2-apache` - linux; amd64

```console
$ docker pull joomla@sha256:bf9b06c67a3a90047c8df16f42c8302dc0e9826145535d735ebcacceb14ee94b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261366485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5caaaf646f4250723d203382108bbffa53896cc99feff88be54696c5eba500e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:17:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:17:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:17:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:17:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:21:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:21:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:21:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:22:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:52:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:17:08 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:17:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:17:08 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:17:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:17:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:20:53 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:20:54 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:20:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:20:54 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:20:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:20:54 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:20:54 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:20:54 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 02:38:13 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 25 Oct 2024 02:38:13 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 25 Oct 2024 02:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 02:58:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 25 Oct 2024 02:58:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 02:58:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 25 Oct 2024 02:58:26 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Fri, 25 Oct 2024 02:58:26 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 02:58:26 GMT
ENV JOOMLA_VERSION=4.4.9
# Fri, 25 Oct 2024 02:58:26 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Fri, 25 Oct 2024 02:58:32 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 25 Oct 2024 02:58:33 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Fri, 25 Oct 2024 02:58:33 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Fri, 25 Oct 2024 02:58:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Oct 2024 02:58:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ab1cc5ca33d8382a34578c5ac4fec4d1f4a381d747e3c9d2e8fd8bdc20b621`  
		Last Modified: Thu, 17 Oct 2024 04:18:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ee5e1490ca9e76fb6078eb2581366decdceea48fa3e65583e2c80e10522849`  
		Last Modified: Thu, 17 Oct 2024 04:19:14 GMT  
		Size: 104.3 MB (104346971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e807ae4973d0b87fd52b4704132912240c54d7c5110dabfbd3e5032ca5249eec`  
		Last Modified: Thu, 17 Oct 2024 04:18:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1846dfbe9adb998f8c506143dfcf02b7dee1b6b39ba6746202c87e2f3e41ff`  
		Last Modified: Thu, 17 Oct 2024 04:19:36 GMT  
		Size: 20.3 MB (20327779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f1d0bbde8147dd947d4227d005cf449ab44cfefebf706b899000054185f9d7`  
		Last Modified: Thu, 17 Oct 2024 04:19:33 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fac5e585cd612eddd957e7c3edb4712bfabc4f504eb4a72e6dc5088776b51b0`  
		Last Modified: Thu, 17 Oct 2024 04:19:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c65c4fca52e66ad639ef8f1b89254b614c937ca676ee12c88c10ef03163b32f`  
		Last Modified: Fri, 25 Oct 2024 02:19:22 GMT  
		Size: 12.5 MB (12459142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2e2799aa38d234b5907b767a6da9cab47e91e6d50b721e6d0156d451fbad8e`  
		Last Modified: Fri, 25 Oct 2024 02:19:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54527c6f928b18fe9aef233c061c29d980603a47607954003ab00bc703bdcce`  
		Last Modified: Fri, 25 Oct 2024 02:19:21 GMT  
		Size: 11.4 MB (11411365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d76291219c34281af41ae9436d8f53096e1059fa1ac9ed2bdebdd77d190ff12`  
		Last Modified: Fri, 25 Oct 2024 02:19:19 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e14935230bbc66875d6e9b6b234732cb402089ab8e04e6704f5830ec8e9be2`  
		Last Modified: Fri, 25 Oct 2024 02:19:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cbeb13063d7e707ba17678d2ee4cf2ff4fa5608fdc3bc1111435561ff46b09`  
		Last Modified: Fri, 25 Oct 2024 02:19:19 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ebedff7e95c370ac6b46c6c19dcd3f6df1e962bfbd9516b2bcac543af8393f`  
		Last Modified: Fri, 25 Oct 2024 03:07:34 GMT  
		Size: 26.3 MB (26255161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d566818e1a9f3b2dfa48138f69e89896732be585295e448261e7d19f5bc357e9`  
		Last Modified: Fri, 25 Oct 2024 03:07:35 GMT  
		Size: 31.5 MB (31496596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badd87ebb6275e326e9545569f904d8687dc610e611d66681a4f32532180cc0a`  
		Last Modified: Fri, 25 Oct 2024 03:07:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303c82660aadbc3f06cc5d98d1d16151a035e161188787eef35e1d245cc405b3`  
		Last Modified: Fri, 25 Oct 2024 03:07:28 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99ebfe77d07e817eb0eb215d9cadc86cc75f8e8a1fdcdf4c13a2bbf18290f1e`  
		Last Modified: Fri, 25 Oct 2024 03:07:28 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cf5ddf314d407aacf22a42d2c362b7e03cbdd47fd1b44bd35328b8e387b71`  
		Last Modified: Fri, 25 Oct 2024 03:07:33 GMT  
		Size: 25.9 MB (25913076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0330382cf75beb407dcdec33c8d8acff8e3bc05eead64dd1680a2e934db29e`  
		Last Modified: Fri, 25 Oct 2024 03:07:28 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de9e015853aa27e416f7dd0d54766163de1853526f1f15f2da7c7274f65c047`  
		Last Modified: Fri, 25 Oct 2024 03:07:28 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:a2a7d3aa83370c2be8c26676d1b2afc0f5f729e0401ea60a81f8f7812a2e456f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231206050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a52317a254555622e74d38efe8b25308f984436ddbb2d5b46a20e0c00898bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:28 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 17 Oct 2024 00:54:29 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:39:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:39:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:40:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:40:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:40:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:48:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:48:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:48:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:48:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:48:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:48:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:48:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:09:07 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 00:35:17 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 00:35:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 00:35:18 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 00:35:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 00:35:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:40:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 00:40:30 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:40:31 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 00:40:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 00:40:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 00:40:32 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:40:32 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 00:40:32 GMT
EXPOSE 80
# Fri, 25 Oct 2024 00:40:32 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 01:11:32 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 25 Oct 2024 01:11:32 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 25 Oct 2024 01:25:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 01:28:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 25 Oct 2024 01:28:46 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 01:28:47 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 25 Oct 2024 01:28:48 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Fri, 25 Oct 2024 01:28:48 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 01:28:48 GMT
ENV JOOMLA_VERSION=4.4.9
# Fri, 25 Oct 2024 01:28:48 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Fri, 25 Oct 2024 01:28:58 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 25 Oct 2024 01:28:59 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Fri, 25 Oct 2024 01:28:59 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Fri, 25 Oct 2024 01:28:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Oct 2024 01:29:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5235299add7bb4a13b494a07f66eb5939b6cb20e1cc0d0f75550967a7376c`  
		Last Modified: Thu, 17 Oct 2024 03:45:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8907632e889fbd259ac6ebe1d70401840bf18fb005d7c35952efd42916d520`  
		Last Modified: Thu, 17 Oct 2024 03:45:21 GMT  
		Size: 82.0 MB (81995968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6a7f456b58f9278213fe4b51fb3844191e9e472c54adce160d2e3ebea1c81e`  
		Last Modified: Thu, 17 Oct 2024 03:45:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19743805d7cb37913f1b3f1b2cf18aa012ad377a421c22b0a52997bbc49d64e5`  
		Last Modified: Thu, 17 Oct 2024 03:45:46 GMT  
		Size: 19.6 MB (19624385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d056f964ef6cf0cfd02b1e7ab1e9df4a4500d9af80762867bf9f4da4ee999f9e`  
		Last Modified: Thu, 17 Oct 2024 03:45:42 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a567fd2c394a19ce53e7a88c0cef2c03c411330889c3b51677db7bd9d1fa408`  
		Last Modified: Thu, 17 Oct 2024 03:45:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19051b235de6dfbfb33dbb4563b65db22d8cc50e32ee918ff27a1005c9e15238`  
		Last Modified: Fri, 25 Oct 2024 00:55:24 GMT  
		Size: 12.5 MB (12457446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3372071af8134f9af497a3fecbc2f41b997a999e496991e046834bfc1fe4cd6c`  
		Last Modified: Fri, 25 Oct 2024 00:55:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea77592d248ec01d8ba9ee5913e4788f1588b00a99cffa7106cb28251564ab63`  
		Last Modified: Fri, 25 Oct 2024 00:55:24 GMT  
		Size: 10.4 MB (10395166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eae1544b7f8f18792fda85e7fa6d60683402b2e54735b0854195e8da97c5bb1`  
		Last Modified: Fri, 25 Oct 2024 00:55:21 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800893d28af528dd5f0dd74fb563e8cc644678420648b2ee9a24e5df6e74617e`  
		Last Modified: Fri, 25 Oct 2024 00:55:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cecafa4446a8d5fe60aba51d2d57b102ef7c73ebfa77efb9f7fd85559a74db`  
		Last Modified: Fri, 25 Oct 2024 00:55:21 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573db5fa1c837f71e733b4e60747f48a9b8dd3a20e8b3acb9b80c6f700fe843e`  
		Last Modified: Fri, 25 Oct 2024 01:35:20 GMT  
		Size: 25.7 MB (25706036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f62996a398a42582741d0d07f01943ac04f6b3868d940c6a5eb23500e09af`  
		Last Modified: Fri, 25 Oct 2024 01:35:20 GMT  
		Size: 28.2 MB (28196557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed91b5726be4a59dc36c985a71e1591708741ae5c654a37233a40102ca9cb93`  
		Last Modified: Fri, 25 Oct 2024 01:35:11 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87393ace868871d1113d548b7d116a6a647ac4ce83869b82e75db4dc6d4329b`  
		Last Modified: Fri, 25 Oct 2024 01:35:10 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d00b07ea76c28584b99b6ce874a6bf738034171d1fd2c3e3273bc017e69291`  
		Last Modified: Fri, 25 Oct 2024 01:35:09 GMT  
		Size: 19.2 KB (19155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b607d7f38a8961bee0abdb722e0836f6c63f414dac6f11f1e0f6b4283f70779`  
		Last Modified: Fri, 25 Oct 2024 01:35:19 GMT  
		Size: 25.9 MB (25913080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194eda1993d80ec52c182f3961974444200daabaadad9bcb28f482113b379e32`  
		Last Modified: Fri, 25 Oct 2024 01:35:09 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732fc17d397f069e574820a049aa521ec813c833e7e12fa468f0fb26c3e5dc2c`  
		Last Modified: Fri, 25 Oct 2024 01:35:09 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:1b1d3754119c2453dc04e07ed732419df82b4971c14fd2abfe8b6f81afcc4554
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219836740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a35d1a24062ae2846c05630c42400a490a24507de98b35df2f4c27df7a82589`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:43:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 03:43:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 03:44:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:44:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 03:44:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 03:47:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 03:47:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 03:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 03:47:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 03:47:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 03:47:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 04:55:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 05:17:32 GMT
ENV PHP_VERSION=8.2.24
# Thu, 17 Oct 2024 05:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 17 Oct 2024 05:17:33 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 17 Oct 2024 05:17:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 05:17:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:20:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 05:20:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:20:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 05:20:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 05:20:27 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 05:20:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 05:20:27 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 05:20:28 GMT
EXPOSE 80
# Thu, 17 Oct 2024 05:20:28 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 06:51:05 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 17 Oct 2024 06:51:05 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 17 Oct 2024 07:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 07:11:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 17 Oct 2024 07:11:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 07:11:28 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 17 Oct 2024 07:11:28 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 17 Oct 2024 07:11:28 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 07:11:28 GMT
ENV JOOMLA_VERSION=4.4.9
# Thu, 17 Oct 2024 07:11:28 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Thu, 17 Oct 2024 07:11:36 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 17 Oct 2024 07:11:36 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 17 Oct 2024 07:11:36 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 17 Oct 2024 07:11:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Oct 2024 07:11:37 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57816ea258091707b20fd42869f1859c1543e794b483b8003de268daf39132a0`  
		Last Modified: Thu, 17 Oct 2024 06:00:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f29e3f6b59ec149599415083926b75214bfab19a179c7ef4d7535bbee364a84`  
		Last Modified: Thu, 17 Oct 2024 06:00:36 GMT  
		Size: 76.2 MB (76163462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace57af7e6d627dfdf6574de994827570ba429858c8118ccf5028e7c121e0e9b`  
		Last Modified: Thu, 17 Oct 2024 06:00:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9863416241c1e20444861f13ebb223232950439972781be1e45b6704fee41682`  
		Last Modified: Thu, 17 Oct 2024 06:00:59 GMT  
		Size: 19.1 MB (19062321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300e0800b02d2903ba85150c9b5f31cab1e364d99e199b1614838bb031e1116c`  
		Last Modified: Thu, 17 Oct 2024 06:00:56 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11748bf3dd7f577b46d343e58bff8badc4bb124233ef94312a971750f9db7079`  
		Last Modified: Thu, 17 Oct 2024 06:00:56 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a79a5772590bdea68581af8a61ec825079e9f2559ae36d96e177ba2af5b3a93`  
		Last Modified: Thu, 17 Oct 2024 06:10:39 GMT  
		Size: 12.4 MB (12441483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0daadb137522ebd25811de579fa90cd7d5bfcde9c99ac03b6c967709727b2d8`  
		Last Modified: Thu, 17 Oct 2024 06:10:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769c73bbd0b724bd005a7656a2ed20f445cb38489e3b6570aedcc1609fd1746a`  
		Last Modified: Thu, 17 Oct 2024 06:10:38 GMT  
		Size: 9.8 MB (9825893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b58b18058dd164bbea7be7c1280247606d068f2acb45fff3ad20a11383a4292`  
		Last Modified: Thu, 17 Oct 2024 06:10:36 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1971991714c968d8aab02b2e589465cc8e146c812b76b41674e58bc33c907ee3`  
		Last Modified: Thu, 17 Oct 2024 06:10:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ee1a85056ab65c49ef7c50ec1cbe6789b2b073129aee04318b321dd24f1f3f`  
		Last Modified: Thu, 17 Oct 2024 06:10:36 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1537d48e1b09fa388beb2c1b5c2ec29c4369526674f384d48301ad9e8eec2344`  
		Last Modified: Thu, 17 Oct 2024 07:18:46 GMT  
		Size: 25.1 MB (25076307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35ea337d96ebafe1c47a4a34a42918f935437b868f624994a11c7f08cbed415`  
		Last Modified: Thu, 17 Oct 2024 07:18:46 GMT  
		Size: 26.6 MB (26605934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a7d140af60196f88267fa67cd513ba5a6b572b4fec6c2409f2726c5134d5b0`  
		Last Modified: Thu, 17 Oct 2024 07:18:42 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36654b03468f6c6dab73b32ea6eaf628cdc6127ab33e5a63b5a49c17a26a23fe`  
		Last Modified: Thu, 17 Oct 2024 07:18:40 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f650beb3a50a437e11ab608029d482af414318716fd874761c6450da81cc20f`  
		Last Modified: Thu, 17 Oct 2024 07:18:40 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893a0f00399a69d1dbb5bee120a5c9418dd2b6c2d71daa3148746548be586228`  
		Last Modified: Thu, 17 Oct 2024 07:18:45 GMT  
		Size: 25.9 MB (25913062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6efaaa9ee475ea5574668280bad0da00c11ca4ad2e889fba95af447fb4172ba`  
		Last Modified: Thu, 17 Oct 2024 07:18:40 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1641af79d46e982e99384f70dc4e2617fd26dfaca6089a2a60619357cdad65ef`  
		Last Modified: Thu, 17 Oct 2024 07:18:40 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:9d793a69a80c7567fcf0edc012da6e3577d7d2c94e17646d90239c586b1046f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252702577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6e4ae2aba8b008b0b6bf12abbc686c313191304c768174f5c1c1d6d102cd61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:35:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:35:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:35:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:35:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:35:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:38:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:38:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:38:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:38:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:38:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:38:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:59:56 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 01:23:47 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 01:23:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 01:23:47 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 01:23:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 01:23:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:27:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:27:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:27:12 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:27:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:27:12 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 01:27:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:27:12 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:27:12 GMT
EXPOSE 80
# Fri, 25 Oct 2024 01:27:12 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 02:52:32 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 25 Oct 2024 02:52:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 25 Oct 2024 03:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 03:10:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 25 Oct 2024 03:10:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 03:10:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 25 Oct 2024 03:10:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Fri, 25 Oct 2024 03:10:31 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 03:10:31 GMT
ENV JOOMLA_VERSION=4.4.9
# Fri, 25 Oct 2024 03:10:31 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Fri, 25 Oct 2024 03:10:36 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 25 Oct 2024 03:10:37 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Fri, 25 Oct 2024 03:10:37 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Fri, 25 Oct 2024 03:10:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Oct 2024 03:10:37 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6530e6e936cdf7969275d55704b89e0466613540a41ab09fa6edc24a35d57e8`  
		Last Modified: Thu, 17 Oct 2024 04:17:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ffd48d74a0a5446013c25727b2812f6f385b0ffe0ff99f0439d18dad5e5e8c`  
		Last Modified: Thu, 17 Oct 2024 04:17:25 GMT  
		Size: 98.1 MB (98131870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7046151abb10af1a2158520721c2b5006584c918b2f36fdb943a5dc36edebe22`  
		Last Modified: Thu, 17 Oct 2024 04:17:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cbece021606df0e0fd4b7b7123856cec73a741c16c93632a0050521f432385`  
		Last Modified: Thu, 17 Oct 2024 04:17:48 GMT  
		Size: 20.3 MB (20325322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce14de3b55afb7a464228d842abfe056cbe1fc2d0809fc69a0206aa13dbdc345`  
		Last Modified: Thu, 17 Oct 2024 04:17:45 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f9962d8983968c3cbbc14b531cea8c72c6c3e0f3e8f36dd3838319b579fc16`  
		Last Modified: Thu, 17 Oct 2024 04:17:45 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5125b3b76c5ba0e6724648c8f4798af50b98e90bd375ae1811f1deeab36faa5`  
		Last Modified: Fri, 25 Oct 2024 02:22:12 GMT  
		Size: 12.5 MB (12458887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ee3ecc14b867ddd8874bfd50ef49db513b3e610e4c5c276ff39039415772c`  
		Last Modified: Fri, 25 Oct 2024 02:22:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848c5be4a9e5a145c773bde98431924758e9e0a39522b86a065c1546ec5e46da`  
		Last Modified: Fri, 25 Oct 2024 02:22:11 GMT  
		Size: 11.4 MB (11419330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e059d1686fe3ea39a3679a73b0a8edee2c9fecb353c15f38fc9047bfec9a9b04`  
		Last Modified: Fri, 25 Oct 2024 02:22:09 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa7e7c0785a7bc161d801044e1a2f01dd87249769446664e7f4adad10597eaf`  
		Last Modified: Fri, 25 Oct 2024 02:22:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d420417b0cb4572f3beba13f282a9d028174c4dfc97e2394f6b618fec3703f8a`  
		Last Modified: Fri, 25 Oct 2024 02:22:09 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c28f5edeaa1a6c0ee58b68326be1c43c106188f0e2ff4af02853beaedc10fc`  
		Last Modified: Fri, 25 Oct 2024 03:19:03 GMT  
		Size: 26.2 MB (26174971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200c8191edee817f399db1a4ff647c08f2797be43135b2c9cc79a3b064403ce6`  
		Last Modified: Fri, 25 Oct 2024 03:19:03 GMT  
		Size: 29.1 MB (29092711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe2ebe1dd983028e706efe1a2a743e9709f74c768f0eec05d34f976c4d0a96b`  
		Last Modified: Fri, 25 Oct 2024 03:19:00 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2683da3e8f6ed04b4db768b52c7cb7a5e38933084f78aee978caee61f2ddde`  
		Last Modified: Fri, 25 Oct 2024 03:18:58 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e499ff283fb1cdec95a86a5b210bbf5f6d1bc33346c106c79347629ce533493`  
		Last Modified: Fri, 25 Oct 2024 03:18:58 GMT  
		Size: 19.1 KB (19149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15e80285a029253f457864c1a647d0b17a645291307ab5b0498ec91d9095f71`  
		Last Modified: Fri, 25 Oct 2024 03:19:02 GMT  
		Size: 25.9 MB (25913062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0a8bad66365b020ef0a2914f548546f9175d4390b089029051565f0ee2e058`  
		Last Modified: Fri, 25 Oct 2024 03:18:58 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ec380957e8e3ca687f913f551504cba14578fc6621c26ac19759491de156f0`  
		Last Modified: Fri, 25 Oct 2024 03:18:58 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; 386

```console
$ docker pull joomla@sha256:f891991935d98eb8ec01df40715e07cff69bc5bec5a6bf300462983fcec857d0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260021287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c964bb8a9dfc6f70ad7ddc2c77a91360aea42c5fcb50e158efba707cf6f22a30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:56 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 17 Oct 2024 00:38:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:15:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:15:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:15:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:15:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:15:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:22:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:22:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:22:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:22:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:22:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:22:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 03:51:18 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 04:38:04 GMT
ENV PHP_VERSION=8.2.24
# Thu, 17 Oct 2024 04:38:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 17 Oct 2024 04:38:04 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 17 Oct 2024 04:38:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 04:38:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:44:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 04:44:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:44:19 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 04:44:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 04:44:19 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 04:44:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 04:44:19 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 04:44:19 GMT
EXPOSE 80
# Thu, 17 Oct 2024 04:44:20 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 06:44:48 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 17 Oct 2024 06:44:48 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 17 Oct 2024 07:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 07:08:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 17 Oct 2024 07:08:20 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 07:08:20 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 17 Oct 2024 07:08:21 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 17 Oct 2024 07:08:21 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 07:08:21 GMT
ENV JOOMLA_VERSION=4.4.9
# Thu, 17 Oct 2024 07:08:21 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Thu, 17 Oct 2024 07:08:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 17 Oct 2024 07:08:30 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 17 Oct 2024 07:08:30 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 17 Oct 2024 07:08:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Oct 2024 07:08:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ade5403812963eef73a48c4f07cea521affbaab25dbb28bfe5359cbc22bac9`  
		Last Modified: Thu, 17 Oct 2024 06:07:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e936af8dfe7f46433beca18a2d23ce12cc58b84c97bd759cde69ae04ffd1ef8f`  
		Last Modified: Thu, 17 Oct 2024 06:07:43 GMT  
		Size: 101.5 MB (101513470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6390a21b9a7d3612aec1c9c3ddfe5307169cf7c8fe4dd367e3bd5be8f7f53934`  
		Last Modified: Thu, 17 Oct 2024 06:07:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df26b407a97966ce11f72a59d30a9c0c723177d7b69a0565ecb1fcb3f09c1baf`  
		Last Modified: Thu, 17 Oct 2024 06:08:08 GMT  
		Size: 20.8 MB (20842838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8733f6ebe17cf6bd9288e771b20ef3e8623fb0118e887ac501fffddccd07ff5b`  
		Last Modified: Thu, 17 Oct 2024 06:08:03 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf9132130b1c398a4e2da6fffcd1f6cdb97ae92cabd3573482cb658a1bf94c7`  
		Last Modified: Thu, 17 Oct 2024 06:08:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fffb98949ffffe17d4149801000c8afd2f5224271b2cfb96c729ba47a2004fa`  
		Last Modified: Thu, 17 Oct 2024 06:18:43 GMT  
		Size: 12.4 MB (12442394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10a0a385ed759eb0c6df8fc11c62fd3a875aac883157df66eaf6c1bed546fdc`  
		Last Modified: Thu, 17 Oct 2024 06:18:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39956836cdf2971a50fd8c7fed2949679c606d545f5c90b4911cc3ca5e48853`  
		Last Modified: Thu, 17 Oct 2024 06:18:43 GMT  
		Size: 11.6 MB (11641378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8071a3f6dfd4f10d248649b7d1637d31f2606b9a6e6d7d25af2c43e059240b7e`  
		Last Modified: Thu, 17 Oct 2024 06:18:40 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044491766997ad5da75dedbe74b1a79c1ca301be6f337329992adb466655f4e5`  
		Last Modified: Thu, 17 Oct 2024 06:18:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12dc0957fd7c889a6460276058d7d9f7e10fdd7452df268dc8fd0eaf1e9a632`  
		Last Modified: Thu, 17 Oct 2024 06:18:40 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aee91b93bbad9dde9c50529a07f3a540b02ffab3592ee952935a8a723c62824`  
		Last Modified: Thu, 17 Oct 2024 07:16:36 GMT  
		Size: 26.7 MB (26700146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f35614acd17f83357585111c612d7c098e3fa56f328ffea3aa992a92e28f0a8`  
		Last Modified: Thu, 17 Oct 2024 07:16:38 GMT  
		Size: 30.8 MB (30793635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d6ba0d253269ae4887ef2350cb7acd760f73da82653b5bff4039c1571ab778`  
		Last Modified: Thu, 17 Oct 2024 07:16:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728076948566e9ab912c852f3e40a5e8a17beb57d04cb23596fec466c964b281`  
		Last Modified: Thu, 17 Oct 2024 07:16:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f08d7bdaddc6c51481b5972df19a5937bc6c3cc8c6e03b5ea17185a163aa1d5`  
		Last Modified: Thu, 17 Oct 2024 07:16:27 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e34641719b6d90d64e449e0867b410c23290e0fba1a11d5acd1fb8b623045fc`  
		Last Modified: Thu, 17 Oct 2024 07:16:35 GMT  
		Size: 25.9 MB (25913058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abca113350c95a304ebdfde518ba7c4520f9c09612e3d5a49a9ff462db76dcae`  
		Last Modified: Thu, 17 Oct 2024 07:16:27 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d45314f3d4802ad49b3266abfb581928d46f75106d08ec7f2ecc18314794c3a`  
		Last Modified: Thu, 17 Oct 2024 07:16:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; mips64le

```console
$ docker pull joomla@sha256:a954b01f3540d127eab11b7d7ae899ba605ed2d93bffba9ab229c0f4e55fd6db
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233133142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96f4d7183473bc8bb0c54bf966c1b538632f8d2206b8855d99ab7c51bd2dfde`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:35 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 17 Oct 2024 01:09:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:19:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 02:19:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 02:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 02:21:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 02:21:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 02:38:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 02:39:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 02:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 02:39:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 02:40:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 02:40:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:40:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 05:56:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 06:59:51 GMT
ENV PHP_VERSION=8.2.24
# Thu, 17 Oct 2024 06:59:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 17 Oct 2024 06:59:59 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 17 Oct 2024 07:00:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 07:00:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 07:15:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 07:16:00 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 07:16:06 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 07:16:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 07:16:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 07:16:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 07:16:21 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 07:16:25 GMT
EXPOSE 80
# Thu, 17 Oct 2024 07:16:28 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 12:48:49 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 17 Oct 2024 12:48:52 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 17 Oct 2024 14:17:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 14:28:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 17 Oct 2024 14:29:03 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 14:29:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 17 Oct 2024 14:29:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 17 Oct 2024 14:29:23 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 14:29:27 GMT
ENV JOOMLA_VERSION=4.4.9
# Thu, 17 Oct 2024 14:29:32 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Thu, 17 Oct 2024 14:30:11 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 17 Oct 2024 14:30:20 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 17 Oct 2024 14:30:26 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 17 Oct 2024 14:30:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Oct 2024 14:30:41 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3add5d8ad97d2ba7877924447ad98d789dbf096a71456bc495d0a7a74e8afb9`  
		Last Modified: Thu, 17 Oct 2024 08:52:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d206c68dc9357055fa42cdf1b67ba24c98962d0c7550f84933512d107f85a2c0`  
		Last Modified: Thu, 17 Oct 2024 08:53:18 GMT  
		Size: 80.7 MB (80667204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3adaa11daa51a3a26c065af83992847000612bf88e53a1dcb9feb819b02e3`  
		Last Modified: Thu, 17 Oct 2024 08:52:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1669fc913ce96fa2d4887bd63e3e183b72f0354914597276391ec0d6a3d04262`  
		Last Modified: Thu, 17 Oct 2024 08:53:57 GMT  
		Size: 20.1 MB (20068775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8771bdfe6c9af3f18291fcf55f0351d9928f5669267b76b3837a0e3a221e5b09`  
		Last Modified: Thu, 17 Oct 2024 08:53:44 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19aed48dd02184a4d00c1fac98d6cebd3771223e6bd7e4189ad3650fb453a9c`  
		Last Modified: Thu, 17 Oct 2024 08:53:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23619230244d23a3d792a5f2e1f3838534bce89db9d9bc9ef996e8b7146c90ae`  
		Last Modified: Thu, 17 Oct 2024 09:03:49 GMT  
		Size: 12.2 MB (12236876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7a6ba66d28711cab9f63eb8477200e453a7b6709e0e4ff961ab0b7bab31b79`  
		Last Modified: Thu, 17 Oct 2024 09:03:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549eca83a945df8baf37ffdcdf6cb951e7aad7ed2c54d36a85063676b93b3df5`  
		Last Modified: Thu, 17 Oct 2024 09:03:52 GMT  
		Size: 10.5 MB (10491707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669992a5358fd606820e725d923ea8ddc7a8e25d9c6e902a0e86bbb02cc90368`  
		Last Modified: Thu, 17 Oct 2024 09:03:43 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed9bd7b7f361b74731ce0fd4146cf90305e3e38aa0e5109a89f193a8063212d`  
		Last Modified: Thu, 17 Oct 2024 09:03:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d711fa630b2dbbb8d562c166675883348a72e0fa45f7d3a45dc8e1697a94a1a0`  
		Last Modified: Thu, 17 Oct 2024 09:03:43 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81df2f543b09499eec46ea07f172a8f4d175667595cd8a41fb8db6d9574c9a`  
		Last Modified: Thu, 17 Oct 2024 14:55:36 GMT  
		Size: 26.0 MB (26025027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0f160abeb43514eb69bf3552a66695e9ef91984aea0c42677fe8c02bfe3323`  
		Last Modified: Thu, 17 Oct 2024 14:55:44 GMT  
		Size: 28.6 MB (28575198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0945749d166e801697195fb807b5805907319e6f368c3cfb15271aef9c24b537`  
		Last Modified: Thu, 17 Oct 2024 14:55:13 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3e8495330096b8c7536c0184064af189abdb562ec7e065e07f160eb8266313`  
		Last Modified: Thu, 17 Oct 2024 14:55:11 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6c5950d25edcf3c4fa77bc02ff3b24e11e55ecfc9d43c17d4f449f380a54a7`  
		Last Modified: Thu, 17 Oct 2024 14:55:11 GMT  
		Size: 19.2 KB (19171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e10b8213c6dc121a790138f9498bb59c76ee3b4866448e8fceb05191689861`  
		Last Modified: Thu, 17 Oct 2024 14:55:44 GMT  
		Size: 25.9 MB (25913463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912c03bdaa9be59b21778112b5124aa99d5ae31617762aa2e7c89402549ddf82`  
		Last Modified: Thu, 17 Oct 2024 14:55:11 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff80e66c5e9399ee70276cd722e4feb15daeb40fc35ce09cfa52383a87be2c0`  
		Last Modified: Thu, 17 Oct 2024 14:55:11 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:61218c32a7e6b1176b692748aba4b91698de8516fa78de0a8417f38c1b301eb7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267145327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2479cb33fcc6cbe1454578d01e52b730cf168fce364730c20073a01b7b93762`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:55:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 01:55:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 01:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:55:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 01:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 01:58:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 01:58:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 01:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 01:59:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 01:59:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 01:59:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:36:25 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 25 Oct 2024 00:25:00 GMT
ENV PHP_VERSION=8.2.25
# Fri, 25 Oct 2024 00:25:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.25.tar.xz.asc
# Fri, 25 Oct 2024 00:25:01 GMT
ENV PHP_SHA256=330b54876ea1d05ade12ee9726167332058bccd58dffa1d4e12117f6b4f616b9
# Fri, 25 Oct 2024 00:25:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 25 Oct 2024 00:25:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 00:28:07 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:28:08 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 00:28:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 00:28:08 GMT
STOPSIGNAL SIGWINCH
# Fri, 25 Oct 2024 00:28:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:28:09 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 00:28:09 GMT
EXPOSE 80
# Fri, 25 Oct 2024 00:28:09 GMT
CMD ["apache2-foreground"]
# Fri, 25 Oct 2024 01:21:22 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 25 Oct 2024 01:21:23 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 25 Oct 2024 01:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 25 Oct 2024 01:48:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 25 Oct 2024 01:48:19 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 01:48:20 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 25 Oct 2024 01:48:21 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Fri, 25 Oct 2024 01:48:22 GMT
VOLUME [/var/www/html]
# Fri, 25 Oct 2024 01:48:22 GMT
ENV JOOMLA_VERSION=4.4.9
# Fri, 25 Oct 2024 01:48:22 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Fri, 25 Oct 2024 01:48:32 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 25 Oct 2024 01:48:34 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Fri, 25 Oct 2024 01:48:35 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Fri, 25 Oct 2024 01:48:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Oct 2024 01:48:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107c787f39ae7163741fce22e3034e0e43a10e9cbe2ac207f64434e68645221`  
		Last Modified: Thu, 17 Oct 2024 03:11:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627c9d0cca1e0cdb09f43b27bb6bf7d4cca0cad4afc8598940b57844dfe38615`  
		Last Modified: Thu, 17 Oct 2024 03:12:13 GMT  
		Size: 103.3 MB (103326981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cec6f65da0d52cc8cb283752415023a1057b44c8df8167e0417aa9e0b89f632`  
		Last Modified: Thu, 17 Oct 2024 03:11:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a6c7dcb4627fcb50a0780a80643b33a0c7eb8fc97cde415a93b5d62392d81d`  
		Last Modified: Thu, 17 Oct 2024 03:12:38 GMT  
		Size: 21.5 MB (21512775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafbf479aff109b64c60ed07d292ff0964425a857bdce0d29ae39eaa8c05d41c`  
		Last Modified: Thu, 17 Oct 2024 03:12:34 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fee26a079f6b552d2d32941008aecadbb3abf8951c2ad54afd96eb2589a1836`  
		Last Modified: Thu, 17 Oct 2024 03:12:34 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bf9a3f50b556a820b3505902b6fda99bb316b0d3cd7c7f179edeb843004ed9`  
		Last Modified: Fri, 25 Oct 2024 01:00:27 GMT  
		Size: 12.5 MB (12458612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a53cfcf50e538e21591ed2db3678db6b4d8402a117fda2c3fba9e0b74738d45`  
		Last Modified: Fri, 25 Oct 2024 01:00:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89416117a014da531bcadaf40966b5f3a080814ffae1f55f673c154e76a7df6`  
		Last Modified: Fri, 25 Oct 2024 01:00:26 GMT  
		Size: 11.8 MB (11828108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe46118398aad8e5e907a0d79726110a2114cea6d1a975d19812d42b817d778f`  
		Last Modified: Fri, 25 Oct 2024 01:00:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0532a4431ae678b4dbe42418912e53dcabc0132cf8c92dbdf84b40a0e565bc27`  
		Last Modified: Fri, 25 Oct 2024 01:00:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7929ed290a546169e077961ca1bfd228bcd18968389b75c46f802ce3855936`  
		Last Modified: Fri, 25 Oct 2024 01:00:24 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d404a248a9a863974c72334adfd92e927bed43fc58b7680c8b2e7997ed0c1b`  
		Last Modified: Fri, 25 Oct 2024 01:59:13 GMT  
		Size: 27.3 MB (27340910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdeb83d459f88ee05d1cc03934e386f16452fa121caff0b9c2955113a40e7d5`  
		Last Modified: Fri, 25 Oct 2024 01:59:14 GMT  
		Size: 31.6 MB (31612566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40609ba80c52efe923ec051bd6b282fb8b5bcac6d8424191acb90c74f995a595`  
		Last Modified: Fri, 25 Oct 2024 01:59:08 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07730ada43319c13ee7bebc4276565e7681466473786433f4b33e260870a0bb2`  
		Last Modified: Fri, 25 Oct 2024 01:59:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea084d14e8ad0af8de9286870fa64a544d8d405e9663464cdcbcf83a7635aa5c`  
		Last Modified: Fri, 25 Oct 2024 01:59:06 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b01f41609cff2df720d9559d2e949c13a17137772dca2855b99093e0d5d2de`  
		Last Modified: Fri, 25 Oct 2024 01:59:11 GMT  
		Size: 25.9 MB (25913062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f09c5db496acb80e8c2ff7aa5b8d4dff7e07005fcde944de26f9dfc63d4f609`  
		Last Modified: Fri, 25 Oct 2024 01:59:06 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66733276c3e5c2d96715575b24376e26026cc46be969cdb3f4d3cd3d4dcdd8b`  
		Last Modified: Fri, 25 Oct 2024 01:59:06 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; s390x

```console
$ docker pull joomla@sha256:caec87bb9ebd23bdf4f5bfae230ea368aa1dd48109b52e6758a596c78e1a3bdb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231536326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc52f049638e1471cbccec6aedd772093971392d0509c84782d02212e1eca95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 02:09:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Oct 2024 02:09:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Oct 2024 02:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 02:09:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Oct 2024 02:09:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 17 Oct 2024 02:13:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 17 Oct 2024 02:13:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 17 Oct 2024 02:13:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 17 Oct 2024 02:13:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 17 Oct 2024 02:13:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Oct 2024 02:13:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Oct 2024 02:51:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 17 Oct 2024 03:05:27 GMT
ENV PHP_VERSION=8.2.24
# Thu, 17 Oct 2024 03:05:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 17 Oct 2024 03:05:28 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 17 Oct 2024 03:05:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Oct 2024 03:05:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:08:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Oct 2024 03:08:05 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:08:05 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Oct 2024 03:08:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Oct 2024 03:08:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 17 Oct 2024 03:08:06 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 17 Oct 2024 03:08:06 GMT
WORKDIR /var/www/html
# Thu, 17 Oct 2024 03:08:06 GMT
EXPOSE 80
# Thu, 17 Oct 2024 03:08:06 GMT
CMD ["apache2-foreground"]
# Thu, 17 Oct 2024 04:10:18 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 17 Oct 2024 04:10:19 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 17 Oct 2024 04:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:25:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 17 Oct 2024 04:25:38 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Oct 2024 04:25:38 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 17 Oct 2024 04:25:39 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 17 Oct 2024 04:25:39 GMT
VOLUME [/var/www/html]
# Thu, 17 Oct 2024 04:25:39 GMT
ENV JOOMLA_VERSION=4.4.9
# Thu, 17 Oct 2024 04:25:39 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Thu, 17 Oct 2024 04:25:44 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 17 Oct 2024 04:25:46 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Thu, 17 Oct 2024 04:25:46 GMT
COPY file:a53a9770ec4ea12b0947f498a820c4cf00b42fbd01a84c1561849a4497baa065 in /makedb.php 
# Thu, 17 Oct 2024 04:25:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Oct 2024 04:25:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641c5b42b9f8e9cc9d65697a8723928dceb047b06377f2d116b9c2a5512b08e6`  
		Last Modified: Thu, 17 Oct 2024 03:32:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e053e76a5c11aa5d9c2fad8f4e883c1ee8ecbb5f99da4b72f7d634499baa8`  
		Last Modified: Thu, 17 Oct 2024 03:32:17 GMT  
		Size: 80.8 MB (80817901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09024721ae9944c22f86461ed99527ff7d8bee6b9b1f1eff3cd1958f41748694`  
		Last Modified: Thu, 17 Oct 2024 03:32:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6555ecb57349a77868c914c1f994918fb11b71be072532ae14ce8d6f30f680`  
		Last Modified: Thu, 17 Oct 2024 03:32:32 GMT  
		Size: 20.1 MB (20099005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abd9390b6a7484b8a8e03acda3fa992d14c0fd34c5f02599c8c829380a9f9af`  
		Last Modified: Thu, 17 Oct 2024 03:32:30 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b03dab143724a784bcb1c6b3d2011f7a1b4423744088d9ff791064fbb0355d`  
		Last Modified: Thu, 17 Oct 2024 03:32:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4cec6286ed44f57e568f7b7bf40516e9197df22d7c0d626381ef27ad62c63b`  
		Last Modified: Thu, 17 Oct 2024 03:36:50 GMT  
		Size: 12.4 MB (12441791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82381c692c74376eea57227525adcdd8037bd6e7afc13bd82ce71e9b0a237f76`  
		Last Modified: Thu, 17 Oct 2024 03:36:48 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb34a6b0de5a27cf0ff5a8203ce3393167839f826fb1b04a6b253b9c3c10e14`  
		Last Modified: Thu, 17 Oct 2024 03:36:50 GMT  
		Size: 10.6 MB (10644688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4781216db481798eda55ee556dbabaa97ec898f0e1edbbbf2c85cfa57ef822`  
		Last Modified: Thu, 17 Oct 2024 03:36:48 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84910e2a431945ee4b2a2247c0ce4d908caa9ad5f5188ff9bbacc902689a4ada`  
		Last Modified: Thu, 17 Oct 2024 03:36:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53ac3959535147a0edd949ad94fc52e2d0c898353505fab4fef45528aa3f9bb`  
		Last Modified: Thu, 17 Oct 2024 03:36:48 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c1681086f2a0e408772752cdd5e96c0346e729eb2574e0987a740bb0c33b57`  
		Last Modified: Thu, 17 Oct 2024 04:31:04 GMT  
		Size: 25.9 MB (25898176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90435c2a8b6c655d2e54d5a55b2a653d27957aa29d6d7753c40585ce8ed53386`  
		Last Modified: Thu, 17 Oct 2024 04:31:05 GMT  
		Size: 28.2 MB (28201501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce55b2445382bd51ad0909be1c1e8656ff32447a0e4eb6932e8da171bf178d0`  
		Last Modified: Thu, 17 Oct 2024 04:31:01 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5f35964bba150e6e2a46496013fcb3715837d2087e03dad8d0a6d85ceba008`  
		Last Modified: Thu, 17 Oct 2024 04:31:00 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dd0043c3c4e6de4857344d517c709eda226104f3dd51f7341182d896b09cfc`  
		Last Modified: Thu, 17 Oct 2024 04:31:00 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d6fde977c983a4166d075bc5f44c116c57f3112a2743ca0c940fb07ee7db18`  
		Last Modified: Thu, 17 Oct 2024 04:31:03 GMT  
		Size: 25.9 MB (25913079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90f79659a4164c9370d8f3f177922a18528adc62099649b75c53cb70d1e291b`  
		Last Modified: Thu, 17 Oct 2024 04:31:00 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dced00607368ae021a3177135520ad2695fb1c88a6a9d87c32ad608b5259c3a`  
		Last Modified: Thu, 17 Oct 2024 04:31:00 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
